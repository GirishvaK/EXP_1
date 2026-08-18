# Ex01 Portfolio
## Date:

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
portfolio.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vignesh | Portfolio</title>
    <link rel="stylesheet" href="style1.css">
    <style>
        

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: url("ai\ back.jpg") no-repeat center center fixed;
            background-size: cover;
            background-attachment: fixed;
            position: relative;
            z-index: 1;
        }

        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.75);
            z-index: -1;
        }

        header {
            background-color: #0d47a1;
            color: white;
            padding: 15px 0;
            text-align: center;
        }

        section {
            background: white;
            margin: 20px auto;
            padding: 20px;
            width: 80%;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            
        }


        h2 {
            color: #0d47a1;
            border-bottom: 2px solid #bbdefb;
            padding-bottom: 5px;
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #0d47a1;
            display: block;
            margin: -60px auto 20px;
            transition: transform 0.3s ease-in-out;
        }

        .profile-pic:hover {
            transform: scale(1.05);
        }

        .project {
            background: #f1f8ff;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 15px;
        }

        footer {
            text-align: center;
            background-color: #0d47a1;
            color: white;
            padding: 10px 0;
            margin-top: 20px;
        }
    </style>
</head>
<body>

<header>
    <h1>Vignesh </h1>
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#internship">Internship</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<section id="about">
    <h2>About Me</h2>
    <img src="img1.png" alt="Vignesh " class="profile-pic">
    <p>Hi! I'm Vignesh , Computer Science student passionate about building innovative tech solutions that make a real-world impact. I specialize in AI-driven applications, full-stack development, and cloud-based architectures. I enjoy working on challenging problems, learning cutting-edge technologies, and turning creative ideas into functional, user-friendly products.</p>
</section>

<section id="projects">
    <h2>Projects</h2>
    <div class="project">
        <h3>Voice-Powered Task Manager</h3>
        <p>Created a productivity app that uses speech recognition to create, update, and track tasks hands-free. Built with React.js, Node.js, and the Web Speech API, enabling voice-based interaction for improved accessibility.</p>
    </div>
    <div class="project">
        <h3>AI-Powered Travel Planner</h3>
        <p>Developed an AI assistant that generates personalized travel itineraries based on user preferences, budget, and weather forecasts. Implemented using Python, Flask, and OpenAI API.</p>
    </div>
    <div class="project">
        <h3>Blockchain-Based Certificate Verification</h3>
        <p>Designed a decentralized platform for storing and verifying academic certificates securely on the blockchain. Tech stack includes Solidity, Ethereum, and Web3.js.</p>
    </div>
</section>

<section id="internship">
    <h2>Internship Experience</h2>
    <p><strong>CloudSphere Technologies | 2024</strong></p>
    <p>Worked on deploying scalable microservices using Kubernetes and Docker, integrating AI-based analytics for system monitoring, and optimizing cloud costs using AWS and GCP tools.</p>
</section>

<section id="education">
    <h2>Education</h2>
    <p><strong>B.E Computer Science and Engineering</strong><br>Saveetha Engineering College (2024-2028)<br>CGPA: 7.9/10</p>
    <p><strong>Higher Secondary Education</strong><br>Sri chaitanya techno School (2022-2023)<br>Percentage: 86%</p>
</section>

<section id="skills">
    <h2>Skills</h2>
    <h3>Technical Skills</h3>
    <ul>
        <li>Programming: Python, Java, JavaScript, Go</li>
        <li>Web Development: React.js, Next.js, Spring Boot, Node.js</li>
        <li>AI/ML: TensorFlow, PyTorch, NLP, Computer Vision</li>
        <li>Cloud & DevOps: AWS, GCP, Docker, Kubernetes</li>
    </ul>
    <h3>Soft Skills</h3>
    <ul>
        <li>Analytical Thinking, Public Speaking, Time Management, Team Collaboration</li>
    </ul>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: vignesh.7@example.com</p>
    <p>Address: Chittoor, Andhra Pradesh, India</p>
    <p>Phone: +91-9515154632</p>
    <p>GitHub: <a href="#">github.com/vignesh757</a></p>
    <p>LinkedIn: <a href="#">linkedin.com/in/vignesh757</a></p>
</section>

<footer>
    <p>&copy; 2026 paladi venkatesh vignesh. All Rights Reserved.</p>
</footer>
```
style.css
```
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
    color: #333;
}

header {
    background-color: #0073e6;
    color: white;
    padding: 15px 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
    gap: 20px;
}

nav ul li {
    display: inline;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

section {
    padding: 20px;
    margin: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    text-align: center;
}

.project {
    background-color: #e6f2ff;
    padding: 15px;
    border-radius: 8px;
    margin: 10px 0;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #0073e6;
    color: white;
    position: relative;
    bottom: 0;
    width: 100%;
}


.profile-pic {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid white;
    margin-top: -40px; 
}

```

## OUTPUT
<img width="1757" height="672" alt="633056105-3b62a84c-3701-4368-9980-ae1d43b56175" src="https://github.com/user-attachments/assets/8ea15fec-7399-43f7-a36f-3c9cd4fc9ecf" />
<img width="1787" height="757" alt="633055841-716e65f3-3d89-4ab2-b91a-380c9af26237" src="https://github.com/user-attachments/assets/10e9f3b4-fa93-4d6c-929b-3caab85f081e" />
<img width="1756" height="896" alt="image" src="https://github.com/user-attachments/assets/f70aeb29-00fa-4d38-a293-f661db81288a" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
