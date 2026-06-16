<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shine and Dandy Cleaning Co.</title>
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --pink: #e8508a;
    --pink-light: #f4a0c0;
    --pink-pale: #fce8f0;
    --pink-soft: #fdf0f6;
    --charcoal: #2d2d2d;
    --gray: #888;
    --white: #ffffff;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Montserrat', sans-serif;
    color: var(--charcoal);
    background: var(--white);
    overflow-x: hidden;
  }

  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 18px 60px;
    background: rgba(255,255,255,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(232,80,138,0.12);
  }
  .nav-logo {
    font-family: 'Great Vibes', cursive;
    font-size: 2rem;
    color: var(--pink);
    letter-spacing: 1px;
  }
  .nav-links {
    display: flex;
    gap: 36px;
    list-style: none;
  }
  .nav-links a {
    text-decoration: none;
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--charcoal);
    transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--pink); }
  .nav-cta {
    background: var(--pink);
    color: white !important;
    padding: 10px 24px;
    border-radius: 30px;
    transition: background 0.3s, transform 0.2s !important;
  }
  .nav-cta:hover { background: #c03d73 !important; transform: translateY(-1px); }

  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, #fff9fc 0%, #fce8f0 40%, #fff 100%);
    padding-top: 80px;
  }
  .hero-sparkles {
    position: absolute;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
  }
  .sparkle {
    position: absolute;
    color: var(--pink-light);
    font-size: 1.2rem;
    animation: twinkle 3s ease-in-out infinite;
    opacity: 0;
  }
  @keyframes twinkle {
    0%, 100% { opacity: 0; transform: scale(0.5) rotate(0deg); }
    50% { opacity: 0.7; transform: scale(1.2) rotate(180deg); }
  }
  .hero-content {
    text-align: center;
    z-index: 2;
    padding: 0 20px;
    animation: fadeUp 1s ease 0.2s both;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-eyebrow {
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--pink);
    margin-bottom: 16px;
  }
  .hero-title {
    font-family: 'Great Vibes', cursive;
    font-size: clamp(4rem, 10vw, 8rem);
    color: var(--pink);
    line-height: 1.1;
    margin-bottom: 8px;
    text-shadow: 2px 2px 20px rgba(232,80,138,0.15);
  }
  .hero-subtitle-block {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    margin-bottom: 16px;
  }
  .hero-subtitle-block .line {
    width: 60px;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--pink-light));
  }
  .hero-subtitle-block .line:last-child {
    background: linear-gradient(90deg, var(--pink-light), transparent);
  }
  .hero-company {
    font-family: 'Montserrat', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: var(--charcoal);
  }
  .hero-tagline {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.1rem, 2.5vw, 1.5rem);
    font-weight: 300;
    font-style: italic;
    color: var(--gray);
    margin-bottom: 40px;
  }
  .hero-tagline span { color: var(--pink); font-style: normal; font-weight: 600; }
  .hero-btns {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .btn-primary {
    background: var(--pink);
    color: white;
    padding: 15px 36px;
    border: none;
    border-radius: 40px;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.3s;
    box-shadow: 0 8px 30px rgba(232,80,138,0.35);
  }
  .btn-primary:hover { background: #c03d73; transform: translateY(-3px); box-shadow: 0 14px 40px rgba(232,80,138,0.45); }
  .btn-secondary {
    background: transparent;
    color: var(--pink);
    padding: 15px 36px;
    border: 2px solid var(--pink-light);
    border-radius: 40px;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.3s;
  }
  .btn-secondary:hover { background: var(--pink-pale); border-color: var(--pink); }
  .hero-badges {
    margin-top: 60px;
    display: flex;
    gap: 32px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .badge {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gray);
  }
  .badge-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--pink);
  }

  .section { padding: 100px 60px; }
  .section-label {
    text-align: center;
    font-size: 0.65rem;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--pink);
    margin-bottom: 14px;
  }
  .section-title {
    text-align: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 300;
    color: var(--charcoal);
    margin-bottom: 16px;
    line-height: 1.2;
  }
  .section-title em { font-style: italic; color: var(--pink); }
  .section-divider {
    width: 60px;
    height: 2px;
    background: linear-gradient(90deg, var(--pink-light), var(--pink));
    margin: 0 auto 60px;
    border-radius: 2px;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 28px;
    max-width: 1100px;
    margin: 0 auto;
  }
  .service-card {
    background: var(--white);
    border: 1px solid rgba(232,80,138,0.12);
    border-radius: 20px;
    padding: 44px 36px;
    text-align: center;
    transition: all 0.4s;
    position: relative;
    overflow: hidden;
  }
  .service-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--pink-soft), transparent);
    opacity: 0;
    transition: opacity 0.4s;
  }
  .service-card:hover { transform: translateY(-8px); border-color: var(--pink-light); box-shadow: 0 20px 60px rgba(232,80,138,0.15); }
  .service-card:hover::before { opacity: 1; }
  .service-icon { font-size: 2.5rem; margin-bottom: 20px; display: block; position: relative; }
  .service-card h3 {
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--charcoal);
    margin-bottom: 14px;
    position: relative;
  }
  .service-card p { font-size: 0.88rem; line-height: 1.75; color: var(--gray); position: relative; }
  .service-card-accent {
    width: 30px; height: 2px;
    background: var(--pink);
    margin: 16px auto 0;
    border-radius: 2px;
    position: relative;
  }

  .why-section {
    background: linear-gradient(135deg, #2d2d2d 0%, #1a1a1a 100%);
    color: white;
    padding: 100px 60px;
    position: relative;
    overflow: hidden;
  }
  .why-section::before {
    content: '';
    position: absolute;
    top: -100px; right: -100px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(232,80,138,0.2) 0%, transparent 70%);
    pointer-events: none;
  }
  .why-section .section-title { color: white; }
  .why-section .section-label { color: var(--pink-light); }
  .why-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 40px;
    max-width: 1000px;
    margin: 0 auto;
  }
  .why-item { text-align: center; padding: 20px; }
  .why-number {
    font-family: 'Great Vibes', cursive;
    font-size: 4rem;
    color: var(--pink);
    line-height: 1;
    margin-bottom: 8px;
  }
  .why-item h4 {
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: white;
    margin-bottom: 12px;
  }
  .why-item p { font-size: 0.85rem; line-height: 1.7; color: rgba(255,255,255,0.55); }

  .process-section { background: var(--pink-soft); padding: 100px 60px; }
  .process-steps {
    display: flex;
    gap: 0;
    max-width: 900px;
    margin: 0 auto;
    position: relative;
    flex-wrap: wrap;
    justify-content: center;
  }
  .process-steps::before {
    content: '';
    position: absolute;
    top: 36px;
    left: 10%; right: 10%;
    height: 2px;
    background: linear-gradient(90deg, var(--pink-light), var(--pink), var(--pink-light));
  }
  .step {
    flex: 1;
    min-width: 160px;
    max-width: 200px;
    text-align: center;
    padding: 0 16px;
    position: relative;
  }
  .step-number {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: var(--white);
    border: 2px solid var(--pink-light);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-family: 'Great Vibes', cursive;
    font-size: 1.8rem;
    color: var(--pink);
    position: relative;
    z-index: 1;
    transition: all 0.3s;
  }
  .step:hover .step-number { background: var(--pink); color: white; border-color: var(--pink); transform: scale(1.1); }
  .step h4 {
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--charcoal);
    margin-bottom: 10px;
  }
  .step p { font-size: 0.82rem; line-height: 1.65; color: var(--gray); }

  .testimonials-section { padding: 100px 60px; background: white; }
  .testimonials-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 28px;
    max-width: 1100px;
    margin: 0 auto;
  }
  .testimonial-card {
    background: var(--pink-soft);
    border-radius: 20px;
    padding: 40px;
    position: relative;
  }
  .testimonial-card::before {
    content: '\201C';
    font-family: 'Great Vibes', cursive;
    font-size: 5rem;
    color: var(--pink-light);
    position: absolute;
    top: 10px; left: 28px;
    line-height: 1;
    opacity: 0.8;
  }
  .stars { color: var(--pink); font-size: 0.9rem; margin-bottom: 16px; letter-spacing: 3px; }
  .testimonial-card p {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.05rem;
    font-style: italic;
    line-height: 1.75;
    color: var(--charcoal);
    margin-bottom: 20px;
  }
  .testimonial-author {
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--pink);
  }

  .contact-section {
    background: linear-gradient(135deg, var(--pink) 0%, #c03d73 100%);
    padding: 100px 60px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .contact-section::before {
    content: '';
    position: absolute;
    top: -80px; left: -80px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
  }
  .contact-section::after {
    content: '';
    position: absolute;
    bottom: -80px; right: -80px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(255,255,255,0.08) 0%, transparent 70%);
  }
  .contact-section .section-label { color: rgba(255,255,255,0.7); }
  .contact-section .section-title { color: white; }
  .contact-form {
    max-width: 560px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 16px;
    position: relative;
    z-index: 1;
  }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .contact-form input,
  .contact-form select,
  .contact-form textarea {
    width: 100%;
    padding: 16px 20px;
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 12px;
    background: rgba(255,255,255,0.15);
    backdrop-filter: blur(10px);
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.85rem;
    outline: none;
    transition: background 0.3s;
  }
  .contact-form input::placeholder,
  .contact-form select::placeholder,
  .contact-form textarea::placeholder { color: rgba(255,255,255,0.6); }
  .contact-form input:focus,
  .contact-form select:focus,
  .contact-form textarea:focus { background: rgba(255,255,255,0.25); }
  .contact-form select option { color: var(--charcoal); background: white; }
  .contact-form textarea { min-height: 120px; resize: vertical; }
  .btn-white {
    background: white;
    color: var(--pink);
    padding: 16px 40px;
    border: none;
    border-radius: 40px;
    font-family: 'Montserrat', sans-serif;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 8px 30px rgba(0,0,0,0.15);
    margin-top: 8px;
  }
  .btn-white:hover { transform: translateY(-3px); box-shadow: 0 16px 40px rgba(0,0,0,0.2); }

  footer {
    background: var(--charcoal);
    color: white;
    padding: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 24px;
  }
  .footer-logo { font-family: 'Great Vibes', cursive; font-size: 2.2rem; color: var(--pink-light); }
  .footer-tagline { font-size: 0.68rem; letter-spacing: 3px; text-transform: uppercase; color: rgba(255,255,255,0.4); margin-top: 6px; }
  .footer-links { display: flex; gap: 28px; flex-wrap: wrap; }
  .footer-links a {
    color: rgba(255,255,255,0.5);
    text-decoration: none;
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    transition: color 0.3s;
  }
  .footer-links a:hover { color: var(--pink-light); }
  .footer-copy { font-size: 0.7rem; color: rgba(255,255,255,0.3); letter-spacing: 1px; }

  .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  @media (max-width: 768px) {
    nav { padding: 16px 24px; }
    .nav-links { display: none; }
    .section, .why-section, .process-section, .testimonials-section, .contact-section { padding: 70px 24px; }
    footer { padding: 40px 24px; flex-direction: column; text-align: center; }
    .form-row { grid-template-columns: 1fr; }
    .process-steps::before { display: none; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-logo">Shine & Dandy</div>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#process">How It Works</a></li>
    <li><a href="#testimonials">Reviews</a></li>
    <li><a href="#contact" class="nav-cta">Book Now</a></li>
  </ul>
</nav>

<section class="hero">
  <div class="hero-sparkles">
    <span class="sparkle" style="top:15%;left:8%;animation-delay:0s">✦</span>
    <span class="sparkle" style="top:25%;left:20%;animation-delay:0.7s">✧</span>
    <span class="sparkle" style="top:10%;left:75%;animation-delay:1.2s">✦</span>
    <span class="sparkle" style="top:60%;left:5%;animation-delay:0.4s">✧</span>
    <span class="sparkle" style="top:70%;left:90%;animation-delay:1.8s">✦</span>
    <span class="sparkle" style="top:40%;left:92%;animation-delay:0.9s">✧</span>
    <span class="sparkle" style="top:80%;left:35%;animation-delay:2.1s">✦</span>
    <span class="sparkle" style="top:20%;left:50%;animation-delay:1.5s">✧</span>
  </div>
  <div class="hero-content">
    <div class="hero-eyebrow">✦ Tecumseh's Premier Cleaning Service ✦</div>
    <div class="hero-title">Shine and Dandy</div>
    <div class="hero-subtitle-block">
      <div class="line"></div>
      <div class="hero-company">Cleaning Co.</div>
      <div class="line"></div>
    </div>
    <div class="hero-tagline">Clean Spaces. <span>Strong Impressions.</span></div>
    <div class="hero-btns">
      <a href="#contact" class="btn-primary">Book a Cleaning</a>
      <a href="#services" class="btn-secondary">View Services</a>
    </div>
    <div class="hero-badges">
      <div class="badge"><div class="badge-dot"></div>Detail-Oriented</div>
      <div class="badge"><div class="badge-dot"></div>Fully Insured</div>
      <div class="badge"><div class="badge-dot"></div>Satisfaction Guaranteed</div>
    </div>
  </div>
</section>

<section id="services" class="section">
  <div class="section-label">What We Offer</div>
  <h2 class="section-title">Our <em>Cleaning</em> Services</h2>
  <div class="section-divider"></div>
  <div class="services-grid">
    <div class="service-card reveal">
      <span class="service-icon">🏢</span>
      <h3>Commercial Cleaning</h3>
      <p>Spotless, professional results for retail spaces, warehouses, and commercial properties of any size. We keep your business looking its best.</p>
      <div class="service-card-accent"></div>
    </div>
    <div class="service-card reveal">
      <span class="service-icon">💼</span>
      <h3>Office Cleaning</h3>
      <p>A clean office boosts morale and productivity. Regular or one-time deep cleans tailored to your team's schedule.</p>
      <div class="service-card-accent"></div>
    </div>
    <div class="service-card reveal">
      <span class="service-icon">🏡</span>
      <h3>Residential Cleaning</h3>
      <p>Your home deserves the same level of care. Weekly, bi-weekly, or move-in/move-out — we treat every home as if it were our own.</p>
      <div class="service-card-accent"></div>
    </div>
    <div class="service-card reveal">
      <span class="service-icon">✨</span>
      <h3>Deep Cleaning</h3>
      <p>When standard isn't enough, our deep clean goes top to bottom — baseboards, appliances, grout lines, and all the spots others miss.</p>
      <div class="service-card-accent"></div>
    </div>
  </div>
</section>

<section class="why-section">
  <div class="section-label">Why Shine & Dandy</div>
  <h2 class="section-title">We Don't Just Clean — <em>We Impress</em></h2>
  <div class="section-divider" style="background: linear-gradient(90deg, rgba(244,160,192,0.4), var(--pink-light))"></div>
  <div class="why-grid">
    <div class="why-item reveal">
      <div class="why-number">100%</div>
      <h4>Satisfaction Guaranteed</h4>
      <p>Not happy? We'll come back and make it right — no questions asked.</p>
    </div>
    <div class="why-item reveal">
      <div class="why-number">5★</div>
      <h4>5-Star Rated</h4>
      <p>Consistently praised for attention to detail and reliability by our growing client base.</p>
    </div>
    <div class="why-item reveal">
      <div class="why-number">✓</div>
      <h4>Fully Insured</h4>
      <p>Every job is fully insured for your peace of mind. We protect your property like it's ours.</p>
    </div>
    <div class="why-item reveal">
      <div class="why-number">♻</div>
      <h4>Eco-Friendly Options</h4>
      <p>We offer green cleaning solutions that are safe for families, pets, and the environment.</p>
    </div>
  </div>
</section>

<section id="process" class="process-section">
  <div class="section-label">Simple & Easy</div>
  <h2 class="section-title">How It <em>Works</em></h2>
  <div class="section-divider"></div>
  <div class="process-steps">
    <div class="step reveal">
      <div class="step-number">1</div>
      <h4>Book Online</h4>
      <p>Fill out our quick form or call us. We'll confirm your appointment within the hour.</p>
    </div>
    <div class="step reveal">
      <div class="step-number">2</div>
      <h4>We Show Up</h4>
      <p>Our team arrives on time, fully equipped with premium supplies and a great attitude.</p>
    </div>
    <div class="step reveal">
      <div class="step-number">3</div>
      <h4>We Clean</h4>
      <p>Every corner, every surface — cleaned to our exacting standard using our proven checklist.</p>
    </div>
    <div class="step reveal">
      <div class="step-number">4</div>
      <h4>You Enjoy</h4>
      <p>Walk into a space that feels brand new. Sit back and enjoy the results.</p>
    </div>
  </div>
</section>

<section id="testimonials" class="testimonials-section">
  <div class="section-label">Happy Clients</div>
  <h2 class="section-title">What People Are <em>Saying</em></h2>
  <div class="section-divider"></div>
  <div class="testimonials-grid">
    <div class="testimonial-card reveal">
      <div class="stars">★★★★★</div>
      <p>I booked them for a deep clean before selling my house and they absolutely transformed the space. Worth every penny — my realtor was stunned.</p>
      <div class="testimonial-author">— Michelle T., Homeowner</div>
    </div>
    <div class="testimonial-card reveal">
      <div class="stars">★★★★★</div>
      <p>Our office has never looked this good. The team is professional, thorough, and always on time. I can't imagine using anyone else.</p>
      <div class="testimonial-author">— James R., Office Manager</div>
    </div>
    <div class="testimonial-card reveal">
      <div class="stars">★★★★★</div>
      <p>They pay attention to things other cleaners overlook. The little details make a huge difference and my clients always comment on how immaculate the space is.</p>
      <div class="testimonial-author">— Sandra K., Property Owner</div>
    </div>
  </div>
</section>

<section id="contact" class="contact-section">
  <div class="section-label">Let's Get Started</div>
  <h2 class="section-title" style="margin-bottom:10px">Book Your <em style="font-style:italic;color:rgba(255,255,255,0.8)">Cleaning</em></h2>
  <p style="color:rgba(255,255,255,0.7);font-size:0.9rem;margin-bottom:50px;letter-spacing:1px;position:relative;z-index:1;">We'll respond within the hour to confirm your appointment.</p>
  <div class="contact-form">
    <div class="form-row">
      <input type="text" placeholder="First Name">
      <input type="text" placeholder="Last Name">
    </div>
    <input type="email" placeholder="Email Address">
    <input type="tel" placeholder="Phone Number">
    <select>
      <option value="" disabled selected>Select Service Type</option>
      <option>Commercial Cleaning</option>
      <option>Office Cleaning</option>
      <option>Residential Cleaning</option>
      <option>Deep Cleaning</option>
      <option>Move-In / Move-Out</option>
    </select>
    <input type="text" placeholder="Preferred Date & Time">
    <textarea placeholder="Tell us about your space or any special requests..."></textarea>
    <button class="btn-white">Request My Booking ✦</button>
  </div>
</section>

<footer>
  <div>
    <div class="footer-logo">Shine & Dandy</div>
    <div class="footer-tagline">Cleaning Co. · Tecumseh </div>
  </div>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#process">How It Works</a>
    <a href="#testimonials">Reviews</a>
    <a href="#contact">Book Now</a>
  </div>
  <div class="footer-copy">© 2025 Shine and Dandy Cleaning Co.</div>
</footer>

<script>
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));

  document.querySelector('.btn-white').addEventListener('click', () => {
    alert('Thank you! We\'ll be in touch within the hour to confirm your booking. ✦');
  });
</script>

</body>
</html>
