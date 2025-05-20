<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Simple Website</title>
    <style>
        /* Basic Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            line-height: 1.6;
        }

        header {
            background: #333;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            gap: 2rem;
            background-color: #444;
            padding: 0.5rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        .hero {
            background: url('https://via.placeholder.com/1200x400') no-repeat center center/cover;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-shadow: 1px 1px 3px black;
            font-size: 2rem;
        }

        section {
            padding: 2rem;
            max-width: 1000px;
            margin: auto;
        }

        .services {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .service {
            background: #f4f4f4;
            padding: 1rem;
            flex: 1;
            min-width: 250px;
            border-radius: 8px;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        input, textarea {
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            background: #333;
            color: white;
            padding: 0.7rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        footer {
            text-align: center;
            padding: 1rem;
            background: #222;
            color: white;
        }
    </style>
</head>
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <nav>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="hero">
        Welcome to My Website
    </div>

    <section id="about">
        <h2>About Us</h2>
        <p>We are a small team passionate about creating awesome websites and applications. Our goal is to deliver high-quality digital products that help businesses grow online.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <div class="services">
            <div class="service">
                <h3>Web Design</h3>
                <p>Custom, responsive designs that reflect your brand and engage your audience.</p>
            </div>
            <div class="service">
                <h3>Development</h3>
                <p>Robust front-end and back-end development for smooth functionality.</p>
            </div>
            <div class="service">
                <h3>SEO</h3>
                <p>Optimize your website to rank better on search engines and reach more customers.</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form class="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea rows="5" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        &copy; 2025 My Website | All rights reserved.
    </footer>

</body>
</html>
