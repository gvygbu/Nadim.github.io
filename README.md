[nadimm.html](https://github.com/user-attachments/files/25254488/nadimm.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Nadim - Web3 Ambassador & Community Moderator.">
    <title>Nadim | Web3 Professional</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        :root {
            --bg-deep: #050505;
            --glass-matte: rgba(20, 20, 20, 0.6);
            --glass-border: rgba(255, 255, 255, 0.08);
            --accent-red: #ff3b3b;
            --accent-glow: rgba(255, 59, 59, 0.4);
            --text-main: #ffffff;
            --text-muted: #a1a1aa;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Outfit', sans-serif; }

        body {
            background-color: var(--bg-deep);
            color: var(--text-main);
            overflow-x: hidden;
            min-height: 100vh;
            padding: 20px;
            padding-bottom: 120px; /* Space for dock */
        }

        /* --- LIQUID BACKGROUND ANIMATION --- */
        .liquid-bg {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1;
            background: #000;
        }
        .orb {
            position: absolute; border-radius: 50%;
            filter: blur(80px); opacity: 0.6;
            animation: floatLiquid 10s infinite alternate ease-in-out;
        }
        .orb-1 { width: 400px; height: 400px; background: #550000; top: -50px; left: -100px; }
        .orb-2 { width: 500px; height: 500px; background: #880000; bottom: -100px; right: -100px; animation-delay: -3s; }
        .orb-3 { width: 300px; height: 300px; background: #ff3b3b; top: 40%; left: 30%; opacity: 0.2; animation-delay: -5s; }

        @keyframes floatLiquid {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(30px, -30px) scale(1.1); }
        }

        /* --- BENTO GRID SYSTEM --- */
        .main-wrapper {
            max-width: 1100px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 20px;
        }

        .bento-card {
            background: var(--glass-matte);
            backdrop-filter: blur(40px);
            -webkit-backdrop-filter: blur(40px);
            border: 1px solid var(--glass-border);
            border-radius: 24px;
            padding: 25px;
            position: relative;
            overflow: hidden;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            box-shadow: 0 10px 30px -10px rgba(0,0,0,0.5);
        }

        .bento-card:hover {
            border-color: var(--accent-red);
            transform: translateY(-5px);
            box-shadow: 0 0 30px var(--accent-glow);
        }

        /* --- GRID PLACEMENTS --- */
        .profile-sec { grid-column: span 12; display: flex; align-items: center; gap: 30px; }
        .stat-box { grid-column: span 4; text-align: center; padding: 20px; }
        
        /* ABOUT SECTION (NEW) */
        .about-text-sec { grid-column: span 8; }
        .trait-sec { grid-column: span 4; }

        .experience-sec { grid-column: span 7; }
        .language-sec { grid-column: span 5; }
        .service-full { grid-column: span 12; }
        .contact-details-sec { grid-column: span 12; }
        .form-sec { grid-column: span 12; }

        @media (max-width: 768px) {
            .profile-sec { flex-direction: column; text-align: center; }
            .stat-box { grid-column: span 12; }
            .about-text-sec, .trait-sec { grid-column: span 12; }
            .experience-sec, .language-sec { grid-column: span 12; }
            .service-grid-inner { grid-template-columns: 1fr; }
        }

        /* --- TYPOGRAPHY --- */
        h1 { font-size: clamp(2.5rem, 5vw, 4rem); font-weight: 800; line-height: 1.1; }
        h1 span { color: var(--accent-red); }
        h2 { font-size: 1.5rem; margin-bottom: 20px; color: #fff; display: flex; align-items: center; gap: 10px; }
        p { color: var(--text-muted); line-height: 1.6; font-size: 1rem; }
        
        .tagline {
            display: inline-block; padding: 6px 14px;
            background: rgba(255, 59, 59, 0.1); border: 1px solid rgba(255, 59, 59, 0.3);
            color: var(--accent-red); border-radius: 50px; font-weight: 600; font-size: 0.85rem;
            margin-bottom: 15px;
        }

        .big-num { font-size: 3rem; font-weight: 800; color: #fff; display: block; }
        .stat-label { font-size: 0.9rem; color: var(--text-muted); font-weight: 500; }

        /* --- TRAIT PILLS --- */
        .trait-list { display: flex; flex-wrap: wrap; gap: 10px; }
        .trait-pill {
            background: #151515; padding: 10px 15px; border-radius: 12px;
            font-size: 0.9rem; color: #fff; border: 1px solid #333; font-weight: 600;
        }
        .trait-pill i { color: var(--accent-red); margin-right: 5px; }

        /* --- EXPERIENCE TIMELINE --- */
        .timeline { position: relative; padding-left: 20px; border-left: 2px solid #333; }
        .t-item { margin-bottom: 25px; position: relative; }
        .t-item::before {
            content: ''; position: absolute; left: -26px; top: 5px;
            width: 10px; height: 10px; background: var(--accent-red);
            border-radius: 50%; box-shadow: 0 0 10px var(--accent-red);
        }
        .t-item:last-child { margin-bottom: 0; }
        .t-role { font-size: 1.1rem; font-weight: 700; color: #fff; }
        .t-desc { font-size: 0.95rem; color: var(--text-muted); margin-top: 5px; }

        /* --- LANGUAGE BARS --- */
        .lang-item { margin-bottom: 18px; }
        .lang-head { display: flex; justify-content: space-between; margin-bottom: 8px; font-size: 0.95rem; font-weight: 600; color: #fff; }
        .lang-bar-bg { width: 100%; height: 8px; background: #1a1a1a; border-radius: 4px; overflow: hidden; }
        .lang-bar-fill { height: 100%; background: var(--accent-red); width: 0; border-radius: 4px; animation: fillBar 1.5s forwards ease-out; }
        
        @keyframes fillBar { to { width: var(--w); } }

        /* --- SERVICE GRID --- */
        .service-grid-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .service-card-mini { 
            background: rgba(255,255,255,0.02); 
            border: 1px solid var(--glass-border);
            padding: 20px; border-radius: 18px;
        }
        .svc-header { display: flex; align-items: center; gap: 10px; margin-bottom: 15px; }
        .svc-icon { 
            width: 40px; height: 40px; border-radius: 10px; 
            background: rgba(255, 59, 59, 0.1); color: var(--accent-red);
            display: flex; align-items: center; justify-content: center; font-size: 1.2rem;
        }
        .svc-title { font-size: 1.2rem; font-weight: 700; color: #fff; }
        .svc-list { list-style: none; }
        .svc-list li { display: flex; gap: 10px; margin-bottom: 10px; font-size: 0.95rem; color: var(--text-muted); }
        .svc-list li i { color: var(--accent-red); margin-top: 5px; }

        /* --- CONTACT VISIBLE --- */
        .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; }
        .contact-card {
            background: rgba(0,0,0,0.3); border: 1px solid var(--glass-border);
            padding: 15px; border-radius: 15px; display: flex; align-items: center; gap: 15px;
            text-decoration: none; transition: 0.3s;
        }
        .contact-card:hover { border-color: var(--accent-red); background: rgba(255,59,59,0.05); }
        .c-icon { width: 45px; height: 45px; border-radius: 12px; display: flex; align-items: center; justify-content: center; font-size: 1.3rem; color: #fff; flex-shrink: 0; }
        .c-twitter { background: #000; }
        .c-telegram { background: #229ED9; }
        .c-discord { background: #5865F2; }
        .c-email { background: var(--accent-red); }
        .c-info { display: flex; flex-direction: column; overflow: hidden; }
        .c-label { font-size: 0.8rem; color: var(--text-muted); font-weight: 600; text-transform: uppercase; }
        .c-value { font-size: 1rem; font-weight: 700; color: #fff; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }

        /* --- FORM --- */
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 15px; }
        input, textarea, select {
            width: 100%; padding: 16px; border-radius: 14px;
            background: #0a0a0a; border: 1px solid #333; color: #fff;
            font-size: 1rem; outline: none; transition: 0.3s;
        }
        select option { background: #000; color: #fff; }
        input:focus, textarea:focus, select:focus { border-color: var(--accent-red); }
        .btn-send {
            width: 100%; padding: 18px; border-radius: 14px;
            background: var(--accent-red); color: white; font-weight: 700; font-size: 1.1rem;
            border: none; cursor: pointer; transition: 0.3s; display: flex; align-items: center; justify-content: center; gap: 10px;
        }
        .btn-send:hover { background: #ff1f1f; transform: translateY(-2px); }

        /* --- DOCK --- */
        .social-dock {
            position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
            display: flex; gap: 15px; padding: 12px 25px;
            background: rgba(15, 15, 15, 0.85); backdrop-filter: blur(20px);
            border-radius: 50px; border: 1px solid #333; z-index: 100;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
        .dock-btn { color: #fff; font-size: 22px; transition: 0.3s; text-decoration: none; display: flex; align-items: center; justify-content: center; }
        .dock-btn:hover { color: var(--accent-red); transform: scale(1.2); }

    </style>
</head>
<body>

    <div class="liquid-bg">
        <div class="orb orb-1"></div>
        <div class="orb orb-2"></div>
        <div class="orb orb-3"></div>
    </div>

    <div class="main-wrapper">
        
        <div class="bento-card profile-sec">
            <div>
                <span class="tagline">Open for Work</span>
                <h1>I am Nadim.<br><span>Web3</span> Manager.</h1>
                <p style="max-width: 600px; margin-top: 15px; font-size: 1.1rem;">
                    I help Crypto Projects grow. I have experience with 400+ projects. I manage communities, stop spammers, and make everything run smoothly.
                </p>
                <div style="margin-top: 25px; display: flex; flex-wrap: wrap; gap: 15px;">
                    <span style="font-size: 14px; background: #151515; padding: 8px 15px; border-radius: 8px; border: 1px solid #222;">
                        <i class="fas fa-graduation-cap" style="color: var(--accent-red); margin-right: 5px;"></i> BBA Honours (Management)
                    </span>
                    <span style="font-size: 14px; background: #151515; padding: 8px 15px; border-radius: 8px; border: 1px solid #222;">
                        <i class="fas fa-history" style="color: var(--accent-red); margin-right: 5px;"></i> 2nd Year Student
                    </span>
                </div>
            </div>
        </div>

        <div class="bento-card stat-box">
            <span class="big-num">90k+</span>
            <span class="stat-label">Community Members</span>
        </div>
        <div class="bento-card stat-box">
            <span class="big-num">400+</span>
            <span class="stat-label">Projects Handled</span>
        </div>
        <div class="bento-card stat-box">
            <span class="big-num">24/7</span>
            <span class="stat-label">Active Support</span>
        </div>

        <div class="bento-card about-text-sec">
            <h2><i class="fas fa-user" style="color:var(--accent-red)"></i> About Me</h2>
            <p style="font-size: 1.05rem; line-height: 1.7;">
                Hello! My name is <strong>Nadim</strong>. I am a student and a Crypto lover. 
                I started trading 5 years ago. I learned a lot about how markets work. 
                Now, I use my skills to help new projects. I like to keep things simple, safe, and fun for everyone.
            </p>
        </div>

        <div class="bento-card trait-sec">
            <h2><i class="fas fa-bolt" style="color:var(--accent-red)"></i> My Vibe</h2>
            <div class="trait-list">
                <div class="trait-pill"><i class="fas fa-bolt"></i> Fast Reply</div>
                <div class="trait-pill"><i class="fas fa-smile"></i> Friendly</div>
                <div class="trait-pill"><i class="fas fa-shield-alt"></i> Honest</div>
                <div class="trait-pill"><i class="fas fa-brain"></i> Smart</div>
                <div class="trait-pill"><i class="fas fa-clock"></i> Active</div>
            </div>
        </div>

        <div class="bento-card experience-sec">
            <h2><i class="fas fa-briefcase" style="color:var(--accent-red)"></i> Experience</h2>
            <div class="timeline">
                <div class="t-item">
                    <div class="t-role">Community Manager</div>
                    <p class="t-desc">Leading a massive 90k+ member crypto community. Managing mods, banning bots, and organizing AMA events.</p>
                </div>
                <div class="t-item">
                    <div class="t-role">Web3 Content Creator</div>
                    <p class="t-desc">Worked with 400+ projects to create video guides, memes, and promotional graphics.</p>
                </div>
                <div class="t-item">
                    <div class="t-role">Crypto Trader</div>
                    <p class="t-desc">Started journey as a trader, learning market psychology and project analysis.</p>
                </div>
            </div>
        </div>

        <div class="bento-card language-sec">
            <h2><i class="fas fa-language" style="color:var(--accent-red)"></i> Languages</h2>
            
            <div class="lang-item">
                <div class="lang-head">
                    <span>Bengali (Native)</span>
                    <span>100%</span>
                </div>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="--w: 100%"></div></div>
            </div>

            <div class="lang-item">
                <div class="lang-head">
                    <span>English (Professional)</span>
                    <span>90%</span>
                </div>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="--w: 90%"></div></div>
            </div>

            <div class="lang-item">
                <div class="lang-head">
                    <span>Hindi (Fluent)</span>
                    <span>85%</span>
                </div>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="--w: 85%"></div></div>
            </div>

            <div style="margin-top: 30px;">
                <h3 style="font-size: 1rem; color: #fff; margin-bottom: 10px;">Favorite Tools</h3>
                <div style="display: flex; flex-wrap: wrap; gap: 8px;">
                    <span style="font-size: 12px; background: #222; padding: 5px 10px; border-radius: 6px; color: #ddd;">Telegram</span>
                    <span style="font-size: 12px; background: #222; padding: 5px 10px; border-radius: 6px; color: #ddd;">Discord</span>
                    <span style="font-size: 12px; background: #222; padding: 5px 10px; border-radius: 6px; color: #ddd;">Canva</span>
                    <span style="font-size: 12px; background: #222; padding: 5px 10px; border-radius: 6px; color: #ddd;">X (Twitter)</span>
                </div>
            </div>
        </div>

        <div class="bento-card service-full">
            <h2><i class="fas fa-layer-group" style="color:var(--accent-red)"></i> What I Can Do For You</h2>
            
            <div class="service-grid-inner">
                
                <div class="service-card-mini">
                    <div class="svc-header">
                        <div class="svc-icon"><i class="fab fa-telegram"></i></div>
                        <div class="svc-title">Telegram Management</div>
                    </div>
                    <ul class="svc-list">
                        <li><i class="fas fa-check"></i> I delete spam links and ban bots instantly.</li>
                        <li><i class="fas fa-check"></i> I pin important news so everyone sees it.</li>
                        <li><i class="fas fa-check"></i> I welcome new members and guide them.</li>
                    </ul>
                </div>

                <div class="service-card-mini">
                    <div class="svc-header">
                        <div class="svc-icon"><i class="fab fa-discord"></i></div>
                        <div class="svc-title">Discord Moderation</div>
                    </div>
                    <ul class="svc-list">
                        <li><i class="fas fa-check"></i> I handle support tickets quickly.</li>
                        <li><i class="fas fa-check"></i> I organize channels and roles.</li>
                        <li><i class="fas fa-check"></i> I host games and events for the community.</li>
                    </ul>
                </div>

                <div class="service-card-mini">
                    <div class="svc-header">
                        <div class="svc-icon"><i class="fab fa-x-twitter"></i></div>
                        <div class="svc-title">Twitter Ambassador</div>
                    </div>
                    <ul class="svc-list">
                        <li><i class="fas fa-check"></i> I post tweets to hype your project.</li>
                        <li><i class="fas fa-check"></i> I reply to big accounts to get attention.</li>
                        <li><i class="fas fa-check"></i> I help increase your followers organically.</li>
                    </ul>
                </div>

                <div class="service-card-mini">
                    <div class="svc-header">
                        <div class="svc-icon"><i class="fas fa-video"></i></div>
                        <div class="svc-title">Content & Graphics</div>
                    </div>
                    <ul class="svc-list">
                        <li><i class="fas fa-check"></i> I make "How-to" videos for users.</li>
                        <li><i class="fas fa-check"></i> I design banners for announcements.</li>
                        <li><i class="fas fa-check"></i> I write simple blogs in English/Hindi.</li>
                    </ul>
                </div>

            </div>
        </div>

        <div class="bento-card contact-details-sec">
            <h2><i class="fas fa-address-book" style="color:var(--accent-red)"></i> Contact Details</h2>
            <div class="contact-grid">
                
                <a href="https://t.me/Nabil_vai11" target="_blank" class="contact-card">
                    <div class="c-icon c-telegram"><i class="fab fa-telegram-plane"></i></div>
                    <div class="c-info">
                        <span class="c-label">Telegram</span>
                        <span class="c-value">@Nabil_vai11</span>
                    </div>
                </a>

                <a href="https://x.com/Al_Nadim_nabil" target="_blank" class="contact-card">
                    <div class="c-icon c-twitter"><i class="fab fa-x-twitter"></i></div>
                    <div class="c-info">
                        <span class="c-label">Twitter</span>
                        <span class="c-value">@Al_Nadim_nabil</span>
                    </div>
                </a>

                <a href="https://discordapp.com/users/1322262720979931216" target="_blank" class="contact-card">
                    <div class="c-icon c-discord"><i class="fab fa-discord"></i></div>
                    <div class="c-info">
                        <span class="c-label">Discord</span>
                        <span class="c-value">Click to Chat</span>
                    </div>
                </a>

                <a href="mailto:nadimskip035@gmail.com" class="contact-card">
                    <div class="c-icon c-email"><i class="fas fa-envelope"></i></div>
                    <div class="c-info">
                        <span class="c-label">Email</span>
                        <span class="c-value">nadimskip035@gmail.com</span>
                    </div>
                </a>

            </div>
        </div>

        <div class="bento-card form-sec">
            <h2><i class="fas fa-paper-plane" style="color:var(--accent-red)"></i> Start a Project with Nadim</h2>
            <p style="margin-bottom: 25px;">Fill this form or message me on Telegram for a quick reply.</p>

            <form action="https://formsubmit.co/nadimskip035@gmail.com" method="POST">
                <input type="hidden" name="_subject" value="New Job Inquiry for Nadim!">
                <input type="hidden" name="_captcha" value="false">

                <div class="form-row">
                    <input type="text" name="name" placeholder="Your Name" required>
                    <input type="email" name="email" placeholder="Your Email" required>
                </div>

                <div class="form-row">
                    <select name="service">
                        <option value="" disabled selected>Service Needed?</option>
                        <option>Community Management</option>
                        <option>Ambassador Role</option>
                        <option>Video & Graphics</option>
                        <option>Just Networking</option>
                    </select>
                    
                    <select name="budget">
                        <option value="" disabled selected>Your Budget</option>
                        <option>Under $500</option>
                        <option>$500 - $1000</option>
                        <option>Over $1000</option>
                        <option>No Budget / Networking</option>
                    </select>
                </div>

                <textarea name="message" rows="5" placeholder="Hi Nadim, I want to discuss..." style="margin-bottom: 20px;" required></textarea>

                <button type="submit" class="btn-send">Send Message <i class="fas fa-arrow-right"></i></button>
            </form>
        </div>

    </div>

    <div class="social-dock">
        <a href="https://x.com/Al_Nadim_nabil" target="_blank" class="dock-btn"><i class="fab fa-x-twitter"></i></a>
        <a href="http://t.me/Nabil_vai11" target="_blank" class="dock-btn"><i class="fab fa-telegram-plane"></i></a>
        <a href="https://discordapp.com/users/1322262720979931216" target="_blank" class="dock-btn"><i class="fab fa-discord"></i></a>
        <a href="mailto:nadimskip035@gmail.com" class="dock-btn"><i class="fas fa-envelope"></i></a>
    </div>

</body>
</html>
