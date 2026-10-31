# Commercial-Website
# AIM
To design and develop a commercial car showroom website named VELOCITY using HTML and CSS, featuring 20 different luxury cars, their images, prices, specifications, services, and contact information with a responsive and attractive user interface.
# ALGORITHM
1. Start the program.
2. Create an HTML document and set the page title as VELOCITY Car Showroom.
3. Design the navigation bar with Home, Cars, About, Services, and Contact links.
4. Create an attractive homepage with a background car image and welcome content.
5. Display popular automobile brands.
6. Create a car collection section containing 20 different cars with images, names, prices, and specifications.
7. Design the About section to describe the showroom.
8. Add a Services section containing car sales, test drive, financing, and maintenance.
9. Create a Contact section with contact information.
10. Apply CSS styles for colours, fonts, layouts, spacing, hover effects, and responsive design.
11. Save the file with the .html extension.
12. Open the webpage using a browser and verify the output.
13. Stop the program.
# PROGRAM
```

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VELOCITY | Premium Car Showroom</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    background: #0b0b0b;
    color: white;
    font-family: Arial, sans-serif;
}

header {
    background: #151515;
    padding: 22px 7%;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
}

.logo {
    font-size: 28px;
    font-weight: bold;
    letter-spacing: 2px;
}

.logo span, .highlight {
    color: #e5a500;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 25px;
}

.nav-links a {
    color: white;
    text-decoration: none;
    transition: .3s;
}

.nav-links a:hover {
    color: #e5a500;
}

.nav-btn, .main-btn {
    background: #e5a500;
    color: black;
    padding: 13px 22px;
    text-decoration: none;
    font-weight: bold;
    display: inline-block;
    transition: .3s;
}

.nav-btn:hover, .main-btn:hover {
    background: white;
    transform: translateY(-3px);
}

/* HERO */

.hero {
    min-height: 650px;
    padding: 100px 8%;
    background:
    linear-gradient(90deg, #080808 5%, rgba(0,0,0,.65), transparent),
    url("https://images.unsplash.com/photo-1503376780353-7e6692767b70?w=1800")
    center/cover no-repeat;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.tagline {
    color: #e5a500;
    letter-spacing: 4px;
    font-size: 12px;
    font-weight: bold;
    margin-bottom: 20px;
}

.hero h1 {
    font-size: 75px;
    line-height: 1.1;
    margin-bottom: 20px;
}

.hero h1 span {
    color: #e5a500;
}

.hero p {
    color: #ccc;
    line-height: 1.8;
    max-width: 450px;
    margin-bottom: 30px;
}

.hero-stats {
    display: flex;
    gap: 65px;
    margin-top: 70px;
}

.hero-stats h2 {
    color: #e5a500;
    font-size: 30px;
}

.hero-stats p {
    font-size: 13px;
    margin: 5px 0;
}

/* BRANDS */

.brands {
    padding: 45px 8%;
    background: #151515;
    text-align: center;
}

.brands p {
    color: #888;
    letter-spacing: 3px;
    font-size: 12px;
}

.brand-list {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 25px;
    margin-top: 30px;
}

.brand-list h2 {
    color: #ddd;
    font-size: 22px;
}

/* CARS */

.cars-section {
    padding: 85px 7%;
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: end;
    margin-bottom: 45px;
    gap: 20px;
}

.section-heading h2 {
    font-size: 42px;
}

.section-heading > p {
    color: #999;
}

.car-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 25px;
}

.car-card {
    background: #181818;
    border: 1px solid #292929;
    overflow: hidden;
    transition: .3s;
}

.car-card:hover {
    transform: translateY(-8px);
    border-color: #e5a500;
}

.car-card img {
    width: 100%;
    height: 190px;
    object-fit: cover;
}

.car-details {
    padding: 22px;
}

.car-type {
    color: #e5a500;
    font-size: 11px;
    letter-spacing: 2px;
}

.car-details h3 {
    font-size: 18px;
    margin: 13px 0;
    min-height: 42px;
}

.price {
    color: #e5a500;
    font-size: 20px;
    font-weight: bold;
}

.specs {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 18px 0;
}

.specs span {
    background: #292929;
    color: #ccc;
    padding: 7px;
    font-size: 11px;
}

.car-btn {
    display: block;
    text-align: center;
    text-decoration: none;
    color: #e5a500;
    border: 1px solid #e5a500;
    padding: 12px;
    transition: .3s;
}

.car-btn:hover {
    background: #e5a500;
    color: black;
}

/* ABOUT */

.about {
    padding: 90px 8%;
    background: #151515;
    display: flex;
    align-items: center;
    gap: 60px;
}

.about-image, .about-content {
    flex: 1;
}

.about-image img {
    width: 100%;
    height: 420px;
    object-fit: cover;
}

.about-content h2 {
    font-size: 42px;
    margin-bottom: 25px;
    line-height: 1.3;
}

.about-content p {
    color: #aaa;
    line-height: 1.8;
    margin-bottom: 25px;
}

.about-stats {
    display: flex;
    gap: 55px;
    margin-bottom: 30px;
}

.about-stats h3 {
    color: #e5a500;
    font-size: 28px;
}

/* SERVICES */

.services {
    padding: 90px 8%;
    text-align: center;
}

.services h2 {
    font-size: 40px;
    margin-bottom: 45px;
}

.service-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    text-align: left;
}

.service-card {
    background: #181818;
    border: 1px solid #292929;
    padding: 30px 22px;
    transition: .3s;
}

.service-card:hover {
    border-color: #e5a500;
    transform: translateY(-5px);
}

.service-card h3 {
    color: #e5a500;
    font-size: 30px;
    margin-bottom: 25px;
}

.service-card h4 {
    font-size: 20px;
    margin-bottom: 15px;
}

.service-card p {
    color: #999;
    font-size: 14px;
    line-height: 1.8;
}

/* CONTACT */

.contact {
    padding: 100px 20px;
    text-align: center;
    background:
    linear-gradient(rgba(0,0,0,.8), rgba(0,0,0,.8)),
    url("https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?w=1600")
    center/cover;
}

.contact h2 {
    font-size: 42px;
    margin-bottom: 20px;
}

.contact p {
    color: #ccc;
    margin-bottom: 30px;
}

/* FOOTER */

footer {
    background: #080808;
    padding: 45px 8%;
    text-align: center;
}

footer p {
    color: #888;
    margin-top: 15px;
}

.copyright {
    border-top: 1px solid #292929;
    padding-top: 20px;
    margin-top: 30px;
    font-size: 13px;
}

/* RESPONSIVE */

@media(max-width: 1100px) {
    .car-container {
        grid-template-columns: repeat(3, 1fr);
    }

    .service-container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media(max-width: 800px) {
    .car-container {
        grid-template-columns: repeat(2, 1fr);
    }

    .about {
        flex-direction: column;
    }

    .nav-links {
        gap: 12px;
        flex-wrap: wrap;
    }
}

@media(max-width: 550px) {
    .car-container, .service-container {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        font-size: 48px;
    }

    .hero-stats {
        gap: 25px;
        flex-wrap: wrap;
    }

    .section-heading {
        flex-direction: column;
        align-items: flex-start;
    }

    .section-heading h2, .services h2,
    .about-content h2, .contact h2 {
        font-size: 32px;
    }

    .nav-btn {
        display: none;
    }

    .brand-list h2 {
        font-size: 16px;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->

<header>
<nav class="navbar">
    <h1 class="logo">VELO<span>CITY.</span></h1>

    <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#cars">Cars</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>

    <a href="#cars" class="nav-btn">Explore Cars</a>
</nav>
</header>

<!-- HERO -->

<section class="hero" id="home">
    <p class="tagline">THE FUTURE OF DRIVING</p>

    <h1>DRIVE YOUR<br><span>DREAMS.</span></h1>

    <p>Discover extraordinary cars that combine luxury,
    performance and innovation. Your dream car is waiting for you.</p>

    <a href="#cars" class="main-btn">Explore Collection →</a>

    <div class="hero-stats">
        <div><h2>150+</h2><p>Premium Cars</p></div>
        <div><h2>25+</h2><p>Luxury Brands</p></div>
        <div><h2>10K+</h2><p>Happy Customers</p></div>
    </div>
</section>

<!-- BRANDS -->

<section class="brands">
    <p>WORLD'S LEADING AUTOMOTIVE BRANDS</p>
    <div class="brand-list">
        <h2>BMW</h2>
        <h2>BENZ</h2>
        <h2>AUDI</h2>
        <h2>PORSCHE</h2>
        <h2>FERRARI</h2>
        <h2>TESLA</h2>
    </div>
</section>

<!-- 20 CARS -->

<section class="cars-section" id="cars">

<div class="section-heading">
    <div>
        <p class="tagline">OUR PREMIUM COLLECTION</p>
        <h2>Explore Our <span class="highlight">Cars</span></h2>
    </div>
    <p>20 exclusive vehicles. One destination.</p>
</div>

<div class="car-container">

<!-- CAR 1 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1555215695-3004980ad54e?w=800" alt="BMW M4">
<div class="car-details">
<p class="car-type">SPORTS SEDAN</p>
<h3>BMW M4 Competition</h3>
<p class="price">₹1.53 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 2 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?w=800" alt="Mercedes">
<div class="car-details">
<p class="car-type">LUXURY SEDAN</p>
<h3>Mercedes-Benz C-Class</h3>
<p class="price">₹60 Lakhs</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 3 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?w=800" alt="Audi">
<div class="car-details">
<p class="car-type">SPORTS CAR</p>
<h3>Audi R8</h3>
<p class="price">₹2.30 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 4 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?w=800" alt="Porsche">
<div class="car-details">
<p class="car-type">SPORTS CAR</p>
<h3>Porsche 911</h3>
<p class="price">₹2.00 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 5 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1511919884226-fd3cad34687c?w=800" alt="Ferrari">
<div class="car-details">
<p class="car-type">SUPERCAR</p>
<h3>Ferrari 488</h3>
<p class="price">₹4.50 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 6 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1519245659620-e859806a8d3b?w=800" alt="Lamborghini">
<div class="car-details">
<p class="car-type">SUPERCAR</p>
<h3>Lamborghini Huracan</h3>
<p class="price">₹3.50 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 7 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1563720223185-11003d516935?w=800" alt="Rolls Royce">
<div class="car-details">
<p class="car-type">ULTRA LUXURY</p>
<h3>Rolls-Royce Ghost</h3>
<p class="price">₹8.95 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 8 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1603584173870-7f23fdae1b7a?w=800" alt="Range Rover">
<div class="car-details">
<p class="car-type">LUXURY SUV</p>
<h3>Range Rover Sport</h3>
<p class="price">₹1.65 Crore</p>
<div class="specs"><span>Automatic</span><span>Diesel</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 9 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?w=800" alt="Toyota">
<div class="car-details">
<p class="car-type">PREMIUM SUV</p>
<h3>Toyota Fortuner</h3>
<p class="price">₹45 Lakhs</p>
<div class="specs"><span>Automatic</span><span>Diesel</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 10 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1552519507-da3b142c6e3d?w=800" alt="Camaro">
<div class="car-details">
<p class="car-type">MUSCLE CAR</p>
<h3>Chevrolet Camaro</h3>
<p class="price">₹70 Lakhs</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 11 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1617814076367-b759c7d7e738?w=800" alt="Mercedes AMG">
<div class="car-details">
<p class="car-type">PERFORMANCE</p>
<h3>Mercedes AMG GT</h3>
<p class="price">₹2.70 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 12 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1607853202273-797f1c22a38e?w=800" alt="McLaren">
<div class="car-details">
<p class="car-type">SUPERCAR</p>
<h3>McLaren 720S</h3>
<p class="price">₹5.00 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 13 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1617469767053-d3b523a0b982?w=800" alt="Tesla">
<div class="car-details">
<p class="car-type">ELECTRIC CAR</p>
<h3>Tesla Model S</h3>
<p class="price">₹1.50 Crore</p>
<div class="specs"><span>Automatic</span><span>Electric</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 14 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1614200187524-dc4b892acf16?w=800" alt="Nissan">
<div class="car-details">
<p class="car-type">SPORTS CAR</p>
<h3>Nissan GT-R</h3>
<p class="price">₹2.12 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 15 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1551830820-330a71b99659?w=800" alt="Jaguar">
<div class="car-details">
<p class="car-type">LUXURY SPORTS</p>
<h3>Jaguar F-Type</h3>
<p class="price">₹1.00 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 16 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1606016159991-dfe4f2746ad5?w=800" alt="Bentley">
<div class="car-details">
<p class="car-type">ULTRA LUXURY</p>
<h3>Bentley Continental</h3>
<p class="price">₹5.50 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 17 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1603386329225-868f9b1ee6c9?w=800" alt="Volvo">
<div class="car-details">
<p class="car-type">LUXURY SUV</p>
<h3>Volvo XC90</h3>
<p class="price">₹1.00 Crore</p>
<div class="specs"><span>Automatic</span><span>Hybrid</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 18 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1606152421802-db97b9c7a11b?w=800" alt="Lexus">
<div class="car-details">
<p class="car-type">PREMIUM SEDAN</p>
<h3>Lexus ES</h3>
<p class="price">₹65 Lakhs</p>
<div class="specs"><span>Automatic</span><span>Hybrid</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 19 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?w=800" alt="Jeep">
<div class="car-details">
<p class="car-type">OFF-ROAD SUV</p>
<h3>Jeep Wrangler</h3>
<p class="price">₹67 Lakhs</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

<!-- CAR 20 -->
<div class="car-card">
<img src="https://images.unsplash.com/photo-1544636331-e26879cd4d9b?w=800" alt="Maserati">
<div class="car-details">
<p class="car-type">LUXURY SPORTS</p>
<h3>Maserati MC20</h3>
<p class="price">₹3.50 Crore</p>
<div class="specs"><span>Automatic</span><span>Petrol</span></div>
<a href="#contact" class="car-btn">Enquire Now →</a>
</div></div>

</div>
</section>

<!-- ABOUT -->

<section class="about" id="about">

<div class="about-image">
<img src="https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?w=1000" alt="Luxury car">
</div>

<div class="about-content">
<p class="tagline">ABOUT VELOCITY</p>
<h2>More Than Just<br>A <span class="highlight">Car Dealership.</span></h2>

<p>At Velocity, we believe every journey deserves something extraordinary. We bring together the world's finest automobiles, offering quality, trust and an exceptional buying experience.</p>

<div class="about-stats">
<div><h3>10+</h3><p>Years Experience</p></div>
<div><h3>5000+</h3><p>Cars Delivered</p></div>
</div>

<a href="#contact" class="main-btn">Know More →</a>
</div>

</section>

<!-- SERVICES -->

<section class="services" id="services">
<p class="tagline">WHAT WE OFFER</p>
<h2>Our Premium <span class="highlight">Services</span></h2>

<div class="service-container">

<div class="service-card">
<h3>01</h3>
<h4>Car Sales</h4>
<p>Explore our exclusive collection of premium automobiles.</p>
</div>

<div class="service-card">
<h3>02</h3>
<h4>Test Drive</h4>
<p>Experience the power and performance before purchasing.</p>
</div>

<div class="service-card">
<h3>03</h3>
<h4>Easy Financing</h4>
<p>Flexible financing options for your dream automobile.</p>
</div>

<div class="service-card">
<h3>04</h3>
<h4>Car Maintenance</h4>
<p>Professional support to keep your vehicle at its best.</p>
</div>

</div>
</section>

<!-- CONTACT -->

<section class="contact" id="contact">
<p class="tagline">GET IN TOUCH</p>
<h2>Ready To Find Your <span class="highlight">Dream Car?</span></h2>
<p>Contact our team today and take the first step towards luxury.</p>
<a href="mailto:info@velocitycars.com" class="main-btn">Contact Us →</a>
</section>

<!-- FOOTER -->

<footer>
<h2 class="logo">VELO<span>CITY.</span></h2>
<p>Experience Luxury. Experience Performance.</p>
<p class="copyright">© 2026 VELOCITY Motors. All Rights Reserved.</p>
</footer>

</body>
</html>


```
# OUTPUT
![alt text](<Screenshot 2026-10-31 162015-1.png>)

![alt text](<Screenshot 2026-10-31 162049-1.png>)

![alt text](<Screenshot 2026-10-31 162106.png>)

![alt text](<Screenshot 2026-10-31 162123.png>)

![alt text](<Screenshot 2026-10-31 162141.png>)

![alt text](<Screenshot 2026-10-31 162152.png>)

![alt text](<Screenshot 2026-10-31 162203.png>)

# RESULT
Thus, the VELOCITY Commercial Car Showroom Website was successfully designed and developed using HTML and CSS. The website displays 20 different cars with their images, prices, and specifications, along with About, Services, and Contact sections in an attractive and responsive layout.