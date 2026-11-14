# 5g-technology-website
A responsive single-page website about 5G technology built with HTML &amp; CSS
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>5G Technology — Basic Project</title>
<style>
    /* ---------- BASIC RESET ---------- */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        background: #0d1117;
        color: #e6edf3;
        font-family: Arial, Helvetica, sans-serif;
        line-height: 1.6;
        font-size: 16px;
    }

    h1, h2, h3 {
        color: #ffffff;
        margin-bottom: 10px;
    }

    p {
        margin-bottom: 15px;
        color: #b8c2cc;
    }

    img {
        width: 100%;
        border-radius: 8px;
        margin: 15px 0;
        display: block;
    }

    a {
        color: #00d4ff;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }

    /* ---------- NAVIGATION ---------- */
    nav {
        background: #161b22;
        padding: 15px 20px;
        border-bottom: 1px solid #30363d;
        text-align: center;
    }

    nav .logo {
        color: #00d4ff;
        font-size: 22px;
        font-weight: bold;
        margin-bottom: 10px;
    }

    nav a {
        color: #b8c2cc;
        margin: 0 10px;
        font-size: 14px;
    }

    nav a:hover {
        color: #00d4ff;
    }

    /* ---------- HERO ---------- */
    .hero {
        background: #1c2333;
        text-align: center;
        padding: 60px 20px;
    }

    .hero h1 {
        font-size: 36px;
        margin-bottom: 15px;
    }

    .hero h1 span {
        color: #00d4ff;
    }

    .hero p {
        max-width: 600px;
        margin: 0 auto 20px;
        font-size: 17px;
    }

    .hero .btn {
        display: inline-block;
        background: #00d4ff;
        color: #0d1117;
        padding: 12px 25px;
        border-radius: 6px;
        font-weight: bold;
    }

    /* ---------- SECTIONS ---------- */
    section {
        max-width: 1000px;
        margin: 0 auto;
        padding: 50px 20px;
    }

    .section-tag {
        color: #00d4ff;
        font-size: 12px;
        text-transform: uppercase;
        letter-spacing: 2px;
        margin-bottom: 8px;
    }

    .section-title {
        font-size: 32px;
        margin-bottom: 12px;
    }

    .section-title span {
        color: #00d4ff;
    }

    .section-sub {
        color: #8b949e;
        font-size: 16px;
        margin-bottom: 30px;
        max-width: 650px;
    }

    /* ---------- CARDS (using flexbox) ---------- */
    .cards {
        display: flex;
        flex-wrap: wrap;
        gap: 16px;
        margin-bottom: 30px;
    }

    .card {
        flex: 1 1 260px;
        background: #161b22;
        border: 1px solid #30363d;
        border-radius: 8px;
        padding: 20px;
    }

    .card .icon {
        font-size: 24px;
        margin-bottom: 10px;
    }

    .card h3 {
        font-size: 17px;
        margin-bottom: 8px;
    }

    .card p {
        font-size: 14px;
        margin: 0;
        color: #8b949e;
    }

    /* ---------- STATS ROW ---------- */
    .stats {
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
        margin-bottom: 25px;
    }

    .stat {
        background: #161b22;
        border: 1px solid #30363d;
        border-radius: 6px;
        padding: 15px 20px;
        text-align: center;
        flex: 1 1 120px;
    }

    .stat strong {
        display: block;
        color: #00d4ff;
        font-size: 22px;
        margin-bottom: 4px;
    }

    .stat small {
        color: #8b949e;
        font-size: 12px;
    }

    /* ---------- TABLES ---------- */
    table {
        width: 100%;
        border-collapse: collapse;
        margin: 20px 0;
        font-size: 14px;
    }

    th {
        background: #161b22;
        color: #00d4ff;
        padding: 12px;
        text-align: left;
        border-bottom: 2px solid #30363d;
    }

    td {
        padding: 12px;
        border-bottom: 1px solid #21262d;
        color: #b8c2cc;
    }

    td.good {
        color: #06ffa5;
    }

    /* ---------- PROGRESS BARS ---------- */
    .bar {
        margin-bottom: 15px;
    }

    .bar-label {
        display: flex;
        justify-content: space-between;
        font-size: 13px;
        margin-bottom: 5px;
        color: #b8c2cc;
    }

    .bar-track {
        height: 8px;
        background: #21262d;
        border-radius: 4px;
        overflow: hidden;
    }

    .bar-fill {
        height: 100%;
        background: #00d4ff;
    }

    /* ---------- TIMELINE (simple) ---------- */
    .timeline {
        border-left: 3px solid #00d4ff;
        padding-left: 20px;
        margin: 20px 0;
    }

    .timeline-item {
        margin-bottom: 20px;
    }

    .timeline-item .year {
        color: #00d4ff;
        font-weight: bold;
        font-size: 14px;
    }

    .timeline-item h4 {
        font-size: 17px;
        color: #ffffff;
        margin: 4px 0;
    }

    .timeline-item p {
        font-size: 14px;
        margin: 0;
        color: #8b949e;
    }

    /* ---------- MYTHS ---------- */
    .myth {
        background: #161b22;
        border: 1px solid #30363d;
        border-radius: 8px;
        margin-bottom: 15px;
        overflow: hidden;
    }

    .myth-header {
        background: #3d1a1a;
        color: #f87171;
        padding: 12px 18px;
        font-weight: bold;
        font-size: 14px;
    }

    .myth-body {
        padding: 15px 18px;
        font-size: 14px;
        color: #b8c2cc;
    }

    .myth-body strong {
        color: #06ffa5;
    }

    /* ---------- FOOTER ---------- */
    footer {
        text-align: center;
        padding: 30px 20px;
        border-top: 1px solid #30363d;
        color: #8b949e;
        font-size: 13px;
        margin-top: 40px;
    }

    /* ---------- MOBILE ---------- */
    @media (max-width: 600px) {
        .hero h1 { font-size: 28px; }
        .section-title { font-size: 24px; }
        nav a { margin: 5px; display: inline-block; }
    }
</style>
</head>
<body>

<!-- ================= NAV ================= -->
<nav>
    <div class="logo">5G</div>
    <a href="#intro">Intro</a>
    <a href="#evolution">Evolution</a>
    <a href="#architecture">Architecture</a>
    <a href="#global">Global</a>
    <a href="#applications">Applications</a>
    <a href="#myths">Myths</a>
    <a href="#stats">Stats</a>
</nav>

<!-- ================= HERO ================= -->
<div class="hero">
    <h1>The World Runs on <span>5G</span></h1>
    <p>How the fifth generation of wireless technology is reshaping industries, connecting billions of devices, and enabling smart cities.</p>
    <a href="#intro" class="btn">Start Reading →</a>
</div>

<!-- ================= QUICK STATS ================= -->
<section>
    <div class="stats">
        <div class="stat"><strong>2.5B</strong><small>Global Users</small></div>
        <div class="stat"><strong>20 Gbps</strong><small>Peak Speed</small></div>
        <div class="stat"><strong>1 ms</strong><small>Low Latency</small></div>
        <div class="stat"><strong>100+</strong><small>Countries</small></div>
    </div>
</section>

<!-- ================= CHAPTER 1: INTRO ================= -->
<section id="intro">
    <div class="section-tag">Chapter 01</div>
    <h2 class="section-title">What is <span>5G?</span></h2>
    <p class="section-sub">5G is the fifth generation of wireless cellular technology. It's not just faster internet — it's a new way for the world to connect.</p>

    <img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?w=1200&q=80" alt="5G Technology">

    <h3>Connect Everything, Not Just People</h3>
    <p>4G connected smartphones. 5G connects billions of devices — machines, sensors, vehicles, and infrastructure — all at the same time.</p>

    <div class="stats">
        <div class="stat"><strong>20x</strong><small>Faster</small></div>
        <div class="stat"><strong>100x</strong><small>Lower Latency</small></div>
        <div class="stat"><strong>1M</strong><small>Devices per km²</small></div>
    </div>

    <h3>Three Main Pillars of 5G</h3>
    <div class="cards">
        <div class="card">
            <div class="icon">🚀</div>
            <h3>eMBB</h3>
            <p><strong>Enhanced Mobile Broadband</strong> — speeds up to 20 Gbps. Enables 8K video, VR, and cloud gaming.</p>
        </div>
        <div class="card">
            <div class="icon">⏱️</div>
            <h3>URLLC</h3>
            <p><strong>Ultra-Reliable Low-Latency</strong> — 1–10 ms. Essential for remote surgery and self-driving cars.</p>
        </div>
        <div class="card">
            <div class="icon">🔗</div>
            <h3>mMTC</h3>
            <p><strong>Massive Machine-Type</strong> — 1 million devices per km². Built for smart cities and IoT.</p>
        </div>
    </div>

    <h3>4G vs 5G</h3>
    <table>
        <tr><th>Aspect</th><th>4G</th><th>5G</th></tr>
        <tr><td>Goal</td><td>Connect People</td><td>Connect Everything</td></tr>
        <tr><td>Architecture</td><td>Hardware-based</td><td>Cloud-native</td></tr>
        <tr><td>Peak Speed</td><td>1 Gbps</td><td class="good">20 Gbps</td></tr>
        <tr><td>Latency</td><td>~30–50 ms</td><td class="good">1–10 ms</td></tr>
    </table>
</section>

<!-- ================= CHAPTER 2: EVOLUTION ================= -->
<section id="evolution">
    <div class="section-tag">Chapter 02</div>
    <h2 class="section-title">40 Years of <span>Evolution</span></h2>
    <p class="section-sub">From analog voice in 1979 to connected intelligence in 2020.</p>

    <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?w=1200&q=80" alt="Evolution">

    <div class="timeline">
        <div class="timeline-item">
            <div class="year">1G · 1979</div>
            <h4>Analog Voice</h4>
            <p>2.4 Kbps. Voice only. The brick phone era.</p>
        </div>
        <div class="timeline-item">
            <div class="year">2G · 1991</div>
            <h4>Digital + SMS</h4>
            <p>Up to 64 Kbps. Text messaging was born.</p>
        </div>
        <div class="timeline-item">
            <div class="year">3G · 2001</div>
            <h4>Mobile Internet</h4>
            <p>2–14 Mbps. Web browsing and video calls arrived.</p>
        </div>
        <div class="timeline-item">
            <div class="year">4G · 2010</div>
            <h4>Mobile Broadband</h4>
            <p>100 Mbps–1 Gbps. HD video and the app economy.</p>
        </div>
        <div class="timeline-item">
            <div class="year">5G · 2020</div>
            <h4>Connected Intelligence</h4>
            <p>1–20 Gbps. Connecting industries and machines.</p>
        </div>
    </div>

    <h3>Speed & Latency Comparison</h3>
    <table>
        <tr><th>Metric</th><th>3G</th><th>4G</th><th>5G</th></tr>
        <tr><td>Peak Speed</td><td>2–14 Mbps</td><td>100 Mbps–1 Gbps</td><td class="good">1–20 Gbps</td></tr>
        <tr><td>Latency</td><td>100–500 ms</td><td>30–50 ms</td><td class="good">1–10 ms</td></tr>
        <tr><td>Devices per km²</td><td>10</td><td>100,000</td><td class="good">1,000,000</td></tr>
    </table>
</section>

<!-- ================= CHAPTER 3: ARCHITECTURE ================= -->
<section id="architecture">
    <div class="section-tag">Chapter 03</div>
    <h2 class="section-title">5G <span>Architecture</span></h2>
    <p class="section-sub">5G moves from hardware-based systems to cloud-native, software-defined networks.</p>

    <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=1200&q=80" alt="Architecture">

    <h3>Three Layers of 5G</h3>
    <div class="cards">
        <div class="card">
            <div class="icon">📱</div>
            <h3>Application Layer</h3>
            <p>Runs eMBB, URLLC, and mMTC services. Exposes network features to developers through APIs.</p>
        </div>
        <div class="card">
            <div class="icon">🧠</div>
            <h3>Core Network Layer</h3>
            <p>Cloud-native functions. Handles authentication, mobility, and routing.</p>
        </div>
        <div class="card">
            <div class="icon">📶</div>
            <h3>Access Network Layer</h3>
            <p>The radio network (gNB) plus edge computing that connects user devices.</p>
        </div>
    </div>

    <h3>Why It Matters</h3>
    <div class="cards">
        <div class="card"><div class="icon">☁️</div><h3>Cloud-Native</h3><p>Scale on demand and deploy updates in minutes.</p></div>
        <div class="card"><div class="icon">✂️</div><h3>Network Slicing</h3><p>One physical network, many virtual networks.</p></div>
        <div class="card"><div class="icon">⚡</div><h3>Edge Computing</h3><p>Process data near users — latency under 1 ms.</p></div>
        <div class="card"><div class="icon">🔒</div><h3>Security</h3><p>Zero-trust and end-to-end encryption by default.</p></div>
    </div>
</section>

<!-- ================= CHAPTER 4: GLOBAL ================= -->
<section id="global">
    <div class="section-tag">Chapter 04</div>
    <h2 class="section-title">India vs <span>The World</span></h2>
    <p class="section-sub">India started 3 years late — then deployed 5G faster than any country in history.</p>

    <img src="https://images.unsplash.com/photo-1524492412937-b28074a5d7da?w=1200&q=80" alt="India">

    <h3>When Each Country Launched 5G</h3>
    <div class="cards">
        <div class="card"><div class="icon">🇰🇷</div><h3>South Korea</h3><p>April 2019 — world's first launch.</p></div>
        <div class="card"><div class="icon">🇺🇸</div><h3>USA</h3><p>April 2019 — same day, mmWave focus.</p></div>
        <div class="card"><div class="icon">🇨🇳</div><h3>China</h3><p>October 2019 — largest deployment.</p></div>
        <div class="card"><div class="icon">🇬🇧</div><h3>UK</h3><p>May 2019 — EE launch in 6 cities.</p></div>
        <div class="card"><div class="icon">🇮🇳</div><h3>India</h3><p>October 2022 — fastest rollout in history.</p></div>
    </div>

    <h3>India's Record</h3>
    <p>India covered 85% of its population in just 2 years — faster than any country before.</p>
    <div class="stats">
        <div class="stat"><strong>300</strong><small>Days to 100M</small></div>
        <div class="stat"><strong>240M+</strong><small>Users</small></div>
        <div class="stat"><strong>10,000+</strong><small>Cities</small></div>
    </div>

    <h3>Population Coverage</h3>
    <div class="bar">
        <div class="bar-label"><span>India</span><span>85%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:85%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>South Korea</span><span>93%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:93%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>USA</span><span>70%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:70%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>Europe (avg)</span><span>60%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:60%"></div></div>
    </div>
</section>

<!-- ================= CHAPTER 5: APPLICATIONS ================= -->
<section id="applications">
    <div class="section-tag">Chapter 05</div>
    <h2 class="section-title">5G <span>Applications</span></h2>
    <p class="section-sub">Beyond faster downloads — real-world uses that change industries.</p>

    <div class="cards">
        <div class="card"><div class="icon">🏥</div><h3>Healthcare</h3><p>Remote robotic surgery with 1 ms latency. Real-time 4K video.</p></div>
        <div class="card"><div class="icon">🚗</div><h3>Autonomous Vehicles</h3><p>V2X communication. At 100 km/h, 50 ms delay = 1.4 m of blind movement.</p></div>
        <div class="card"><div class="icon">🏭</div><h3>Smart Factories</h3><p>Wireless robots, predictive maintenance, digital twins.</p></div>
        <div class="card"><div class="icon">🏙️</div><h3>Smart Cities</h3><p>1 million sensors per km² — traffic, air quality, waste.</p></div>
        <div class="card"><div class="icon">🎮</div><h3>Entertainment</h3><p>Cloud gaming, live VR concerts, holographic calls.</p></div>
        <div class="card"><div class="icon">🌾</div><h3>Agriculture</h3><p>Autonomous tractors, drone fleets, smart sensor networks.</p></div>
    </div>

    <img src="https://images.unsplash.com/photo-1551076805-e1869033e561?w=1200&q=80" alt="Medical">
    <h3>Remote Surgery is Already Real</h3>
    <p>In 2019, surgeons performed a 5G remote brain surgery — operating on a patient 3,000 km away with 1 ms command latency.</p>
</section>

<!-- ================= CHAPTER 6: MYTHS ================= -->
<section id="myths">
    <div class="section-tag">Chapter 06</div>
    <h2 class="section-title">Myths vs <span>Reality</span></h2>
    <p class="section-sub">5G has been surrounded by misinformation. Here's what the science says.</p>

    <div class="myth">
        <div class="myth-header">Myth: "5G is more dangerous than 4G"</div>
        <div class="myth-body"><strong>Reality:</strong> 5G follows the same safety limits (SAR) as 4G. Higher frequency ≠ higher danger. Beamforming actually reduces unnecessary exposure.</div>
    </div>

    <div class="myth">
        <div class="myth-header">Myth: "5G caused COVID-19"</div>
        <div class="myth-body"><strong>Reality:</strong> Radio waves cannot carry viruses — physically impossible. COVID-19 spread in countries with no 5G at all. WHO confirmed this as misinformation.</div>
    </div>

    <div class="myth">
        <div class="myth-header">Myth: "5G kills birds"</div>
        <div class="myth-body"><strong>Reality:</strong> No scientific evidence links 5G to bird deaths. Birds have lived around cell towers since 1979. Viral videos were debunked.</div>
    </div>

    <div class="myth">
        <div class="myth-header">Myth: "5G is just faster 4G"</div>
        <div class="myth-body"><strong>Reality:</strong> Speed is only one part. URLLC enables surgery. mMTC enables 1M devices per km². It's a completely different platform.</div>
    </div>

    <h3>What Global Health Bodies Say</h3>
    <table>
        <tr><th>Organization</th><th>Position</th></tr>
        <tr><td>WHO</td><td>No health risk evidence from 5G within guidelines</td></tr>
        <tr><td>ICNIRP</td><td>Safe under current exposure limits</td></tr>
        <tr><td>FDA (USA)</td><td>No link between mobile RF and health problems</td></tr>
        <tr><td>IEEE</td><td>5G radiation is 50× below safety thresholds</td></tr>
    </table>
</section>

<!-- ================= CHAPTER 7: STATISTICS ================= -->
<section id="stats">
    <div class="section-tag">Chapter 07</div>
    <h2 class="section-title">5G by the <span>Numbers</span></h2>
    <p class="section-sub">From 13 million users in 2019 to 2.5 billion in 2024 — the fastest technology adoption in history.</p>

    <div class="stats">
        <div class="stat"><strong>2.5B</strong><small>Global Users</small></div>
        <div class="stat"><strong>300+</strong><small>Networks</small></div>
        <div class="stat"><strong>$13.2T</strong><small>GDP Impact (2030)</small></div>
        <div class="stat"><strong>22.8M</strong><small>Jobs Created</small></div>
    </div>

    <h3>Global 5G Adoption</h3>
    <table>
        <tr><th>Year</th><th>Users</th><th>Growth</th></tr>
        <tr><td>2019</td><td>13 million</td><td>—</td></tr>
        <tr><td>2020</td><td>220 million</td><td class="good">+1,592%</td></tr>
        <tr><td>2021</td><td>620 million</td><td class="good">+182%</td></tr>
        <tr><td>2022</td><td>1.1 billion</td><td class="good">+77%</td></tr>
        <tr><td>2023</td><td>1.8 billion</td><td class="good">+64%</td></tr>
        <tr><td>2024</td><td>2.5 billion</td><td class="good">+39%</td></tr>
    </table>

    <h3>Top 5G Countries (2024)</h3>
    <div class="bar">
        <div class="bar-label"><span>South Korea</span><span>90%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:90%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>China</span><span>50%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:50%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>USA</span><span>40%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:40%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>Japan</span><span>35%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:35%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>India</span><span>20%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:20%"></div></div>
    </div>

    <h3>India's 5G in Numbers</h3>
    <div class="stats">
        <div class="stat"><strong>240M+</strong><small>5G Users</small></div>
        <div class="stat"><strong>85%</strong><small>Coverage</small></div>
        <div class="stat"><strong>600K+</strong><small>Base Stations</small></div>
        <div class="stat"><strong>$30B+</strong><small>Investment</small></div>
    </div>

    <h3>India Market Share</h3>
    <div class="bar">
        <div class="bar-label"><span>Reliance Jio</span><span>58%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:58%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>Airtel</span><span>38%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:38%"></div></div>
    </div>
    <div class="bar">
        <div class="bar-label"><span>Vi</span><span>4%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:4%"></div></div>
    </div>
</section>

<!-- ================= FOOTER ================= -->
<footer>
    © 2024 · 5G Technology Student Project · Data from GSMA, TRAI & ITU
</footer>

</body>
</html>
