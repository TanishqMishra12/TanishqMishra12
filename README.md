<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Tanishq Mishra – GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0a0a0f;
    --surface: #111118;
    --border: #1e1e2e;
    --accent: #00f5a0;
    --accent2: #00d4ff;
    --accent3: #ff6b6b;
    --text: #e2e2e8;
    --muted: #6b6b7e;
    --glow: 0 0 20px rgba(0, 245, 160, 0.15);
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    min-height: 100vh;
    padding: 40px 20px;
    overflow-x: hidden;
  }

  /* Subtle grid bg */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,245,160,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,245,160,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }

  /* HEADER */
  .header {
    text-align: center;
    padding: 60px 0 40px;
    animation: fadeDown 0.8s ease both;
  }

  .ascii {
    font-family: 'JetBrains Mono', monospace;
    font-size: clamp(5px, 1.3vw, 11px);
    line-height: 1.2;
    color: var(--accent);
    text-shadow: 0 0 30px rgba(0,245,160,0.4);
    letter-spacing: 0.05em;
    white-space: pre;
    display: inline-block;
  }

  .tagline {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 400;
    color: var(--muted);
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-top: 24px;
  }

  .tagline span {
    color: var(--accent);
  }

  /* BADGES */
  .badges {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 24px;
  }

  .badge {
    padding: 6px 14px;
    border: 1px solid var(--border);
    border-radius: 3px;
    font-size: 11px;
    font-family: 'JetBrains Mono', monospace;
    text-decoration: none;
    transition: all 0.2s;
    color: var(--text);
    background: var(--surface);
  }

  .badge:hover {
    border-color: var(--accent);
    color: var(--accent);
    box-shadow: var(--glow);
  }

  .badge.green { border-color: #00ea64; color: #00ea64; }
  .badge.blue { border-color: var(--accent2); color: var(--accent2); }
  .badge.red { border-color: var(--accent3); color: var(--accent3); }

  /* DIVIDER */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent), var(--accent2), transparent);
    margin: 40px 0;
    opacity: 0.3;
  }

  /* YAML BLOCK */
  .yaml-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    border-radius: 4px;
    padding: 24px 28px;
    font-size: 13px;
    line-height: 2;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .yaml-key { color: var(--accent2); }
  .yaml-dash { color: var(--muted); }
  .yaml-val { color: var(--text); }
  .yaml-string { color: #f9c86e; }
  .yaml-comment { color: var(--muted); }

  /* SECTION HEADER */
  .section-label {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* STACK TABLE */
  .stack-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
    animation: fadeUp 0.8s 0.3s ease both;
  }

  .stack-table tr {
    border-bottom: 1px solid var(--border);
  }

  .stack-table tr:last-child { border-bottom: none; }

  .stack-table td {
    padding: 14px 16px;
  }

  .stack-table td:first-child {
    color: var(--muted);
    width: 140px;
    white-space: nowrap;
  }

  .stack-table td:last-child {
    color: var(--text);
  }

  .tag {
    display: inline-block;
    background: rgba(0,245,160,0.07);
    border: 1px solid rgba(0,245,160,0.15);
    border-radius: 3px;
    padding: 2px 8px;
    font-size: 11px;
    color: var(--accent);
    margin: 2px 3px 2px 0;
  }

  /* PROJECTS */
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 24px 28px;
    margin-bottom: 16px;
    transition: all 0.25s;
    animation: fadeUp 0.8s 0.4s ease both;
    position: relative;
    overflow: hidden;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    opacity: 0;
    transition: opacity 0.2s;
  }

  .project-card:hover {
    border-color: rgba(0,245,160,0.3);
    transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(0,0,0,0.4), var(--glow);
  }

  .project-card:hover::before { opacity: 1; }

  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .project-arrow {
    color: var(--accent);
    font-size: 12px;
  }

  .project-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 14px;
  }

  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; }

  /* CREDENTIALS */
  .cred-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 24px 28px;
    font-size: 12px;
    line-height: 2.2;
    animation: fadeUp 0.8s 0.5s ease both;
  }

  .cred-line {
    display: flex;
    align-items: center;
    gap: 0;
  }

  .cred-icon { color: var(--accent); margin-right: 10px; }

  .cred-label { color: var(--text); min-width: 220px; }

  .cred-dots {
    flex: 1;
    border-bottom: 1px dotted var(--border);
    margin: 0 12px;
    position: relative;
    top: -3px;
  }

  .cred-val { color: var(--muted); font-size: 11px; text-align: right; }

  /* FOOTER */
  .footer {
    text-align: center;
    padding: 40px 0 20px;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.15em;
    animation: fadeUp 0.8s 0.6s ease both;
  }

  /* ANIMATIONS */
  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Cursor blink */
  .cursor {
    display: inline-block;
    width: 8px;
    height: 14px;
    background: var(--accent);
    animation: blink 1s step-end infinite;
    vertical-align: middle;
    margin-left: 2px;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HEADER -->
  <div class="header">
    <pre class="ascii">████████╗ █████╗ ███╗   ██╗██╗███████╗██╗  ██╗ ██████╗
╚══██╔══╝██╔══██╗████╗  ██║██║██╔════╝██║  ██║██╔═══██╗
   ██║   ███████║██╔██╗ ██║██║███████╗███████║██║   ██║
   ██║   ██╔══██║██║╚██╗██║██║╚════██║██╔══██║██║▄▄ ██║
   ██║   ██║  ██║██║ ╚████║██║███████║██║  ██║╚██████╔╝
   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝╚══════╝╚═╝  ╚═╝ ╚══▀▀═╝</pre>

    <p class="tagline">Building AI that <span>ships</span>, not just demos<span class="cursor"></span></p>

    <div class="badges">
      <a href="#" class="badge blue">↗ LinkedIn</a>
      <a href="#" class="badge red">✉ Email</a>
      <a href="#" class="badge green">★★★★★ HackerRank Python & Java</a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- YAML -->
  <div class="yaml-block">
    <div><span class="yaml-key">focus</span><span class="yaml-comment">:</span></div>
    <div>&nbsp;&nbsp;<span class="yaml-dash">-</span> <span class="yaml-val">Retrieval-Augmented Generation (RAG)</span></div>
    <div>&nbsp;&nbsp;<span class="yaml-dash">-</span> <span class="yaml-val">Agentic AI & LLM Orchestration</span></div>
    <div>&nbsp;&nbsp;<span class="yaml-dash">-</span> <span class="yaml-val">NLP & Production ML Systems</span></div>
    <br/>
    <div><span class="yaml-key">currently_building</span><span class="yaml-comment">:</span> <span class="yaml-string">"Graph-based AI agents with cyclic reasoning"</span></div>
    <div><span class="yaml-key">passionate_about</span><span class="yaml-comment">:</span> <span class="yaml-string">"Systems that are fast, accurate, and actually useful"</span></div>
  </div>

  <div class="divider"></div>

  <!-- STACK -->
  <div class="section-label">⚡ Stack</div>
  <table class="stack-table">
    <tr>
      <td>Languages</td>
      <td>
        <span class="tag">Python</span>
        <span class="tag">Java</span>
        <span class="tag">C++</span>
        <span class="tag">SQL</span>
      </td>
    </tr>
    <tr>
      <td>AI / ML</td>
      <td>
        <span class="tag">PyTorch</span>
        <span class="tag">LangChain</span>
        <span class="tag">LangGraph</span>
        <span class="tag">RAG</span>
        <span class="tag">NLP</span>
        <span class="tag">LLMs</span>
      </td>
    </tr>
    <tr>
      <td>Infra & Tools</td>
      <td>
        <span class="tag">FastAPI</span>
        <span class="tag">Docker</span>
        <span class="tag">Streamlit</span>
        <span class="tag">Qdrant</span>
        <span class="tag">Firecrawl</span>
        <span class="tag">Inngest</span>
      </td>
    </tr>
  </table>

  <div class="divider"></div>

  <!-- PROJECTS -->
  <div class="section-label">🛠️ Projects</div>

  <div class="project-card">
    <div class="project-title">
      <span class="project-arrow">→</span> Web AI Agent
    </div>
    <p class="project-desc">
      Autonomous agent that scrapes, reasons, and structures web data using cyclic LangGraph architecture.
      Handles JS-heavy sites, persists memory across crawls, and integrates cleanly into CI/CD pipelines.
    </p>
    <div class="project-tags">
      <span class="tag">Python</span>
      <span class="tag">LangGraph</span>
      <span class="tag">LangChain</span>
      <span class="tag">Firecrawl</span>
      <span class="tag">Agentic AI</span>
    </div>
  </div>

  <div class="project-card">
    <div class="project-title">
      <span class="project-arrow">→</span> RAG Document Assistant
    </div>
    <p class="project-desc">
      Production QA system over PDFs — <strong style="color:var(--accent)">95% accuracy</strong>,
      <strong style="color:var(--accent2)">60% faster</strong> queries via event-driven Inngest pipeline,
      sub-second Qdrant vector search.
    </p>
    <div class="project-tags">
      <span class="tag">Python</span>
      <span class="tag">RAG</span>
      <span class="tag">FastAPI</span>
      <span class="tag">Docker</span>
      <span class="tag">Qdrant</span>
      <span class="tag">Streamlit</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- CREDENTIALS -->
  <div class="section-label">🏅 Credentials</div>
  <div class="cred-block">
    <div class="cred-line">
      <span class="cred-icon">✦</span>
      <span class="cred-label">HackerRank 5-Star</span>
      <span class="cred-dots"></span>
      <span class="cred-val">Python & Java</span>
    </div>
    <div class="cred-line">
      <span class="cred-icon">✦</span>
      <span class="cred-label">HackerRank Certified</span>
      <span class="cred-dots"></span>
      <span class="cred-val">Python (Intermediate) · Problem Solving</span>
    </div>
    <div class="cred-line">
      <span class="cred-icon">✦</span>
      <span class="cred-label">Applied ML in Python</span>
      <span class="cred-dots"></span>
      <span class="cred-val">University of Michigan × Coursera</span>
    </div>
  </div>

  <div class="footer">Always building. Always learning.</div>

</div>
</body>
</html>
