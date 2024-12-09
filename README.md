# SCT_WD_01

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Navigation Menu</title>
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Times New Roman', 'Times, serif';
      line-height: 1.6;
    }

    /* Navbar Styling */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background-color: #333;
      z-index: 1000;
      transition: background-color 0.3s ease;
    }

    .nav-menu {
      display: flex;
      justify-content: center;
      padding: 10px 0;
      list-style: none;
    }

    .nav-menu li {
      margin: 0 15px;
    }

    .nav-menu a {
      text-decoration: none;
      color: white;
      font-size: 18px;
      transition: color 0.3s ease;
    }

    .nav-menu a:hover {
      color: #00bcd4;
      text-decoration: underline;
    }

    /* Change Navbar Background on Scroll */
    .navbar.scrolled {
      background-color: #222;
    }

    /* Content Sections */
    .content section {
      height: 100vh;
      padding: 40px 20px;
      text-align: center;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
    .home {
      padding: 20px;
      transition: 3s;
    }
    #home {
      background: #FCC737;
      transition-duration: 3s ;
    }

    #about {
      background: #F26B0F;
      transition-duration: 3s;
    }

    #services {
      background: #E73879;
      transition-duration: 3s;
    }

    #contact {
      background: #7E1891;
      transition-duration: 3s;
    }

    /* Section Content Styling */
    .section-content {
      width: 80%;
      max-width: 900px;
      margin-top: 20px;
      font-size: 18px;
      line-height: 1.6;
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <ul class="nav-menu">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <div class="content">
    <section id="home">
      <h1>Welcome to the Home Section</h1>
      <div class="section-content">
        <p>This is the home section. Here, you'll find an introduction to the website and an overview of what we offer. We aim to provide the best services for all your needs. Scroll down to explore more!</p>
      </div>
    </section>

    <section id="about">
      <h1>About Us</h1>
      <div class="section-content">
        <p>Learn more about our company and the team behind it. We are committed to providing top-notch services and creating meaningful experiences for our customers. Our expertise spans various domains, ensuring we meet your expectations every time.</p>
      </div>
    </section>

    <section id="services">
      <h1>Our Services</h1>
      <div class="section-content">
        <p>We offer a wide range of services tailored to meet your specific needs. Whether you’re looking for web development, design solutions, or consultation, we’ve got you covered. Explore our services and see how we can help you achieve your goals.</p>
      </div>
    </section>

    <section id="contact">
      <h1>Contact Us</h1>
      <div class="section-content">
        <p>Have any questions or want to get in touch? Reach out to us via the contact form or email. We look forward to hearing from you and working together on exciting projects!</p>
      </div>
    </section>
  </div>

  <script>
    // Select the navbar
    const navbar = document.querySelector('.navbar');

    // Add event listener for scroll
    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    });
  </script>

</body>
</html>
