---
layout: page
title: End of Course Review
permalink: /eoc/
---

{% include nav/eoc.html %}

<div class="eoc-container">
    <div class="welcome-section">
        <h1>🎓 End of Course Review</h1>
        <p class="intro-text">Welcome to your comprehensive end of course review! This page serves as a central hub for all your course accomplishments, learnings, and project showcases.</p>
    </div>

    <div class="content-grid">
        <div class="card">
            <h2>📚 Course Overview</h2>
            <p>Explore the major projects and milestones we've covered throughout the course:</p>
            <ul>
                <li>Website Development Journey</li>
                <li>Programming Fundamentals</li>
                <li>Project-Based Learning</li>
                <li>Technical Skills Development</li>
            </ul>
            <a href="{{site.baseurl}}/overview" class="button">View Overview</a>
        </div>

        <div class="card">
            <h2>✅ Homework Certification</h2>
            <p>Review your completed assignments and achievements:</p>
            <ul>
                <li>Completed Assignments</li>
                <li>Learning Milestones</li>
                <li>Skill Development Progress</li>
            </ul>
            <a href="{{site.baseurl}}/homework" class="button">View Certifications</a>
        </div>

        <div class="card">
            <h2>🌟 Student Showcase</h2>
            <p>Check out the amazing work created by students:</p>
            <ul>
                <li>Project Highlights</li>
                <li>Innovative Solutions</li>
                <li>Creative Implementations</li>
            </ul>
            <a href="{{site.baseurl}}/showcase" class="button">View Showcase</a>
        </div>
    </div>

    <div class="skills-section">
        <h2>🛠️ Skills Acquired</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>Programming Languages</h3>
                <ul>
                    <li>Python</li>
                    <li>JavaScript</li>
                    <li>HTML/CSS</li>
                </ul>
            </div>
            <div class="skill-category">
                <h3>Development Tools</h3>
                <ul>
                    <li>GitHub</li>
                    <li>VSCode</li>
                    <li>Jupyter Notebooks</li>
                </ul>
            </div>
            <div class="skill-category">
                <h3>Key Concepts</h3>
                <ul>
                    <li>Pair Programming</li>
                    <li>Project Management</li>
                    <li>Web Development</li>
                </ul>
            </div>
        </div>
    </div>

    <style>
        .eoc-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .welcome-section {
            text-align: center;
            margin-bottom: 40px;
        }

        .intro-text {
            font-size: 1.2em;
            color: #666;
            max-width: 800px;
            margin: 0 auto;
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .card {
            background: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h2 {
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .card ul {
            list-style-type: none;
            padding-left: 0;
        }

        .card li {
            margin: 10px 0;
            padding-left: 20px;
            position: relative;
        }

        .card li:before {
            content: "•";
            position: absolute;
            left: 0;
            color: #3498db;
        }

        .button {
            display: inline-block;
            padding: 10px 20px;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 15px;
            transition: background 0.3s ease;
        }

        .button:hover {
            background: #2980b9;
        }

        .skills-section {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 10px;
            margin-top: 40px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .skill-category {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .skill-category h3 {
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .skill-category ul {
            list-style-type: none;
            padding-left: 0;
        }

        .skill-category li {
            margin: 8px 0;
            padding-left: 20px;
            position: relative;
        }

        .skill-category li:before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #27ae60;
        }
    </style>
</div>

