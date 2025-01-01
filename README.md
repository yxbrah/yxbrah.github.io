<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Data Analyst Portfolio</title>
    <style>
        body {
            font-family: 'Courier New', Courier, monospace;
            background-color: #000;
            color: #fff;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        header, footer {
            background: linear-gradient(90deg, #1a1a1a, #333);
            text-align: center;
            padding: 15px 0;
            color: #fff;
            box-shadow: 0 2px 5px rgba(255, 255, 255, 0.2);
        }
        nav ul {
            list-style: none; padding: 0; display: flex; justify-content: center;
        }
        nav ul li {
            margin: 0 15px;
        }
        nav ul li a {
            color: #fff; text-decoration: none; font-weight: bold; cursor: pointer;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #00e6e6;
        }
        section {
            display: none; padding: 40px; margin: 20px auto; max-width: 800px;
            background: #1a1a1a; border-radius: 10px; box-shadow: 0 4px 10px rgba(255, 255, 255, 0.2);
        }
        section.active {
            display: block;
        }
        h1, h2, h3 { color: #00e6e6; }
        .project a, .form-container button {
            padding: 10px 20px; background: #00e6e6; color: #000; text-decoration: none;
            border-radius: 8px; font-weight: bold; transition: 0.3s;
        }
        .project a:hover, .form-container button:hover {
            background: #fff; color: #00e6e6;
        }
        .form-container input {
            margin: 10px 0; padding: 10px; width: 80%; max-width: 400px; color: #fff;
            background: #000; border: 1px solid #00e6e6; border-radius: 5px;
        }
        .form-container input:focus {
            outline: none; border-color: #fff;
        }
        #cursor {
            position: fixed; top: 0; left: 0; width: 20px; height: 20px;
            background: #00e6e6; border-radius: 50%; pointer-events: none;
            transform: translate(-50%, -50%); z-index: 9999; box-shadow: 0 0 10px #00e6e6;
            transition: transform 0.1s ease;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", () => {
            const cursor = document.createElement("div");
            cursor.id = "cursor";
            document.body.appendChild(cursor);

            document.querySelectorAll("nav ul li a").forEach((link, index) => {
                link.addEventListener("click", () => {
                    document.querySelectorAll("section").forEach(section => section.classList.remove("active"));
                    document.querySelectorAll("section")[index].classList.add("active");
                });
            });

            document.addEventListener("mousemove", e => {
                cursor.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
            });
        });
    </script>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a>Home</a></li>
                <li><a>About</a></li>
                <li><a>Projects</a></li>
                <li><a>Contact</a></li>
                <li><a>Sign Up</a></li>
            </ul>
        </nav>
    </header>

    <section class="active">
        <h1>Welcome to My Portfolio</h1>
        <p>Explore my work, projects, and insights in the world of data analytics.</p>
    </section>

    <section>
        <h1>About Me</h1>
        <p>Hi, I'm [Your Name], a passionate data analyst with experience in uncovering insights from data and creating impactful visualizations.</p>
    </section>

    <section>
        <h2>Projects</h2>
        <div class="project">
            <h3>Project 1: Sales Analysis Dashboard</h3>
            <p>A dashboard built with Power BI to analyze sales performance over time.</p>
            <a href="https://github.com/yourusername/project1" target="_blank">View Project</a>
        </div>
        <div class="project">
            <h3>Project 2: Customer Segmentation</h3>
            <p>A Python-based project to segment customers using machine learning techniques.</p>
            <a href="https://github.com/yourusername/project2" target="_blank">View Project</a>
        </div>
        <div class="project">
            <h3>Project 3: E-commerce Data Analysis</h3>
            <p>An in-depth analysis of e-commerce data to identify trends and optimize marketing strategies.</p>
            <a href="https://github.com/yourusername/project3" target="_blank">View Project</a>
        </div>
    </section>

    <section>
        <h2>Contact</h2>
        <p>If you'd like to connect, feel free to reach out to me via email or LinkedIn.</p>
        <ul>
            <li>Email: <a href="mailto:your.email@example.com">your.email@example.com</a></li>
            <li>LinkedIn: <a href="https://linkedin.com/in/yourprofile" target="_blank">yourprofile</a></li>
        </ul>
    </section>

    <section>
        <h2>Sign Up</h2>
        <div class="form-container">
            <form>
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <button type="submit">Submit</button>
            </form>
        </div>
    </section>

    <footer>
        &copy; 2025 My Portfolio
    </footer>
</body>
</html>
