html, body {
    height: 100%;
    margin: 0;
    padding: 0;
    overflow-x: hidden; /* Prevent horizontal overflow */
    font-family: Arial, sans-serif;
    font-size: 120%; /* Increase the base font size by 20% */
    scroll-behavior: smooth; /* Enable smooth scrolling */
}

.background-image {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('back4.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    z-index: -1; /* Ensure the background image is behind the content */
}

.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.7);
    z-index: 2; /* Ensure the navbar is above the background image and content */
    padding: 10px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.navbar .logo {
    margin-left: 20px;
}

.navbar .logo img {
    width: 50px; /* Adjust the size of the logo */
    height: auto;
}
.navbar ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    gap: 20px;
}

.navbar li {
    display: inline;
    position: relative; /* Needed for the dropdown */
}

.navbar a {
    color: white;
    text-decoration: none;
    font-size: 16px;
    padding: 10px 20px;
    display: block;
}

.navbar a:hover {
    background: rgba(255, 255, 255, 0.2);
    border-radius: 5px;
}

.content {
    position: relative;
    z-index: 1; /* Ensure the content is above the background image */
    color: white;
    text-align: center;
    padding: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Full viewport height */
}

.highlight {
    background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black background */
    display: inline-block; /* Adjusts the background to the width of the text */
    padding: 10px 20px; /* Adds padding around the text */
    border-radius: 5px; /* Optional: Adds rounded corners */
    overflow: hidden; /* To hide the sliding effect overflow */
    position: relative; /* For positioning the sliding effect */
}

.slide-in::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: white;
    animation: slide-in 2s ; /* Continuous animation */
}

@keyframes slide-in {
    to {
        left: 100%;
    }
}

h3 {
    margin: 0;
    font-weight: normal;
    color: rgb(255, 255, 255); /* Change font color to a more appealing color */
    font-family: "Arial", sans-serif; /* Change font family to a more attractive type */
    font-size: 24px; /* Adjust font size */
    opacity: 0; /* Start with opacity 0 for smooth animation */
    animation: fade-in 2s ease-in-out forwards; /* Smooth fade-in animation */
    animation-delay: 2s; /* Delay before starting the animation again */
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

/* Dropdown styles */
.dropdown {
    position: relative;
}

.dropdown-content {
    display: none;
    position: left;
    left: 0; /* Align dropdown content to the left */
    background-color: rgba(0, 0, 0, 0.7);
    min-width: 200px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 3;
}

.dropdown-content a {
    color: white;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 5px;
}

.dropdown:hover .dropdown-content {
    display: block;
}

/* Section styles */

.section {
    
    padding: 60px 20px;
    text-align: center;
    margin-top: auto; 
    margin-left: auto;
    margin-right: auto;
    background-color: rgba(0, 0, 0, 0.5); 
    border-radius: 20px; 
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); 
    transition: all 0.5s ease; /* Add transition for smooth animation */
    width: 800px;
    color: white;
}

#home, #about, #service1, #service2, #service3, #project1, #project2, #project3, #address {
    margin-top: 100px; /* Additional spacing for better visual separation */
}

h2, h3, p {
    margin-bottom: 20px; /* Add spacing between headings and paragraphs */
}

/* Smooth rounded boxes for content */
.content-box {
    background-color: rgba(0, 0, 0, 0.5); /* Background color for content boxes */
    border-radius: 10px; /* Rounded corners for content boxes */
    padding: 20px; /* Padding for content boxes */
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1); /* Optional: Adds a shadow effect */
    color: rgb(255, 252, 252);
    align-items: center;
    transition: all 0.5s ease; /* Add transition for smooth animation */
}

h2 {
  color: rgb(163, 163, 224);
}

.section:hover, .content-box:hover {
    transform: scale(1.05); /* Scale up slightly on hover */
}

.logo-final {
    margin-bottom: -300px; /* Adjust this value to decrease the distance */
    margin-top: 170px;
    opacity: 0; /* Start with opacity 0 for smooth animation */
    animation: fade-in 2s ease-in-out forwards; /* Smooth fade-in animation */
    animation-delay: 2s; /* Delay before starting the animation again */
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CONSTRUCTIONS AND DEVELOPERS</title>
    <link rel="stylesheet" href="prac1.css">
</head>
<body>
    <div class="logo-final">
        <center>   
        <img src="logo-final.png" alt="Logo-final" width="300" height="300">
        </center>
    </div>
    <div class="background-image"></div>
    <nav class="navbar">
        <div class="logo">
            <img src="logo-final.png" alt="Logo">
        </div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About Us</a></li>
            <li class="dropdown">
                <a href="#services" class="dropbtn">Services</a>
                <div class="dropdown-content">
                    <a href="#service1">Architectural Design</a>
                    <a href="#service2">Construction Management</a>
                    <a href="#service3">Renovation and Remodeling</a>
                </div>
            </li>
            <li class="dropdown">
                <a href="#projects" class="dropbtn">Projects</a>
                <div class="dropdown-content">
                    <a href="#project1">Residential Complex</a>
                    <a href="#project2">Commercial Building</a>
                    <a href="#project3">Industrial Park</a>
                </div>
            </li>
            <li class="dropdown">
                <a href="#contact" class="dropbtn">Contact Us</a>
                <div class="dropdown-content">
                    <a href="mailto:contact@narayanaconstructors.com">Email: ncb@narayanaconstructors.com</a>
                    <a href="tel:+1234567890">Phone: 9386582658</a>
                    <a href="#address">Address: 123 Builder Street, Banglore , India</a>
                </div>
            </li>
        </ul>
    </nav>
    <div class="content">
        <h1 class="highlight slide-in">NARAYANA CONSTRUCTORS AND BUILDERS</h1>
        <center>
            <h3>"We just don't construct we create homes, shape cities, and build futures"</h3>
        </center> 
    </div>

    <!-- Home Section -->
    <section id="home" class="section">
        <h2>Welcome to Narayana Constructors and Builders</h2>
        <p>At Narayana Constructors and Builders, we are dedicated to creating not<br>just buildings but homes and spaces that shape the future. With years of<br>experience in the construction industry, we pride ourselves on our<br>commitment to quality, innovation, and customer satisfaction.</p>
    </section>

    <!-- About Us Section -->
    <section id="about" class="section">
        <h2>About Us</h2>
        <p>Narayana Constructors and Builders was founded with the vision to transform<br>the construction landscape by integrating cutting-edge technology,<br>sustainable practices, and a customer-centric approach. Our team of<br>experienced professionals is passionate about delivering projects that exceed<br>expectations and create lasting value for our clients and communities.</p>
    </section>

    <!-- Services Section -->
    <section id="service1" class="section">
        <h2>Architectural Design</h2>
        <p>Our architectural design services bring your vision to life with<br>innovative and sustainable solutions.</p>
    </section>
    <section id="service2" class="section">
        <h2>Construction Management</h2>
        <p>We provide comprehensive construction management services to ensure<br>your project is completed on time and within budget.</p>
    </section>
    <section id="service3" class="section">
        <h2>Renovation and Remodeling</h2>
        <p>Transform your existing spaces with our expert renovation<br>and remodeling services.</p>
    </section>

    <!-- Projects Section -->
    <section id="project1" class="section">
        <h2>Residential Complex</h2>
        <p>Our residential complex projects are designed to provide<br>comfortable and sustainable living spaces.</p>
    </section>
    <section id="project2" class="section">
        <h2>Commercial Building</h2>
        <p>We specialize in building modern commercial spaces that<br>meet the needs of today's businesses.</p>
    </section>
    <section id="project3" class="section">
        <h2>Industrial Park</h2>
        <p>We specialize in building Industrial Park that<br>meet the needs of today's businesses.</p>
    </section>
</body>
</html>


