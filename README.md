<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Chang Industries Cars</title>
    <!-- Include Font Awesome stylesheet -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
        integrity="sha512-xr6H8rUH8WBSzH3U/B8Rr+HteZMheIeY/pq9eKGdb8SZMyiExE3BiYRPYRmiKwlA3tJ9k1MsD6mp0gFU11LIaQ=="
        crossorigin="anonymous" />
    <style>
        body {
            font-family: 'Calibri', sans-serif;
            background-color: #f00; /* Red background */
            color: #00f; /* Blue text color */
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            text-align: center;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px;
            font-size: 24px;
        }

        nav {
            background-color: #007BFF; /* Updated color for the navigation bar */
            padding: 10px;
            display: flex;
            justify-content: space-around; /* Adjusted space-around for better alignment */
            align-items: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold; /* Bold text for navigation links */
        }

        .page-content {
            display: none;
            margin: 20px;
            padding: 20px;
            background-color: #fff; /* White background for content sections */
            border-radius: 10px;
        }

        #search-bar {
            margin-top: 10px;
        }

        iframe {
            width: 100%; /* Make the video responsive */
            height: 400px; /* Adjust the height as needed */
        }

        #accessibility-options {
            margin-top: 20px;
            color: #fff; /* White color for accessibility options */
        }

        #chat-interface {
            margin-top: 20px;
            padding: 20px;
            background-color: #fff; /* White background */
            border-radius: 10px;
            color: #333; /* Dark text color */
        }

        #page-descriptions {
            margin-top: 20px;
            border: 2px solid red; /* Red border for page descriptions */
            padding: 10px;
        }

        .icon-button {
            text-decoration: none;
            color: #333;
            margin: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .icon-button img {
            width: 80px;
            height: 80px;
        }
    </style>
</head>

<body>
    <nav>
        <a href="#home">Home</a>
        <a href="#vans">Vans</a>
        <a href="#hybrid-cars">Hybrid Cars</a>
        <a href="#payment">Payment & Contact Us</a> <!-- Merged page link -->
        <!-- Search bar -->
        <input type="text" id="search-bar" placeholder="Search...">
    </nav>

    <header>Welcome to Chang Industries Cars</header>

    <!-- Page Descriptions for Home -->
    <div id="page-descriptions">
        <p>Cars Made in China and Distributed Globally</p>
        <p>Welcome to Chang Industries Car, where we manufacture and distribute high-quality cars made in China to
            customers around the world. Explore our offerings and connect with us through social media, contact us for
            inquiries, and proceed with secure payments.</p>
        <p>Slogan: Driving Innovation, Shaping the Future</p>
        <p>欢迎来到张氏汽车工业 - Welcome to Chang's Car Industries</p>
    </div>

    <!-- Sections for different pages -->
    <div id="home" class="page-content">
        <!-- Remove the text box on the home page -->
    </div>

    <div id="vans" class="page-content">
        <h2>Vans</h2>
        <p>This is the model of vans that Chang's Car Industries offers you as a customer.</p>
        <!-- Embedded YouTube video for Vans -->
        <iframe width="560" height="315" src="https://www.youtube.com/embed/7r5FyzPX3W8" frameborder="0"
            allowfullscreen></iframe>
    </div>

    <div id="hybrid-cars" class="page-content">
        <h2>Hybrid Cars</h2>
        <p>This is the model of hybrid cars that Chang's Car Industries offers you as a customer.</p>
        <!-- Embedded YouTube video for Hybrid Cars -->
        <iframe width="560" height="315" src="https://www.youtube.com/embed/ht36CeDLxmI" frameborder="0"
            allowfullscreen></iframe>
    </div>

    <div id="payment" class="page-content">
        <h2>Payment & Contact Us</h2> <!-- Updated heading -->
        <p>This is the Payment page content. The video below shows how to pay on our website.</p>
        <!-- Embedded YouTube video for Payment -->
        <iframe width="560" height="315" src="https://www.youtube.com/embed/tS2GGOLA9KQ" frameborder="0"
            allowfullscreen></iframe>
        <!-- Additional content for Payment & Contact Us -->
        <p>Contact us for any assistance or inquiries.</p>
        <p>Email: info@changcars.com</p>
    </div>

    <div id="accessibility-options">
        <label for="read-aloud">Read Aloud:</label>
        <input type="checkbox" id="read-aloud">

        <label for="sign-language">Sign Language:</label>
        <input type="checkbox" id="sign-language">
    </div>

    <div id="chat-interface">
        <h2>Customer Assistance Chat</h2>
        <div id="chat-messages"></div>
        <input type="text" id="chat-input" placeholder="Type your message...">
        <button onclick="sendMessage()">Send</button>
    </div>

    <!-- Additional script and functions here -->
    <script>
        // JavaScript for handling page navigation
        const pages = ["home", "vans", "hybrid-cars", "payment"]; // Updated page list

        function showPage(pageId) {
            pages.forEach(page => {
                const element = document.getElementById(page);
                const descriptionElement = document.getElementById("page-descriptions");
                if (page === pageId) {
                    element.style.display = "block";
                    descriptionElement.style.display = (page === "home") ? "block" : "none";
                } else {
                    element.style.display = "none";
                }
            });
        }

        // Initial page display
        showPage("home");

        // Navigation click event listeners
        pages.forEach(page => {
            const link = document.querySelector(`nav a[href="#${page}"]`);
            if (link) {
                link.addEventListener("click", (event) => {
                    event.preventDefault();
                    showPage(page);
                });
            }
        });
    </script>
</body>

</html>
