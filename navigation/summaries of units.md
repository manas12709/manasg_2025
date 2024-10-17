---
layout: page
title: Summary of all units
permalink: /summary/
---

{% include nav/summary.html %}

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

<h2>Part 1 - Fundamentals (Quick Review)</h2>

<table>
    <thead>
        <tr>
            <th>Unit</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-1">3.1 Variables</a></td>
            <td>
                <ul>
                    <li>Variables store information that can be reused and changed.</li>
                    <li>Data types include integers, floats, strings, and booleans.</li>
                    <li>Use descriptive variable names for clarity.</li>
                    <li>Scope defines where a variable can be accessed in a program.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-2/">3.2 Data Abstraction</a></td>
            <td>
                <ul>
                    <li>Data abstraction simplifies code by hiding complex details.</li>
                    <li>Functions and data structures allow for easier management of data.</li>
                    <li>Abstraction helps break down large problems into smaller parts.</li>
                    <li>Data encapsulation prevents direct access to some data fields.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-3">3.3 Mathematical Expressions</a></td>
            <td>
                <ul>
                    <li>Operators include +, -, *, /, and % (modulus) for calculations.</li>
                    <li>Follows order of operations: parentheses, exponents, multiplication/division, addition/subtraction (PEMDAS).</li>
                    <li>Use math libraries for complex operations like square roots and trigonometry.</li>
                    <li>Modulus (%) returns the remainder of a division.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-4">3.4 Strings</a></td>
            <td>
                <ul>
                    <li>Strings are sequences of characters used for text manipulation.</li>
                    <li>Common methods: slicing, concatenation, and formatting.</li>
                    <li>Escape characters like \n (newline) and \t (tab) format output.</li>
                    <li>String indexing allows access to individual characters.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-5">3.5 Booleans</a></td>
            <td>
                <ul>
                    <li>Booleans represent True or False values.</li>
                    <li>Comparison operators: ==, !=, >, <, >=, <= compare values.</li>
                    <li>Boolean logic: AND, OR, NOT used for combining conditions.</li>
                    <li>Booleans are often used in conditionals to control program flow.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-6">3.6 Conditionals</a></td>
            <td>
                <ul>
                    <li>If-else statements control the flow of the program based on conditions.</li>
                    <li>Conditions evaluate to True or False.</li>
                    <li>Multiple conditions can be combined using logical operators.</li>
                    <li>Else-if chains are used to test multiple conditions.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-7">3.7 Nested Conditionals</a></td>
            <td>
                <ul>
                    <li>Nested if statements allow for complex decision-making.</li>
                    <li>Important to maintain proper indentation for clarity.</li>
                    <li>Nested conditionals can sometimes be simplified using logical operators.</li>
                    <li>Used for multi-layered decision logic.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-8">3.8 Iteration</a></td>
            <td>
                <ul>
                    <li>Loops (for, while) repeat tasks until conditions are met.</li>
                    <li>For loops iterate over sequences like lists or ranges.</li>
                    <li>While loops continue until a condition evaluates to False.</li>
                    <li>Break and continue statements alter loop behavior.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-10">3.10 Lists</a></td>
            <td>
                <ul>
                    <li>Assigning Values: Assign values to list elements.</li>
                    <li>Inserting Elements: Insert elements at specific positions in the list.</li>
                    <li>Appending Elements: Append new elements to the end of the list.</li>
                    <li>Removing Elements: Remove elements from the list.</li>
                </ul>
            </td>
        </tr>
