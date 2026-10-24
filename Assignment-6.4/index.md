Here is your complete Assignment 6.4 — Positioning Practice using HTML and CSS. It includes a sticky navigation bar, a fixed floating contact button, an absolute-positioned badge inside a card, a relative parent, and z-index to control overlapping elements.

Create a file named Assignment-6.4.html and paste the following code into it.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.4 - Positioning Practice</title>

    <style>
        * {
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f3f6fb;
            color: #333;
        }

        /* Header */
        header {
            background-color: #173b70;
            color: white;
            text-align: center;
            padding: 25px 15px;
        }

        header h1 {
            margin: 0;
        }

        /* Sticky navigation bar */
        nav {
            position: sticky;
            top: 0;
            z-index: 1000;
            background-color: #2457a7;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            padding: 12px;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 8px 14px;
            border-radius: 5px;
        }

        nav a:hover {
            background-color: #173b70;
        }

        /* Main content */
        section {
            max-width: 1000px;
            min-height: 400px;
            margin: 25px auto;
            padding: 30px 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 3px 10px #00000012;
            scroll-margin-top: 75px;
        }

        section h2 {
            color: #2457a7;
        }

        /* Card with relative positioning */
        .card {
            position: relative;
            max-width: 400px;
            margin: 30px auto;
            padding: 25px;
            border: 1px solid #ddd;
            border-radius: 12px;
            background-color: #f9fbff;
            box-shadow: 0 4px 12px #00000015;
        }

        .card h3 {
            color: #173b70;
            margin-top: 10px;
        }

        /* Badge positioned absolutely inside card */
        .badge {
            position: absolute;
            top: -12px;
            right: -10px;
            z-index: 2;
            background-color: #e63946;
            color: white;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: bold;
        }

        /* Overlapping elements demonstrating z-index */
        .overlap-demo {
            position: relative;
            height: 160px;
            max-width: 350px;
            margin: 30px auto;
        }

        .layer {
            position: absolute;
            width: 180px;
            height: 100px;
            padding: 15px;
            border-radius: 8px;
            color: white;
            font-weight: bold;
        }

        .layer-one {
            top: 0;
            left: 10px;
            z-index: 1;
            background-color: #2878c8;
        }

        .layer-two {
            top: 35px;
            left: 100px;
            z-index: 3;
            background-color: #e63946;
        }

        /* Fixed floating contact button */
        .contact-button {
            position: fixed;
            right: 25px;
            bottom: 25px;
            z-index: 2000;
            display: inline-block;
            padding: 14px 20px;
            background-color: #168653;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            box-shadow: 0 4px 12px #00000035;
            font-weight: bold;
        }

        .contact-button:hover {
            background-color: #106b41;
        }

        /* Footer */
        footer {
            background-color: #173b70;
            color: white;
            text-align: center;
            padding: 20px;
        }

        @media (max-width: 600px) {
            section {
                margin: 15px 10px;
                padding: 20px 15px;
            }

            nav {
                gap: 3px;
            }

            nav a {
                padding: 8px;
                font-size: 14px;
            }

            .contact-button {
                right: 15px;
                bottom: 15px;
            }
        }
    </style>
</head>

<body>

    <header id="home">
        <h1>Positioning Practice</h1>
        <p>Assignment 6.4 - HTML and CSS</p>
    </header>

    <!-- Sticky navigation bar -->
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#courses">Courses</a>
        <a href="#positioning">Positioning</a>
        <a href="#contact">Contact</a>
    </nav>

    <!-- Section 1 -->
    <section id="about">
        <h2>1. About Our College</h2>
        <p>
            Welcome to our college webpage. Our college provides a
            learning environment where students develop their knowledge,
            technical skills, creativity, and confidence.
        </p>
        <p>
            This webpage demonstrates different CSS positioning
            properties. Scroll down to explore the sections and observe
            how the navigation bar remains at the top.
        </p>
    </section>

    <!-- Section 2 -->
    <section id="courses">
        <h2>2. Our Courses</h2>
        <p>We provide learning opportunities in several subjects:</p>

        <ul>
            <li>Web Development</li>
            <li>Computer Science</li>
            <li>Information Technology</li>
            <li>Database Management</li>
            <li>Programming Fundamentals</li>
        </ul>

        <!-- Relative parent and absolute badge -->
        <div class="card">
            <span class="badge">POPULAR</span>
            <h3>Web Development Course</h3>
            <p>
                Learn HTML, CSS, and JavaScript to create modern,
                responsive websites.
            </p>
            <p><strong>Level:</strong> Beginner</p>
            <p><strong>Mode:</strong> Practical Learning</p>
        </div>
    </section>

    <!-- Section 3 -->
    <section id="positioning">
        <h2>3. CSS Positioning Properties</h2>

        <h3>Sticky Navigation</h3>
        <p>
            The navigation bar uses position: sticky and top: 0.
            It stays at the top of the viewport when you scroll down.
        </p>

        <h3>Fixed Contact Button</h3>
        <p>
            The green contact button stays in the bottom-right corner
            of the screen, even while the page scrolls.
        </p>

        <h3>Absolute Badge and Relative Parent</h3>
        <p>
            The course card uses position: relative. The badge uses
            position: absolute, allowing it to appear at the top-right
            corner of the card.
        </p>

        <h3>Z-Index Demonstration</h3>
        <p>
            The red box has a higher z-index than the blue box, so it
            appears in front where they overlap.
        </p>

        <div class="overlap-demo">
            <div class="layer layer-one">
                Blue Layer<br>
                z-index: 1
            </div>

            <div class="layer layer-two">
                Red Layer<br>
                z-index: 3
            </div>
        </div>
    </section>

    <!-- Section 4 -->
    <section id="contact">
        <h2>4. Contact Us</h2>
        <p>
            Thank you for visiting our webpage.
            You can use the floating contact button to jump to this
            contact section from anywhere on the page.
        </p>
        <p><strong>Email:</strong> student@example.com</p>
        <p><strong>Phone:</strong> +91 98765 43210</p>
    </section>

    <!-- Fixed floating contact button -->
    <a href="#contact" class="contact-button">
        Contact / Help
    </a>

    <footer>
        <p>Assignment 6.4 - Positioning Practice</p>
        <p>Created using HTML and CSS</p>
    </footer>

</body>
</html>



Explanation of the CSS properties
Property	Purpose in this assignment
position: sticky	Keeps the navigation bar at the top while scrolling.
position: fixed	Keeps the contact button in the bottom-right corner of the screen.
position: relative	Makes the course card the reference point for its badge.
position: absolute	Places the badge at the top-right corner of the card.
z-index	Controls which overlapping elements appear in front.

How to complete your submission
1. Save the code as Assignment-6.4.html.
2. Open it in Google Chrome.
3. Scroll down to verify that the navigation bar stays at the top and the green contact button stays in the bottom-right corner.
4. Check that the red POPULAR badge appears on the course card and that the red layer overlaps the blue layer.
5. Take screenshots using Win + Shift + S.
For your submission, include:
- Assignment-6.4.html — the completed webpage.
- Assignment-6.4-Screenshot.png — a screenshot showing the sticky navigation bar, floating contact button, and positioned badge.
Tip: Take one screenshot near the top of the page showing the navigation and floating button, and another showing the course card with the POPULAR badge. This will clearly demonstrate that you have completed all the required steps.