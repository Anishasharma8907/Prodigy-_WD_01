<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        /* Navigation menu styling */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: #333;
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 10px 0;
            transition: background-color 0.3s ease;
        }

        .navbar.scrolled {
            background-color: #555;
        }

        .navbar a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            font-size: 16px;
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        .navbar a:hover {
            background-color: white;
            color: #333;
            border-radius: 4px;
        }

        section {
            height: 100vh;
            padding: 20px;
        }

        #section1 {
            background-color: #f4f4f4;
        }

        #section2 {
            background-color: #ddd;
        }

        #section3 {
            background-color: #bbb;
        }
    </style>
</head>
<body>

    <!-- Navigation menu -->
    <div class="navbar" id="navbar">
        <a href="#section1">Home</a>
        <a href="#section2">About</a>
        <a href="#section3">Contact</a>
    </div>

    <!-- Page sections -->
    <section id="section1">
        <h1>Home</h1>
        <p>Welcome to the home section of the page.</p>
    </section>
    <section id="section2">
        <h1>About</h1>
        <p>This is the about section of the page.</p>
    </section>
    <section id="section3">
        <h1>Contact</h1>
        <p>Get in touch with us through this section.</p>
    </section>

    <script>
        // Change navbar style on scroll
        window.addEventListener('scroll', function () {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>

</body>
</html>
