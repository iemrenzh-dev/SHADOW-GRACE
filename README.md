<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SHADOW & GRACE | Premiere Fine Art & Boudoir</title>
    
    <!-- Sophisticated Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@200;300;400;600&display=swap" rel="stylesheet">

    <style>
        :root {
            --bg-deep: #050505;
            --bg-card: #0F0F0F;
            --pink-blush: #F4C2C2; /* Naughty/Soft Pink accent */
            --pink-muted: #D9A7A7;
            --text-main: #FFFFFF;
            --text-muted: #94A3B8;
            --font-head: 'Playfair Display', serif;
            --font-body: 'Inter', sans-serif;
            --border: rgba(244, 194, 194, 0.15);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        body {
            background-color: var(--bg-deep);
            color: var(--text-main);
            font-family: var(--font-body);
            line-height: 1.7;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 { font-family: var(--font-head); font-weight: 400; text-transform: uppercase; letter-spacing: 3px; }
        .italic { font-style: italic; text-transform: none; font-family: 'Playfair Display'; }
        p { font-weight: 300; }

        /* Navigation */
        nav {
            position: fixed;
            top: 0; width: 100%; z-index: 1000;
            padding: 25px 5%;
            display: flex; justify-content: space-between; align-items: center;
            background: rgba(5, 5, 5, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
        }
        .brand-logo { font-size: 24px; letter-spacing: 6px; }
        .brand-logo span { color: var(--pink-blush); }
        .nav-links a { text-decoration: none; color: var(--text-muted); font-size: 11px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; margin-left: 30px; transition: 0.3s; }
        .nav-links a:hover { color: var(--pink-blush); }

        /* Hero Section */
        #hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.7)), 
                        url('https://4kwallpapers.com/images/wallpapers/sydney-sweeney-1920x1080-25603.jpg?1710510906?auto=compress&cs=tinysrgb&w=1600') center/cover no-repeat;
            padding: 0 5%;
        }
        .hero-content h1 { font-size: clamp(40px, 8vw, 100px); line-height: 0.9; margin-bottom: 30px; }
        .hero-content span { color: var(--pink-blush); font-size: 13px; letter-spacing: 5px; text-transform: uppercase; display: block; margin-bottom: 20px; }

        .btn {
            display: inline-block;
            padding: 20px 50px;
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-size: 11px;
            font-weight: 600;
            transition: 0.4s;
            background: var(--pink-blush);
            color: #000;
        }
        .btn:hover { background: #fff; transform: translateY(-3px); box-shadow: 0 10px 20px rgba(244, 194, 194, 0.2); }

        /* Container Section */
        .container { max-width: 1400px; margin: 0 auto; padding: 0 5%; }
        section { padding: 120px 0; }
        .section-header { text-align: center; margin-bottom: 80px; }
        .section-header h2 { font-size: 50px; margin-bottom: 20px; }
        .section-header p { color: var(--text-muted); text-transform: uppercase; letter-spacing: 3px; font-size: 12px; }

        /* FOUR BOXES: Photography Styles/Projects */
        .style-grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
            gap: 20px; 
        }
        .style-card { 
            background: var(--bg-card); 
            border: 1px solid var(--border); 
            overflow: hidden; 
            position: relative;
        }
        .style-card img { 
            width: 100%; 
            height: 450px; 
            object-fit: cover; 
            filter: grayscale(0.6); 
            transition: 0.8s ease; 
        }
        .style-card:hover img { filter: grayscale(0); transform: scale(1.05); }
        .style-info { 
            padding: 30px; 
            background: linear-gradient(to top, var(--bg-card) 70%, transparent);
        }
        .style-info h3 { font-size: 22px; margin-bottom: 10px; color: var(--pink-blush); }
        .style-info p { font-size: 13px; color: var(--text-muted); }

        /* Investment/Pricing */
        .price-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        .price-card { padding: 60px 40px; background: var(--bg-card); border: 1px solid var(--border); text-align: center; }
        .price-card.featured { border-color: var(--pink-blush); box-shadow: 0 0 30px rgba(244, 194, 194, 0.05); }
        .price-card h3 { font-size: 26px; margin-bottom: 15px; }
        .price-card .cost { font-size: 45px; font-family: var(--font-head); color: var(--pink-blush); margin-bottom: 30px; display: block; }
        .price-card ul { list-style: none; margin-bottom: 40px; text-align: left; }
        .price-card li { margin-bottom: 15px; font-size: 13px; color: var(--text-muted); border-bottom: 1px solid rgba(255,255,255,0.03); padding-bottom: 10px; }

        /* FAQ Section */
        .faq-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); gap: 60px; }
        .faq-item h4 { font-size: 18px; margin-bottom: 15px; color: var(--pink-blush); border-left: 3px solid var(--pink-blush); padding-left: 15px; }
        .faq-item p { font-size: 15px; color: var(--text-muted); padding-left: 18px; }

        /* Footer */
        footer { padding: 80px 0; border-top: 1px solid var(--border); text-align: center; }
        .footer-logo { font-size: 30px; margin-bottom: 30px; display: block; letter-spacing: 5px; }
        .socials { display: flex; justify-content: center; gap: 40px; margin-bottom: 30px; }
        .socials a { color: var(--text-muted); text-decoration: none; font-size: 11px; letter-spacing: 2px; text-transform: uppercase; transition: 0.3s; }
        .socials a:hover { color: var(--pink-blush); }

    </style>
</head>
<body>

    <nav>
        <div class="brand-logo">SHADOW <span>&</span> GRACE</div>
        <div class="nav-links">
            <a href="#hero">Home</a>
            <a href="#projects">Projects</a>
            <a href="#investment">Pricing</a>
            <a href="#faq">FAQ</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <!-- 1. HERO -->
    <section id="hero">
        <div class="hero-content">
            <span>Intimacy • Shadow • Art</span>
            <h1>ARTISTRY IN THE <br><span class="italic">Unveiled Form.</span></h1>
            <a href="#projects" class="btn">Explore Portfolio</a>
        </div>
    </section>

    <!-- 2. FOUR BOXES: PROJECTS & STYLES -->
    <section id="projects" class="container">
        <div class="section-header">
            <p>Our Signature Styles</p>
            <h2>PHOTOGRAPHY <span class="italic">Series</span></h2>
        </div>
        <div class="style-grid">
            <!-- Box 1 -->
            <div class="style-card">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQOkIgyTTBZvN4CIdGOWQWhmT59ITCc5HRz0w&s?auto=compress&cs=tinysrgb&w=800">
                <div class="style-info">
                    <h3>The Noir Project</h3>
                    <p>Dramatic low-key lighting focused on high contrast and deep shadows to emphasize silhouette and mystery.</p>
                </div>
            </div>
            <!-- Box 2 -->
            <div class="style-card">
                <img src="https://i.pinimg.com/736x/95/0f/20/950f202b8152aeb504241bd82072db88.jpg?auto=compress&cs=tinysrgb&w=800">
                <div class="style-info">
                    <h3>Ethereal Glow</h3>
                    <p>High-key, soft focus photography using natural light to create a romantic, airy, and timeless atmosphere.</p>
                </div>
            </div>
            <!-- Box 3 -->
            <div class="style-card">
                <img src="https://i.pinimg.com/736x/2d/7f/fe/2d7ffe7e87b3eee10766b517b65cd62c.jpg?auto=compress&cs=tinysrgb&w=800">
                <div class="style-info">
                    <h3>Textural Studies</h3>
                    <p>Exploring the interplay between skin and fine fabrics like silk and lace for an editorial, high-fashion feel.</p>
                </div>
            </div>
          
        </div>
    </section>

    <!-- 3. INVESTMENT / PRICING -->
    <section id="investment" style="background: #080808; border-top: 1px solid var(--border); border-bottom: 1px solid var(--border);">
        <div class="container">
            <div class="section-header">
                <p>Private Art Sessions</p>
                <h2>THE <span class="italic">Investment</span></h2>
            </div>
            <div class="price-grid">
                <div class="price-card">
                    <h3>The Study</h3>
                    <span class="cost">$650</span>
                    <ul>
                        <li>60 Minute Private Session</li>
                        <li>1 Artistic Direction</li>
                        <li>5 Hand-Retouched Master Files</li>
                        <li>Private Digital Gallery</li>
                    </ul>
                    <a href="#contact" class="btn" style="padding: 15px 30px;">Inquire</a>
                </div>
                <div class="price-card featured">
                    <h3>The Collection</h3>
                    <span class="cost">$1,200</span>
                    <ul>
                        <li>3 Hour Experience</li>
                        <li>3 Wardrobe Changes</li>
                        <li>15 Hand-Retouched Master Files</li>
                        <li>Professional Hair & Makeup</li>
                        <li>$100 Print Credit</li>
                    </ul>
                    <a href="#contact" class="btn" style="padding: 15px 30px;">Inquire</a>
                </div>
                <div class="price-card">
                    <h3>The Heirloom</h3>
                    <span class="cost">$2,800</span>
                    <ul>
                        <li>Full Day Studio Booking</li>
                        <li>Unlimited Wardrobe</li>
                        <li>All High-Res Retouched Files</li>
                        <li>Hand-Bound Italian Art Book</li>
                        <li>Luxury Gift Box Packaging</li>
                    </ul>
                    <a href="#contact" class="btn" style="padding: 15px 30px;">Inquire</a>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. FAQ SECTION -->
    <section id="faq" class="container">
        <div class="section-header">
            <p>Your Comfort First</p>
            <h2>FREQUENTLY <span class="italic">Asked</span></h2>
        </div>
        <div class="faq-grid">
            <div class="faq-item">
                <h4>How is my privacy protected?</h4>
                <p>Discretion is our core value. Images are never shared publicly without signed, written consent. Your gallery is password-protected and hosted on encrypted servers.</p>
            </div>
            <div class="faq-item">
                <h4>What if I'm not a model?</h4>
                <p>99% of our clients aren't models. Our job is to guide you through every breath and pose, ensuring you look and feel like a work of art.</p>
            </div>
            <div class="faq-item">
                <h4>What should I bring?</h4>
                <p>We provide a comprehensive "Prep Guide" upon booking. We also offer a curated client closet of silks and lace for your use.</p>
            </div>
            <div class="faq-item">
                <h4>Do you retouch the photos?</h4>
                <p>Yes. We specialize in artful retouching—enhancing skin tone and lighting while preserving your natural, authentic beauty.</p>
            </div>
        </div>
    </section>

    <!-- 5. CONTACT -->
    <section id="contact" style="background: var(--bg-card);">
        <div class="container" style="max-width: 800px; text-align: center;">
            <h2 style="font-size: 50px; margin-bottom: 20px;">BEGIN YOUR <span class="italic">Story</span></h2>
            <p style="color: var(--text-muted); margin-bottom: 50px;">Strictly confidential inquiries for private sessions.</p>
            <form onsubmit="event.preventDefault(); alert('Private Inquiry Received.');">
                <input type="text" placeholder="NAME" style="width: 100%; padding: 20px; background: #000; border: 1px solid var(--border); color: #fff; margin-bottom: 15px; outline: none; font-family: var(--font-body);">
                <input type="email" placeholder="EMAIL" style="width: 100%; padding: 20px; background: #000; border: 1px solid var(--border); color: #fff; margin-bottom: 15px; outline: none; font-family: var(--font-body);">
                <textarea rows="5" placeholder="WHAT IS YOUR VISION?" style="width: 100%; padding: 20px; background: #000; border: 1px solid var(--border); color: #fff; margin-bottom: 30px; outline: none; font-family: var(--font-body);"></textarea>
                <button type="submit" class="btn" style="width: 100%;">Submit Private Inquiry</button>
            </form>
        </div>
    </section>

    <footer>
        <span class="brand-logo footer-logo">SHADOW <span>&</span> GRACE</span>
        <div class="socials">
            <a href="#">Instagram</a>
            <a href="#">Privacy</a>
            <a href="#">Terms</a>
        </div>
        <p style="color: #444; font-size: 10px; letter-spacing: 2px;">© 2024 SHADOW & GRACE ARTISTRY. ALL CONTENT PROTECTED UNDER COPYRIGHT LAW.</p>
    </footer>

</body>
</html>
