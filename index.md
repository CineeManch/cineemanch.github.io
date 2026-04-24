<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CineeManch | Cinema ki har baat, hamare saath</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-black: #050505;
            --accent-red: #e50914;
        }

        body {
            background-color: var(--bg-black);
            color: white;
            font-family: 'Inter', sans-serif;
            margin: 0;
        }

        /* THE HERO SECTION USES YOUR BANNER.PNG */
        .hero-section {
            width: 100%;
            height: 90vh; /* This makes it take up most of the screen */
            background: 
                linear-gradient(to bottom, rgba(0,0,0,0) 60%, var(--bg-black) 100%), 
                url('Banner.png');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: flex-end; /* Puts buttons at the bottom of the image */
            justify-content: center;
            padding-bottom: 100px;
        }

        .btn-red {
            background: var(--accent-red);
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            text-transform: uppercase;
            margin: 10px;
            display: inline-block;
        }

        .stats-container {
            display: flex;
            justify-content: space-around;
            padding: 50px 5%;
            background: #111;
            text-align: center;
        }

        .stat-item h2 { color: var(--accent-red); margin: 0; font-size: 2.5rem; }
        .stat-item p { color: #888; text-transform: uppercase; font-size: 0.8rem; }
    </style>
</head>
<body>

    <section class="hero-section">
        <div style="text-align: center;">
            <a href="https://youtube.com/@cineemanch" class="btn-red">▶ Watch Latest Review</a>
            <a href="#" class="btn-red" style="background:none; border: 2px solid white;">Subscribe</a>
        </div>
    </section>

    <div class="stats-container">
        <div class="stat-item">
            <h2>50K+</h2>
            <p>Subscribers</p>
        </div>
        <div class="stat-item">
            <h2>2M+</h2>
            <p>Total Views</p>
        </div>
        <div class="stat-item">
            <h2>300+</h2>
            <p>Videos</p>
        </div>
    </div>

</body>
</html>
