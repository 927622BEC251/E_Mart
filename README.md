# E_Mart
[6:04 pm, 16/10/2024] Sujiith: <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Business App</title>
    <style>
        /* CSS Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        header nav {
            margin: 10px 0;
        }

        header nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-size: 18px;
        }

        h1, h2, h3 {
            text-align: center;
            color: #333;
        }

        main {
            padding: 20px;
        }

        .section {
            margin: 40px 0;
            text-align: center;
        }

        .section p {
            max-width: 800px;
            margin: 20px auto;
            line-height: 1.6;
            color: #555;
        }

        .services-list {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .service-item {
            background-color: white;
            border: 1px solid #ddd;
            padding: 20px;
            width: 300px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            transition: box-shadow 0.3s ease;
        }

        .service-item:hover {
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        form {
            max-width: 500px;
            margin: 0 auto;
            text-align: left;
        }

        form label, form input, form textarea {
            display: block;
            width: 100%;
            margin-bottom: 10px;
        }

        form input, form textarea {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        form button {
            background-color: #333;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }

        form button:hover {
            background-color: #555;
        }
    </style>
</head>
<body>

    <!-- Header and Navigation -->
    <header>
        <h1>ABC Business Services</h1>
        <nav>
            <a href="#" onclick="showSection('home')">Home</a>
            <a href="#" onclick="showSection('services')">Services</a>
            <a href="#" onclick="showSection('about')">About Us</a>
            <a href="#" onclick="showSection('contact')">Contact</a>
        </nav>
    </header>

    <!-- Main Content Area -->
    <main>
        <!-- Home Section -->
        <section id="home" class="section">
            <h2>Welcome to ABC Business Services</h2>
            <p>We provide top-notch solutions to cater to all your business needs. Our professional team is dedicated to delivering excellent service and customer satisfaction.</p>
        </section>

        <!-- Services Section -->
        <section id="services" class="section" style="display:none;">
            <h2>Our Services</h2>
            <div class="services-list">
                <div class="service-item">
                    <h3>Consulting</h3>
                    <p>We offer expert business consulting services to help you streamline your operations and improve efficiency.</p>
                </div>
                <div class="service-item">
                    <h3>Marketing</h3>
                    <p>Our marketing strategies are designed to boost your brand visibility and drive more customer engagement.</p>
                </div>
                <div class="service-item">
                    <h3>Financial Advisory</h3>
                    <p>Get professional advice on financial management and investment opportunities to grow your business.</p>
                </div>
            </div>
        </section>

        <!-- About Us Section -->
        <section id="about" class="section" style="display:none;">
            <h2>About Us</h2>
            <p>ABC Business Services was founded with the aim of providing quality business solutions to companies of all sizes. With a team of experts in various fields, we ensure that our clients get the best service and achieve their business goals.</p>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="section" style="display:none;">
            <h2>Contact Us</h2>
            <form id="contact-form">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="5" required></textarea>

                <button type="submit">Submit</button>
            </form>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>© 2024 ABC Business Services. All Rights Reserved.</p>
    </footer>

    <script>
        // JavaScript: Dynamic Navigation
        function showSection(sectionId) {
            const sections = document.querySelectorAll('main .section');
            sections.forEach(section => {
                section.style.display = 'none';
            });
            document.getElementById(sectionId).style.display = 'block';
        }

        // Show Home section by default
        document.addEventListener('DOMContentLoaded', function() {
            showSection('home');
        });

        // Contact form submission
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Thank you for contacting us! We will get back to you soon.');
            // Reset form after submission
            event.target.reset();
        });
    </script>

</body>
</html>
