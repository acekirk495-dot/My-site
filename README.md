<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Upper Bicutan National High School | Official Homepage</title>
  <style>
    /* =========================================
       DESIGN PRINCIPLES & COLOR SYSTEM
       - Contrast: High-contrast navy/charcoal text on light surfaces
       - Hierarchy: Clear typographic scale from h1 down to body/captions
       - Balance & Alignment: Symmetrical grids and centered/left-aligned rhythm
       - White Space: Generous padding and section spacing for readability
       ========================================= */
    :root {
      --primary: #0f2c59;       /* Deep Navy */
      --primary-dark: #081a36;  /* Darker Navy for high contrast */
      --accent: #d97706;        /* Warm Gold/Amber accent */
      --accent-soft: #fef3c7;   /* Soft Gold tint */
      --bg-page: #f8fafc;       /* Clean Off-White background */
      --bg-surface: #ffffff;    /* Pure White cards/sections */
      --bg-alt: #eef2f6;        /* Subtle alternating section background */
      --text-main: #1e293b;     /* High-contrast Slate */
      --text-muted: #475569;    /* Secondary Muted Slate */
      --border: #cbd5e1;
      --radius: 10px;
      --shadow: 0 4px 14px rgba(15, 44, 89, 0.08);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Segoe UI", Roboto, Arial, sans-serif;
      background-color: var(--bg-page);
      color: var(--text-main);
      line-height: 1.65;
    }

    .container {
      width: min(1120px, 92%);
      margin: 0 auto;
    }

    /* ---------- HEADER & NAVIGATION MENU ---------- */
    header {
      background-color: var(--primary-dark);
      color: #ffffff;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.18);
    }

    .header-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 14px 0;
      gap: 20px;
      flex-wrap: wrap;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .brand-badge {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background-color: var(--accent);
      color: var(--primary-dark);
      font-weight: 800;
      display: grid;
      place-items: center;
      font-size: 1rem;
      flex-shrink: 0;
    }

    .brand-title {
      font-size: 1.05rem;
      font-weight: 700;
      letter-spacing: 0.3px;
    }

    .brand-sub {
      font-size: 0.78rem;
      color: #cbd5e1;
    }

    nav ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      gap: 8px 16px;
      align-items: center;
    }

    nav a {
      color: #f8fafc;
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 500;
      padding: 6px 8px;
      border-radius: 6px;
      transition: background-color 0.2s ease, color 0.2s ease;
    }

    nav a:hover,
    nav a:focus {
      background-color: rgba(255, 255, 255, 0.14);
      color: var(--accent-soft);
    }

    /* ---------- WELCOME BANNER (HERO) ---------- */
    .welcome-banner {
      background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 60%, #1d4ed8 100%);
      color: #ffffff;
      padding: 84px 0;
      text-align: center;
    }

    .welcome-banner .tag {
      display: inline-block;
      background-color: rgba(255, 255, 255, 0.14);
      color: var(--accent-soft);
      padding: 6px 14px;
      border-radius: 999px;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 18px;
    }

    .welcome-banner h1 {
      font-size: clamp(2rem, 4vw, 3rem);
      line-height: 1.2;
      margin-bottom: 18px;
      font-weight: 800;
    }

    .welcome-banner p {
      max-width: 700px;
      margin: 0 auto 30px;
      font-size: 1.08rem;
      color: #e2e8f0;
    }

    .btn-group {
      display: flex;
      justify-content: center;
      gap: 14px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 12px 24px;
      border-radius: 8px;
      font-weight: 600;
      text-decoration: none;
      transition: transform 0.15s ease, background-color 0.2s ease;
    }

    .btn-primary {
      background-color: var(--accent);
      color: var(--primary-dark);
    }

    .btn-primary:hover {
      background-color: #f59e0b;
      transform: translateY(-1px);
    }

    .btn-secondary {
      background-color: transparent;
      color: #ffffff;
      border: 1.5px solid rgba(255, 255, 255, 0.65);
    }

    .btn-secondary:hover {
      background-color: rgba(255, 255, 255, 0.12);
    }

    /* ---------- SECTION RHYTHM & HIERARCHY ---------- */
    section {
      padding: 72px 0;
    }

    section:nth-of-type(even) {
      background-color: var(--bg-alt);
    }

    .section-header {
      max-width: 720px;
      margin-bottom: 40px;
    }

    .section-header.centered {
      margin-left: auto;
      margin-right: auto;
      text-align: center;
    }

    .section-kicker {
      color: var(--primary);
      font-size: 0.82rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 6px;
    }

    .section-header h2 {
      font-size: clamp(1.55rem, 2.8vw, 2.15rem);
      color: var(--primary-dark);
      margin-bottom: 10px;
    }

    .section-header p {
      color: var(--text-muted);
    }

    /* ---------- ABOUT SECTION ---------- */
    .about-grid {
      display: grid;
      grid-template-columns: 1.3fr 1fr;
      gap: 36px;
      align-items: center;
    }

    .about-card {
      background-color: var(--bg-surface);
      padding: 28px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      border-left: 5px solid var(--primary);
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .stat-box {
      background-color: var(--bg-surface);
      padding: 22px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      text-align: center;
    }

    .stat-number {
      font-size: 1.7rem;
      font-weight: 800;
      color: var(--primary);
    }

    .stat-label {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-top: 4px;
    }

    /* ---------- MISSION, VISION, AND CORE VALUES ---------- */
    .mvv-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 24px;
    }

    .card {
      background-color: var(--bg-surface);
      padding: 28px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      border-top: 4px solid var(--primary);
    }

    .card h3 {
      color: var(--primary-dark);
      font-size: 1.2rem;
      margin-bottom: 12px;
    }

    .card ul {
      padding-left: 18px;
      color: var(--text-main);
    }

    .card li {
      margin-bottom: 8px;
    }

    /* ---------- ACADEMIC PROGRAMS ---------- */
    .programs-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 22px;
    }

    .program-item {
      background-color: var(--bg-surface);
      padding: 24px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }

    .program-badge {
      display: inline-block;
      background-color: var(--accent-soft);
      color: #92400e;
      font-size: 0.78rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 6px;
      margin-bottom: 10px;
    }

    .program-item h3 {
      color: var(--primary-dark);
      margin-bottom: 8px;
      font-size: 1.12rem;
    }

    .program-item p {
      color: var(--text-muted);
      font-size: 0.94rem;
    }

    /* ---------- GALLERY ---------- */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }

    .gallery-card {
      background-color: var(--bg-surface);
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow);
    }

    .gallery-thumb {
      height: 165px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      font-size: 1rem;
      color: #ffffff;
      padding: 16px;
      text-align: center;
    }

    .thumb-1 { background: linear-gradient(135deg, #0f2c59, #2563eb); }
    .thumb-2 { background: linear-gradient(135deg, #1e3a8a, #0d9488); }
    .thumb-3 { background: linear-gradient(135deg, #92400e, #d97706); }
    .thumb-4 { background: linear-gradient(135deg, #1e293b, #475569); }

    .gallery-caption {
      padding: 14px 16px;
      font-size: 0.9rem;
      color: var(--text-main);
    }

    /* ---------- EVENTS AND ACHIEVEMENTS ---------- */
    .events-layout {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 28px;
    }

    .list-card {
      background-color: var(--bg-surface);
      padding: 28px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .list-card h3 {
      color: var(--primary-dark);
      margin-bottom: 18px;
      padding-bottom: 10px;
      border-bottom: 2px solid var(--bg-alt);
    }

    .list-entry {
      margin-bottom: 18px;
    }

    .list-entry:last-child {
      margin-bottom: 0;
    }

    .date-tag {
      font-size: 0.8rem;
      font-weight: 700;
      color: #b45309;
      display: block;
      margin-bottom: 2px;
    }

    .list-entry h4 {
      color: var(--primary-dark);
      font-size: 1rem;
      margin-bottom: 4px;
    }

    .list-entry p {
      font-size: 0.92rem;
      color: var(--text-muted);
    }

    /* ---------- SCHOOL CLUB ORGANIZATIONS (JHS & SHS) ---------- */
    .clubs-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
    }

    .club-group {
      background-color: var(--bg-surface);
      padding: 28px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .club-group h3 {
      color: var(--primary-dark);
      margin-bottom: 14px;
      font-size: 1.18rem;
    }

    .club-group ul {
      list-style: none;
    }

    .club-group li {
      padding: 10px 0;
      border-bottom: 1px solid var(--bg-alt);
      font-size: 0.95rem;
    }

    .club-group li:last-child {
      border-bottom: none;
    }

    /* ---------- CONTACT INFORMATION ---------- */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 24px;
    }

    .contact-box {
      background-color: var(--bg-surface);
      padding: 26px;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .contact-box h3 {
      color: var(--primary-dark);
      font-size: 1.08rem;
      margin-bottom: 10px;
    }

    .contact-box p {
      color: var(--text-muted);
      font-size: 0.94rem;
    }

    /* ---------- FOOTER ---------- */
    footer {
      background-color: var(--primary-dark);
      color: #e2e8f0;
      padding: 36px 0;
      text-align: center;
      font-size: 0.9rem;
    }

    footer p + p {
      margin-top: 6px;
      color: #94a3b8;
      font-size: 0.82rem;
    }

    @media (max-width: 820px) {
      .about-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <!-- 1. HEADER & 2. NAVIGATION MENU -->
  <header>
    <div class="container header-inner">
      <div class="brand">
        <div class="brand-badge" aria-hidden="true">UBNHS</div>
        <div>
          <div class="brand-title">Upper Bicutan National High School</div>
          <div class="brand-sub">Taguig City • Department of Education</div>
        </div>
      </div>

      <nav aria-label="Main Navigation">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#mvv">Mission &amp; Vision</a></li>
          <li><a href="#programs">Academics</a></li>
          <li><a href="#gallery">Gallery</a></li>
          <li><a href="#events">Events</a></li>
          <li><a href="#clubs">Clubs</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- 3. WELCOME BANNER -->
  <section class="welcome-banner" id="home">
    <div class="container">
      <span class="tag">Welcome to UBNHS</span>
      <h1>Empowering Learners for Excellence, Character, and Service</h1>
      <p>
        Upper Bicutan National High School nurtures disciplined, critical-thinking, and compassionate
        Junior and Senior High School learners ready to lead in a changing world.
      </p>
      <div class="btn-group">
        <a href="#programs" class="btn btn-primary">Explore Academic Programs</a>
        <a href="#contact" class="btn btn-secondary">Get in Touch</a>
      </div>
    </div>
  </section>

  <!-- 4. ABOUT SECTION -->
  <section id="about">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">About Our School</div>
        <h2>A Community Dedicated to Quality Public Education</h2>
        <p>
          Serving students in Upper Bicutan, Taguig City, our school fosters academic rigor,
          holistic development, and strong partnerships with families and the local community.
        </p>
      </div>

      <div class="about-grid">
        <div class="about-card">
          <p>
            Upper Bicutan National High School provides accessible, inclusive, and learner-centered
            education across Junior High School and Senior High School. Through dedicated educators,
            student-led organizations, and values-driven instruction, learners build strong academic
            foundations alongside leadership and civic responsibility.
          </p>
        </div>

        <div class="stats-grid">
          <div class="stat-box">
            <div class="stat-number">JHS &amp; SHS</div>
            <div class="stat-label">Complete Secondary Pathways</div>
          </div>
          <div class="stat-box">
            <div class="stat-number">4 Core</div>
            <div class="stat-label">DepEd Values in Action</div>
          </div>
          <div class="stat-box">
            <div class="stat-number">Active</div>
            <div class="stat-label">Student Clubs &amp; Councils</div>
          </div>
          <div class="stat-box">
            <div class="stat-number">Taguig</div>
            <div class="stat-label">Community-Anchored Campus</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 5. MISSION, VISION, AND CORE VALUES -->
  <section id="mvv">
    <div class="container">
      <div class="section-header centered">
        <div class="section-kicker">Guiding Principles</div>
        <h2>Mission, Vision, and Core Values</h2>
        <p>Our foundational commitment to every learner and stakeholder.</p>
      </div>

      <div class="mvv-grid">
        <div class="card">
          <h3>Mission</h3>
          <p>
            To protect and promote the right of every Filipino to quality, equitable, culture-based,
            and complete basic education where students learn in a child-friendly, gender-sensitive,
            safe, and motivating environment.
          </p>
        </div>

        <div class="card">
          <h3>Vision</h3>
          <p>
            We dream of Filipinos who passionately love their country and whose values and competencies
            enable them to realize their full potential and contribute meaningfully to building the nation.
          </p>
        </div>

        <div class="card">
          <h3>Core Values</h3>
          <ul>
            <li><strong>Maka-Diyos</strong> (Love of God / Faith)</li>
            <li><strong>Maka-tao</strong> (Compassion &amp; Respect for Others)</li>
            <li><strong>Makakalikasan</strong> (Care for the Environment)</li>
            <li><strong>Makabansa</strong> (Love of Country &amp; Civic Duty)</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- 6. ACADEMIC PROGRAMS -->
  <section id="programs">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">Academics</div>
        <h2>Academic Programs</h2>
        <p>Structured learning tracks designed to prepare students for college, careers, and lifelong learning.</p>
      </div>

      <div class="programs-grid">
        <div class="program-item">
          <span class="program-badge">Grades 7–10</span>
          <h3>Junior High School (JHS)</h3>
          <p>Core competencies in English, Mathematics, Science, Filipino, Araling Panlipunan, MAPEH, and TLE.</p>
        </div>

        <div class="program-item">
          <span class="program-badge">SHS Academic Track</span>
          <h3>General Academic Strand (GAS)</h3>
          <p>Flexible interdisciplinary preparation covering humanities, social sciences, research, and management.</p>
        </div>

        <div class="program-item">
          <span class="program-badge">SHS Academic Track</span>
          <h3>STEM, ABM &amp; HUMSS</h3>
          <p>Specialized strands supporting science and technology, business and accountancy, and humanities/social sciences.</p>
        </div>

        <div class="program-item">
          <span class="program-badge">SHS TVL Track</span>
          <h3>Technical-Vocational-Livelihood</h3>
          <p>Hands-on practical skills and industry-aligned competencies for immediate career readiness.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- 7. GALLERY -->
  <section id="gallery">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">Campus Life</div>
        <h2>Photo Gallery</h2>
        <p>Highlights from classrooms, school activities, and student milestones.</p>
      </div>

      <div class="gallery-grid">
        <div class="gallery-card">
          <div class="gallery-thumb thumb-1">Classroom Learning</div>
          <div class="gallery-caption">Interactive lessons and collaborative group discussions across grade levels.</div>
        </div>

        <div class="gallery-card">
          <div class="gallery-thumb thumb-2">Science &amp; Research</div>
          <div class="gallery-caption">Student inquiries, experiments, and academic presentations.</div>
        </div>

        <div class="gallery-card">
          <div class="gallery-thumb thumb-3">School Events</div>
          <div class="gallery-caption">Cultural showcases, campus celebrations, and recognition programs.</div>
        </div>

        <div class="gallery-card">
          <div class="gallery-thumb thumb-4">Campus Grounds</div>
          <div class="gallery-caption">Safe, welcoming learning spaces supporting student growth.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- 8. EVENTS AND ACHIEVEMENTS -->
  <section id="events">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">Updates &amp; Milestones</div>
        <h2>Events and Achievements</h2>
        <p>Recent highlights and upcoming school activities for learners and parents.</p>
      </div>

      <div class="events-layout">
        <div class="list-card">
          <h3>Upcoming &amp; Recent Events</h3>
          <div class="list-entry">
            <span class="date-tag">School Year Calendar</span>
            <h4>Quarterly Academic &amp; Performance Reviews</h4>
            <p>Consultation and progress updates for students, parents, and subject advisers.</p>
          </div>
          <div class="list-entry">
            <span class="date-tag">Campus Highlight</span>
            <h4>Student Leadership &amp; Organization Assemblies</h4>
            <p>Planning sessions for club projects, peer mentoring, and community outreach.</p>
          </div>
        </div>

        <div class="list-card">
          <h3>Notable Achievements</h3>
          <div class="list-entry">
            <span class="date-tag">Academic Excellence</span>
            <h4>Research &amp; Policy Awareness Initiatives</h4>
            <p>Learners actively engaging in evidence-based inquiry and school policy advocacy.</p>
          </div>
          <div class="list-entry">
            <span class="date-tag">Student Development</span>
            <h4>Co-Curricular &amp; Community Participation</h4>
            <p>Students representing the school in academic, creative, and civic programs.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 9. SCHOOL CLUB ORGANIZATIONS (JHS AND SHS) -->
  <section id="clubs">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">Student Involvement</div>
        <h2>School Club Organizations (JHS and SHS)</h2>
        <p>Clubs and organizations that help students discover talents, build leadership, and serve others.</p>
      </div>

      <div class="clubs-grid">
        <div class="club-group">
          <h3>Junior High School (JHS) Clubs</h3>
          <ul>
            <li><strong>Supreme Secondary Learner Government (SSLG)</strong> – Student governance and leadership</li>
            <li><strong>Science &amp; Technology Club</strong> – Experiments, discovery, and innovation</li>
            <li><strong>Campus Journalism / Writers' Guild</strong> – Writing, reporting, and communication</li>
            <li><strong>Performing Arts &amp; Cultural Club</strong> – Music, dance, theater, and heritage</li>
          </ul>
        </div>

        <div class="club-group">
          <h3>Senior High School (SHS) Organizations</h3>
          <ul>
            <li><strong>SHS Learner Council</strong> – Senior student advocacy and campus initiatives</li>
            <li><strong>Research &amp; Inquiry Society</strong> – Quantitative, qualitative, and policy research</li>
            <li><strong>Digital Media &amp; Communications Club</strong> – Presentation design, media, and storytelling</li>
            <li><strong>Peer Facilitators &amp; Civic Action Group</strong> – Student wellbeing and community service</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- 10. CONTACT INFORMATION -->
  <section id="contact">
    <div class="container">
      <div class="section-header">
        <div class="section-kicker">Reach Out</div>
        <h2>Contact Information</h2>
        <p>Connect with Upper Bicutan National High School for inquiries, records, and announcements.</p>
      </div>

      <div class="contact-grid">
        <div class="contact-box">
          <h3>Address</h3>
          <p>Upper Bicutan, Taguig City, Metro Manila, Philippines</p>
        </div>

        <div class="contact-box">
          <h3>Office Hours</h3>
          <p>Monday – Friday: 7:00 AM – 4:00 PM<br />(Excluding official holidays)</p>
        </div>

        <div class="contact-box">
          <h3>Official Channels</h3>
          <p>Visit the school registrar or front office for official enrollment and document requests.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- 11. FOOTER -->
  <footer>
    <div class="container">
      <p><strong>Upper Bicutan National High School</strong> • Taguig City</p>
      <p>Designed with HTML &amp; CSS applying Balance, Contrast, Alignment, White Space, and Hierarchy.</p>
    </div>
  </footer>

</body>
</html>
