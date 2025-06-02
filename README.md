<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Urban Threads - Clothing Brand</title>
    <style>
        /* Reset and Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            line-height: 1.6;
            color: #333;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* Navbar */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
            background: #000;
            color: #fff;
            position: sticky;
            top: 0;
        }

        .logo img {
            width: 120px;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 1.5rem;
        }

        .nav-links li a {
            color: #fff;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        .nav-links li a:hover {
            color: #f39c12;
        }

        /* Hero Section */
        .hero {
            background: url('https://source.unsplash.com/1600x900/?fashion,clothing') center/cover no-repeat;
            height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
        }

        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: #f39c12;
            color: #fff;
            border-radius: 4px;
            transition: background 0.3s ease;
        }

        .btn:hover {
            background: #e67e22;
        }

        /* Products */
        .products {
            padding: 4rem 2rem;
            text-align: center;
        }

        .products h2 {
            margin-bottom: 2rem;
            font-size: 2rem;
        }

        .product-grid {
            display: grid;
            gap: 2rem;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        }

        .product-card {
            background: #f5f5f5;
            padding: 1rem;
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .product-card img {
            width: 100%;
            border-radius: 8px;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-card h3 {
            margin-top: 1rem;
            font-size: 1.2rem;
        }

        .product-card p {
            color: #f39c12;
            font-weight: bold;
        }

        /* About */
        .about {
            padding: 4rem 2rem;
            background: #333;
            color: #fff;
            text-align: center;
        }

        .about h2 {
            margin-bottom: 1rem;
            font-size: 2rem;
        }

        /* Contact */
        .contact {
            padding: 4rem 2rem;
            text-align: center;
        }

        .contact h2 {
            margin-bottom: 1rem;
            font-size: 2rem;
        }

        .contact a {
            color: #f39c12;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 1rem;
            background: #000;
            color: #fff;
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.2rem;
            }

            .hero-content p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="navbar">
            <div class="logo">
                <img src="https://via.placeholder.com/120x40?text=Urban+Threads" alt="Urban Threads Logo">
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#shop">Shop</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Urban Threads</h1>
            <p>Redefining street fashion for the modern generation.</p>
            <a href="#shop" class="btn">Shop Now</a>
        </div>
    </section>

    <section id="shop" class="products">
        <h2>Our Collection</h2>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://source.unsplash.com/400x400/?hoodie,clothing" alt="Classic Hoodie">
                <h3>Classic Hoodie</h3>
                <p>$49.99</p>
            </div>
            <div class="product-card">
                <img src="https://source.unsplash.com/400x400/?jacket,fashion" alt="Urban Jacket">
                <h3>Urban Jacket</h3>
                <p>$79.99</p>
            </div>
            <div class="product-card">
                <img src="https://source.unsplash.com/400x400/?jeans,denim" alt="Denim Jeans">
                <h3>Denim Jeans</h3>
                <p>$59.99</p>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <h2>About Us</h2>
        <p>At Urban Threads, we blend comfort with style. Our clothing is designed for trendsetters who believe fashion should empower. Discover the perfect outfit for any vibe.</p>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>Have questions or want to collaborate? Drop us a line at <a href="mailto:info@urbanthreads.com">info@urbanthreads.com</a>.</p>
    </section>

    <footer>
        <p>&copy; 2025 Urban Threads. All rights reserved.</p>
    </footer>
</body>
</html>
