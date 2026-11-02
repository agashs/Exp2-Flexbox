# Ex02 Commercial Flexbox
## Date:02-11-2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM:
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NovaStore - Commercial Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <div class="navbar">
            <h2 class="logo">Nova<span>Store</span></h2>

            <nav>
                <a href="#home">Home</a>
                <a href="#products">Products</a>
                <a href="#about">About Us</a>
                <a href="#contact">Contact</a>
                <a href="#account">Account</a>
            </nav>

            <div class="cart">
                Cart: <span id="cart-count">0</span>
            </div>
        </div>
    </header>

    <!-- Home Section -->
    <section class="hero" id="home">
        <div class="hero-text">
            <h1>Shop Smart,<br>
                <span>Live Better!</span>
            </h1>

            <p>
                Discover the latest trends, gadgets and
                amazing deals only at NovaStore.
            </p>

            <a href="#products" class="btn">Shop Now</a>
        </div>

        <div class="hero-image">
            <img
                src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=800&q=80"
                alt="Headphones">
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <h2>Our Products</h2>
        <p class="subtitle">Explore our popular collections</p>

        <div class="product-container">

            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=500&q=80"
                    alt="Sneakers">
                <h3>Sneakers</h3>
                <p>₹2,999</p>
                <button class="btn add-to-cart"
                    data-product="Sneakers">Add to Cart</button>
            </div>

            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=500&q=80"
                    alt="Smart Watch">
                <h3>Smart Watch</h3>
                <p>₹4,999</p>
                <button class="btn add-to-cart"
                    data-product="Smart Watch">Add to Cart</button>
            </div>

            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1606220945770-b5b6c2c55bf1?auto=format&fit=crop&w=500&q=80"
                    alt="Earbuds">
                <h3>Earbuds</h3>
                <p>₹1,999</p>
                <button class="btn add-to-cart"
                    data-product="Earbuds">Add to Cart</button>
            </div>

            <div class="product-card">
                <img
                    src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?auto=format&fit=crop&w=500&q=80"
                    alt="Backpack">
                <h3>Backpack</h3>
                <p>₹1,499</p>
                <button class="btn add-to-cart"
                    data-product="Backpack">Add to Cart</button>
            </div>

        </div>

        <p id="cart-message"></p>
    </section>

    <!-- About Us Section -->
    <section class="about" id="about">
        <div class="about-image">
            <img
                src="https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=900&q=80"
                alt="Our Store">
        </div>

        <div class="about-text">
            <h2>About Us</h2>
            <p>
                NovaStore is your one-stop destination for
                fashion, gadgets and more. We provide quality
                products at affordable prices.
            </p>
            <a href="#contact" class="btn">Learn More</a>
        </div>
    </section>

    <!-- Account Section -->
    <section class="account" id="account">
        <h2>My Account</h2>
        <p>Join NovaStore for a better shopping experience.</p>
        <a href="mailto:support@novastore.example?subject=Account%20Help"
            class="btn">Login / Sign Up</a>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <h2>Contact Us</h2>
        <p>Have any questions? Feel free to contact us.</p>
        <p>Email: support@novastore.example</p>
        <p>Phone: +91 98765 43210</p>
    </section>

    <!-- Footer -->
    <footer>
        <h2 class="logo">Nova<span>Store</span></h2>

        <div class="social-links">
            <a href="https://www.instagram.com/">Instagram</a>
            <a href="https://www.facebook.com/">Facebook</a>
            <a href="https://www.youtube.com/">YouTube</a>
        </div>

        <p>&copy; 2026 NovaStore. All rights reserved.</p>
    </footer>

    <!-- Simple Add to Cart Function -->
    <script>
        let count = 0;

        const buttons = document.querySelectorAll(".add-to-cart");

        buttons.forEach(function(button) {
            button.addEventListener("click", function() {
                count++;

                document.getElementById("cart-count").textContent = count;

                document.getElementById("cart-message").textContent =
                    button.dataset.product + " added to cart!";
            });
        });
    </script>

</body>
</html>

css 

/* General Styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #f8f7fc;
    color: #211d32;
    line-height: 1.6;
}

a {
    text-decoration: none;
}

img {
    width: 100%;
    display: block;
    object-fit: cover;
}

section {
    scroll-margin-top: 90px;
}

/* Navigation Bar */
header {
    background: #11101d;
    color: white;
    position: sticky;
    top: 0;
    z-index: 100;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
    padding: 18px 6%;
}

.logo {
    color: white;
    font-size: 28px;
    font-weight: bold;
}

.logo span {
    color: #9b4dff;
}

nav {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

nav a {
    color: white;
    font-weight: bold;
    transition: 0.3s;
}

nav a:hover {
    color: #a65aff;
}

.cart {
    font-weight: bold;
}

#cart-count {
    background: #8b3dff;
    padding: 4px 10px;
    border-radius: 20px;
}

/* Home Section */
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 40px;
    padding: 60px 8%;
    background: linear-gradient(120deg, #11101d, #302052);
    color: white;
}

.hero-text {
    flex: 1;
}

.hero-text h1 {
    font-size: 48px;
    line-height: 1.2;
    margin-bottom: 20px;
}

.hero-text h1 span {
    color: #a65aff;
}

.hero-text p {
    font-size: 18px;
    margin-bottom: 25px;
    max-width: 450px;
}

.hero-image {
    flex: 1;
}

.hero-image img {
    height: 320px;
    border-radius: 20px;
}

/* Buttons */
.btn {
    display: inline-block;
    background: #8b3dff;
    color: white;
    border: none;
    border-radius: 25px;
    padding: 10px 22px;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
}

.btn:hover {
    background: #6924d6;
    transform: translateY(-3px);
}

/* Products Section */
.products {
    padding: 60px 6%;
    text-align: center;
}

.products > h2 {
    font-size: 34px;
}

.subtitle {
    color: #777;
    margin-bottom: 30px;
}

.product-container {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    gap: 25px;
}

.product-card {
    flex: 1 1 220px;
    max-width: 260px;
    background: white;
    padding: 18px;
    border-radius: 15px;
    box-shadow: 0 5px 18px #00000012;
    transition: 0.3s;
}

.product-card:hover {
    transform: translateY(-7px);
    box-shadow: 0 10px 25px #00000020;
}

.product-card img {
    height: 170px;
    border-radius: 10px;
    margin-bottom: 12px;
}

.product-card h3 {
    margin-bottom: 5px;
}

.product-card p {
    font-weight: bold;
    margin-bottom: 12px;
}

.product-card .btn {
    width: 100%;
}

#cart-message {
    color: #7025e8;
    font-weight: bold;
    margin-top: 20px;
}

/* About Us Section */
.about {
    display: flex;
    align-items: center;
    gap: 40px;
    padding: 55px 8%;
    background: #eee5ff;
}

.about-image,
.about-text {
    flex: 1;
}

.about-image img {
    height: 300px;
    border-radius: 15px;
}

.about-text h2 {
    font-size: 34px;
    margin-bottom: 15px;
}

.about-text p {
    margin-bottom: 20px;
}

/* Account Section */
.account {
    text-align: center;
    padding: 45px 20px;
    background: white;
}

.account h2 {
    font-size: 28px;
    margin-bottom: 10px;
}

.account p {
    margin-bottom: 20px;
}

/* Contact Section */
.contact {
    text-align: center;
    padding: 45px 20px;
    background: #f0ebfa;
}

.contact h2 {
    font-size: 28px;
    margin-bottom: 12px;
}

.contact p {
    margin-bottom: 8px;
}

/* Footer */
footer {
    background: #11101d;
    color: white;
    text-align: center;
    padding: 30px 20px;
}

footer .logo {
    margin-bottom: 15px;
}

.social-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 15px;
}

.social-links a {
    color: #c9a8ff;
    transition: 0.3s;
}

.social-links a:hover {
    color: white;
}

footer p {
    font-size: 14px;
    color: #ccc;
}

/* Responsive Design */
@media (max-width: 768px) {
    .navbar {
        justify-content: center;
        text-align: center;
    }

    nav {
        justify-content: center;
    }

    .hero {
        flex-direction: column;
        text-align: center;
    }

    .hero-text h1 {
        font-size: 38px;
    }

    .hero-text p {
        margin-left: auto;
        margin-right: auto;
    }

    .hero-image img {
        height: 250px;
    }

    .about {
        flex-direction: column;
        text-align: center;
    }

    .about-image img {
        height: 230px;
    }
}

@media (max-width: 480px) {
    nav {
        gap: 12px;
    }

    nav a {
        font-size: 14px;
    }

    .hero-text h1 {
        font-size: 32px;
    }

    .product-card {
        max-width: 100%;
    }
}
```
## OUTPUT

![alt text](<Screenshot 2026-11-02 152620.png>)
## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
