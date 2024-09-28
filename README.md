<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
    <style>
        /* Basic styling */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color:darkred;
        }
        h1, h2 {
            color: #2c3e50;
        }
        section {
            margin-bottom: 20px;
            display: none; /* Initially hide sections */
        }
        a {
            color: #2980b9;
            text-decoration: none;
            cursor: pointer;
        }
        a:hover {
            color: #e74c3c;
        }
    </style>
</head>
<body>

    <h1>Welcome to My Home Page</h1>
    <p>Navigate through different sections below to find information about my education, experience, and projects.</p>

    <!-- Links to trigger showing sections -->
    <ol>
        <li><a id="showEducation">Education<img src="https://png.pngtree.com/png-clipart/20190516/original/pngtree-education-logo-vector-image-png-image_4092981.jpg" height="100"></a> <span class="abbreviation">(DE)</span></li>
        <li><a id="showskills">skills<img src="https://w7.pngwing.com/pngs/478/306/png-transparent-soft-skills-technology-engineer-science-technology-electronics-label-logo.png" height="90"></a> <span class="abbreviation">(DE)</span></li>
        <br>
        <li><a id="showProjects">Projects<img src="https://cdn.textstudio.com/output/sample/normal/9/1/6/5/project-logo-321-5619.png" width="100"></a> <span class="abbreviation">(DE)</span></li>
    </ol>

    <!-- Sections that will be shown dynamically -->
    <section id="educationSection">
        <h2>Education</h2>
        <p>Here is the information about my education:</p>
        <ol>
            <li>I have completed my bachelor's degree in BVRIT-Narsapur </li>
            <br>
            <a href="home page.html">back to home page</a>
        </ol>
    </section>

    <section id="skillsSection">
        <h2>Experience</h2>
        <p>Here is the information about my skills:</p>
        <ol>
            <li>HTML.</li>
            <li>JAVa.</li>
            <li>SQL.</li>
            <br>
            <a href="home page.html">back to home page</a>
        </ol>
    </section>

    <section id="projectsSection">
        <h2>Projects</h2>
        <p>Here is the information about my projects:</p>
        <ol>
            <li>Project 1: generating of electricity from waste materials by using Aurdino UNO and GSM module.</li>
            <li>Project 2:Ai physio speak.</li>
            <br>
            <a href="home page.html">back to home page</a>
        </ol>
    </section>

    <!-- JavaScript for toggling visibility -->
    <script>
        // Get the links and sections
        const showEducation = document.getElementById('showEducation');
        const showskills = document.getElementById('showskills');
        const showProjects = document.getElementById('showProjects');
        
        const educationSection = document.getElementById('educationSection');
        const skillsSection = document.getElementById('skillsSection');
        const projectsSection = document.getElementById('projectsSection');

        // Add event listeners to links to show respective sections
        showEducation.addEventListener('click', function() {
            educationSection.style.display = 'block'; // Show Education section
            skillsSection.style.display = 'none'; // Hide others
            projectsSection.style.display = 'none';   // Hide others
        });

        showskills.addEventListener('click', function() {
            educationSection.style.display = 'none';  // Hide others
            skillsSection.style.display = 'block'; // Show Experience section
            projectsSection.style.display = 'none';   // Hide others
        });

        showProjects.addEventListener('click', function() {
            educationSection.style.display = 'none';  // Hide others
            skillsSection.style.display = 'none'; // Hide others
            projectsSection.style.display = 'block';  // Show Projects section
        });
    </script>

</body>
</html>
