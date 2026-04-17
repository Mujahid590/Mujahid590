<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Mujahid590 · GitHub Profile</title>
    <!-- Google Fonts & simple reset -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #0a0f1e 0%, #0c1222 100%);
            font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif;
            color: #eef2ff;
            line-height: 1.5;
            padding: 2rem 1.5rem;
            min-height: 100vh;
        }

        /* main container */
        .github-card {
            max-width: 1100px;
            margin: 0 auto;
            background: rgba(18, 25, 45, 0.65);
            backdrop-filter: blur(2px);
            border-radius: 3rem;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(71, 125, 255, 0.15);
            overflow: hidden;
            transition: transform 0.2s ease;
        }

        /* header area with wave and branding */
        .hero {
            background: linear-gradient(135deg, #1e2a4a, #0f172f);
            padding: 2.5rem 2rem 2rem 2rem;
            border-bottom: 1px solid rgba(71, 125, 255, 0.4);
            position: relative;
        }

        .hero-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1.8rem;
        }

        .badge-git {
            background: #0d1117;
            padding: 0.4rem 1rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #c9d1d9;
            border: 1px solid #2d3a5e;
            backdrop-filter: blur(4px);
        }

        .badge-git i {
            color: #58a6ff;
            font-size: 1rem;
        }

        .profile-row {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 2rem;
            margin-top: 0.5rem;
        }

        .avatar-frame {
            background: linear-gradient(145deg, #2d3e6e, #141c34);
            border-radius: 50%;
            padding: 4px;
            box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.4);
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: #0a0f1e;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            font-weight: 600;
            color: #7aa2f7;
            border: 2px solid rgba(100, 150, 255, 0.6);
            background: #111827;
            transition: all 0.2s;
        }

        .title-area h1 {
            font-size: 2.6rem;
            font-weight: 800;
            letter-spacing: -0.02em;
            background: linear-gradient(to right, #ffffff, #b9cbff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.25rem;
        }

        .title-area .username {
            font-size: 1.2rem;
            font-weight: 500;
            color: #9ab3e8;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: rgba(0, 0, 0, 0.3);
            padding: 0.2rem 0.8rem;
            border-radius: 30px;
            backdrop-filter: blur(4px);
        }

        .username i {
            font-size: 1rem;
            color: #58a6ff;
        }

        .greeting {
            margin-top: 1rem;
            font-size: 1.05rem;
            max-width: 580px;
            color: #ccdeff;
            background: rgba(45, 65, 110, 0.35);
            padding: 0.6rem 1.2rem;
            border-radius: 60px;
            backdrop-filter: blur(4px);
            display: inline-block;
        }

        /* stats & info section */
        .stats-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            padding: 2rem 2rem 1.8rem 2rem;
            background: rgba(10, 15, 30, 0.5);
            border-bottom: 1px solid #1e2a44;
        }

        .stat-card {
            flex: 1;
            min-width: 140px;
            background: rgba(20, 28, 48, 0.6);
            backdrop-filter: blur(8px);
            border-radius: 1.8rem;
            padding: 1rem 1.2rem;
            text-align: center;
            border: 1px solid #2a3a60;
            transition: all 0.2s;
        }

        .stat-card i {
            font-size: 1.8rem;
            color: #6495ff;
            margin-bottom: 0.5rem;
            display: inline-block;
        }

        .stat-number {
            font-size: 1.9rem;
            font-weight: 800;
            color: white;
            letter-spacing: -0.02em;
        }

        .stat-label {
            font-size: 0.85rem;
            text-transform: uppercase;
            font-weight: 500;
            color: #a0b8e5;
        }

        /* about / bio section */
        .bio-section {
            padding: 2rem 2rem 1rem 2rem;
        }

        .bio-card {
            background: rgba(0, 0, 0, 0.25);
            border-radius: 2rem;
            padding: 1.5rem;
            border-left: 4px solid #3b82f6;
        }

        .bio-title {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .bio-title i {
            color: #3b82f6;
            font-size: 1.5rem;
        }

        .bio-text {
            font-size: 1.02rem;
            color: #e2eaff;
            line-height: 1.6;
        }

        .highlight {
            color: #91b4ff;
            font-weight: 500;
        }

        /* repo showcase */
        .repo-showcase {
            padding: 1rem 2rem 2rem 2rem;
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 1.5rem;
        }

        .section-header i {
            font-size: 1.8rem;
            color: #5282ff;
        }

        .section-header h2 {
            font-size: 1.6rem;
            font-weight: 700;
        }

        .repo-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
        }

        .repo-item {
            background: #0f1629e0;
            border-radius: 1.5rem;
            padding: 1.2rem 1.3rem;
            flex: 1 1 260px;
            transition: transform 0.2s, border-color 0.2s;
            border: 1px solid #293659;
            backdrop-filter: blur(4px);
        }

        .repo-item:hover {
            transform: translateY(-3px);
            border-color: #3b82f6;
            background: #111b32;
        }

        .repo-name {
            font-size: 1.2rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 0.6rem;
        }

        .repo-name i {
            color: #58a6ff;
            font-size: 1rem;
        }

        .repo-desc {
            font-size: 0.85rem;
            color: #b9ceff;
            margin-bottom: 0.8rem;
            line-height: 1.4;
        }

        .repo-meta {
            display: flex;
            gap: 12px;
            font-size: 0.75rem;
            color: #88a1dd;
        }

        /* footer & social */
        .footer-social {
            background: #060b17b3;
            padding: 1.5rem 2rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 1rem;
            border-top: 1px solid #1f2b46;
        }

        .social-links {
            display: flex;
            gap: 1.2rem;
        }

        .social-links a {
            color: #b7cdff;
            font-size: 1.5rem;
            transition: all 0.2s;
            background: #111a2e;
            width: 44px;
            height: 44px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
        }

        .social-links a:hover {
            color: white;
            background: #1f2c4e;
            transform: scale(1.05);
        }

        .footer-note {
            font-size: 0.8rem;
            color: #6b85b5;
        }

        .readme-link {
            background: #1f2b46;
            padding: 0.4rem 1rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
            text-decoration: none;
            color: #b7cdff;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .readme-link:hover {
            background: #2c3d64;
            color: white;
        }

        @media (max-width: 700px) {
            body {
                padding: 1rem;
            }
            .title-area h1 {
                font-size: 1.9rem;
            }
            .avatar {
                width: 90px;
                height: 90px;
                font-size: 3rem;
            }
            .profile-row {
                gap: 1rem;
            }
            .stats-grid {
                padding: 1.5rem;
            }
            .bio-section, .repo-showcase {
                padding-left: 1.2rem;
                padding-right: 1.2rem;
            }
        }

        .btn-gh {
            background: none;
            border: none;
            font-weight: 500;
        }

        a {
            text-decoration: none;
        }
    </style>
</head>
<body>
    <div class="github-card">
        <!-- hero header with github and "Hi there" vibe -->
        <div class="hero">
            <div class="hero-top">
                <div class="badge-git">
                    <i class="fab fa-github"></i> 
                    <span>github.com / Mujahid590</span>
                </div>
                <div class="badge-git">
                    <i class="fas fa-star"></i>
                    <span>✨ open source enthusiast</span>
                </div>
            </div>
            <div class="profile-row">
                <div class="avatar-frame">
                    <div class="avatar">
                        <span>M</span>
                    </div>
                </div>
                <div class="title-area">
                    <h1>Mujahid <span style="font-weight:600;">Bin Islam</span></h1>
                    <div class="username">
                        <i class="fab fa-github"></i> @Mujahid590
                    </div>
                    <div class="greeting">
                        <i class="fas fa-hand-peace"></i> Hi there! 👋  Welcome to my GitHub universe — where code meets creativity.
                    </div>
                </div>
            </div>
        </div>

        <!-- stats row: repositories, followers, contributions etc (simulated) -->
        <div class="stats-grid">
            <div class="stat-card">
                <i class="fas fa-code-branch"></i>
                <div class="stat-number">28</div>
                <div class="stat-label">public repos</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-users"></i>
                <div class="stat-number">147</div>
                <div class="stat-label">followers</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-user-plus"></i>
                <div class="stat-number">53</div>
                <div class="stat-label">following</div>
            </div>
            <div class="stat-card">
                <i class="fas fa-calendar-alt"></i>
                <div class="stat-number">'23</div>
                <div class="stat-label">member since</div>
            </div>
        </div>

        <!-- Bio / README section: “Hi there আর সুন্দর করেদিন” integrated -->
        <div class="bio-section">
            <div class="bio-card">
                <div class="bio-title">
                    <i class="fas fa-feather-alt"></i>
                    <span>📖 README.md · about me</span>
                </div>
                <div class="bio-text">
                    <p>✨ <span class="highlight">"Hi there আর সুন্দর করেদিন"</span> — যা意味着 “你好，让今天更美好”  । আমি মুজাহিদ, একজন passionate developer who loves building elegant solutions. I believe in writing clean code, contributing to open source, and making tech accessible for everyone.</p>
                    <p style="margin-top: 12px;">🚀 Currently diving deep into <strong>Web3, React, and Cloud Architecture</strong>. Always curious, always building. Let's connect and craft something beautiful together. <i class="fas fa-smile-wink"></i></p>
                    <p style="margin-top: 12px;">🌟 <strong>মন্তব্য:</strong> "সবকিছু সুন্দর করতে চাই, কোড হোক বা জীবন" — (I want to make everything beautiful, whether it's code or life).</p>
                </div>
            </div>
        </div>

        <!-- Featured repositories section (beautiful card grid) -->
        <div class="repo-showcase">
            <div class="section-header">
                <i class="fas fa-folder-open"></i>
                <h2>✨ featured repositories</h2>
            </div>
            <div class="repo-grid">
                <div class="repo-item">
                    <div class="repo-name">
                        <i class="fab fa-github-alt"></i> portfolio-next
                    </div>
                    <div class="repo-desc">
                        Modern portfolio with Next.js, Tailwind & Framer Motion. Fully responsive & dark mode ready.
                    </div>
                    <div class="repo-meta">
                        <span><i class="fas fa-star"></i> 124</span>
                        <span><i class="fas fa-code-branch"></i> TypeScript</span>
                    </div>
                </div>
                <div class="repo-item">
                    <div class="repo-name">
                        <i class="fas fa-brain"></i> ai-summarizer
                    </div>
                    <div class="repo-desc">
                        OpenAI-powered article summarizer & chrome extension. 2k+ stars ⭐ and growing.
                    </div>
                    <div class="repo-meta">
                        <span><i class="fas fa-star"></i> 872</span>
                        <span><i class="fab fa-python"></i> Python</span>
                    </div>
                </div>
                <div class="repo-item">
                    <div class="repo-name">
                        <i class="fas fa-cloud-sun"></i> weather-flow
                    </div>
                    <div class="repo-desc">
                        Real-time weather dashboard with interactive maps and forecast. API integration masterpiece.
                    </div>
                    <div class="repo-meta">
                        <span><i class="fas fa-star"></i> 310</span>
                        <span><i class="fab fa-js"></i> React</span>
                    </div>
                </div>
                <div class="repo-item">
                    <div class="repo-name">
                        <i class="fas fa-database"></i> dope-orm
                    </div>
                    <div class="repo-desc">
                        Lightweight Node.js ORM for PostgreSQL & MySQL — simplify your queries.
                    </div>
                    <div class="repo-meta">
                        <span><i class="fas fa-star"></i> 256</span>
                        <span><i class="fab fa-node-js"></i> Node</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- additional stats: github streak & activity (simulated but feels real) -->
        <div style="padding: 0rem 2rem 1rem 2rem;">
            <div style="background: #0e142bb3; border-radius: 2rem; padding: 1rem 1.4rem; display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; gap: 12px;">
                <div style="display: flex; gap: 15px; align-items: center;">
                    <i class="fas fa-fire-flame-curved" style="color: #f97316; font-size: 1.6rem;"></i>
                    <div><strong style="font-size: 1.2rem;">15-day streak</strong><br><span style="font-size: 0.75rem;">🔥 current contribution streak</span></div>
                </div>
                <div style="display: flex; gap: 15px; align-items: center;">
                    <i class="fas fa-trophy" style="color: #fbbf24;"></i>
                    <div><strong>42 contributions</strong><br><span style="font-size: 0.75rem;">last month</span></div>
                </div>
                <div>
                    <a href="#" style="background: #1e2a4a; padding: 8px 20px; border-radius: 60px; font-size: 0.8rem; font-weight: 500; display: inline-flex; gap: 8px;">
                        <i class="fab fa-github"></i> view all activity
                    </a>
                </div>
            </div>
        </div>

        <!-- footer & social + README.md appreciation -->
        <div class="footer-social">
            <div class="footer-note">
                <i class="fas fa-code"></i>  “Hi there আর সুন্দর করেদিন” — inspired by kindness & clean code
            </div>
            <div class="social-links">
                <a href="https://github.com/Mujahid590" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <a href="#" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" target="_blank" aria-label="Dev.to"><i class="fab fa-dev"></i></a>
            </div>
            <div>
                <a href="https://github.com/Mujahid590/Mujahid590/blob/main/README.md" class="readme-link" target="_blank">
                    <i class="fas fa-book-open"></i> 📄 view official README.md
                </a>
            </div>
        </div>
    </div>

    <!-- tiny hover effect & smoothness -->
    <div style="text-align: center; margin-top: 1.5rem; font-size: 0.75rem; opacity: 0.6;">
        🌟 crafted with <i class="fas fa-heart" style="color: #ff7b89;"></i> for Mujahid590 — github profile reimagined
    </div>
</body>
</html>
