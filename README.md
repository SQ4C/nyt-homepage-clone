# nyt-homepage-clone
A responsive New York Times–style homepage clone built with pure HTML, CSS, and minimal JavaScript. Includes modern typography, realistic layout sections, dark mode, and mobile responsiveness.



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>New York Times - Home (Clone)</title>

  <!-- NYT‑style serif + clean sans-serif -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Source+Sans+Pro:wght@300;400;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --bg: #f7f7f5;
      --text: #111;
      --card: #ffffff;
      --border: #ddd;
    }

    /* DARK MODE VARIABLES */
    .dark {
      --bg: #1a1a1a;
      --text: #f5f5f5;
      --card: #2b2b2b;
      --border: #444;
    }

    body {
      margin: 0;
      font-family: 'Playfair Display', serif;
      background: var(--bg);
      color: var(--text);
      transition: 0.3s ease;
    }

    /* Navbar */
    .top-nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 25px;
      background: var(--card);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .logo {
      font-size: 36px;
      font-weight: 700;
    }
    .menu {
      display: flex;
      gap: 20px;
      font-family: 'Source Sans Pro', sans-serif;
      font-size: 15px;
      font-weight: 600;
    }

    /* Dark Mode Toggle */
    .toggle-btn {
      padding: 6px 12px;
      border: 1px solid var(--border);
      background: var(--card);
      cursor: pointer;
      border-radius: 5px;
      font-family: 'Source Sans Pro', sans-serif;
    }

    /* Main Layout */
    .container {
      width: 90%;
      margin: auto;
      padding: 35px 0;
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 40px;
    }

    img {
      width: 100%;
      border-radius: 6px;
    }

    .headline {
      background: var(--card);
      padding: 20px;
      border: 1px solid var(--border);
    }
    .headline h1 {
      font-size: 42px;
      line-height: 1.2;
    }
    .headline p {
      font-size: 18px;
      font-family: 'Source Sans Pro', sans-serif;
      margin-top: 10px;
    }

    /* Sidebar */
    .sidebar {
      background: var(--card);
      padding: 20px;
      border: 1px solid var(--border);
    }
    .sidebar h3 {
      margin-bottom: 12px;
      font-size: 20px;
    }
    .sidebar ul {
      list-style: none;
      padding: 0;
      font-family: 'Source Sans Pro', sans-serif;
    }
    .sidebar ul li {
      padding: 8px 0;
      border-bottom: 1px solid var(--border);
    }

    /* Sections */
    .section-title {
      width: 90%;
      margin: auto;
      font-size: 26px;
      margin-top: 40px;
      border-bottom: 2px solid var(--border);
      padding-bottom: 8px;
    }

    .article-grid {
      width: 90%;
      margin: auto;
      margin-top: 20px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .article-card {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 15px;
      border-radius: 6px;
    }
    .article-card h4 {
      font-size: 18px;
      margin-bottom: 10px;
    }
    .article-card p {
      font-family: 'Source Sans Pro', sans-serif;
      font-size: 14px;
    }

    /* Responsive */
    @media (max-width: 900px) {
      .container {
        grid-template-columns: 1fr;
      }
      .article-grid {
        grid-template-columns: 1fr 1fr;
      }
    }
    @media (max-width: 600px) {
      .article-grid {
        grid-template-columns: 1fr;
      }
      .logo {
        font-size: 28px;
      }
    }
  </style>
</head>
<body>
  <header class="top-nav">
    <div class="logo">The New York Times</div>
    <nav class="menu">
      <span>World</span>
      <span>Politics</span>
      <span>Business</span>
      <span>Tech</span>
      <span>Sports</span>
      <span>Arts</span>
    </nav>
    <button class="toggle-btn" onclick="toggleDark()">Dark Mode</button>
  </header>

  <main class="container">

    <!-- Main Headline -->
    <section class="headline">
      <img src="https://images.unsplash.com/photo-1496307042754-b4aa456c4a2d" />
      <h1>Major Global Event Unfolds as Leaders Respond</h1>
      <p>
        A closer look at today’s top story from across the world, showcasing a
        modern news layout inspired by the New York Times homepage.
      </p>
    </section>

    <!-- Sidebar Latest -->
    <aside class="sidebar">
      <h3>Latest Updates</h3>
      <ul>
        <li>Breaking: Market shows strong recovery</li>
        <li>Tech: New AI model changes everything</li>
        <li>Sports: Championship results announced</li>
        <li>World: Global summit concludes</li>
      </ul>
    </aside>
  </main>

  <!-- More News Section -->
  <h2 class="section-title">Top Stories</h2>
  <section class="article-grid">
    <div class="article-card">
      <img src="https://images.unsplash.com/photo-1522199710521-72d69614c702" />
      <h4>Economy Sees Unexpected Growth</h4>
      <p>New data shows surprising trends across multiple markets.</p>
    </div>
    <div class="article-card">
      <img src="https://images.unsplash.com/photo-1518770660439-4636190af475" />
      <h4>AI Revolution Reaches New Peak</h4>
      <p>Researchers reveal breakthrough advancements in deep learning.</p>
    </div>
    <div class="article-card">
      <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee" />
      <h4>World Leaders Agree on New Climate Goals</h4>
      <p>A transformative move expected to impact global policies.</p>
    </div>
  </section>

  <!-- Opinion Section -->
  <h2 class="section-title">Opinion</h2>
  <section class="article-grid">
    <div class="article-card">
      <h4>Why Society Must Adapt Faster</h4>
      <p>A deep reflection on rapid technological change.</p>
    </div>
    <div class="article-card">
      <h4>The Future of Work After Automation</h4>
      <p>How AI and robotics will reshape professional life.</p>
    </div>
    <div class="article-card">
      <h4>What We Learned From Recent Global Events</h4>
      <p>Examining the shifting dynamics of global power.</p>
    </div>
  </section>

  <script>
    function toggleDark() {
      document.body.classList.toggle('dark');
    }
  </script>
</body>
</html>
