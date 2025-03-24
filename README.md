<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Provoke Interest</title>
    <style>
        /* Reset default margins and padding */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #808080; /* Gray background */
            color: #d3d3d3; /* Light gray text */
            font-family: Tahoma, sans-serif;
            line-height: 1.6;
        }

        /* Header styles */
        header {
            background-color: #404040; /* Dark gray */
            height: 100px;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            height: 100%;
        }

        .logo-placeholder {
            width: 100px;
            height: 100px;
            background-color: #000;
        }

        /* Navigation styles */
        .nav-btn {
            background-color: transparent;
            border: none;
            color: #d3d3d3;
            font-size: 18px;
            cursor: pointer;
            padding: 10px 20px;
        }

        .nav-menu {
            display: none;
            position: fixed;
            top: 100px;
            left: 100px;
            right: 0;
            background-color: #404040;
            padding: 20px;
        }

        .nav-menu.active {
            display: block;
        }

        .nav-menu a {
            display: block;
            color: #d3d3d3;
            text-decoration: none;
            padding: 10px 0;
        }

        .nav-menu a:hover {
            color: #ffffff;
        }

        /* Main content styles */
        main {
            margin-top: 120px; /* Space for fixed header */
            padding: 20px;
        }

        .article-section {
            margin-bottom: 20px;
        }

        .article-image {
            width: 100%;
            height: 60vw; /* 60% of viewport width */
            background-color: #000;
            margin-bottom: 10px;
        }

        .article-link {
            color: #d3d3d3;
            text-decoration: none;
            display: block;
            text-align: center;
        }

        .article-link:hover {
            color: #ffffff;
        }

        /* Footer styles */
        footer {
            background-color: #404040;
            height: 100px;
            padding: 20px;
            text-align: center;
        }

        /* Tablet and desktop styles */
        @media (min-width: 768px) {
            .article-grid {
                display: grid;
                grid-template-columns: repeat(3, 1fr);
                gap: 20px;
            }

            .article-image {
                height: calc(33.33vw * 0.6); /* Maintain 60% height ratio */
            }

            .nav-menu {
                left: auto;
                right: 0;
                width: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- Header section -->
    <header>
        <div class="header-content">
            <div class="logo-placeholder">
                <!-- 100x100 black box for logo -->
                <!-- Future image path: "images/logo.png" -->
            </div>
            <button class="nav-btn" onclick="toggleMenu()">MORE</button>
        </div>
    </header>

    <!-- Navigation menu -->
    <nav class="nav-menu" id="navMenu">
        <a href="LinkNewPage.html">Link New Page</a>
        <a href="LinkNewPage.html">Link New Page</a>
        <a href="LinkNewPage.html">Link New Page</a>
        <a href="LinkNewPage.html">Link New Page</a>
        <a href="LinkNewPage.html">Link New Page</a>
        <a href="LinkNewPage.html">Link New Page</a>
    </nav>

    <!-- Main content -->
    <main>
        <div class="article-grid">
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image1.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image2.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image3.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image4.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image5.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
            <div class="article-section">
                <div class="article-image">
                    <!-- Black box, future path: "images/image6.png" -->
                </div>
                <a href="#" class="article-link">Link New Article</a>
            </div>
        </div>
    </main>

    <!-- Footer section -->
    <footer>
        <p>Created by a Private Investigator</p>
    </footer>

    <!-- JavaScript for menu toggle -->
    <script>
        function toggleMenu() {
            const menu = document.getElementById('navMenu');
            menu.classList.toggle('active');
        }

        // Close menu when clicking outside
        document.addEventListener('click', function(event) {
            const menu = document.getElementById('navMenu');
            const navBtn = document.querySelector('.nav-btn');
            if (!menu.contains(event.target) && !navBtn.contains(event.target)) {
                menu.classList.remove('active');
            }
        });
    </script>
</body>
</html>