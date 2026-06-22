# B.Premiumclean
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>B.Premium Cleaning | Total Care for Home, Pets, & Rides</title>

<style>
:root {
    --primary-brand: #0f342e;
    --accent-soft: #e2ece9;
    --bg-light: #fbfbfa;
    --bg-card: #ffffff;
    --text-dark: #1c2826;
    --text-muted: #53625f;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}

body {
    background-color: var(--bg-light);
    color: var(--text-dark);
    line-height: 1.6;
}

/* NAV BAR */
header {
    background-color: var(--bg-card);
    border-bottom: 1px solid var(--accent-soft);
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 100;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

.logo {
    font-size: 22px;
    font-weight: 700;
    color: var(--primary-brand);
    letter-spacing: -0.5px;
}

.logo span {
    color: var(--text-muted);
    font-weight: 300;
}

nav button {
    background: none;
    border: none;
    color: var(--text-dark);
    font-size: 16px;
    font-weight: 500;
    margin-left: 20px;
    cursor: pointer;
    transition: 0.3s;
    padding: 5px 0;
}

nav button:hover, nav button.active-nav {
    color: var(--primary-brand);
    border-bottom: 2px solid var(--primary-brand);
}

/* PAGE WRAPPERS */
.page {
    display: none;
    padding: 140px 20px 80px;
    max-width: 1200px;
    margin: auto;
    animation: fadeIn 0.5s ease-in-out;
}

.page.active-page {
    display: block;
}

/* HERO SECTION & PICTURE STYLING */
.hero {
    text-align: center;
}

.hero h1 {
    font-size: 42px;
    margin-bottom: 20px;
    color: var(--primary-brand);
    font-weight: 800;
}

.hero .tagline {
    font-size: 22px;
    color: var(--text-muted);
    margin-bottom: 40px;
    font-style: italic;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
}

.hero-image-container {
    max-width: 800px;
    margin: 40px auto 0;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(0,0,0,0.05);
}

.hero-image-container img {
    width: 100%;
    height: auto;
    max-height: 450px;
    object-fit: cover;
    display: block;
}

.btn-premium {
    background: var(--primary-brand);
    color: #ffffff;
    padding: 16px 40px;
    font-weight: 600;
    text-decoration: none;
    border-radius: 6px;
    transition: 0.3s;
    display: inline-block;
    box-shadow: 0 4px 15px rgba(15, 52, 46, 0.15);
    cursor: pointer;
    border: none;
    font-size: 16px;
}

.btn-premium:hover {
    background: #174d44;
    transform: translateY(-2px);
}

/* GRIDS & CARDS */
h2.section-title {
    font-size: 32px;
    color: var(--primary-brand);
    text-align: center;
    margin-bottom: 10px;
}

p.section-subtitle {
    text-align: center;
    color: var(--text-muted);
    margin-bottom: 40px;
}

.grid-3 {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin-bottom: 50px;
}

.card {
    background: var(--bg-card);
    padding: 35px 25px;
    border: 1px solid var(--accent-soft);
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.01);
}

.card h3 {
    color: var(--primary-brand);
    margin-bottom: 15px;
    font-size: 22px;
    border-bottom: 2px solid var(--accent-soft);
    padding-bottom: 10px;
}

.price-row {
    display: flex;
    justify-content: space-between;
    padding: 8px 0;
    border-bottom: 1px dashed var(--accent-soft);
}

.price-row span:last-child {
    font-weight: 700;
    color: var(--primary-brand);
}

.highlight-box {
    background: var(--accent-soft);
    padding: 25px;
    border-radius: 8px;
    margin: 30px 0;
    border-left: 5px solid var(--primary-brand);
}

.highlight-box h4 {
    color: var(--primary-brand);
    margin-bottom: 10px;
}

/* CONTACT PAGE STYLING */
.contact-container {
    max-width: 700px;
    margin: 0 auto;
    text-align: center;
}

.contact-card {
    background: var(--bg-card);
    padding: 40px;
    border-radius: 12px;
    border: 1px solid var(--accent-soft);
    box-shadow: 0 10px 30px rgba(0,0,0,0.02);
    margin-top: 30px;
}

.email-display-box {
    background: var(--bg-light);
    border: 2px dashed var(--primary-brand);
    padding: 10px 20px;
    font-size: 16px;
    font-weight: 600;
    color: var(--primary-brand);
    margin: 15px auto;
    border-radius: 6px;
    display: inline-block;
    letter-spacing: 0.5px;
}

/* CUSTOM APP POPUP BOX */
.fallback-popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: var(--bg-card);
    border: 2px solid var(--primary-brand);
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.15);
    z-index: 200;
    width: 90%;
    max-width: 450px;
    text-align: center;
    animation: fadeIn 0.3s ease-in-out;
}

.popup-overlay {
    display: none;
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0,0,0,0.4);
    z-index: 199;
}

/* FOOTER */
footer {
    background: var(--primary-brand);
    text-align: center;
    padding: 40px;
    color: var(--accent-soft);
    font-size: 14px;
    margin-top: 80px;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translate(-50%, -45%); }
    to { opacity: 1; transform: translate(-50%, -50%); }
}

/* MOBILE OPTIMIZATIONS */
@media (max-width: 768px) {
    nav button { margin-left: 10px; font-size: 14px; }
    .hero h1 { font-size: 30px; }
    .hero .tagline { font-size: 18px; margin-bottom: 30px; }
    .hero-image-container { margin-top: 30px; }
    .hero-image-container img { max-height: 220px; } /* Caps image height perfectly on phones */
}
</style>
</head>

<body>

<header>
    <div class="nav-container">
        <div class="logo">B.Premium <span>Cleaning</span></div>
        <nav>
            <button id="nav-home" class="active-nav" onclick="switchPage('home')">Home</button>
            <button id="nav-services" onclick="switchPage('services')">Services & Pricing</button>
            <button id="nav-contact" onclick="switchPage('contact')">Book Now</button>
        </nav>
    </div>
</header>

<!-- PAGE 1: HOME PAGE -->
<main id="page-home" class="page active-page">
    <div class="hero">
        <h1>Breazy’s Premium Cleaning Services</h1>
        <p class="tagline">“From Your Floors to Your Four-Legged Friends, We Exceed Every Expectation.”</p>
        <button class="btn-premium" onclick="switchPage('services')">Explore Our Services & Rates</button>
        
        <div class="hero-image-container">
            <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1200&q=80" alt="Beautiful layout inside a clean premium modern home">
        </div>
    </div>
</main>

<!-- PAGE 2: SERVICES & PRICING PAGE -->
<section id="page-services" class="page">
    <h2 class="section-title">Our Premium Services & Pricing</h2>
    <p class="section-subtitle">Total Care for Your Home, Pets, and Rides. Flexible pricing tailored to your unique requirements.</p>

    <div class="grid-3">
        <div class="card">
            <h3>Home Cleaning Care</h3>
            <p style="font-size:14px; color:var(--text-muted); margin-bottom:15px;">Baseline estimates below. Firm quotes are guaranteed following your initial home visit assessment.</p>
            <div class="price-row"><span>1-Bedroom Baseline</span> <span>$80 – $200</span></div>
            <div class="price-row"><span>2-Bedroom Baseline</span> <span>$110 – $300</span></div>
            <div class="price-row"><span>3-Bedroom Baseline</span> <span>$160 – $400</span></div>
            <div class="price-row"><span>4-Bedroom Baseline</span> <span>$275 – $500</span></div>
            <div class="highlight-box" style="margin: 20px 0 0 0; padding: 15px;">
                <h4>✨ Recurring Service Perks</h4>
                <p style="font-size: 14px;">Enjoy an additional <strong>10-20% discount</strong>, all specialized add-on charges completely waived, and priority weekly or biweekly scheduling.</p>
            </div>
        </div>

        <div class="card">
            <h3>Add-Ons & Pressure Washing</h3>
            <div class="price-row"><span>Organizing Care</span> <span>$45 – $100 / hr</span></div>
            <div class="price-row"><span>Laundry Services</span> <span>$5 – $30 / load</span></div>
            <div class="price-row"><span>Window Cleaning</span> <span>$5 – $10 / window</span></div>
            <div class="price-row"><span>Baseboard Detailed Care</span> <span>Starting $15 / room</span></div>
            
            <h4 style="color:var(--primary-brand); margin: 20px 0 10px; font-size:16px; border-top:1px solid var(--accent-soft); padding-top:15px;">Pressure Washing Rates</h4>
            <div class="price-row"><span>Driveways</span> <span>$75 – $500</span></div>
            <div class="price-row"><span>Full House Ext.</span> <span>$150 – $1,200</span></div>
            <div class="price-row"><span>Roof & Gutters</span> <span>$200 – $1,200</span></div>
            <div class="price-row"><span>Decks & Fences</span> <span>$100 – $500</span></div>
        </div>

        <div class="card">
            <h3>Pet Care & Premium Rides</h3>
            <p style="font-size:14px; color:var(--text-muted); margin-bottom:10px;"><strong>Hospital-Grade Experience:</strong> Having worked at multiple animal hospitals in town, I am fully trained to safely restrain and keep your pets completely calm, safe, and happy.</p>
            <h4 style="color:var(--primary-brand); font-size:15px; margin-top:10px;">Dogs & Cats Care</h4>
            <p style="font-size:13px; color:var(--text-muted); margin-bottom:5px;">Baths, nail trims, ear cleaning, thorough brush through, and dog anal glands.</p>
            <h4 style="color:var(--primary-brand); font-size:15px; margin-top:15px;">Pet Sitting & Walking</h4>
            <p style="font-size:13px; color:var(--text-muted);">Arranged entirely to best fit each individual client's scheduling and pet preferences.</p>
        </div>
    </div>

    <div class="highlight-box">
        <h4>📌 Baseline Estimate Disclaimers & Next Steps</h4>
        <p>• <strong>Initial House Visit Requirement:</strong> A final, firm price is provided only after an on-site visit.<br>
        • <strong>Variable Factors:</strong> Final quotes vary based on total square footage, clutter, and layout requirements.<br>
        • <strong>Pet Safety Note:</strong> Unsure of your pet's grooming temperament? I will provide a clear highest and lowest rate layout that I promise not to exceed.</p>
    </div>
    
    <div style="text-align:center; margin-top:20px;">
        <button class="btn-premium" onclick="switchPage('contact')">Proceed to Consultation Booking</button>
    </div>
</section>

<!-- PAGE 3: CONTACT & BOOKING PAGE -->
<section id="page-contact" class="page">
    <div class="contact-container">
        <h2 class="section-title">Schedule Your Consultation</h2>
        <p class="section-subtitle">Lock in your guaranteed rate. Arrangements for initial assessments are handled securely through direct email channels.</p>
        
        <div class="contact-card">
            <h3 style="border:none; color:var(--primary-brand); margin-bottom:10px;">Send An Inquiry</h3>
            <p style="color:var(--text-muted); font-size:15px; margin-bottom:15px;">Tap below to instantly open an email draft. Once your review passes, a direct priority line will be extended to finalize your scheduling.</p>
            
            <div class="email-display-box">B.PremiumClean@Gmail.com</div>
            
            <button class="btn-premium" onclick="handleEmailClick()" style="display:block; width:100%; max-width:350px; margin:15px auto 0;">
                Click to Open Email Template
            </button>
        </div>
    </div>
</section>

<!-- APP FALLBACK POPUP BOX -->
<div id="popup-overlay" class="popup-overlay" onclick="closePopup()"></div>
<div id="fallback-popup" class="fallback-popup">
    <h3 style="color:var(--primary-brand); margin-bottom:10px;">Inquiry Template Ready!</h3>
    <p style="font-size:14px; color:var(--text-dark); margin-bottom:15px;">Since you are previewing inside a mobile sandbox app, direct email links are restricted. Copy our email address below to send your request:</p>
    <p style="font-weight:600; color:var(--primary-brand); font-size:16px; margin-bottom:20px; background:var(--accent-soft); padding:10px; border-radius:4px;">B.PremiumClean@Gmail.com</p>
    <button class="btn-premium" onclick="closePopup()" style="padding:10px 25px;">Got It</button>
</div>

<footer>
    &copy; 2026 Breazy’s Premium Cleaning. Total Care for Your Home, Pets, and Rides. All Rights Reserved.
</footer>

<script>
function switchPage(pageId) {
    document.querySelectorAll('.page').forEach(page => page.classList.remove('active-page'));
    document.querySelectorAll('nav button').forEach(btn => btn.classList.remove('active-nav'));
    document.getElementById('page-' + pageId).classList.add('active-page');
    document.getElementById('nav-' + pageId).classList.add('active-nav');
    window.scrollTo({top: 0, behavior: 'smooth'});
}

function handleEmailClick() {
    var mailtoUrl = "mailto:B.PremiumClean@Gmail.com?subject=B.Premium%20New%20Inquiry%20Request&body=Hello!%20I%20would%20like%20to%20schedule%20an%20initial%20visit%20assessment.%0A%0AHome%20Details%20(Bed/Bath/Sq%20Ft):%0APet%20Details%20(Name/Type/Photo%20Attached?):%0AAdd-on%20Interests%20(Pressure%20wash/Windows/Organizing):";
    
    window.location.href = mailtoUrl;
    
    setTimeout(function() {
        document.getElementById('popup-overlay').style.display = 'block';
        document.getElementById('fallback-popup').style.display = 'block';
    }, 500);
}

function closePopup() {
    document.getElementById('popup-overlay').style.display = 'none';
    document.getElementById('fallback-popup').style.display = 'none';
}
</script>

</body>
- [ ] </html>