
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stay Real Media™</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            padding-bottom: 150px; /* Increased padding to accommodate footer */
        }
        .header {
            background-color: #333;
            color: #fff;
            padding: 20px;
        }
        .heartbeat {
            display: inline-block;
            font-size: 2em;
            animation: heartbeat 1.5s infinite;
        }
        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }
        .container {
            padding: 20px;
        }
        .info {
            margin: 20px auto;
            padding: 20px;
            max-width: 800px;
            background-color: #fff;
            border: 2px solid #ccc; /* Add border around content */
            border-radius: 8px; /* Rounded corners */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add subtle shadow */
        }
        h2 {
            color: #333;
        }
        .button {
            padding: 10px 20px;
            margin: 10px;
            background-color: #000;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            text-decoration: none;
        }
        .button:hover {
            background-color: #444;
        }
        .content {
            display: none; /* Hide content by default */
            margin-top: 20px;
        }
        .footer {
            background-color: #333;
            color: #fff;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
            font-size: 14px; /* Reduced font size for the footer */
        }
        .footer p {
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>Stay Real Media™ <span class="heartbeat">🍒</span></h1>
    </div>
    <div class="container">
        <div class="info">
            <h2>About Us</h2>
            <p>Welcome to Stay Real Media™. We are committed to bringing you the best in live broadcasts, podcasts, and media content. Our mission is to provide high-quality and engaging content to our audience.</p>
        </div>
        <div class="info">
            <h2>Our Services</h2>
            <ul>
                <li>Live Broadcasts: Stay tuned for live events and broadcasts from various industries.</li>
                <li>Podcasts: Enjoy a wide range of podcasts covering different topics and interests.</li>
                <li>Media Content: Explore our collection of images, videos, and audio files for entertainment and education.</li>
            </ul>
        </div>
        <div class="info">
            <h2>Our Mission</h2>
            <p>Stay Real Media™ is a non-profit organization dedicated to helping disadvantaged people. Our goal is to provide valuable resources and opportunities to those in need through our various media channels.</p>
        </div>
        <button class="button" aria-expanded="false" aria-controls="live-broadcast" onclick="showContent('live-broadcast', this)">Live Broadcast</button>
        <button class="button" aria-expanded="false" aria-controls="podcast" onclick="showContent('podcast', this)">Podcast</button>
        <button class="button" aria-expanded="false" aria-controls="images" onclick="showContent('images', this)">Images</button>
        <button class="button" aria-expanded="false" aria-controls="videos" onclick="showContent('videos', this)">Videos</button>
        <button class="button" aria-expanded="false" aria-controls="audio" onclick="showContent('audio', this)">Audio</button>
        
        <div id="live-broadcast" class="content" role="region">
            <h2>Live Broadcast</h2>
            <p>Placeholder for live broadcast content. Add your live broadcast embed here.</p>
        </div>
        <div id="podcast" class="content" role="region">
            <h2>Podcast</h2>
            <p>Placeholder for podcast content. Add your podcast embed here.</p>
        </div>
        <div id="images" class="content" role="region">
            <h2>Images</h2>
            <img src="c:/users/TIFOSATOR98/Pictures/Screenshot_20220514-175557.jpg" alt="Screenshot_20220514-175557">
        </div>
        <div id="videos" class="content" role="region">
            <h2>Videos</h2>
            <video controls>
                <source src="c:/users/TIFOSATOR98/videos/VID_20240814_174527.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
        <div id="audio" class="content" role="region">
            <h2>Audio</h2>
            <audio controls>
                <source src="c:/users/TIFOSATOR98/music/zero one eight.mp3" type="audio/mp3">
                Your browser does not support the audio tag.
            </audio>
        </div>
    </div>
    <footer class="footer">
        <p>Thank you for visiting Stay Real Media™. We hope you enjoy your stay with us and find our content valuable. We appreciate your support and look forward to having you visit again soon!</p>
        <p>&copy; 2024 Stay Real Media™. All rights reserved.</p>
    </footer>
    <script>
        function showContent(id, button) {
            // Hide all content sections
            var contents = document.querySelectorAll('.content');
            contents.forEach(function(content) {
                content.style.display = 'none';
            });

            // Show the selected content section
            var selectedContent = document.getElementById(id);
            if (selectedContent) {
                selectedContent.style.display = 'block';
            }

            // Update aria-expanded for accessibility
            var buttons = document.querySelectorAll('.button');
            buttons.forEach(function(btn) {
                btn.setAttribute('aria-expanded', 'false');
            });
            button.setAttribute('aria-expanded', 'true');
        }
    </script>
</body>
</html>
