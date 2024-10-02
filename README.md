# PRODIGY_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ProDigy Infotech - Responsive Landing Page</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        .nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: #333;
            padding: 1rem;
            transition: all 0.3s ease;
        }
        .nav.scrolled {
            background-color: #555;
            padding: 0.5rem 1rem;
        }
        .nav-list {
            list-style-type: none;
            display: flex;
            justify-content: center;
        }
        .nav-item {
            margin: 0 1rem;
        }
        .nav-link {
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            transition: color 0.3s ease;
        }
        .nav-link:hover {
            color: #ffd700;
        }
        .section {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2rem;
            color: white;
        }
        #home { background-color: #3498db; }
        #about { background-color: #2ecc71; }
        #services { background-color: #e74c3c; }
        #contact { background-color: #9b59b6; }
    </style>
</head>
<body>
    <nav class="nav">
        <ul class="nav-list">
            <li class="nav-item"><a href="#home" class="nav-link">Home</a></li>
            <li class="nav-item"><a href="#about" class="nav-link">About</a></li>
            <li class="nav-item"><a href="#services" class="nav-link">Services</a></li>
            <li class="nav-item"><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
    </nav>

    <section id="home" class="section">
        <h1>Welcome to ProDigy Infotech</h1>
    </section>
    <section id="about" class="section">
        <h2>About Us</h2>
    </section>
    <section id="services" class="section">
        <h2>Our Services</h2>
    </section>
    <section id="contact" class="section">
        <h2>Contact Us</h2>
    </section>

    <script>
        const nav = document.querySelector('.nav');
        const navLinks = document.querySelectorAll('.nav-link');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                nav.classList.add('scrolled');
            } else {
                nav.classList.remove('scrolled');
            }
        });

        navLinks.forEach(link => {
            link.addEventListener('mouseover', () => {
                link.style.fontSize = '1.2rem';
            });
            link.addEventListener('mouseout', () => {
                link.style.fontSize = '1.1rem';
            });
        });
    </script>
</body>
</html>
