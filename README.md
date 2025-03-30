<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gavin Kress</title>
  <link rel="icon" href="/assets/favicon-cerebellum.ico" type="image/x-icon" />
  <style>
    body {
      background-color: #0d1117;
      color: #c9d1d9;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
    }
    header {
      padding: 2rem;
      text-align: center;
      background: #161b22;
      border-bottom: 1px solid #30363d;
    }
    header h1 {
      font-size: 2.5rem;
      margin: 0;
    }
    header p {
      margin: 0.5rem 0 0;
      font-size: 1.2rem;
    }
    section {
      padding: 2rem;
      max-width: 900px;
      margin: auto;
    }
    .highlight {
      color: #58a6ff;
    }
    .project-list {
      margin-top: 2rem;
    }
    .project-list a {
      color: #58a6ff;
      display: block;
      margin-bottom: 0.5rem;
      text-decoration: none;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: #161b22;
      border-top: 1px solid #30363d;
      font-size: 0.9rem;
    }
    .terminal {
      font-family: monospace;
      background: #0d1117;
      border: 1px solid #30363d;
      padding: 1rem;
      margin-top: 2rem;
      border-radius: 8px;
      animation: fadeIn 2s ease-in-out;
    }
    .logo {
      max-width: 100px;
      margin: 1rem auto;
      display: block;
    }
    @keyframes typeEffect {
      from { width: 0; }
      to { width: 100%; }
    }
    .typewriter span {
      display: inline-block;
      overflow: hidden;
      white-space: nowrap;
      border-right: 2px solid #58a6ff;
      animation: typeEffect 4s steps(40, end), blink .75s step-end infinite;
    }
    @keyframes blink {
      50% { border-color: transparent; }
    }
    .readme-content {
      background: #161b22;
      padding: 1rem;
      border-radius: 8px;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <header>
    <img src="/assets/brain-implant.png" alt="Brain Implant Logo" class="logo" />
    <h1>Gavin Kress</h1>
    <p>Neurosymbiotic Dev | Med Student | MechE MS | 🧠🚀</p>
  </header>

  <section>
    <div class="terminal typewriter">
      <span>> Initializing uplink to <span class="highlight">Neural Hub</span>...<br>> Loading protocols: medicine, AI, security, systems design...<br>> Status: <span class="highlight">Connected</span></span>
    </div>

    <h2>README Sync</h2>
    <p>This page pulls from my <a href="https://github.com/gavinkress/gavinkress" class="highlight">personal GitHub README</a> and syncs to:</p>
    <ul>
      <li><a href="https://github.com/Gavin-Kress/.github" class="highlight">Gavin-Kress Organization Profile</a></li>
      <li><a href="https://github.com/enterprises/GavinKress" class="highlight">GavinKress Enterprise Overview</a></li>
    </ul>

    <h2>Live Personal README</h2>
    <div class="readme-content" id="readme"></div>

    <h2>Projects</h2>
    <div class="project-list">
      <a href="https://github.com/gavinkress">Personal Repos</a>
      <a href="https://github.com/Gavin-Kress">Enterprise/Org Repos</a>
      <a href="mailto:me@gavinkress.org">Contact Me</a>
    </div>
  </section>

  <footer>
    &copy; 2025 Gavin Kress — Synapse Secure, Mindfully Engineered 🧠
  </footer>

  <script>
    fetch('https://raw.githubusercontent.com/gavinkress/gavinkress/main/README.md')
      .then(res => res.text())
      .then(md => {
        document.getElementById('readme').textContent = md;
      })
      .catch(err => {
        document.getElementById('readme').textContent = 'Failed to load README.';
        console.error(err);
      });
  </script>
</body>
</html>
