---
layout: page
title: Snake
permalink: /snake/
---

<style>
    /* Christmas Theme */
    body {
        background: url('https://www.transparenttextures.com/patterns/christmas.png') #003366;
        color: white;
        font-family: 'Arial', sans-serif;
        overflow: auto; /* Ensures scrolling works */
        height: 100%; /* Fix for scroll issue */
        margin: 0; /* Removes any default margin */
        position: relative; /* To position snowflakes correctly */
    }

    canvas {
        border: 3px solid #fff;
        background: url('https://i.imgur.com/dQF6XUd.png') center/cover no-repeat;
        box-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
        margin: 20px auto;
        display: block;
        z-index: 2;
    }

    #game-over {
        font-size: 2.5em;
        color: #ff0000;
        text-shadow: 0 0 10px rgba(255, 0, 0, 0.8);
        text-align: center;
        display: none;
    }

    .button-container {
        text-align: center;
        margin-top: 10px;
    }

    .button-container button {
        padding: 10px 20px;
        margin: 5px;
        background-color: #007bff;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        box-shadow: 0 0 5px rgba(255, 255, 255, 0.7);
    }

    .button-container button:hover {
        background-color: #0056b3;
    }

    .snowflake {
        position: absolute;
        top: -10px;
        font-size: 1.5em;
        color: white;
        animation: fall linear infinite;
        z-index: 1;
    }

    @keyframes fall {
        0% {
            opacity: 1;
            transform: translateY(0) rotate(0deg);
        }
        100% {
            opacity: 0;
            transform: translateY(100vh) rotate(360deg);
        }
    }

    /* Snowy background for the Snake Game area */
    .game-container {
        background: url('https://img-new.cgtrader.com/items/4249139/adc2375500/large/4k-seamless-snow-square-material-04-3d-model-adc2375500.jpg') center/cover no-repeat;
        padding: 20px;
        margin: 0 auto;
        width: fit-content;
        box-shadow: 0 0 15px rgba(255, 255, 255, 0.8);
    }

</style>

<h1 id="game-over">Game Over! Merry Christmas!</h1>

<!-- Container for the Snake Game -->
<div class="game-container">
    <canvas id="gameCanvas" width="400" height="400"></canvas>

    <div class="button-container">
        <button id="slow-btn">Slow Mode</button>
        <button id="fast-btn">Fast Mode</button>
        <button id="wall-btn">Wall On/Off</button>
        <button id="theme-btn">Switch Theme</button>
    </div>
</div>

<script>
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");
    const box = 20;
    let snake = [{ x: 9 * box, y: 10 * box }];
    let food = {
        x: Math.floor(Math.random() * 19 + 1) * box,
        y: Math.floor(Math.random() * 19 + 1) * box
    };
    let direction;
    let score = 0;
    let speed = 100;
    let wallOn = true;

    document.addEventListener("keydown", changeDirection);

    function changeDirection(event) {
        if (event.keyCode == 37 && direction != "RIGHT") direction = "LEFT";
        else if (event.keyCode == 38 && direction != "DOWN") direction = "UP";
        else if (event.keyCode == 39 && direction != "LEFT") direction = "RIGHT";
        else if (event.keyCode == 40 && direction != "UP") direction = "DOWN";
    }

    // Prevent page scrolling when arrow keys are pressed
    document.addEventListener("keydown", function(event) {
        if (["ArrowUp", "ArrowDown", "ArrowLeft", "ArrowRight"].includes(event.key)) {
            event.preventDefault(); // Prevent the default action (scrolling)
        }
    });

    function collision(head, array) {
        return array.some(segment => head.x === segment.x && head.y === segment.y);
    }

    function draw() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        for (let i = 0; i < snake.length; i++) {
            ctx.fillStyle = i === 0 ? "#FFFFFF" : "#000000";
            ctx.fillRect(snake[i].x, snake[i].y, box, box);
            ctx.font = "20px Arial";
            if (i === 0) {
                ctx.fillText("⛷️", snake[i].x, snake[i].y + box);
            }
        }

        // Christmas Cookie Food
        const cookieImg = new Image();
        cookieImg.src = "data:image/jpeg;base64,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";
        ctx.drawImage(cookieImg, food.x, food.y, box, box);

        let snakeX = snake[0].x;
        let snakeY = snake[0].y;

        if (direction == "LEFT") snakeX -= box;
        if (direction == "UP") snakeY -= box;
        if (direction == "RIGHT") snakeX += box;
        if (direction == "DOWN") snakeY += box;

        if (snakeX == food.x && snakeY == food.y) {
            score++;
            food = {
                x: Math.floor(Math.random() * 19 + 1) * box,
                y: Math.floor(Math.random() * 19 + 1) * box
            };
        } else {
            snake.pop();
        }

        let newHead = { x: snakeX, y: snakeY };

        if (wallOn && (snakeX < 0 || snakeY < 0 || snakeX >= canvas.width || snakeY >= canvas.height || collision(newHead, snake))) {
            document.getElementById("game-over").style.display = "block";
            clearInterval(game);
        } else {
            if (!wallOn) {
                if (snakeX < 0) snakeX = canvas.width - box;
                if (snakeX >= canvas.width) snakeX = 0;
                if (snakeY < 0) snakeY = canvas.height - box;
                if (snakeY >= canvas.height) snakeY = 0;
            }

            snake.unshift(newHead);
        }

        ctx.fillStyle = "white";
        ctx.font = "20px Arial";
        ctx.fillText("Score: " + score, 10, 30);
    }

    let game = setInterval(draw, speed);

    document.getElementById("slow-btn").addEventListener("click", function() {
        clearInterval(game);
        speed = 200;
        game = setInterval(draw, speed);
    });

    document.getElementById("fast-btn").addEventListener("click", function() {
        clearInterval(game);
        speed = 50;
        game = setInterval(draw, speed);
    });

    document.getElementById("wall-btn").addEventListener("click", function() {
        wallOn = !wallOn;
    });

    const themes = ['#003366', '#ff0000', '#00ff00', '#ffcc00'];
    let currentTheme = 0;
    document.getElementById("theme-btn").addEventListener("click", function() {
        document.body.style.backgroundColor = themes[++currentTheme % themes.length];
    });

    function createSnowflakes() {
        const snowflake = document.createElement('div');
        snowflake.classList.add('snowflake');
        snowflake.style.left = Math.random() * window.innerWidth + 'px';
        snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
        snowflake.textContent = '❄';
        document.body.appendChild(snowflake);

        setTimeout(() => snowflake.remove(), 5000);
    }

    setInterval(createSnowflakes, 100);
</script>

<iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/5OP7itTh52BMfZS1DJrdlv?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
