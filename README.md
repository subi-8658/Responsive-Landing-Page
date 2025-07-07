# Responsive-Landing-Page
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Landing Page</title>
  <style>
    /* Reset default */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Navbar Styles */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: #1a1a2e;
      color: white;
      padding: 15px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: background-color 0.3s ease;
      z-index: 1000;
    }

    .navbar.scrolled {
      background-color: #0f3460;
    }

    .logo {
      font-size: 1.5em;
      font-weight: bold;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    .nav-links li a {
      color: white;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    .nav-links li a:hover {
      color: #ffcc00;
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: linear-gradient(to right, #16213e, #0f3460);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 50px;
      padding-top: 120px;
    }

    .hero h1 {
      font-size: 3em;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 1.2em;
      max-width: 700px;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .nav-links {
        flex-direction: column;
        gap: 10px;
      }

      .hero h1 {
        font-size: 2em;
      }

      .hero p {
        font-size: 1em;
      }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header class="navbar" id="navbar">
    <div class="logo">Prodigy InfoTech</div>
    <nav>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">Features</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <h1>Responsive Landing Page</h1>
    <p>Create an interactive navigation menu that changes color or style when scrolled or hovered.</p>
  </section>

  <!-- Script -->
  <script>
    window.addEventListener("scroll", function () {
      const navbar = document.getElementById("navbar");
      navbar.classList.toggle("scrolled", window.scrollY > 50);
    });
  </script>

</body>
</html>
