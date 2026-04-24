<header class="container-fluid p-0">
    <div class="banner-container">
        <img src="banner.jpg" alt="Cineemanch Banner" class="img-fluid w-100 banner-img">
    </div>
</header>

<style>
    :root {
        --bg-deep: #0f1012;
        --sidebar-bg: #16181b;
        --accent-red: #e50914;
        --text-dim: #a0a0a0;
    }

    body {
        background-color: var(--bg-deep);
        color: white;
        font-family: 'Inter', sans-serif;
        overflow-x: hidden;
        margin: 0;
    }

    /* Banner Styling */
    .banner-container {
        width: 100%;
        max-height: 400px; 
        overflow: hidden;
        border-bottom: 2px solid var(--accent-red);
        position: relative;
    }
    
    .banner-img {
        width: 100%;
        height: 400px;
        object-fit: cover;
        object-position: center;
        /* Cinematic fade at the bottom */
        mask-image: linear-gradient(to bottom, black 85%, transparent 100%);
        -webkit-mask-image: linear-gradient(to bottom, black 85%, transparent 100%);
    }

    /* Layout Structure */
    .app-container {
        display: flex;
        flex-wrap: wrap;
    }

    /* Column 1: Left Nav */
    .side-nav {
        flex: 0 0 250px;
        background-color: var(--sidebar-bg);
        height: 100vh;
        position: sticky;
        top: 0;
        border-right: 1px solid #2d2d2d;
        padding: 2rem;
    }

    .brand-logo {
        font-weight: 800;
        font-size: 1.8rem;
        color: var(--accent-red);
        margin-bottom: 3rem;
        text-transform: uppercase;
        display: block;
        text-decoration: none;
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
        flex: 1;
        min-width: 0; /* Prevents flex items from overflowing */
        padding: 0; /* Removed padding so banner hits edges */
    }

    .content-padding {
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
        flex: 0 0 320px;
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
        padding: 1rem;
        margin-bottom: 1.5rem;
        border-left: 4px solid var(--accent-red);
        transition: transform 0.2s;
    }

    .feed-item:hover {
        transform: scale(1.02);
    }

    /* Responsive Adjustments */
    @media (max-width: 1200px) {
        .right-feed { display: none; } /* Hide feed on smaller desktops */
    }

    @media (max-width: 992px) {
        .side-nav {
            flex: 1 1 100%;
            height: auto;
            position: relative;
            border-right: none;
            border-bottom: 1px solid #2d2d2d;
        }
        .main-content { flex: 1 1 100%; }
    }
</style>
