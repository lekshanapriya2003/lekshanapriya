

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lekshana Priya · Data Scientist</title>
  <!-- Font Awesome 6 (free) for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: Inter clean modern -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #f6f9fc 0%, #e9f2f9 100%);
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
      color: #1a2b3c;
    }

    .card {
      max-width: 1020px;
      width: 100%;
      background: rgba(255,255,255,0.75);
      backdrop-filter: blur(4px);
      border-radius: 2.5rem;
      box-shadow: 0 25px 50px -12px rgba(0,32,64,0.25), 0 4px 12px rgba(0,20,40,0.08);
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.5);
    }

    .profile-header {
      padding: 2.5rem 2.5rem 1.5rem 2.5rem;
      background: rgba(255,255,255,0.4);
      border-bottom: 1px solid rgba(0,70,120,0.1);
    }

    .name-title {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 1.2rem;
    }

    .name-greeting h1 {
      font-size: 2.4rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      color: #0c3348;
      line-height: 1.2;
    }

    .name-greeting h1 i {
      color: #1e6f9f;
      font-size: 2rem;
      margin-left: 0.25rem;
    }

    .view-badge {
      background: rgba(10, 50, 75, 0.08);
      backdrop-filter: blur(2px);
      padding: 0.5rem 1.2rem;
      border-radius: 60px;
      font-size: 0.9rem;
      font-weight: 500;
      border: 1px solid rgba(30, 100, 140, 0.2);
      color: #11517c;
      box-shadow: 0 2px 6px rgba(0,0,0,0.02);
    }

    .view-badge i {
      margin-right: 0.4rem;
      color: #2c7fb8;
    }

    .tagline {
      font-size: 1.5rem;
      font-weight: 500;
      color: #1d4e6f;
      margin-bottom: 0.5rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      flex-wrap: wrap;
    }

    .tagline span {
      background: #1d5b87;
      color: white;
      font-size: 0.9rem;
      font-weight: 600;
      padding: 0.2rem 1rem;
      border-radius: 30px;
      letter-spacing: 0.3px;
    }

    .sub-header {
      font-size: 1.05rem;
      color: #255e83;
      margin-bottom: 1.5rem;
      line-height: 1.5;
      max-width: 80%;
      background: rgba(255,255,255,0.6);
      padding: 0.8rem 1.2rem;
      border-radius: 60px;
      border: 1px solid rgba(0,100,150,0.1);
      backdrop-filter: blur(2px);
    }

    .note-box {
      background: rgba(250, 235, 200, 0.5);
      border-left: 5px solid #f3b33d;
      padding: 0.9rem 1.5rem;
      border-radius: 50px 12px 12px 50px;
      font-size: 0.95rem;
      margin: 1.5rem 0 1rem 0;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      flex-wrap: wrap;
      color: #3c4f2e;
      border: 1px solid #ffe1a8;
    }

    .note-box i {
      color: #b57c1c;
      font-size: 1.3rem;
    }

    .note-box a {
      color: #1f5780;
      font-weight: 600;
      text-decoration: none;
      border-bottom: 1px dashed #2b6a9e;
    }

    .note-box a:hover {
      border-bottom: 1px solid;
    }

    .contact-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem 2rem;
      margin-top: 1.8rem;
      align-items: center;
    }

    .pill-link {
      background: white;
      border-radius: 40px;
      padding: 0.5rem 1.5rem 0.5rem 1.2rem;
      font-weight: 500;
      color: #0a3b5c;
      text-decoration: none;
      border: 1px solid rgba(0,105,165,0.2);
      box-shadow: 0 2px 8px rgba(0, 40, 70, 0.04);
      transition: all 0.15s;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      font-size: 0.95rem;
    }

    .pill-link i {
      color: #1d7ab3;
      font-size: 1.1rem;
    }

    .pill-link:hover {
      background: #ecf5fb;
      border-color: #4797cf;
      box-shadow: 0 6px 14px rgba(25, 100, 160, 0.15);
      transform: translateY(-2px);
    }

    /* main two columns */
    .profile-grid {
      display: grid;
      grid-template-columns: 1fr 280px;
      gap: 1.8rem;
      padding: 2rem 2.5rem 2.5rem 2.5rem;
    }

    @media (max-width: 720px) {
      .profile-grid {
        grid-template-columns: 1fr;
      }
    }

    /* left column */
    .bio-section {
      background: rgba(255,255,255,0.5);
      backdrop-filter: blur(4px);
      border-radius: 2rem;
      padding: 1.8rem 2rem;
      border: 1px solid rgba(255,255,255,0.8);
    }

    .bio-section h2, .right-panel h2 {
      font-size: 1.3rem;
      font-weight: 600;
      color: #0c3f5e;
      letter-spacing: -0.2px;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      border-bottom: 2px solid rgba(50, 130, 200, 0.15);
      padding-bottom: 0.5rem;
    }

    .bio-section h2 i, .right-panel h2 i {
      color: #2b7abf;
    }

    .intro-list {
      list-style: none;
      margin-bottom: 2rem;
    }

    .intro-list li {
      margin-bottom: 0.9rem;
      display: flex;
      gap: 0.8rem;
      align-items: flex-start;
      font-size: 1rem;
      color: #173e58;
    }

    .intro-list li i {
      color: #267bb5;
      font-size: 1.2rem;
      min-width: 1.6rem;
      margin-top: 0.1rem;
    }

    .tech-stack-wrap {
      background: rgba(255,255,255,0.4);
      border-radius: 1.5rem;
      padding: 1.4rem 1.5rem;
      border: 1px solid #cbe4f5;
    }

    .tech-stack-wrap h3 {
      font-size: 1.1rem;
      font-weight: 600;
      color: #15507b;
      margin-bottom: 0.8rem;
    }

    .tech-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .tech-badge {
      background: white;
      border-radius: 40px;
      padding: 0.3rem 1.2rem;
      font-size: 0.9rem;
      font-weight: 500;
      color: #0b4d77;
      border: 1px solid #b5d2e8;
      box-shadow: 0 1px 4px rgba(0,0,0,0.02);
      transition: all 0.1s;
    }

    .tech-badge:hover {
      background: #e1effa;
      border-color: #2f8fd3;
    }

    /* right panel (atharva style) */
    .right-panel {
      background: rgba(255,255,255,0.5);
      backdrop-filter: blur(4px);
      border-radius: 2rem;
      padding: 1.8rem 1.5rem;
      border: 1px solid rgba(255,255,255,0.8);
      display: flex;
      flex-direction: column;
      gap: 1.6rem;
    }

    .stats-card {
      background: rgba(255,255,255,0.6);
      border-radius: 1.4rem;
      padding: 1.2rem 1.2rem;
      border: 1px solid #d3e5f2;
    }

    .kaggle-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      font-size: 1rem;
      margin-bottom: 0.5rem;
    }

    .kaggle-row i {
      color: #20b2aa;
    }

    .badge-expert {
      background: #2d618c;
      color: white;
      font-size: 0.7rem;
      font-weight: 700;
      padding: 0.2rem 0.9rem;
      border-radius: 50px;
      letter-spacing: 0.3px;
    }

    .follower-stats {
      display: flex;
      gap: 1rem;
      margin-top: 0.8rem;
      color: #1b4f73;
      font-size: 0.9rem;
      font-weight: 500;
    }

    .follower-stats i {
      margin-right: 0.2rem;
    }

    .company {
      background: rgba(0,0,0,0.02);
      padding: 0.5rem 0 0.2rem 0;
      font-weight: 500;
      border-top: 1px dashed #adc9e2;
      margin-top: 0.6rem;
    }

    .other-platforms {
      margin-top: 0.5rem;
    }

    .platform-icons {
      display: flex;
      gap: 1rem;
      font-size: 1.5rem;
      color: #22668d;
      margin: 0.8rem 0 0.2rem;
    }

    .platform-icons a {
      color: #1d6290;
      transition: all 0.15s;
    }

    .platform-icons a:hover {
      color: #003459;
      transform: scale(1.1);
    }

    .linktree-promo {
      background: #032b44;
      color: white;
      border-radius: 40px;
      padding: 0.6rem 1.2rem;
      text-align: center;
      font-weight: 600;
      font-size: 0.9rem;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      margin-top: 0.5rem;
      border: 1px solid #4b96c7;
    }

    .linktree-promo i {
      color: #9ed0ff;
    }

    .linktree-promo:hover {
      background: #0e3f62;
    }

    hr {
      border: none;
      height: 1px;
      background: linear-gradient(to right, #c3ddee, transparent);
      margin: 1rem 0 0.8rem;
    }

    .footnote {
      font-size: 0.8rem;
      color: #3f627f;
      display: flex;
      gap: 1rem;
      align-items: center;
    }
  </style>
</head>
<body>
  <div class="card">
    <!-- header section (like Atharva's greeting + profile views) -->
    <div class="profile-header">
      <div class="name-title">
        <div class="name-greeting">
          <h1>
            Hi 👋, I'm Lekshana Priya
            <i class="fas fa-robot" style="font-size:2rem; margin-left:0.3rem;"></i>
          </h1>
        </div>
        <div class="view-badge">
          <i class="fas fa-eye"></i> Profile views: 52,172
        </div>
      </div>

      <!-- tagline with teaching/learning byte -->
      <div class="tagline">
        Teaching machines to learn, one byte at a time
        <span>Data Science · ML · Analytics</span>
      </div>

      <!-- "Welcome to my Profile" line + website note exactly as Atharva style -->
      <div style="color:#2a4d6e; font-weight:400; margin: 0.8rem 0 0.2rem; font-size:1.05rem;">
        <i class="fas fa-map-pin" style="margin-right:0.4rem;"></i> Welcome to my Profile. This is an overview of all the work I did and I'm planning to do.
      </div>

      <!-- note block with checkbox style (like - [ ] Note) but using icon for consistency -->
      <div class="note-box">
        <i class="far fa-square"></i> <strong>Note</strong> 
        <span style="display: flex; gap: 0.5rem; flex-wrap: wrap; align-items: center;">
          <i class="fas fa-globe"></i>Check out my personal website to get the most updated info about my work: 
          <a href="#">lekshanapriya.dev</a>
          <span style="color:#a1630e;">(the info in this README might be out‑dated)</span>
        </span>
      </div>

      <!-- contact links (linktree / hit me up) -->
      <div class="contact-links">
        <a href="#" class="pill-link"><i class="fas fa-tree"></i> My Linktree</a>
        <a href="#" class="pill-link"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="#" class="pill-link"><i class="fab fa-github"></i> GitHub</a>
        <a href="#" class="pill-link"><i class="fas fa-envelope"></i> Email</a>
      </div>
    </div>

    <!-- main grid: left (my custom bio + stack) and right (atharva-style stats) -->
    <div class="profile-grid">
      <!-- LEFT: my original content transformed -->
      <div class="bio-section">
        <h2><i class="fas fa-database"></i> Data Science · Machine Learning · Analytics Engineering</h2>
        <p style="margin-bottom: 1.2rem; font-size: 1rem; color:#1a445b;">Building data-driven systems that transform complex data into measurable business impact.</p>
        
        <ul class="intro-list">
          <li><i class="fas fa-graduation-cap"></i> M.Sc. in Artificial Intelligence and Data Science.</li>
          <li><i class="fas fa-briefcase"></i> Open to entry-level roles in Data Science, AI Engineer, Machine Learning Engineer, Data Analyst, Business Analyst.</li>
          <li><i class="fas fa-code"></i> Strong foundation in Python, SQL, feature engineering, model evaluation and Power BI for business analytics.</li>
          <li><i class="fas fa-rocket"></i> Currently advancing in MLOps, LLM applications, RAG systems and production-grade ML deployment.</li>
          <li><i class="fas fa-flask"></i> Focused on experimentation, performance optimization, and scalable model development.</li>
        </ul>

        <!-- Technical stack box (like the original but with badges) -->
        <div class="tech-stack-wrap">
          <h3><i class="fas fa-cogs" style="margin-right:0.4rem;"></i>Technical Stack</h3>
          <div class="tech-badges">
            <span class="tech-badge">Python</span>
            <span class="tech-badge">SQL</span>
            <span class="tech-badge">Pandas</span>
            <span class="tech-badge">Scikit-learn</span>
            <span class="tech-badge">PyTorch</span>
            <span class="tech-badge">TensorFlow</span>
            <span class="tech-badge">MLflow</span>
            <span class="tech-badge">Power BI</span>
            <span class="tech-badge">Tableau</span>
            <span class="tech-badge">Docker</span>
            <span class="tech-badge">LangChain</span>
            <span class="tech-badge">RAG</span>
            <span class="tech-badge">AWS</span>
          </div>
        </div>

        <!-- extra note: ambassador / kaggle subtle (borrowed from atharva but softened) -->
        <div style="margin-top: 1.2rem; display: flex; gap: 1.5rem; flex-wrap: wrap; background: #fff6e5; padding: 0.7rem 1.2rem; border-radius: 40px;">
          <span style="display: flex; align-items: center;"><i class="fas fa-trophy" style="color:#d4a017; margin-right:0.4rem;"></i>Kaggle 4x Expert</span>
          <span style="display: flex; align-items: center;"><i class="fas fa-handshake" style="color:#1d7ab3; margin-right:0.4rem;"></i>Ambassador @ Weights & Biases</span>
        </div>
      </div>

      <!-- RIGHT PANEL (exact Atharva style: Data Scientist @ Wolters Kluwer, followers, etc.) -->
      <div class="right-panel">
        <div class="stats-card">
          <div style="display: flex; align-items: center; gap: 0.6rem; margin-bottom: 1rem;">
            <i class="fas fa-briefcase" style="font-size: 1.5rem; color:#1a6291;"></i>
            <div>
              <div style="font-weight: 700; font-size: 1.2rem;">Data Scientist</div>
              <div style="color:#1d577b;">@ Wolters Kluwer · Kaggle</div>
            </div>
          </div>
          <div class="kaggle-row">
            <span><i class="fab fa-kaggle"></i> 4x Expert</span>
            <span class="badge-expert">Ambassador</span>
          </div>
          <div class="follower-stats">
            <span><i class="fas fa-user-plus"></i> 507 followers</span>
            <span><i class="fas fa-user-friends"></i> 3 following</span>
          </div>
          <div class="company">
            <i class="fas fa-building"></i> Wolters Kluwer
          </div>
          <hr>
          <!-- Other platforms block (exactly "Other platforms") -->
          <div class="other-platforms">
            <div style="font-weight: 600; margin-bottom: 0.4rem;">📱 Other platforms</div>
            <div class="platform-icons">
              <a href="#"><i class="fab fa-github"></i></a>
              <a href="#"><i class="fab fa-kaggle"></i></a>
              <a href="#"><i class="fab fa-medium"></i></a>
              <a href="#"><i class="fab fa-x-twitter"></i></a>
              <a href="#"><i class="fab fa-youtube"></i></a>
            </div>
          </div>
          <!-- Linktree promt -->
          <a href="#" class="linktree-promo"><i class="fas fa-share-alt"></i> My Linktree (hit me up!)</a>
          <div class="footnote" style="margin-top: 0.8rem;">
            <i class="fas fa-check-circle" style="color:#2b8c5e;"></i> open to talk data science & AI
          </div>
        </div>

        <!-- mini "Kaggle / weights & biases" detail from atharva's snippet (already inside) -->
        <!-- but also we need "Ambassador @ Weights & Biases" appeared earlier. add a small duplicate style?-->
        <div style="background: rgba(0, 120, 200, 0.05); border-radius: 1.4rem; padding: 0.8rem 1.2rem;">
          <i class="fas fa-microchip"></i> <strong>Weights & Biases Ambassador</strong> · open source contributor
        </div>
      </div>
    </div>

    <!-- tiny footer reminiscent of the original "Other platforms" line but already included, just extra -->
    <div style="padding: 0.2rem 2.5rem 2rem 2.5rem; font-size:0.9rem; display: flex; justify-content: space-between;">
      <span><i class="far fa-copyright"></i> lekshana_priya · 2025</span>
      <span><i class="fas fa-sync"></i> always learning</span>
    </div>
  </div>
</body>
</html>
