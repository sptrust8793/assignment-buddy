<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AssignmentBuddy — Project README & Documentation</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0f172a;
      --card-bg: #1e293b;
      --border: #334155;
      --text: #f8fafc;
      --muted: #94a3b8;
      --primary: #38bdf8;
      --accent: #22c55e;
      --code-bg: #090d16;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Inter', system-ui, sans-serif;
      background-color: var(--bg);
      color: var(--text);
      line-height: 1.6;
      padding: 40px 20px;
    }
    .container {
      max-width: 860px;
      margin: 0 auto;
    }
    header {
      border-bottom: 1px solid var(--border);
      padding-bottom: 24px;
      margin-bottom: 32px;
    }
    .badge {
      display: inline-block;
      background: rgba(56, 189, 248, 0.1);
      color: var(--primary);
      padding: 4px 12px;
      border-radius: 20px;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 12px;
      border: 1px solid rgba(56, 189, 248, 0.2);
    }
    h1 { font-size: 2.25rem; font-weight: 800; margin-bottom: 8px; color: #fff; }
    p.subtitle { color: var(--muted); font-size: 1.1rem; }
    section { margin-bottom: 40px; }
    h2 { font-size: 1.5rem; font-weight: 700; color: #fff; margin-bottom: 16px; border-bottom: 1px solid var(--border); padding-bottom: 8px; }
    h3 { font-size: 1.15rem; font-weight: 600; color: var(--primary); margin: 20px 0 10px; }
    p { margin-bottom: 12px; color: var(--muted); }
    ul { list-style: none; margin-bottom: 16px; }
    li { position: relative; padding-left: 24px; margin-bottom: 8px; color: var(--muted); }
    li::before { content: "✓"; position: absolute; left: 0; color: var(--accent); font-weight: bold; }
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 16px; margin: 20px 0; }
    .card { background: var(--card-bg); border: 1px solid var(--border); border-radius: 12px; padding: 20px; }
    .card h4 { color: #fff; font-size: 1rem; margin-bottom: 6px; }
    .card p { font-size: 0.9rem; margin-bottom: 0; }
    pre {
      background: var(--code-bg);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 16px;
      overflow-x: auto;
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.88rem;
      color: #e2e8f0;
      margin: 16px 0;
    }
    code { font-family: 'JetBrains Mono', monospace; background: var(--card-bg); padding: 2px 6px; border-radius: 4px; font-size: 0.88rem; color: var(--primary); }
    footer { border-top: 1px solid var(--border); padding-top: 24px; color: var(--muted); font-size: 0.88rem; text-align: center; }
  </style>
</head>
<body>

<div class="container">
  <header>
    <span class="badge">Documentation</span>
    <h1>Assignment Buddy</h1>
    <p class="subtitle">Single-page web landing page for college assignment requests via WhatsApp.</p>
  </header>

  <section id="overview">
    <h2>Project Overview</h2>
    <p><strong>Assignment Buddy</strong> is a responsive web application designed to help college students structure and submit assignment requests directly to a dedicated WhatsApp contact number.</p>
  </section>

  <section id="features">
    <h2>Key Features</h2>
    <div class="grid">
      <div class="card">
        <h4>WhatsApp Integration</h4>
        <p>Converts client input fields into formatted WhatsApp message URLs without requiring backend databases.</p>
      </div>
      <div class="card">
        <h4>Paper Aesthetic</h4>
        <p>Uses styled notebooks, lined backgrounds, and handwriting fonts (Caveat & Inter) for student appeal.</p>
      </div>
      <div class="card">
        <h4>Interactive UI</h4>
        <p>Includes customizable modal popups, floating action buttons, toast alerts, and custom visual ripple clicks.</p>
      </div>
      <div class="card">
        <h4>Form Field Routing</h4>
        <p>Captures course details, deadlines, language choices, page counts, and custom structural requirements.</p>
      </div>
    </div>
  </section>

  <section id="tech-stack">
    <h2>Tech Stack</h2>
    <ul>
      <li><strong>HTML5</strong>: Native document architecture and semantic elements.</li>
      <li><strong>CSS3</strong>: Responsive grid layout, animations, interactive state styling, and responsive media queries.</li>
      <li><strong>JavaScript (ES6+)</strong>: Form event listening, string construction, modal dialog control, and dynamic DOM manipulation.</li>
      <li><strong>Google Fonts API</strong>: Fonts <code>Inter</code> (body typography) and <code>Caveat</code> (handwritten styling).</li>
    </ul>
  </section>

  <section id="configuration">
    <h2>Configuration</h2>
    <p>To update the target WhatsApp receiver number, update the <code>phone</code> string variable in the script block of <code>AssignmentBuddy_Attractive-1.html</code>:</p>
    <pre><code>// Update with target country code + phone number (no plus sign or special characters)
const phone = "919336640118";</code></pre>
  </section>

  <section id="payload">
    <h2>WhatsApp Message Structure</h2>
    <p>When a user submits the request form, the script formats the payload into the following structure for WhatsApp link dispatch:</p>
    <pre>🎓 *NEW COLLEGE ASSIGNMENT REQUEST*

👤 Student: [Name]
🎓 Course/Year: [Course]
📚 Subject: [Subject]
📅 Deadline: [Deadline]
📝 Type: [Assignment Type]
📄 Pages/Questions: [Pages]
🌐 Language: [Language]

✍️ *Exact Requirements:*
[Details & Special Instructions]</pre>
  </section>

  <footer>
    <p>© 2026 AssignmentBuddy Project Documentation • MIT License</p>
  </footer>
</div>

</body>
</html>
