Description
This is a personal portfolio website built to showcase your skills, education, and projects. 
It is fully responsive and contains interactive elements such as a navigation bar with a hamburger menu for smaller screens, an animated hero section, and contact form integration.

Table of Contents
Description
Technologies Used
Project Structure
Features
Code Documentation
HTML
CSS
JavaScript
Setup Instructions
Contact Information

Technologies Used
HTML5
CSS3
JavaScript (ES6)
Responsive Design (media queries, flexbox)
EmailJS for form submission

Project Structure
Portfolio Website/
│
├── index.html          # Main HTML file
├── css/
│   └── myport.css      # Stylesheet for the project
├── js/
│   └── myport.js       # JavaScript file for interactive elements
└── images/
    └── profile.jpg     # Example image files
Features
Responsive Design: Works on desktop, tablet, and mobile devices using media queries.
Interactive Hamburger Menu: Appears on smaller screens and toggles the navigation menu.
Hero Section with Call to Action: Buttons for actions like "Hire Me" and "Get Resume."
Skills and Education: Displays skills and educational qualifications in card-like components.
Contact Form: Users can fill in their name, email, and message, integrated with EmailJS.
Footer with Social Links: Links to various social media profiles and sites.

Code Documentation
HTML
The index.html file contains the structure of the portfolio website, 
divided into sections such as the navigation bar, hero, about, education, skills, projects, and contact. Each section is wrapped inside div elements for easier styling.
<header>
  <nav class="navbar">
    <div class="logo">
      <h1 class="logo-heading">Your Logo</h1>
    </div>
    <ul class="menu">
      <li class="menu-list-items"><a href="#about">About</a></li>
      <li class="menu-list-items"><a href="#skills">Skills</a></li>
      <li class="menu-list-items"><a href="#projects">Projects</a></li>
      <li class="menu-list-items"><a href="#contact">Contact</a></li>
    </ul>
    <div id="hamburger" class="hamburger">
      <span class="hamburger-icon">☰</span>
      <span class="cross-icon" style="display: none;">✖</span>
    </div>
  </nav>
</header>
CSS
The myport.css file styles each section with modern and responsive design principles. It uses flexbox for layout and media queries for responsiveness. The hero section includes a full-screen background image, while other sections like skills and education are laid out in grid-like containers.

Example of CSS styling for the navbar:
.navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    top: 0;
    width: 100%;
    background-image: linear-gradient(90deg, #74D7BB, #53C8B6, #35A99C);
}

.menu .menu-list {
    display: flex;
    list-style: none;
}

.hamburger {
    display: none;
    color: #fff;
    font-size: 25px;
}
JavaScript
The myport.js file handles interactivity for the site, primarily focusing on the hamburger menu that appears on smaller screens. The following script toggles between showing and hiding the menu items when the hamburger icon is clicked.
const hamburger = document.getElementById('hamburger');
const menu = document.querySelector('.menu');

hamburger.addEventListener('click', function () {
    const hamIcon = this.querySelector('.hamburger-icon');
    const crossIcon = this.querySelector('.cross-icon');
    if (hamIcon.style.display === "none") {
        hamIcon.style.display = "inline-block";
        menu.style.display = "none";
        crossIcon.style.display = "none";
    } else {
        crossIcon.style.display = "inline-block";
        hamIcon.style.display = "none";
        menu.style.display = "block";
    }
});


