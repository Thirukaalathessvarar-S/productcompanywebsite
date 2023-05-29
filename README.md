# Web Design for a Software Product Company

## AIM:

To design a static website for a software product company company.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Updating the sample content.

### Step 4:

Choose the appropriate style and color scheme.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
index.html
```
<!DOCTYPE html>
<html>
<head>
  <title>CISUM Tees</title>
  <link rel="stylesheet" type="text/css" href="style.css">
  <style>
    /* Add your custom styles here */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f8e7d8;
    }
  
    /* Add your custom styles here */
  
    .banner {
      margin: 0;
      padding: 0;
      background-image: linear-gradient(to top right, rgba(228,221,221, 0.50) 20%, rgba(0,0,0, 0.60 ) 25%), url(Eswar.png);
      background-position: top;
      background-size: cover;
      background-repeat: no-repeat;
      height: 555px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  
    .banner-button {
      font-size: 18px;
      background-color: #ff5c5c;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 4px;
      cursor: pointer;
      text-transform: uppercase;
      transition: background-color 0.3s ease;
    }
  
    .banner-button:hover {
      background-color: #ff4242;
    }
  
    main {
      padding: 40px;
    }
  
    section {
      margin-bottom: 40px;
    }
  
    h2 {
      font-size: 32px;
      margin-bottom: 20px;
    }
  
    .product-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 20px;
    }
  
    .product {
      text-align: center;
    }
  
    .product img {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
      border-radius: 4px;
      margin-bottom: 10px;
    }
  
    .person-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 20px;
    }
  
    .person {
      text-align: center;
    }
  
    .person img {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
      border-radius: 50%;
      margin-bottom: 10px;
    }
  
    address {
      font-style: normal;
      margin-bottom: 10px;
    }
  
    footer {
      background-color: #333;
      color: #fff;
      padding: 20px;
      text-align: center;
    }

    /* Menu styles */
    .menu-icon {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 60px;
      height: 40px;
      cursor: pointer;
      position: absolute;
      top: 20px;
      left: 20px;
      z-index: 9999;
    }
  
    .menu-line {
      width: 100%;
      height: 2px;
      background-color: #000;
      margin-bottom: 4px;
    }
  
    .menu {
      display: none;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      z-index: 999;
    }
  
    .menu.open {
      display: block;
    }
  
    .menu ul {
      list-style: none;
      padding: 0;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  
    .menu ul li {
      margin-bottom: 10px;
    }
  
    .menu ul li a {
      text-decoration: none;
      color: #fff;
    }

    .footer-column {
      text-align: center;
    }

    .footer-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .social-media-list {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 10px;
    }

    .social-media-list li {
      margin-right: 10px;
    }

    .social-media-list li:last-child {
      margin-right: 0;
    }

    .social-media-list li a {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: #fff;
    }

    .social-media-list li a img {
      width: 20px;
      height: 20px;
      margin-right: 5px;
    }

    .terms-list {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 10px;
    }

    .terms-list li {
      margin-right: 10px;
    }

    .terms-list li:last-child {
      margin-right: 0;
    }

    .terms-list li a {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: #fff;
    }

    .terms-list li a img {
      width: 20px;
      height: 20px;
      margin-right: 5px;
    }
  </style>
</head>
<body>
  <div class="banner">
    <div>
      <div class="banner-content">
        <h1 class="banner-title">
          <span class="highlight">WELCOME ! </span>
        </h1>
        <h5 class="banner-subtitle">Click on the below button to get started into CISUM fashion world</h5>
        <button class="banner-button" onclick="toggleRegistrationForm()">Get started</button>
        <!-- Registration Form -->
        <div class="registration-form" id="registrationForm">
          <div class="registration-form-inner">
            <h2>Create Account</h2>
            <form>
              <label for="username">Username</label>
              <input type="text" id="username" name="username" required>

              <label for="password">Password</label>
              <input type="password" id="password" name="password" required>

              <button type="submit">Sign Up</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script>
    function toggleRegistrationForm() {
      const registrationForm = document.getElementById("registrationForm");
      registrationForm.classList.toggle("open");
    }
  </script>

  <header>
    <div class="menu-icon" onclick="document.querySelector('.menu').classList.toggle('open')">
      <div class="menu-line"></div>
      <div class="menu-line"></div>
      <div class="menu-line"></div>
      <span>Menu</span>
    </div>
    <div class="menu">
      <ul>
        <li><a href="basictees.html">Basic Tees</a></li>
        <li><a href="oversized-tshirt.html">Oversized T-Shirt</a></li>
        <li><a href="polo-shirt.html">Polo Shirt</a></li>
      </ul>
    </div>
  </header>
  <section>
    <h2>Featured People</h2>
    <div class="person-grid">
      <div class="person">
        <img src="person1.jpg" alt="Person 1">
        <h3>Eswar musk & Lingesh bezos</h3>
        <address>32, lol colony, North area, Chennai - India</address>
      </div>
      <!-- Add more person elements here -->
    </div>
  </section>

  <footer>
    <div class="footer-content">
      <div class="footer-column">
        <h4>Social Media</h4>
        <ul class="social-media-list">
          <li>
            <a href="https://www.instagram.com/eswar_018_/?igshid=NTc4MTIwNjQ2YQ%3D%3D">
              <img src="insta logo-fotor-bg-remover-2023052412530.png" alt="Instagram Logo">
              Instagram
            </a>
          </li>
        </ul>
      </div>
      
      <div class="footer-column">
        <h4>Contact Information</h4>
        <p>Email: eswar2005s@gmail.com</p>
        <p>Phone: 123-456-7890</p>
        <p>Address: Saveetha Nagar, Thandalam, Chennai</p>
      </div>
      <div class="footer-column">
        <div class="column">

        <h4>Legal</h4>
        <ul class="terms-list">
          <li>
            <a href="terms.html">
            <img src="accept.png" alt="Terms logo">
            Terms and Condition
          </a>
        </li>
        </ul>
      </div>
      
    </div>
    
  </footer>
  <footer>
    <p>&copy;2023 CISUM . All rights reserved.</p>
  </footer>
</body>
</html>
```
Polo-shirt.html
```
<!DOCTYPE html>
<html>
<head>
  <title>Polo Shirt</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <header>
    <nav>
      <ul class="menu">
        <li><a href="index.html">Home</a></li>
        <li><a href="oversized-tshirt.html">Oversized T-Shirt</a></li>
        <li><a href="basic-tees.html">Basic Tees</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="polo-shirt">
      <h2>Polo Shirt</h2>
      <div class="product-grid">
        <div class="product">
          <img src="model6.jpg" alt="Polo Shirt 1">
          <h3>Pale green Polo Shirt 1</h3>
          <p>Step into a world of comfort with our Oversized Black T-Shirt. Made from high-quality fabric, it wraps you in a cloud of softness that you'll never want to take off. The timeless black color adds a touch of versatility, allowing you to effortlessly pair it with any outfit.</p>
          <button>Add to Cart</button>
        </div>
        <!-- Add more polo shirt elements here -->
      </div>
    </section>
  </main>

  <footer>
    &copy; 2023 CISUM. All rights reserved.
  </footer>
</body>
</html>
```
Style.css
```

body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f8e7d8;
  }
  
.menu-icon {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 60px; /* Increase the width */
    height: 40px; /* Increase the height */
    cursor: pointer;
    position: absolute;
    top: 10px;
    left: 10px;
    z-index: 9999;
  }
  
  .menu-line {
    width: 100%;
    height: 2px;
    background-color: #000;
    margin-bottom: 100px;
  }
  
  
  .menu-line {
    width: 100%;
    height: 2px;
    background-color: #000;
    margin-bottom: 100px;
  }
  
  
  .menu-line {
    width: 100%;
    height: 2px;
    background-color: #000;
    margin-bottom: 100px;
  }
  
  .menu {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 999;
  }
  
  .menu.open {
    display: block;
  }
  
  .menu ul {
    list-style: none;
    padding: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  
  .menu ul li {
    margin-bottom: 10px;
  }
  
  .menu ul li a {
    text-decoration: none;
    color: #fff;
  }
  
  .banner {
    margin: 0;
    padding: 0;
    background-image: linear-gradient(to top right, rgba(228, 221, 221, 0.5) 20%, rgba(0, 0, 0, 0.8) 40%), url("Eswar.png");
    background-position: top;
    background-size: cover;
    background-repeat: no-repeat;
    height: 508px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  .banner-subtitle {
    text-align: center;
    margin-top: 10px;
    color: #fff;
  }
  
  
  .banner-button {
    font-size: 18px;
    background-color: #ff5c5c;
    color: #cc1111;
    border: none;
    padding: 10px 20px;
    border-radius: 4px;
    cursor: pointer;
    text-transform: uppercase;
    transition: background-color 0.3s ease;
    text-align: center;
    position: absolute;
    bottom: 150px;
    left: 50%;
    transform: translateX(-50%);
  }
  
  .banner-button:hover {
    background-color: #ff4242;
    text-align: center;
  }

  
  .registration-form {
    display: none;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 999;
  }

  .registration-form.open {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .registration-form-inner {
    background-color: #fff;
    padding: 20px;
    border-radius: 4px;
  }

  .registration-form label {
    display: block;
    margin-bottom: 10px;
  }

  .registration-form input[type="text"],
  .registration-form input[type="password"] {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }

  .registration-form button {
    font-size: 18px;
    background-color: #ff5c5c;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 4px;
    cursor: pointer;
    text-transform: uppercase;
    transition: background-color 0.3s ease;
  }

  .registration-form button:hover {
    background-color: #ff4242;
  }
  
  .banner-title {
    font-size: 48px; /* Adjust the font size as desired */
    font-weight: bold; /* Add font weight if desired */
    text-transform: uppercase; /* Apply uppercase if desired */
    text-align: center; /* Center align the text */
  }
  
  .highlight {
    color: #180202; /* Set the color for the highlights */
  }
  
  
  
  
  main {
    padding: 40px;
  }
  
  section {
    margin-bottom: 40px;
  }
  
  h2 {
    font-size: 32px;
    margin-bottom: 20px;
  }
  
  .product-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
  }
  
  .product {
    text-align: center;
  }
  
  .product img {
    width: 100%;
    max-height: 200px;
    object-fit: cover;
    border-radius: 4px;
    margin-bottom: 10px;
  }
  
  .person-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
  }
  
  .person {
    text-align: center;
  }
  
  .person img {
    width: 100%;
    max-height: 200px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 10px;
  }
  
  address {
    font-style: normal;
    margin-bottom: 10px;
  }
  
  footer {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
  }
  ```



## OUTPUT:
![2023-05-29 (5)](https://github.com/Thirukaalathessvarar-S/productcompanywebsite/assets/121166390/3a031a39-b4f2-4886-a1f0-c78c18e36fac)
![2023-05-29 (6)](https://github.com/Thirukaalathessvarar-S/productcompanywebsite/assets/121166390/220fd102-27ba-485c-9c14-a5f153a3ff97)
![2023-05-29 (8)](https://github.com/Thirukaalathessvarar-S/productcompanywebsite/assets/121166390/56c6d8e7-64ea-48d4-a2ab-15a3ac4de52d)
![2023-05-29 (9)](https://github.com/Thirukaalathessvarar-S/productcompanywebsite/assets/121166390/b140dc49-5779-4345-a782-654dee1fc349)

## Result:
Thus a website is designed for the software product company and the HTML,CSS code are validated.
