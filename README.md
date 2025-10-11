<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AXONEM - Premium Connected Fashion</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }
        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 14, 23, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            transition: background 0.3s ease;
        }
        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #00D4FF;
            text-decoration: none;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-weight: 400;
            transition: color 0.3s ease;
        }
        .nav-links a:hover {
            color: #00D4FF;
        }
        .cta-btn {
            background: linear-gradient(135deg, #00D4FF, #0099CC);
            color: #fff;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
        .cta-btn:hover {
            transform: scale(1.05);
        }
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(10, 14, 23, 0.7), rgba(10, 14, 23, 0.7)), url('https://via.placeholder.com/1920x1080/0A0E17/00D4FF?text=AXONEM+Hero+Image') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
            position: relative;
        }
        .hero-content h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }
        .hero-content p {
            font-size: 1.5rem;
            font-weight: 300;
            margin-bottom: 2rem;
            opacity: 0;
            animation: fadeInUp 1s ease 0.3s forwards;
        }
        .hero-btn {
            background: transparent;
            color: #fff;
            border: 2px solid #00D4FF;
            padding: 1rem 2rem;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            opacity: 0;
            animation: fadeInUp 1s ease 0.6s forwards;
        }
        .hero-btn:hover {
            background: #00D4FF;
            transform: translateY(-3px);
        }
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        /* Sections */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #0A0E17;
            position: relative;
        }
        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background: #00D4FF;
        }
        /* Featured Products */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        .product-card {
            background: #fff;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease forwards;
        }
        .product-card:nth-child(2) { animation-delay: 0.2s; }
        .product-card:nth-child(3) { animation-delay: 0.4s; }
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 212, 255, 0.2);
        }
        .product-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        .product-info {
            padding: 1.5rem;
        }
        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #0A0E17;
        }
        .product-info p {
            color: #666;
            margin-bottom: 1rem;
        }
        .price {
            font-size: 1.5rem;
            font-weight: 600;
            color: #00D4FF;
        }
        /* About Section */
        .about {
            background: #f8f9fa;
            text-align: center;
        }
        .about p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            color: #555;
        }
        /* Footer */
        footer {
            background: #0A0E17;
            color: #fff;
            text-align: center;
            padding: 2rem;
        }
        .social-links {
            margin-top: 1rem;
        }
        .social-links a {
            color: #00D4FF;
            margin: 0 1rem;
            font-size: 1.5rem;
            text-decoration: none;
        }
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none; /* Add mobile menu JS if needed */
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .hero-content p {
                font-size: 1.2rem;
            }
            section {
                padding: 3rem 1rem;
            }
        }
        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="#" class="logo">AXONEM</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <button class="cta-btn">Shop Now</button>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>AXONEM</h1>
            <p>Where Fashion Meets Neural Innovation</p>
            <button class="hero-btn" onclick="document.getElementById('products').scrollIntoView();">Discover Collection</button>
        </div>
    </section>

    <section id="products">
        <h2>Featured Collection</h2>
        <div class="products-grid">
            <div class="product-card">
                <img src="https://via.placeholder.com/400x250/0A0E17/00D4FF?text=Neural+Jacket" alt="Neural Jacket">
                <div class="product-info">
                    <h3>Neural Jacket</h3>
                    <p>Sleek, tech-infused outerwear for the modern explorer.</p>
                    <div class="price">$299</div>
                </div>
            </div>
            <div class="product-card">
                <img src="https://via.placeholder.com/400x250/0A0E17/00D4FF?text=Synapse+Shirt" alt="Synapse Shirt">
                <div class="product-info">
                    <h3>Synapse Shirt</h3>
                    <p>Breathable fabric with subtle circuit patterns.</p>
                    <div class="price">$149</div>
                </div>
            </div>
            <div class="product-card">
                <img src="https://via.placeholder.com/400x250/0A0E17/00D4FF?text=Axon+Pants" alt="Axon Pants">
                <div class="product-info">
                    <h3>Axon Pants</h3>
                    <p>Versatile, durable denim reimagined for connectivity.</p>
                    <div class="price">$199</div>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <h2>About AXONEM</h2>
        <p>AXONEM redefines premium clothing by blending cutting-edge design with neural-inspired aesthetics. Our collections are crafted for those who live connected—innovative, bold, and timeless. Every piece is made with sustainable materials, ensuring luxury that lasts.</p>
        <button class="cta-btn" onclick="document.getElementById('products').scrollIntoView();">Explore More</button>
    </section>

    <footer id="contact">
        <p>&copy; 2023 AXONEM. All rights reserved.</p>
        <div class="social-links">
            <a href="#">Instagram</a>
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
        </div>
    </footer>

    <script>
        // Simple scroll effect for header
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(10, 14, 23, 0.98)';
            } else {
                header.style.background = 'rgba(10, 14, 23, 0.95)';
            }
        });
    </script>
</body>
</html>
