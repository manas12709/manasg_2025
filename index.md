---
layout: base
title: Escape the Maze
description: An interactive maze game to challenge your skills!
author: Manas Goel
image: /images/mario_animation.png
hide: false
---

{% include nav/home.html %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        background-color: #f0f8ff;
        margin: 0;
        padding: 0;
        text-align: center;
        overflow-x: hidden; /* Prevents horizontal scroll */
    }

    h1 {
        font-size: 3.5em;
        color: #ff6347;
        margin-top: 30px;
        animation: slideInDown 1s;
        letter-spacing: 2px;
        text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.2);
    }

    p {
        font-size: 1.5em;
        color: #333;
        margin-bottom: 30px;
        animation: fadeIn 1.5s;
    }

    .game-container {
        position: relative;
        width: 400px;
        height: 400px;
        margin: 50px auto;
        border: 5px solid #ff6347;
        border-radius: 10px;
        background-color: #e6f7ff;
        box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        overflow: hidden;
        animation: bounceIn 1s;
    }

    .player-avatar {
        position: absolute;
        width: 40px;
        height: 40px;
        background-color: #ff6347;
        border-radius: 50%;
        cursor: pointer;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        transition: transform 0.3s ease;
    }

    .player-avatar:hover {
        transform: scale(1.1);
    }

    .score-board {
        font-size: 2em;
        color: #ff6347;
        margin-top: 20px;
        background-color: #e6f7ff;
        padding: 15px;
        border-radius: 8px;
        display: inline-block;
        animation: fadeIn 2s;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }

    button {
        font-size: 1.5em;
        background-color: #ff6347;
        color: white;
        border: none;
        padding: 12px 24px;
        border-radius: 8px;
        cursor: pointer;
        margin-top: 30px;
        transition: background-color 0.3s, box-shadow 0.3s;
        box-shadow: 0 5px 15px rgba(255, 99, 71, 0.3);
    }

    button:hover {
        background-color: #d95f43;
        box-shadow: 0 5px 20px rgba(255, 99, 71, 0.5);
    }

    /* Animations */
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

    @keyframes bounceIn {
        from {
            opacity: 0;
            transform: scale(0.9);
        }
        to {
            opacity: 1;
            transform: scale(1);
        }
</style>

<h1>Escape the Maze!</h1>
<p>Click to move through the maze and collect points!</p>

<div class="game-container" id="game-container">
    <div id="player" class="player-avatar"></div>
</div>

<div class="score-board">
    Score: <span id="score">0</span>
</div>

<!-- Reset Button -->
<button id="reset-btn">Reset Game</button>

<script>
    const player = document.getElementById('player');
    const scoreBoard = document.getElementById('score');
    const resetBtn = document.getElementById('reset-btn');
    const container = document.getElementById('game-container');
    let score = 0;

    const targetPosition = {
        x: Math.floor(Math.random() * (container.offsetWidth - player.offsetWidth)),
        y: Math.floor(Math.random() * (container.offsetHeight - player.offsetHeight))
    };

    player.style.left = targetPosition.x + 'px';
    player.style.top = targetPosition.y + 'px';

    function movePlayer(event) {
        const rect = container.getBoundingClientRect();
        const offsetX = event.clientX - rect.left - player.offsetWidth / 2;
        const offsetY = event.clientY - rect.top - player.offsetHeight / 2;

        // Check bounds
        if (offsetX < 0) offsetX = 0;
        if (offsetY < 0) offsetY = 0;
        if (offsetX > container.offsetWidth - player.offsetWidth) offsetX = container.offsetWidth - player.offsetWidth;
        if (offsetY > container.offsetHeight - player.offsetHeight) offsetY = container.offsetHeight - player.offsetHeight;

        player.style.left = offsetX + 'px';
        player.style.top = offsetY + 'px';

        if (Math.abs(offsetX - targetPosition.x) < 40 && Math.abs(offsetY - targetPosition.y) < 40) {
            score++;
            scoreBoard.textContent = score;
            targetPosition.x = Math.floor(Math.random() * (container.offsetWidth - player.offsetWidth));
            targetPosition.y = Math.floor(Math.random() * (container.offsetHeight - player.offsetHeight));
            player.style.left = targetPosition.x + 'px';
            player.style.top = targetPosition.y + 'px';
        }
    }

    container.addEventListener('click', movePlayer);

    // Reset Game
    resetBtn.addEventListener('click', function() {
        score = 0;
        scoreBoard.textContent = score;
        targetPosition.x = Math.floor(Math.random() * (container.offsetWidth - player.offsetWidth));
        targetPosition.y = Math.floor(Math.random() * (container.offsetHeight - player.offsetHeight));
        player.style.left = targetPosition.x + 'px';
        player.style.top = targetPosition.y + 'px';
    });
</script>

## Manas Goel