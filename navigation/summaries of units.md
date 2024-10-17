---
layout: page
title: Summary of all units 
permalink: /summary/
---

{% include nav/summary.html %}

<details>
    <summary>Click to view CSS code</summary>
    <pre>
        <code>
            <style>
                body {
                    font-family: 'Poppins', sans-serif;
                    margin: 0;
                    padding: 0;
                    text-align: center;
                    overflow: hidden; /* Prevents scrollbars */
                    background: linear-gradient(135deg, #00c6ff, #0072ff, #00bfff, #1e90ff); /* Gradient with ocean colors */
                    animation: gradient 15s ease infinite; /* Animate the background */
                }

                @keyframes gradient {
                    0% { background: #00c6ff; } /* Starting color */
                    25% { background: #0072ff; } /* Second color */
                    50% { background: #00bfff; } /* Third color */
                    75% { background: #1e90ff; } /* Fourth color */
                    100% { background: #00c6ff; } /* Ending color */
                }

                /* Submenu styling */
                .submenu {
                    color: black; /* Set text color to black */
                    background-color: rgba(255, 255, 255, 0.8); /* Optional: Add a background to increase contrast */
                    padding: 10px; /* Optional: Add padding */
                    border-radius: 5px; /* Optional: Round the corners */
                    display: none; /* Hide the submenu initially */
                }

                .submenu a {
                    color: black; /* Ensure links in submenu are also black */
                    text-decoration: none; /* Optional: Remove underline from links */
                }

                .submenu a:hover {
                    text-decoration: underline; /* Optional: Underline on hover */
                }
            </style>
        </code>
    </pre>
</details>

<h2>Part 1 - Fundamentals (Quick Review)</h2>

<div class="submenu">
    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-1">3.1 Variables</a></summary>
        <ul>
            <li>Variables store information that can be reused and changed.</li>
            <li>Data types include integers, floats, strings, and booleans.</li>
            <li>Use descriptive names to make your code easier to understand.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-2/">3.2 Data Abstraction</a></summary>
        <ul>
            <li>Data abstraction hides complex details, making code easier to manage.</li>
            <li>Functions and data structures simplify repetitive tasks.</li>
            <li>Helps in managing large data sets by breaking them down into simpler parts.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-3">3.3 Mathematical Expressions</a></summary>
        <ul>
            <li>Operators: +, -, *, /, % (modulus) for calculations.</li>
            <li>Order of operations: parentheses, exponents, multiplication/division, addition/subtraction (PEMDAS).</li>
            <li>Use math libraries for complex calculations like square roots and exponents.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-4">3.4 Strings</a></summary>
        <ul>
            <li>Strings are sequences of characters, used for text manipulation.</li>
            <li>Common methods: slicing, concatenation, and formatting.</li>
            <li>Escape characters like \n (newline) and \t (tab) help format output.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-5">3.5 Booleans</a></summary>
        <ul>
            <li>Booleans represent True or False values.</li>
            <li>Comparison operators: ==, !=, >, <, >=, <= to compare values.</li>
            <li>Boolean logic: AND, OR, NOT used to combine conditions.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-6">3.6 Conditionals</a></summary>
        <ul>
            <li>If-else statements control the flow of the program based on conditions.</li>
            <li>Conditions evaluate to True or False.</li>
            <li>Nested conditionals allow multiple decisions based on different conditions.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-7">3.7 Nested Conditionals</a></summary>
        <ul>
            <li>Use nested if statements to handle multiple layers of conditions.</li>
            <li>Important to maintain proper indentation to avoid confusion.</li>
            <li>Can replace deep nesting with logical operators for simplicity.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-8">3.8 Iteration</a></summary>
        <ul>
            <li>Loops (for, while) allow repetition of tasks until conditions are met.</li>
            <li>For loops iterate over sequences like lists or ranges.</li>
            <li>While loops continue until a condition is False.</li>
        </ul>
    </details>

    <details>
        <summary><a href="https://nighthawkcoders.github.io/portfolio_2025/csp/big-idea/p2/3-10">3.10 Lists</a></summary>
        <ul>
            <li>Lists store multiple items in a single variable.</li>
            <li>Common operations: append, remove, sort, and slicing.</li>
            <li>Useful for storing collections of data like names, numbers, etc.</li>
        </ul>
    </details>
</div>

<style>
    h2 {
        font-size: 2em;
        color: #333;
        margin-top: 20px;
        text-align: center;
    }

    .submenu {
        font-family: 'Poppins', sans-serif;
        max-width: 800px;
        margin: 30px auto;
        background-color: #f0f4f7;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    details {
        margin-bottom: 20px;
    }

    summary {
        font-size: 1.5em;
        cursor: pointer;
        padding: 10px;
        background-color: #0072ff;
        color: white;
        border-radius: 5px;
        margin-bottom: 5px;
        text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        transition: background-color 0.3s ease;
    }

    summary:hover {
        background-color: #0056b3;
    }

    ul {
        list-style-type: disc;
        margin-left: 20px;
        margin-top: 10px;
    }

    li {
        font-size: 1.1em;
        margin-bottom: 5px;
    }
</style>


