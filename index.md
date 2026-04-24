<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cineemanch | Front Page</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        :root {
            --bg-deep: #0a0b0c;
            --sidebar-bg: #121416;
            --accent-red: #e50914;
            --text-dim: #9ca3af;
        }

        body {
            background-color: var(--bg-deep);
            color: white;
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }

        /* Column 1: Left Nav */
        .side-nav {
            background-color: var(--sidebar-bg);
            height: 100vh;
            position: sticky;
            top: 0;
            border-right: 1px solid #2d2d2d;
            padding: 2rem;
        }

        .nav-link {
            color: var(--text-dim);
            font-weight: 600;
            padding: 0.8rem 1rem;
            border-radius: 8px;
            transition: all 0.3s;
            margin-bottom: 0.5rem;
            display: block;
            text-decoration: none;
        }

        .nav-link:hover, .nav-link.active {
            background: rgba(229, 9, 20, 0.1);
            color: var(--accent-red);
        }

        /* Column 2: Center Spotlight */
        .main-content {
            padding: 2rem;
        }

        .video-spotlight {
            background: #1a1d20;
            border-radius: 16px;
            padding: 1.5rem;
            border: 1px solid #333;
        }

        /* Column 3: Right Chronological Feed */
        .right-feed {
            height: 100vh;
            position: sticky;
            top: 0;
            padding: 2rem;
            border-left: 1px solid #2d2d2d;
            overflow-y: auto;
        }

        .feed-item {
            background: #1a1d20;
            border-radius: 10px;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--accent-red);
            transition: transform 0.2s;
        }

        .feed-item:hover {
            transform: scale(1.02);
        }

        .brand-logo {
            font-weight: 800;
            font-size: 1.8rem;
            color: var(--accent-red);
            margin-bottom: 3rem;
            text-transform: uppercase;
        }

        @media (max-width: 992px) {
            .side-nav, .right-feed { height: auto; position: relative; border: none; }
        }
    </style>
</head>
<body>

<div class="container-fluid">
    <div class="row">
        
        <nav class="col-lg-2 side-nav d-none d-lg-block">
            <div class="brand-logo text-center">Cineemanch</div>
            <a href="#" class="nav-link active">Home</a>
            <a href="#video-reviews" class="nav-link">Movie Reviews</a>
            <a href="#blog" class="nav-link">Written Blog</a>
            <hr class="text-secondary">
            <a href="https://youtube.com/@cineemanch" class="nav-link">YouTube</a>
            <a href="#" class="nav-link">Instagram</a>
        </nav>

        <main class="col-lg-7 main-content">
            <div class="d-flex justify-content-between align-items-center mb-4">
                <h2 class="fw-bold">Latest Release</h2>
                <span class="badge bg-danger">LIVE NOW</span>
            </div>

            <div class="video-spotlight mb-5">
                <div class="ratio ratio-16x9 mb-4">
                    <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" allowfullscreen></iframe>
                </div>
                <h1 class="fw-bold h2 mb-3">Is This the Best Film of 2026? | Full Breakdown</h1>
                <p class="text-secondary">We explore the nuances of the cinematography and the shocking twist at the end. Make sure to watch until the final minute for our Cineemanch Verdict.</p>
                <div class="mt-4">
                    <button class="btn btn-danger me-2">Watch on YouTube</button>
                    <button class="btn btn-outline-light">Read Full Blog Review</button>
                </div>
            </div>

            <section id="movie-reviews" class="mt-5">
                <h3 class="fw-bold mb-4">Trending Analysis</h3>
                <div class="row g-4">
                    <div class="col-md-6">
                        <div class="p-3 bg-dark border rounded">
                            <h5 class="fw-bold">War Machine 2026</h5>
                            <p class="small text-secondary">A masterclass in tension...</p>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="p-3 bg-dark border rounded">
                            <h5 class="fw-bold">Sci-Fi Revival</h5>
                            <p class="small text-secondary">Why old tech is back...</p>
                        </div>
                    </div>
                </div>
            </section>
        </main>

        <aside class="col-lg-3 right-feed">
            <h4 class="fw-bold mb-4">Feed History</h4>
            
            <div class="feed-item p-3">
                <div class="text-danger small fw-bold mb-1">YESTERDAY</div>
                <h6 class="fw-bold mb-1">Interstellar 2 Theory</h6>
                <p class="small text-secondary mb-0">Breaking down the physics...</p>
            </div>

            <div class="feed-item p-3">
                <div class="text-danger small fw-bold mb-1">2 DAYS AGO</div>
                <h6 class="fw-bold mb-1">The Oscar Snubs</h6>
                <p class="small text-secondary mb-0">Who got left out this year?</p>
            </div>

            <div class="feed-item p-3">
                <div class="text-danger small fw-bold mb-1">4 DAYS AGO</div>
                <h6 class="fw-bold mb-1">Indie Gem Review</h6>
                <p class="small text-secondary mb-0">Silent Echo is a must-watch.</p>
            </div>

            <div class="text-center mt-4">
                <a href="#" class="text-danger text-decoration-none small fw-bold">LOAD MORE →</a>
            </div>
        </aside>

    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>            height: 200px;
            object-fit: cover;
        }

        .badge-rating {
            background-color: var(--accent-red);
            font-weight: 700;
        }

        .footer {
            padding: 40px 0;
            border-top: 1px solid #2a2e32;
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand brand-name" href="#">CINEEMANCH</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#blog">Written Reviews</a></li>
                    <li class="nav-item"><a class="nav-link" href="https://www.youtube.com/@cineemanch" target="_blank">YouTube</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <section class="spotlight-section">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-7">
                    <div class="video-container">
                        <div class="ratio ratio-16x9">
                            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Latest Review" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5 mt-4 mt-lg-0 ps-lg-5">
                    <span class="text-danger fw-bold text-uppercase">New Video Review</span>
                    <h1 class="spotlight-title">Is This the Best Sci-Fi of 2026?</h1>
                    <p class="text-secondary lead">We dive deep into the cinematography and narrative structure of the latest blockbuster. Check out the full breakdown in our video.</p>
                    <a href="https://www.youtube.com/@cineemanch" class="btn btn-danger btn-lg px-4 mt-3">Subscribe on YouTube</a>
                </div>
            </div>
        </div>
    </section>

    <section class="blog-section" id="blog">
        <div class="container">
            <div class="d-flex justify-content-between align-items-end mb-5">
                <div>
                    <h2 class="fw-bold">Latest Written Reviews</h2>
                    <p class="text-secondary mb-0">Deep dives and critical analysis.</p>
                </div>
                <a href="#" class="text-danger text-decoration-none fw-bold">View All Posts →</a>
            </div>

            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">8.5/10</span>
                            <h4 class="card-title fw-bold">War Machine: A Technical Masterclass</h4>
                            <p class="card-text text-secondary">A breakdown of the sound design and why this film demands a theater experience...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">6.0/10</span>
                            <h4 class="card-title fw-bold">The Sequel Nobody Asked For</h4>
                            <p class="card-text text-secondary">Does this franchise still have legs, or is it running on nostalgia? Our honest take...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">9.2/10</span>
                            <h4 class="card-title fw-bold">Indie Gems: 'Silent Echo'</h4>
                            <p class="card-text text-secondary">Why this small-budget project is outshining the major studios this season...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer text-center">
        <div class="container">
            <p>© 2026 Cineemanch. All rights reserved.</p>
            <div class="d-flex justify-content-center gap-3">
                <a href="#" class="text-secondary text-decoration-none">Twitter</a>
                <a href="#" class="text-secondary text-decoration-none">Instagram</a>
                <a href="https://www.youtube.com/@cineemanch" class="text-secondary text-decoration-none">YouTube</a>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>                                <p class="card-text text-secondary small">${video.description.substring(0, 100)}...</p>
                            </div>
                        </div>
                    </div>
                `;
                feedContainer.innerHTML += cardHtml;
            });

        } catch (error) {
            console.error("Feed Error:", error);
            document.getElementById('youtube-feed').innerHTML = "<p class='text-danger'>Failed to load feed. Check API Key.</p>";
        }
    }

    buildVideoFeed();
</script>            height: 200px;
            object-fit: cover;
        }

        .badge-rating {
            background-color: var(--accent-red);
            font-weight: 700;
        }

        .footer {
            padding: 40px 0;
            border-top: 1px solid #2a2e32;
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand brand-name" href="#">CINEEMANCH</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#blog">Written Reviews</a></li>
                    <li class="nav-item"><a class="nav-link" href="https://www.youtube.com/@cineemanch" target="_blank">YouTube</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <section class="spotlight-section">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-7">
                    <div class="video-container">
                        <div class="ratio ratio-16x9">
                            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Latest Review" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5 mt-4 mt-lg-0 ps-lg-5">
                    <span class="text-danger fw-bold text-uppercase">New Video Review</span>
                    <h1 class="spotlight-title">Is This the Best Sci-Fi of 2026?</h1>
                    <p class="text-secondary lead">We dive deep into the cinematography and narrative structure of the latest blockbuster. Check out the full breakdown in our video.</p>
                    <a href="https://www.youtube.com/@cineemanch" class="btn btn-danger btn-lg px-4 mt-3">Subscribe on YouTube</a>
                </div>
            </div>
        </div>
    </section>

    <section class="blog-section" id="blog">
        <div class="container">
            <div class="d-flex justify-content-between align-items-end mb-5">
                <div>
                    <h2 class="fw-bold">Latest Written Reviews</h2>
                    <p class="text-secondary mb-0">Deep dives and critical analysis.</p>
                </div>
                <a href="#" class="text-danger text-decoration-none fw-bold">View All Posts →</a>
            </div>

            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">8.5/10</span>
                            <h4 class="card-title fw-bold">War Machine: A Technical Masterclass</h4>
                            <p class="card-text text-secondary">A breakdown of the sound design and why this film demands a theater experience...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">6.0/10</span>
                            <h4 class="card-title fw-bold">The Sequel Nobody Asked For</h4>
                            <p class="card-text text-secondary">Does this franchise still have legs, or is it running on nostalgia? Our honest take...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>

                <div class="col-md-4">
                    <div class="card review-card">
                        <div class="card-body">
                            <span class="badge badge-rating mb-2">9.2/10</span>
                            <h4 class="card-title fw-bold">Indie Gems: 'Silent Echo'</h4>
                            <p class="card-text text-secondary">Why this small-budget project is outshining the major studios this season...</p>
                            <a href="#" class="btn btn-outline-light btn-sm mt-2">Read More</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer text-center">
        <div class="container">
            <p>© 2026 Cineemanch. All rights reserved.</p>
            <div class="d-flex justify-content-center gap-3">
                <a href="#" class="text-secondary text-decoration-none">Twitter</a>
                <a href="#" class="text-secondary text-decoration-none">Instagram</a>
                <a href="https://www.youtube.com/@cineemanch" class="text-secondary text-decoration-none">YouTube</a>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
