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
        overflow: auto; /* Enable scrolling */
        background: linear-gradient(135deg, #00c6ff, #0072ff, #00bfff, #1e90ff);
        animation: gradient 15s ease infinite;
        color: #fff;
    }

    @keyframes gradient {
        0% { background: #00c6ff; }
        25% { background: #0072ff; }
        50% { background: #00bfff; }
        75% { background: #1e90ff; }
        100% { background: #00c6ff; }
    }

    h2 {
        font-size: 2.5rem;
        color: #0047ab;
        margin-top: 20px;
        text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);
        text-transform: uppercase;
    }

    table {
        width: 95%;
        margin: 40px auto;
        border-collapse: collapse;
        background: linear-gradient(135deg, rgba(255,255,255,0.2), rgba(255,255,255,0.1));
        border-radius: 15px;
        box-shadow: 0 15px 30px rgba(0,0,0,0.3);
        overflow: hidden;
        position: relative;
        transition: all 0.5s ease;
    }

    table:hover {
        transform: scale(1.03);
        box-shadow: 0 25px 40px rgba(0, 0, 0, 0.4);
    }

    thead {
        background: rgba(0, 123, 255, 0.85);
        color: #fff;
    }

    th {
        padding: 20px;
        font-size: 1.3rem;
        font-weight: bold;
        text-transform: uppercase;
        letter-spacing: 0.1em;
        text-align: left;
        position: sticky;
        top: 0;
        background: rgba(0, 123, 255, 0.95);
    }

    tbody {
        background-color: rgba(255, 255, 255, 0.8);
        border-radius: 15px;
    }

    td {
        padding: 20px;
        border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        font-size: 1.1rem;
        text-align: left;
        color: #333;
        position: relative;
        overflow: hidden;
        transition: background-color 0.4s ease, color 0.4s ease;
    }

    td:hover {
        background: rgba(100, 181, 246, 0.3);
        color: #007bff;
    }

    td::before {
        content: "";
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: rgba(0, 123, 255, 0.15);
        transition: left 0.5s ease;
    }

    td:hover::before {
        left: 0;
    }

    td a {
        color: #007bff;
        text-decoration: none;
        font-weight: bold;
        transition: color 0.3s ease;
    }

    td a:hover {
        color: #0056b3;
        text-shadow: 0 0 10px rgba(0, 123, 255, 0.8);
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

    /* Advanced CSS Animations */
    tbody tr {
        animation: rowSlideIn 1.5s ease-in-out;
    }

    @keyframes rowSlideIn {
        0% {
            opacity: 0;
            transform: translateY(20px);
        }
        100% {
            opacity: 1;
            transform: translateY(0);
        }
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
        width: 12px;
    }

    ::-webkit-scrollbar-track {
        background: rgba(0, 0, 0, 0.1);
        border-radius: 10px;
    }

    ::-webkit-scrollbar-thumb {
        background: rgba(0, 123, 255, 0.5);
        border-radius: 10px;
    }

    ::-webkit-scrollbar-thumb:hover {
        background: rgba(0, 123, 255, 0.8);
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
            <td><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-2">3.2 Data Abstraction</a></td>
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
        <!-- Add more rows here -->
    </tbody>
</table>
