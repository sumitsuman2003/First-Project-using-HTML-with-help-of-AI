# First-Project-using-HTML-with-help-of-AI
Zomato Clone
//HTML CODE
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zomato - Order food Online</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
<div class="logo">
<img src="logo zomato.avif" alt=" ">
</div>
<ul>
<li><a href="/investor.html">Investor Relations</a></li>
<li><a href="/Add.html">Add restaurant</a></li>
<li><a href="">Log in</a></li>
<li><a href="">Sign up</a></li>
</ul>
</header>
<main>
<section>
<!-- Use img/zomato.avif as background-->
<img src="https://b.zmtcdn.com/web_assets/81f3ff974d82520780078ba1cfbd453a1583259680.png" alt="">
<img src="https://b.zmtcdn.com/web_assets/8313a97515fcb0447d2d77c276532a511583262271.png" alt="">
<p>Find the best restaurants, cafés and bars in India</p>
<input placeholder="Search for restaurant, Cuisine or a dish">
</section>
<section>
<h2 class="sc-dln2kl-0 cHkolX">Popular locations in India </h2>
<!-- Location Input -->
<div class="location-container">
<input type="text" id="locationInput" placeholder="Enter your location">
<button id="detectLocation">📍 Detect</button>
</div>
</section>
</main>

<footer>
Copyright &copy; 2025 | All rights reserved

</footer>

<script src="js/script.js"></script>

</body>
</html>

//CSS CODE    

/* Reset & base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    }
    
    body {
    background-color: #fff;
    color: #333;
    overflow-x: hidden;
    }
    
    /* Header styling */
    header {
    background-color: #e23744; /* Zomato Red */
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 60px;
    }
    
    header .logo img {
    height: 45px;
    }
    
    header ul {
    list-style: none;
    display: flex;
    gap: 30px;
    }
    
    header ul li a {
    color: white;
    text-decoration: none;
    font-weight: 500;
    transition: opacity 0.3s ease;
    }
    
    header ul li a:hover {
    opacity: 0.8;
    }
    
    /* Main section */
    main {
    text-align: center;
    position: relative;
    background: url('https://b.zmtcdn.com/web_assets/81f3ff974d82520780078ba1cfbd453a1583259680.png') no-repeat center center/cover;
    height: 90vh;
    padding-top: 100px;
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    }
    
    main img:first-child {
    width: 250px;
    margin-bottom: 20px;
    }
    
    main img:nth-child(2) {
    width: 100%;
    max-width: 400px;
    margin-bottom: 30px;
    }
    
    main p {
    font-size: 26px;
    font-weight: 600;
    margin-bottom: 20px;
    }
    
    main input {
    padding: 15px 20px;
    width: 400px;
    max-width: 80%;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    outline: none;
    margin-bottom: 20px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }
    
    /* Footer */
    footer {
    background-color: lch(33.34% 72.19 38.89);
    text-align: center;
    padding: 20px;
    font-size: 14px;
    color: hsl(0, 40%, 98%);
    }
    
    /* Responsive tweaks */
    @media screen and (max-width: 768px) {
    header {
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    padding: 20px;
    }
    
    main {
    height: auto;
    padding: 60px 20px;
    }
    
    main input {
    width: 90%;
    }
    }

  //JAVA SCRIPT

      document.addEventListener("DOMContentLoaded", () => {
    const searchInput = document.querySelector("main input");
    
    // Logging input for dev/testing purposes
    searchInput.addEventListener("input", () => {
    console.log(`User is typing: ${searchInput.value}`);
    });
    
    // Add simple alerts for nav links
    const links = document.querySelectorAll("header ul li a");
    
    links.forEach(link => {
    link.addEventListener("click", (e) => {
    e.preventDefault();
    alert("This feature is coming soon!");
    });
    });
    
    // Welcome based on time
    const hour = new Date().getHours();
    let greeting = "Welcome!";
    if (hour < 12) greeting = "Good morning!";
    else if (hour < 18) greeting = "Good afternoon!";
    else greeting = "Good evening!";
    
    console.log(greeting);
    });
