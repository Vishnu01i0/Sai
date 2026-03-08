# Sai
For You!
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Women's Day</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,400;1,600&family=Great+Vibes&family=Quicksand:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #fff8f5;
            --bg-deep: #fff1eb;
            --fg: #3d2a2a;
            --fg-light: #6b4a4a;
            --accent: #c9184a;
            --accent-soft: #ff4d6d;
            --accent-light: #ff8fa3;
            --accent-pale: #ffb3c1;
            --card: rgba(255, 255, 255, 0.85);
            --card-border: rgba(201, 24, 74, 0.15);
            --gold: #d4a574;
            --gold-light: #e8c9a8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background: var(--bg);
            color: var(--fg);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Background layers */
        .bg-layer {
            position: fixed;
            inset: 0;
            pointer-events: none;
            z-index: 0;
        }

        .bg-gradient {
            background: 
                radial-gradient(ellipse 80% 60% at 50% 0%, rgba(255, 143, 163, 0.2) 0%, transparent 60%),
                radial-gradient(ellipse 60% 50% at 80% 80%, rgba(201, 24, 74, 0.08) 0%, transparent 50%),
                radial-gradient(ellipse 50% 40% at 10% 60%, rgba(212, 165, 116, 0.1) 0%, transparent 50%),
                linear-gradient(180deg, var(--bg) 0%, var(--bg-deep) 100%);
        }

        /* Floating hearts container */
        .hearts-container {
            position: fixed;
            inset: 0;
            overflow: hidden;
            pointer-events: none;
            z-index: 1;
        }

        .floating-heart {
            position: absolute;
            opacity: 0;
            animation: floatHeart linear infinite;
            pointer-events: none;
        }

        @keyframes floatHeart {
            0% {
                transform: translateY(100vh) rotate(0deg) scale(0);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            90% {
                opacity: 0.4;
            }
            100% {
                transform: translateY(-20vh) rotate(360deg) scale(1);
                opacity: 0;
            }
        }

        /* Main content */
        .main-content {
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 2rem 1rem;
            gap: 2.5rem;
        }

        /* Hero section */
        .hero {
            text-align: center;
            max-width: 800px;
            animation: fadeInUp 1.2s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-title {
            font-family: 'Great Vibes', cursive;
            font-size: clamp(2.5rem, 8vw, 5rem);
            color: var(--accent);
            margin-bottom: 1rem;
            line-height: 1.2;
            text-shadow: 2px 2px 20px rgba(201, 24, 74, 0.15);
        }

        .hero-subtitle {
            font-family: 'Cormorant Garamond', serif;
            font-size: clamp(1.1rem, 3vw, 1.5rem);
            font-weight: 400;
            color: var(--fg-light);
            font-style: italic;
            line-height: 1.6;
            max-width: 600px;
            margin: 0 auto;
        }

        .hero-divider {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
        }

        .divider-line {
            width: 60px;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--accent-soft), transparent);
        }

        .divider-heart {
            color: var(--accent-soft);
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        /* Message card */
        .message-card {
            background: var(--card);
            backdrop-filter: blur(20px);
            border: 1px solid var(--card-border);
            border-radius: 24px;
            padding: 2.5rem 2rem;
            max-width: 650px;
            width: 100%;
            box-shadow: 
                0 4px 30px rgba(201, 24, 74, 0.08),
                0 1px 3px rgba(201, 24, 74, 0.05);
            animation: fadeInUp 1.4s ease-out;
            position: relative;
            overflow: hidden;
        }

        .message-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-pale), var(--accent-soft), var(--accent), var(--accent-soft), var(--accent-pale));
        }

        .message-card-header {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .message-card-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--accent);
            letter-spacing: 0.02em;
        }

        .message-content {
            font-family: 'Quicksand', sans-serif;
            font-size: 1rem;
            line-height: 1.9;
            color: var(--fg);
            white-space: pre-line;
        }

        .message-signature {
            text-align: right;
            margin-top: 1.5rem;
            font-family: 'Great Vibes', cursive;
            font-size: 1.8rem;
            color: var(--accent);
        }

        /* Valentine section */
        .valentine-section {
            text-align: center;
            animation: fadeInUp 1.6s ease-out;
        }

        .valentine-question {
            font-family: 'Cormorant Garamond', serif;
            font-size: clamp(1.5rem, 4vw, 2.2rem);
            font-weight: 600;
            color: var(--fg);
            margin-bottom: 2rem;
        }

        .buttons-container {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            position: relative;
            min-height: 60px;
        }

        .btn {
            font-family: 'Quicksand', sans-serif;
            font-size: 1.1rem;
            font-weight: 600;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            border: none;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(255,255,255,0.3) 0%, transparent 50%);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .btn:hover::before {
            opacity: 1;
        }

        .btn-yes {
            background: linear-gradient(135deg, var(--accent-soft) 0%, var(--accent) 100%);
            color: white;
            box-shadow: 0 4px 20px rgba(201, 24, 74, 0.35);
        }

        .btn-yes:hover {
            transform: scale(1.08);
            box-shadow: 0 8px 30px rgba(201, 24, 74, 0.45);
        }

        .btn-yes:active {
            transform: scale(0.98);
        }

        .btn-no {
            background: linear-gradient(135deg, #e8e8e8 0%, #d0d0d0 100%);
            color: #666;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.2s ease;
        }

        /* Success message */
        .success-message {
            position: fixed;
            inset: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 248, 245, 0.95);
            backdrop-filter: blur(10px);
            z-index: 100;
            opacity: 0;
            visibility: hidden;
            transition: all 0.5s ease;
        }

        .success-message.active {
            opacity: 1;
            visibility: visible;
        }

        .success-content {
            text-align: center;
            padding: 2rem;
            animation: successPop 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
        }

        @keyframes successPop {
            0% {
                opacity: 0;
                transform: scale(0.5);
            }
            100% {
                opacity: 1;
                transform: scale(1);
            }
        }

        .success-heart {
            font-size: 5rem;
            color: var(--accent);
            animation: heartBeat 0.6s ease infinite alternate;
            margin-bottom: 1.5rem;
        }

        @keyframes heartBeat {
            from { transform: scale(1); }
            to { transform: scale(1.15); }
        }

        .success-title {
            font-family: 'Great Vibes', cursive;
            font-size: clamp(2rem, 6vw, 3.5rem);
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .success-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: clamp(1.2rem, 3vw, 1.6rem);
            color: var(--fg-light);
            font-style: italic;
        }

        /* Celebration hearts burst */
        .celebration-heart {
            position: fixed;
            pointer-events: none;
            z-index: 101;
            animation: burstHeart 1.5s ease-out forwards;
        }

        @keyframes burstHeart {
            0% {
                opacity: 1;
                transform: translate(0, 0) scale(1) rotate(0deg);
            }
            100% {
                opacity: 0;
                transform: translate(var(--tx), var(--ty)) scale(0) rotate(var(--rot));
            }
        }

        /* Music toggle */
        .music-toggle {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--card);
            border: 1px solid var(--card-border);
            box-shadow: 0 4px 20px rgba(201, 24, 74, 0.15);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent);
            transition: all 0.3s ease;
            z-index: 50;
        }

        .music-toggle:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 25px rgba(201, 24, 74, 0.25);
        }

        .music-toggle.playing {
            background: linear-gradient(135deg, var(--accent-soft), var(--accent));
            color: white;
        }

        .music-toggle svg {
            width: 24px;
            height: 24px;
        }

        .music-bars {
            display: flex;
            gap: 2px;
            align-items: flex-end;
            height: 16px;
        }

        .music-bar {
            width: 3px;
            background: currentColor;
            border-radius: 2px;
            animation: musicBar 0.8s ease-in-out infinite;
        }

        .music-bar:nth-child(1) { height: 60%; animation-delay: 0s; }
        .music-bar:nth-child(2) { height: 100%; animation-delay: 0.2s; }
        .music-bar:nth-child(3) { height: 40%; animation-delay: 0.4s; }
        .music-bar:nth-child(4) { height: 80%; animation-delay: 0.1s; }

        @keyframes musicBar {
            0%, 100% { transform: scaleY(1); }
            50% { transform: scaleY(0.5); }
        }

        .music-toggle:not(.playing) .music-bar {
            animation: none;
            height: 3px !important;
        }

        /* Reduced motion */
        @media (prefers-reduced-motion: reduce) {
            *, *::before, *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }

        /* Mobile adjustments */
        @media (max-width: 640px) {
            .main-content {
                padding: 1.5rem 1rem;
                gap: 2rem;
            }

            .message-card {
                padding: 2rem 1.5rem;
            }

            .message-content {
                font-size: 0.95rem;
            }

            .buttons-container {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }

            .btn {
                width: 100%;
                max-width: 200px;
            }

            .music-toggle {
                bottom: 1rem;
                right: 1rem;
                width: 44px;
                height: 44px;
            }
        }

        /* Focus states */
        .btn:focus-visible,
        .music-toggle:focus-visible {
            outline: 3px solid var(--accent-light);
            outline-offset: 3px;
        }

        /* Loading animation */
        .page-loader {
            position: fixed;
            inset: 0;
            background: var(--bg);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }

        .page-loader.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .loader-heart {
            color: var(--accent);
            animation: loaderPulse 1s ease-in-out infinite;
        }

        @keyframes loaderPulse {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.3); opacity: 0.7; }
        }
    </style>
</head>
<body>
    <!-- Page loader -->
    <div class="page-loader" id="pageLoader">
        <svg class="loader-heart" width="60" height="60" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
        </svg>
    </div>

    <!-- Background layers -->
    <div class="bg-layer bg-gradient"></div>
    <div class="hearts-container" id="heartsContainer"></div>

    <!-- Main content -->
    <main class="main-content">
        <!-- Hero section -->
        <section class="hero">
            <h1 class="hero-title">Happy Women's Day</h1>
            <p class="hero-subtitle">
                to the most strongest and lovely person that I met in my life.
            </p>
            <div class="hero-divider">
                <span class="divider-line"></span>
                <svg class="divider-heart" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
                </svg>
                <span class="divider-line"></span>
            </div>
        </section>

        <!-- Message card -->
        <article class="message-card">
            <div class="message-card-header">
                <h2 class="message-card-title">A Letter From My Heart</h2>
            </div>
            <div class="message-content">I love you Sai.
Nenu maruthunnanu.
Nenu nannu complete change chesukuntanu.
Naa alochana vidhanam chala pathaga undhi Sai.
Nenu ila ala anukuntu untanu kani nenu marthunnanu Sai.
Naakosam konni rojulu wait chesthava.
Endhukante if I achieve all my dreams in my life but if I don't have you with me, I feel like I achieved nothing Sai.
You're the biggest achievement in my life.
Infact you are the biggest thing in my life, my little cute Lotte Choco Pie.
I used to say that you are my female version and even now I say the same Sai.
You are precious always.
Once again Happy Women's Day my love.</div>
            <div class="message-signature">Forever Yours</div>
        </article>

        <!-- Valentine section -->
        <section class="valentine-section">
            <h3 class="valentine-question">Will you be my Valentine again?</h3>
            <div class="buttons-container" id="buttonsContainer">
                <button class="btn btn-yes" id="btnYes" aria-label="Yes, I will be your Valentine">
                    Yes
                </button>
                <button class="btn btn-no" id="btnNo" aria-label="No">
                    No
                </button>
            </div>
        </section>
    </main>

    <!-- Success message overlay -->
    <div class="success-message" id="successMessage" role="dialog" aria-labelledby="successTitle">
        <div class="success-content">
            <svg class="success-heart" width="80" height="80" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>
            </svg>
            <h2 class="success-title" id="successTitle">You just made me the happiest person in the world.</h2>
            <p class="success-text">I love you, always and forever.</p>
        </div>
    </div>

    <!-- Music toggle button -->
    <button class="music-toggle" id="musicToggle" aria-label="Toggle background music">
        <div class="music-bars">
            <span class="music-bar"></span>
            <span class="music-bar"></span>
            <span class="music-bar"></span>
            <span class="music-bar"></span>
        </div>
    </button>

    <!-- Background music (royalty-free romantic piano) -->
    <audio id="bgMusic" loop preload="auto">
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <script>
        // Initialize variables first
        const pageLoader = document.getElementById('pageLoader');
        const heartsContainer = document.getElementById('heartsContainer');
        const btnYes = document.getElementById('btnYes');
        const btnNo = document.getElementById('btnNo');
        const buttonsContainer = document.getElementById('buttonsContainer');
        const successMessage = document.getElementById('successMessage');
        const musicToggle = document.getElementById('musicToggle');
        const bgMusic = document.getElementById('bgMusic');

        // Heart colors for variety
        const heartColors = [
            '#c9184a',
            '#ff4d6d',
            '#ff8fa3',
            '#ffb3c1',
            '#d4a574',
            '#ff758f'
        ];

        // Create floating hearts
        function createFloatingHeart() {
            const heart = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
            heart.setAttribute('class', 'floating-heart');
            heart.setAttribute('viewBox', '0 0 24 24');
            heart.setAttribute('fill', heartColors[Math.floor(Math.random() * heartColors.length)]);
            heart.innerHTML = '<path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>';
            
            const size = Math.max(12, Math.random() * 24 + 12);
            heart.style.width = size + 'px';
            heart.style.height = size + 'px';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDuration = Math.max(8, Math.random() * 12 + 8) + 's';
            heart.style.animationDelay = Math.random() * 5 + 's';
            
            heartsContainer.appendChild(heart);
            
            // Remove heart after animation
            setTimeout(() => {
                if (heart.parentNode) {
                    heart.parentNode.removeChild(heart);
                }
            }, 20000);
        }

        // Create celebration hearts burst
        function createCelebrationHearts(x, y) {
            const numHearts = 30;
            
            for (let i = 0; i < numHearts; i++) {
                const heart = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
                heart.setAttribute('class', 'celebration-heart');
                heart.setAttribute('viewBox', '0 0 24 24');
                heart.setAttribute('fill', heartColors[Math.floor(Math.random() * heartColors.length)]);
                heart.innerHTML = '<path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/>';
                
                const size = Math.max(16, Math.random() * 32 + 16);
                heart.style.width = size + 'px';
                heart.style.height = size + 'px';
                heart.style.left = x + 'px';
                heart.style.top = y + 'px';
                
                const angle = (i / numHearts) * Math.PI * 2;
                const distance = Math.max(100, Math.random() * 200 + 100);
                const tx = Math.cos(angle) * distance;
                const ty = Math.sin(angle) * distance - 100;
                const rot = Math.random() * 720 - 360;
                
                heart.style.setProperty('--tx', tx + 'px');
                heart.style.setProperty('--ty', ty + 'px');
                heart.style.setProperty('--rot', rot + 'deg');
                
                document.body.appendChild(heart);
                
                setTimeout(() => {
                    if (heart.parentNode) {
                        heart.parentNode.removeChild(heart);
                    }
                }, 1500);
            }
        }

        // Move No button away playfully
        let noAttempts = 0;
        const funnyMessages = [
            'No',
            'Are you sure?',
            'Really?',
            'Think again!',
            'Please?',
            'Pretty please?',
            'I will be sad :(',
            'One more chance?',
            'Come on...',
            'Fine, but I love you!'
        ];

        function moveNoButton() {
            noAttempts++;
            
            if (noAttempts >= funnyMessages.length) {
                noAttempts = funnyMessages.length - 1;
            }
            
            btnNo.textContent = funnyMessages[noAttempts];
            
            const containerRect = buttonsContainer.getBoundingClientRect();
            const btnRect = btnNo.getBoundingClientRect();
            
            // Calculate new position within viewport
            const maxX = Math.min(window.innerWidth - btnRect.width - 20, containerRect.right + 100);
            const minX = Math.max(20, containerRect.left - 150);
            const maxY = Math.min(window.innerHeight - btnRect.height - 100, containerRect.bottom + 80);
            const minY = Math.max(100, containerRect.top - 80);
            
            const newX = Math.random() * (maxX - minX) + minX;
            const newY = Math.random() * (maxY - minY) + minY;
            
            btnNo.style.position = 'fixed';
            btnNo.style.left = newX + 'px';
            btnNo.style.top = newY + 'px';
            btnNo.style.transition = 'all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1)';
            btnNo.style.zIndex = '60';
        }

        // Event listeners
        btnYes.addEventListener('click', function(e) {
            const rect = btnYes.getBoundingClientRect();
            const x = rect.left + rect.width / 2;
            const y = rect.top + rect.height / 2;
            
            createCelebrationHearts(x, y);
            
            setTimeout(() => {
                successMessage.classList.add('active');
            }, 300);
        });

        btnNo.addEventListener('mouseenter', moveNoButton);
        btnNo.addEventListener('focus', moveNoButton);
        btnNo.addEventListener('touchstart', function(e) {
            e.preventDefault();
            moveNoButton();
        }, { passive: false });

        // Music toggle
        let isPlaying = false;
        bgMusic.volume = 0.3;

        musicToggle.addEventListener('click', function() {
            if (isPlaying) {
                bgMusic.pause();
                musicToggle.classList.remove('playing');
            } else {
                bgMusic.play().catch(() => {
                    console.log('Audio autoplay prevented');
                });
                musicToggle.classList.add('playing');
            }
            isPlaying = !isPlaying;
        });

        // Initialize floating hearts
        function initHearts() {
            // Create initial batch
            for (let i = 0; i < 8; i++) {
                setTimeout(createFloatingHeart, i * 500);
            }
            
            // Continue creating hearts
            setInterval(createFloatingHeart, 2000);
        }

        // Hide loader and start animations
        window.addEventListener('load', function() {
            setTimeout(() => {
                pageLoader.classList.add('hidden');
                initHearts();
            }, 800);
        });

        // Handle visibility change to manage animations
        document.addEventListener('visibilitychange', function() {
            if (document.hidden && isPlaying) {
                bgMusic.pause();
            } else if (!document.hidden && isPlaying) {
                bgMusic.play();
            }
        });

        // Keyboard accessibility for success message
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && successMessage.classList.contains('active')) {
                successMessage.classList.remove('active');
            }
        });

        // Reset No button on resize
        window.addEventListener('resize', function() {
            if (noAttempts > 0) {
                btnNo.style.position = '';
                btnNo.style.left = '';
                btnNo.style.top = '';
            }
        });
    </script>
</body>
</html>
