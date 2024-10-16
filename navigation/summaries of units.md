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



