---
layout: page
title: Big Idea 5 Summaries
permalink: /bigidea5summary/
---

{% include nav/bigidea5.html %}

<style>
    body {
        font-family: 'Poppins', sans-serif;
        margin: 0;
        padding: 0;
        text-align: center;
        overflow: auto;
        background: linear-gradient(135deg, #00c6ff, #0072ff, #00bfff, #1e90ff);
        animation: gradient 15s ease infinite;
    }

    @keyframes gradient {
        0% { background: #00c6ff; }
        25% { background: #0072ff; }
        50% { background: #00bfff; }
        75% { background: #1e90ff; }
        100% { background: #00c6ff; }
    }

    table {
        width: 90%;
        margin: 30px auto;
        border-collapse: collapse;
        background: rgba(255, 255, 255, 0.9);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        border-radius: 15px;
        transition: transform 0.5s ease, box-shadow 0.5s ease, background 0.3s ease;
    }

    table:hover {
        transform: scale(1.05);
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
        background: rgba(255, 255, 255, 0.95);
    }

    th, td {
        padding: 20px;
        border-bottom: 1px solid #ddd;
        text-align: left;
        font-size: 1.1rem;
        transition: background-color 0.3s ease, color 0.3s ease;
    }

    th {
        background: linear-gradient(135deg, #007bff, #1e90ff);
        color: white;
        font-weight: bold;
        font-size: 1.3rem;
        text-transform: uppercase;
        letter-spacing: 0.05em;
        border-bottom: 2px solid white;
    }

    td {
        background-color: #f5f7fa;
        color: #333;
    }

    td:hover {
        background-color: #e1f5ff;
        color: #007bff;
        cursor: pointer;
        transform: translateX(5px);
        transition: transform 0.2s ease;
    }

    td a {
        color: #007bff;
        text-decoration: none;
        font-weight: bold;
        transition: color 0.3s ease;
    }

    td a:hover {
        color: #0056b3;
        text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
    }

    h2 {
        font-size: 2.5rem;
        color: #0047ab;
        margin-top: 20px;
        text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);
        text-transform: uppercase;
    }

    ul {
        list-style-type: disc;
        margin-left: 20px;
        line-height: 1.6;
    }

    li {
        margin-bottom: 8px;
        font-size: 1.05rem;
        transition: color 0.3s ease;
    }

    li:hover {
        color: #007bff;
    }
</style>

<table>
    <thead>
        <tr>
            <th>Unit</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Digital Divide</td>
            <td>The gap between those who have access to modern technology and those who do not; impacts education, economy, and equity.</td>
        </tr>
        <tr>
            <td>Computing Bias</td>
            <td>Bias in algorithms/data can reinforce discrimination; it's crucial to identify and correct bias in computing systems.</td>
        </tr>
        <tr>
            <td>Crowd Sourcing</td>
            <td>Using public contributions (data, ideas, or work) to solve problems; seen in platforms like Wikipedia or open-source projects.</td>
        </tr>
        <tr>
            <td>Legal And Ethical Concerns</td>
            <td>Focuses on privacy, intellectual property, hacking, and consequences of violating digital laws or ethical principles.</td>
        </tr>
        <tr>
            <td>Safe Computing</td>
            <td>Covers cybersecurity best practices like strong passwords, encryption, and secure data handling to stay safe online.</td>
        </tr>
        <tr>
            <td>Binary</td>
            <td>Binary is the language of computers; represents all data using 0s and 1s; essential for understanding how systems operate.</td>
        </tr>
        <tr>
            <td>Random Algorithms</td>
            <td>Algorithms that produce different results on different runs, often used for simulations, games, and randomized security.</td>
        </tr>
        <tr>
            <td>Big O</td>
            <td>Big O notation describes algorithm efficiency—how it scales with input size; helps compare performance of algorithms.</td>
        </tr>
        <tr>
            <td>Undecidable Problems and Graphs</td>
            <td>Some problems can't be solved by computers (undecidable); graphs help visualize networks and solve related challenges.</td>
        </tr>
        <tr>
            <td>Binary Base 2 Math</td>
            <td>Covers binary arithmetic and conversions between binary and decimal; crucial for low-level data processing.</td>
        </tr>
        <tr>
            <td>Base 64</td>
            <td>A method to encode binary data into text using 64 characters; commonly used in email and data storage.</td>
        </tr>
    </tbody>
</table>
