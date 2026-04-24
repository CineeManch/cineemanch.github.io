<section class="blog-section">
    <div class="container">
        <div class="d-flex justify-content-between align-items-end mb-5">
            <div>
                <h2 class="fw-bold text-white">Video Reviews</h2>
                <p class="text-secondary mb-0">Latest uploads from Cineemanch</p>
            </div>
        </div>

        <div class="row g-4" id="youtube-feed">
            <div class="col-12 text-center text-secondary">
                <p>Loading your latest reviews...</p>
            </div>
        </div>
    </div>
</section>

<script>
    const API_KEY = 'YOUR_API_KEY_HERE'; 
    const CHANNEL_ID = 'UC_p470C_vL8_hK_kR0V-WWA'; // Cineemanch ID

    async function buildVideoFeed() {
        try {
            // 1. Get the 'Uploads' playlist ID
            const channelUrl = `https://www.googleapis.com/youtube/v3/channels?part=contentDetails&id=${CHANNEL_ID}&key=${API_KEY}`;
            const channelRes = await fetch(channelUrl);
            const channelData = await channelRes.json();
            const uploadsId = channelData.items[0].contentDetails.relatedPlaylists.uploads;

            // 2. Get the latest 10 videos from that playlist
            const playlistUrl = `https://www.googleapis.com/youtube/v3/playlistItems?part=snippet&playlistId=${uploadsId}&maxResults=10&key=${API_KEY}`;
            const playlistRes = await fetch(playlistUrl);
            const playlistData = await playlistRes.json();
            
            const feedContainer = document.getElementById('youtube-feed');
            feedContainer.innerHTML = ''; // Clear the loading text

            // 3. Loop through videos and create HTML cards
            playlistData.items.forEach(item => {
                const video = item.snippet;
                const videoId = video.resourceId.videoId;
                
                const cardHtml = `
                    <div class="col-md-6 col-lg-4">
                        <div class="card review-card h-100" style="background: #1a1d20; border: 1px solid #333; border-radius: 12px; overflow: hidden;">
                            <div class="ratio ratio-16x9">
                                <iframe src="https://www.youtube.com/embed/${videoId}" allowfullscreen></iframe>
                            </div>
                            <div class="card-body">
                                <h5 class="card-title fw-bold text-white">${video.title}</h5>
                                <p class="card-text text-secondary small">${video.description.substring(0, 100)}...</p>
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
