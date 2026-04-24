<style>
    /* Adding a geometric font to match your banner's "Cineemanch" logo */
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@800&family=Inter:wght@400;600;800&display=swap');

    :root {
        --bg-deep: #0a0a0b;
        --sidebar-bg: #121214;
        --accent-red: #e50914;
        --text-dim: #b3b3b3;
    }

    body {
        background-color: var(--bg-deep);
        color: white;
        font-family: 'Inter', sans-serif;
        margin: 0;
        overflow-x: hidden;
    }

    /* 1. Header & Banner - Optimized for your Theater Image */
    .banner-wrapper {
        width: 100%;
        background-color: var(--bg-deep);
        border-bottom: 3px solid var(--accent-red);
        overflow: hidden;
        position: relative;
    }

    .hero-banner {
        width: 100%;
        max-height: 450px; /* Increased to show more of that beautiful theater ceiling */
        object-fit: cover;
        display: block;
        /* Sharper cinematic fade for a professional look */
        mask-image: linear-gradient(to bottom, black 85%, transparent 100%);
        -webkit-mask-image: linear-gradient(to bottom, black 85%, transparent 100%);
    }

    /* 2. Brand Identity - Matches the font style in your banner */
    .brand-title {
        font-family: 'Orbitron', sans-serif; /* Geometric/Tech font like your logo */
        font-weight: 800;
        color: var(--accent-red);
        font-size: 1.6rem;
        text-transform: uppercase;
        letter-spacing: 2px;
        margin-bottom: 2rem;
        display: block;
        text-decoration: none;
    }

    /* 3. Column Layout */
    .app-container {
        display: flex;
        flex-wrap: wrap;
    }

    .side-nav {
        flex: 0 0 260px;
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
        transition: 0.3s ease;
        margin-bottom: 0.5rem;
        display: block;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 0.85rem;
        letter-spacing: 1px;
    }

    .nav-link:hover, .nav-link.active {
        background: rgba(229, 9, 20, 0.15);
        color: white;
        border-left: 3px solid var(--accent-red);
    }

    .main-content { 
        flex: 1;
        min-width: 0;
        padding: 2.5rem; 
    }

    .video-spotlight {
        background: #16181b;
        border-radius: 16px;
        padding: 1.5rem;
        border: 1px solid #2d2d2d;
        box-shadow: 0 20px 40px rgba(0,0,0,0.6);
    }

    .right-feed {
        flex: 0 0 320px;
        height: 100vh;
        position: sticky;
        top: 0;
        padding: 2rem;
        border-left: 1px solid #2d2d2d;
        overflow-y: auto;
        background: rgba(10, 10, 11, 0.5);
    }

    .feed-item {
        background: #1a1d20;
        border-radius: 12px;
        margin-bottom: 1.5rem;
        border-left: 4px solid var(--accent-red);
        transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        padding: 10px;
    }

    .feed-item:hover { 
        transform: scale(1.03); 
        background: #25282c;
    }

    /* 4. Responsive Design */
    @media (max-width: 992px) {
        .app-container { flex-direction: column; }
        .side-nav, .right-feed { 
            flex: 1 1 auto; 
            height: auto; 
            position: relative; 
            border: none; 
            padding: 1.5rem; 
        }
        .hero-banner { max-height: 250px; }
    }
</style>        }

        .nav-link:hover, .nav-link.active {
            background: rgba(229, 9, 20, 0.1);
            color: var(--accent-red);
        }

        .main-content { padding: 2.5rem; }

        .video-spotlight {
            background: #1a1d20;
            border-radius: 16px;
            padding: 1.5rem;
            border: 1px solid #333;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

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
            margin-bottom: 1.2rem;
            border-left: 4px solid var(--accent-red);
            transition: 0.2s;
        }

        .feed-item:hover { transform: translateX(5px); }

        /* 3. Scroll Reveal Elements */
        #scroll-logo {
            max-height: 40px;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.4s ease-out;
        }

        #scroll-logo.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .brand-title {
            font-weight: 800;
            color: var(--accent-red);
            font-size: 1.4rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        @media (max-width: 992px) {
            .side-nav, .right-feed { height: auto; position: relative; border: none; padding: 1.5rem; }
            .hero-banner { max-height: 200px; }
        }
    </style>
</head>
<body>

    <div class="banner-wrapper">
        <img src="Modern Gaming Cover YouTube Channel Art-2.jpg" alt="Cineemanch Banner" class="hero-banner">
    </div>

    <div class="container-fluid">
        <div class="row">
            
            <nav class="col-lg-2 side-nav d-none d-lg-block">
                <div class="text-center mb-5">
                    <img src="Modern Gaming Cover YouTube Channel Art-2.jpg" id="scroll-logo" alt="Logo">
                    <div class="brand-title mt-2">Cineemanch</div>
                </div>
                
                <a href="#" class="nav-link active">Home</a>
                <a href="#video-reviews" class="nav-link">Movie Reviews</a>
                <a href="#blog" class="nav-link">Written Blog</a>
                <hr class="text-secondary">
                <a href="https://youtube.com/@cineemanch" target="_blank" class="nav-link">YouTube Channel</a>
            </nav>

            <main class="col-lg-7 main-content">
                <h2 class="fw-bold mb-4">Featured Review</h2>
                <div class="video-spotlight">
                    <div class="ratio ratio-16x9 mb-4">
                        <iframe src="https://www.youtube.com/embed/FrqmF_AEU5s" title="The Batman Review" allowfullscreen></iframe>
                    </div>
                    <h1 class="fw-bold h2 mb-3">The Batman: A Visual Masterclass</h1>
                    <p class="text-secondary lead">Does Matt Reeves' vision hold up under the Cineemanch lens? We break down the lighting, the score, and the soul of Gotham.</p>
                </div>
                
                <section id="blog" class="mt-5 pt-5">
                    <h3 class="fw-bold mb-4">Latest Blog Posts</h3>
                    <div class="row g-4">
                        <div class="col-md-6">
                            <div class="p-3 bg-dark border rounded">
                                <span class="badge bg-danger mb-2">9.5/10</span>
                                <h5 class="fw-bold">The Technical Brilliance of Batman</h5>
                                <p class="small text-secondary">A written deep-dive into the cinematography...</p>
                            </div>
                        </div>
                    </div>
                </section>
            </main>

            <aside class="col-lg-3 right-feed">
                <h4 class="fw-bold mb-4">Recent Uploads</h4>
                
                <div class="feed-item p-3">
                    <div class="text-danger small fw-bold">NEW</div>
                    <h6 class="fw-bold">The Batman 2026 Analysis</h6>
                    <p class="small text-secondary mb-0">Visual breakdown of the year's biggest hit.</p>
                </div>

                <div class="feed-item p-3">
                    <div class="text-secondary small fw-bold">PREVIOUS</div>
                    <h6 class="fw-bold">Why Sound Matters</h6>
                    <p class="small text-secondary mb-0">Exploring Dolby Atmos in modern cinema.</p>
                </div>
            </aside>

        </div>
    </div>

    <script>
        window.onscroll = function() {
            const logo = document.getElementById('scroll-logo');
            const banner = document.querySelector('.banner-wrapper');
            
            // If user scrolls past 300px (roughly the banner height)
            if (window.scrollY > 300) {
                logo.classList.add('visible');
            } else {
                logo.classList.remove('visible');
            }
        };
    </script>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
