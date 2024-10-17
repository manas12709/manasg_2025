---
layout: page
title: Lesson Hacks and Homework
permalink: /sprint2/
---

{% include nav/lessons.html %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        margin: 0;
        padding: 0;
        text-align: center;
        background: linear-gradient(135deg, #00c6ff, #0072ff, #00bfff, #1e90ff); 
        animation: gradient 10s ease infinite;
    }

    @keyframes gradient {
        0% { background: #00c6ff; }
        25% { background: #0072ff; }
        50% { background: #00bfff; }
        75% { background: #1e90ff; }
        100% { background: #00c6ff; }
    }

    h2 {
        font-size: 2.5em;
        color: white;
        text-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        margin-top: 30px;
        transition: color 0.3s ease;
    }

    h2:hover {
        color: #ffd700;
    }

    .content {
        background-color: rgba(255, 255, 255, 0.9);
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        margin: 40px auto;
        width: 90%;
        max-width: 1000px;
        transition: transform 0.3s ease;
    }

    .content:hover {
        transform: scale(1.02);
    }

    details {
        background-color: #0072ff;
        color: white;
        padding: 15px;
        border-radius: 8px;
        margin-bottom: 20px;
        transition: all 0.3s ease;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }

    details:hover {
        background-color: #005bb5;
        box-shadow: 0 6px 18px rgba(0, 0, 0, 0.3);
    }

    summary {
        font-size: 1.5em;
        cursor: pointer;
        transition: color 0.3s ease;
    }

    summary:hover {
        color: #ffd700;
    }

    pre, code {
        background-color: #f5f5f5;
        color: #333;
        padding: 20px;
        border-radius: 10px;
        font-size: 1em;
        text-align: left;
        overflow-x: auto;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    pre:hover, code:hover {
        box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
    }

</style>

<h2>Lesson Hacks and Homework</h2>

<div class="content">
    <p>Below are the lesson hacks and homework assignments for this sprint. Click on each section to view detailed content and code snippets.</p>

    <details>
        <summary>Click to view CSS code</summary>
        <pre>
            <code>
                /* Example CSS snippet */
                body {
                    font-family: 'Poppins', sans-serif;
                    margin: 0;
                    padding: 0;
                    text-align: center;
                    background: linear-gradient(135deg, #00c6ff, #0072ff, #00bfff, #1e90ff);
                    animation: gradient 10s ease infinite;
                }

                @keyframes gradient {
                    0% { background: #00c6ff; }
                    25% { background: #0072ff; }
                    50% { background: #00bfff; }
                    75% { background: #1e90ff; }
                    100% { background: #00c6ff; }
                }
            </code>
        </pre>
    </details>

    <!-- Add more content or sections as needed -->
</div>
