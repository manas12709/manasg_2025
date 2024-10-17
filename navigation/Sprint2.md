---
layout: page
title: Lesson hacks and homework
permalink: /sprint2/
---

{% include nav/lessons.html %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        margin: 0;
        padding: 0;
        text-align: center;
        overflow: hidden;
        background: linear-gradient(135deg, #ffafbd, #ffc3a0, #ffeb3b, #ff9800);
        animation: gradient 15s ease infinite;
        color: #333;
    }

    @keyframes gradient {
        0% { background: #ffafbd; }
        25% { background: #ffc3a0; }
        50% { background: #ffeb3b; }
        75% { background: #ff9800; }
        100% { background: #ffafbd; }
    }

    h1, h2 {
        font-size: 2.5em;
        text-transform: uppercase;
        letter-spacing: 2px;
        animation: textGlow 2s ease-in-out infinite alternate;
    }

    @keyframes textGlow {
        from { text-shadow: 0 0 10px #ffffff, 0 0 20px #ffafbd; }
        to { text-shadow: 0 0 20px #ffffff, 0 0 40px #ffc3a0; }
    }

    .content {
        width: 80%;
        margin: 50px auto;
        background: rgba(255, 255, 255, 0.85);
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        transition: transform 0.4s ease, background-color 0.6s ease;
    }

    .content:hover {
        transform: scale(1.05);
        background-color: rgba(255, 245, 240, 0.95);
    }

    p {
        font-size: 1.2em;
        line-height: 1.6;
    }

    a {
        color: #ff5722;
        text-decoration: none;
        transition: color 0.3s ease;
    }

    a:hover {
        color: #e64a19;
        text-shadow: 0 0 10px rgba(255, 87, 34, 0.8);
    }

</style>

<div class="content">
    <h1>Lesson Hacks and Homework</h1>
    <p>Welcome to the lesson hacks and homework section. Here you'll find assignments for all your lessons. Stay up to date with your work and make the most out of your learning experience!</p>
    <!-- More content can go here -->
</div>
