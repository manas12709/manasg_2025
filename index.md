---
layout: base
title: Escape the Maze!
description: Navigate through the maze to collect treasures!
author: Manas Goel
image: /images/mario_animation.png
hide: false
---

{% include nav/home.html %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        margin: 0;
        padding: 0;
        text-align: center;
        overflow: hidden; /* Prevents scrollbars */
        background: linear-gradient(135deg, #ff6e7f, #bfe9ff, #ff512f, #dd2476); /* Gradient with warm reds and sunset oranges */
        animation: gradient 15s ease infinite; /* Animate the background */
    }

    @keyframes gradient {
        0% { background: #ff6e7f; } /* Starting color */
        25% { background: #ff512f; } /* Second color */
        50% { background: #dd2476; } /* Third color */
        75% { background: #bfe9ff; } /* Fourth color */
        100% { background: #ff6e7f; } /* Ending color */
    }
    
    h1 {
        font-size: 3em;
        color: #ffffff;
        margin-top: 20px;
        animation: slideInDown 1s;
        letter-spacing: 2px;
        text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
    }

    p {
        font-size: 1.5em;
        color: #ffffff;
        margin-bottom: 20px;
        animation: fadeIn 1.5s;
        text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
    }

    .maze-container {
        position: relative;
        width: 400px;
        height: 400px;
        margin: 50px auto;
        border: 2px solid #ffffff;
        border-radius: 10px;
        background-color: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        overflow: hidden;
    }

    .player {
        position: absolute;
        width: 30px;
        height: 30px;
        background-color: #ff6347;
        border-radius: 50%;
        transition: transform 0.3s ease;
        left: 10px; /* Start position */
        top: 10px;  /* Start position */
    }

    .treasure {
        position: absolute;
        width: 20px;
        height: 20px;
        background-color: gold;
        border-radius: 50%;
    }

    .obstacle {
        position: absolute;
        width: 40px;
        height: 40px;
        background-color: gray;
    }

    .score-board {
        font-size: 1.8em;
        color: #ffffff;
        margin-top: 20px;
        background-color: rgba(0, 122, 204, 0.8);
        padding: 10px;
        border-radius: 8px;
        display: inline-block;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
    }

    button {
        font-size: 1.5em;
        background-color: #007acc;
        color: white;
        border: none;
        padding: 10px 20px;
        border-radius: 8px;
        cursor: pointer;
        margin-top: 30px;
        transition: background-color 0.3s, box-shadow 0.3s;
        box-shadow: 0 5px 15px rgba(0, 122, 204, 0.3);
    }

    button:hover {
        background-color: #005fa3;
        box-shadow: 0 5px 20px rgba(0, 122, 204, 0.5);
    }

    @keyframes slideInDown {
        from {
            opacity: 0;
            transform: translateY(-50px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
</style>

<h1>Escape the Maze!</h1>
<p>Collect treasures while avoiding obstacles!</p>

<div class="maze-container" id="maze">
    <div id="player" class="player"></div>
    <div id="treasure" class="treasure"></div>
    <div id="obstacle" class="obstacle"></div>
</div>

<div class="score-board">
    Score: <span id="score">0</span>
</div>

<!-- Reset Button -->
<button id="reset-btn">Reset Game</button>

<script>
    const player = document.getElementById('player');
    const treasure = document.getElementById('treasure');
    const obstacle = document.getElementById('obstacle');
    const scoreBoard = document.getElementById('score');
    const resetBtn = document.getElementById('reset-btn');
    let score = 0;

    // Initialize game
    function initGame() {
        score = 0;
        scoreBoard.textContent = score;
        placeTreasure();
        placeObstacle();
        player.style.left = '10px';
        player.style.top = '10px';
    }

    // Place treasure in random position
    function placeTreasure() {
        const maze = document.getElementById('maze');
        const maxX = maze.offsetWidth - treasure.offsetWidth;
        const maxY = maze.offsetHeight - treasure.offsetHeight;
        const randomX = Math.floor(Math.random() * maxX);
        const randomY = Math.floor(Math.random() * maxY);
        
        treasure.style.left = randomX + 'px';
        treasure.style.top = randomY + 'px';
    }

    // Place obstacle in random position
    function placeObstacle() {
        const maze = document.getElementById('maze');
        const maxX = maze.offsetWidth - obstacle.offsetWidth;
        const maxY = maze.offsetHeight - obstacle.offsetHeight;
        const randomX = Math.floor(Math.random() * maxX);
        const randomY = Math.floor(Math.random() * maxY);
        
        obstacle.style.left = randomX + 'px';
        obstacle.style.top = randomY + 'px';
    }

    // Move player with arrow keys
    document.addEventListener('keydown', function(event) {
        const playerRect = player.getBoundingClientRect();
        const mazeRect = document.getElementById('maze').getBoundingClientRect();

        if (event.key === 'ArrowUp' && playerRect.top > mazeRect.top) {
            player.style.top = playerRect.top - mazeRect.top - 30 + 'px'; // Move up
        }
        if (event.key === 'ArrowDown' && playerRect.bottom < mazeRect.bottom) {
            player.style.top = playerRect.top - mazeRect.top + 30 + 'px'; // Move down
        }
        if (event.key === 'ArrowLeft' && playerRect.left > mazeRect.left) {
            player.style.left = playerRect.left - mazeRect.left - 30 + 'px'; // Move left
        }
        if (event.key === 'ArrowRight' && playerRect.right < mazeRect.right) {
            player.style.left = playerRect.left - mazeRect.left + 30 + 'px'; // Move right
        }
        checkCollision();
    });

    // Check collision with treasure and obstacle
    function checkCollision() {
        const playerRect = player.getBoundingClientRect();
        const treasureRect = treasure.getBoundingClientRect();
        const obstacleRect = obstacle.getBoundingClientRect();

        // Collision with treasure
        if (playerRect.x < treasureRect.x + treasureRect.width &&
            playerRect.x + playerRect.width > treasureRect.x &&
            playerRect.y < treasureRect.y + treasureRect.height &&
            playerRect.y + playerRect.height > treasureRect.y) {
            score++;
            scoreBoard.textContent = score;
            placeTreasure(); // New treasure position
        }

        // Collision with obstacle
        if (playerRect.x < obstacleRect.x + obstacleRect.width &&
            playerRect.x + playerRect.width > obstacleRect.x &&
            playerRect.y < obstacleRect.y + obstacleRect.height &&
            playerRect.y + playerRect.height > obstacleRect.y) {
            alert("Game Over! Final Score: " + score);
            initGame(); // Restart the game
        }
    }

    // Reset Game
    resetBtn.addEventListener('click', initGame);

    // Start game on page load
    window.onload = initGame;
</script>

## Manas Goel
Cannot wait to learn how to make a better game!