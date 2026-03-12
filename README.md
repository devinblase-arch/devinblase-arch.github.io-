<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>10× with AI — People Team</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --navy:#071c2c;--navy2:#0d2640;--navy3:#112d4a;--border:#1a3a56;
      --blue:#1f64f6;--blue-lt:#4080ff;--blue-dim:rgba(31,100,246,0.12);
      --text:#dde6f0;--muted:#7a96b0;--dim:#3d5a72;--white:#ffffff;
      --red:#E94560;--green:#22c55e;--amber:#f59e0b;--teal:#0ea5e9;--purple:#a78bfa;
      --font:'Inter',system-ui,-apple-system,sans-serif;
      --mono:'JetBrains Mono','SF Mono',monospace;
    }
    body{background:var(--navy);color:var(--text);font-family:var(--font);font-size:15px;line-height:1.7;}
    .hero{position:relative;background:linear-gradient(160deg,#071c2c 0%,#0b2240 50%,#0a1e38 100%);border-bottom:1px solid var(--border);overflow:hidden;padding:56px 56px 48px;}
    .hero-bg{position:absolute;right:-80px;top:-80px;width:520px;height:520px;opacity:0.06;pointer-events:none;}
    .hero-logo{display:flex;align-items:center;gap:12px;margin-bottom:32px;}
    .hero-logo-mark{width:32px;height:32px;border-radius:8px;background:var(--blue-dim);border:1px solid rgba(31,100,246,.3);display:flex;align-items:center;justify-content:center;font-size:16px;}
    .hero-divider{width:1px;height:20px;background:var(--border);}
    .hero-label{font-size:11px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:var(--muted);}
    .hero-eyebrow{font-size:11px;font-weight:700;letter-spacing:0.14em;text-transform:uppercase;color:var(--blue-lt);display:flex;align-items:center;gap:10px;margin-bottom:18px;}
    .hero-eyebrow::after{content:'';flex:none;width:48px;height:1px;background:var(--blue);opacity:0.5;}
    h1{font-size:clamp(1.8rem,4vw,2.6rem);font-weight:800;line-height:1.12;color:var(--white);letter-spacing:-0.03em;margin-bottom:16px;}
    h1 .accent{color:var(--blue-lt);}
    h1 .accent-green{color:var(--green);}
    .hero-sub{font-size:1rem;color:var(--muted);max-width:700px;line-height:1.7;margin-bottom:32px;}
    .hero-badges{display:flex;flex-wrap:wrap;gap:10px;}
    .badge{display:inline-flex;align-items:center;gap:6px;padding:5px 12px;border-radius:6px;font-size:11.5px;font-weight:600;border:1px solid;}
    .badge .dot{width:6px;height:6px;border-radius:50%;flex-shrink:0;}
    .badge-done{color:var(--green);border-color:rgba(34,197,94,.3);background:rgba(34,197,94,.07);}
    .badge-done .dot{background:var(--green);}
    .badge-info{color:var(--teal);border-color:rgba(14,165,233,.3);background:rgba(14,165,233,.07);}
    .badge-info .dot{background:var(--teal);}
    .badge-date{color:var(--muted);border-color:var(--border);background:rgba(255,255,255,.03);}
    .badge-purple{color:var(--purple);border-color:rgba(167,139,250,.3);background:rgba(167,139,250,.07);}
    .badge-purple .dot{background:var(--purple);}
    .toc{background:var(--navy2);border-bottom:1px solid var(--border);padding:0 56px;display:flex;gap:0;overflow-x:auto;}
    .toc a{display:block;padding:14px 16px;font-size:12.5px;font-weight:600;color:var(--muted);border-bottom:2px solid transparent;white-space:nowrap;transition:color .15s,border-color .15s;text-decoration:none;}
    .toc a:hover{color:var(--white);border-color:var(--blue);}
    .page{max-width:1100px;margin:0 auto;padding:52px 56px 80px;}
    .section{margin-bottom:72px;}
    .section-header{display:flex;align-items:center;gap:16px;margin-bottom:28px;}
    .section-header h2{font-size:1.15rem;font-weight:700;color:var(--white);letter-spacing:-0.01em;}
    .section-rule{flex:1;height:1px;background:linear-gradient(90deg,var(--border) 0%,transparent 100%);}
    .section-tag{font-size:11px;color:var(--muted);background:var(--navy2);border:1px solid var(--border);border-radius:4px;padding:3px 9px;white-space:nowrap;}
    .intro-box{background:linear-gradient(135deg,rgba(31,100,246,.06) 0%,rgba(14,165,233,.03) 100%);border:1px solid rgba(31,100,246,.22);border-radius:12px;padding:28px 32px;margin-bottom:48px;}
    .intro-pill{display:inline-flex;align-items:center;gap:6px;padding:4px 12px;background:var(--blue-dim);border:1px solid rgba(31,100,246,.35);border-radius:20px;font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:0.1em;color:var(--blue-lt);margin-bottom:16px;}
    .intro-lead{font-size:1.05rem;color:var(--text);line-height:1.7;font-weight:500;}
    .intro-lead strong{color:var(--white);}
    .card{background:var(--navy2);border:1px solid var(--border);border-radius:10px;padding:20px 22px;}
    .card h3{font-size:13px;font-weight:700;color:var(--white);margin-bottom:10px;display:flex;align-items:center;gap:8px;}
    .card h3 .card-dot{width:6px;height:6px;border-radius:50%;background:var(--blue);flex-shrink:0;}
    .card p,.card li{font-size:13px;color:var(--muted);line-height:1.65;}
    .card ul{padding-left:16px;}
    .card ul li{margin-bottom:5px;}
    .card-blue{background:var(--blue-dim);border-color:rgba(31,100,246,.3);border-left:3px solid var(--blue);}
    .card-blue h3{color:#93b8ff;}
    .card-blue h3 .card-dot{background:var(--blue-lt);}
    .card-blue p,.card-blue li{color:#8aaede;}
    .card-teal{background:rgba(14,165,233,.05);border-color:rgba(14,165,233,.25);border-left:3px solid var(--teal);}
    .card-teal h3{color:var(--teal);}
    .card-teal h3 .card-dot{background:var(--teal);}
    .card-teal p,.card-teal li{color:#5aafce;}
    .card-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
    .cap-callout{background:linear-gradient(135deg,rgba(31,100,246,.07) 0%,rgba(14,165,233,.04) 100%);border:1px solid rgba(31,100,246,.28);border-left:3px solid var(--blue-lt);border-radius:8px;padding:16px 20px;margin-bottom:20px;font-size:14px;font-weight:600;color:var(--white);line-height:1.6;}
    .not-ambitious{margin-top:16px;border-top:1px solid var(--border);padding-top:14px;}
    .not-ambitious-label{font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--dim);margin-bottom:10px;display:flex;align-items:center;gap:8px;}
    .not-ambitious-label::after{content:'';flex:1;height:1px;background:var(--border);}
    .na-items{display:flex;flex-direction:column;gap:5px;}
    .na-item{font-size:12px;color:var(--dim);line-height:1.5;padding-left:14px;position:relative;}
    .na-item::before{content:'–';position:absolute;left:0;color:var(--border);}
    .cap-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
    .cap-card{background:var(--navy2);border:1px solid var(--border);border-radius:10px;padding:20px 22px;}
    .cap-header{display:flex;align-items:center;gap:10px;margin-bottom:14px;}
    .cap-icon{width:34px;height:34px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0;}
    .cap-icon-blue{background:var(--blue-dim);border:1px solid rgba(31,100,246,.3);}
    .cap-icon-green{background:rgba(34,197,94,.08);border:1px solid rgba(34,197,94,.25);}
    .cap-icon-teal{background:rgba(14,165,233,.08);border:1px solid rgba(14,165,233,.25);}
    .cap-icon-purple{background:rgba(167,139,250,.08);border:1px solid rgba(167,139,250,.25);}
    .cap-icon-amber{background:rgba(245,158,11,.08);border:1px solid rgba(245,158,11,.25);}
    .cap-title{font-size:13.5px;font-weight:700;color:var(--white);}
    .cap-sub{font-size:11px;color:var(--dim);margin-top:1px;}
    .cap-items{display:flex;flex-direction:column;gap:8px;}
    .cap-item{display:flex;gap:10px;align-items:flex-start;}
    .cap-item-dot{width:5px;height:5px;border-radius:50%;flex-shrink:0;margin-top:7px;}
    .cap-item-blue .cap-item-dot{background:var(--blue-lt);}
    .cap-item-green .cap-item-dot{background:var(--green);}
    .cap-item-teal .cap-item-dot{background:var(--teal);}
    .cap-item-purple .cap-item-dot{background:var(--purple);}
    .cap-item-amber .cap-item-dot{background:var(--amber);}
    .cap-item-text{font-size:12.5px;color:var(--muted);line-height:1.55;}
    .cap-item-text strong{color:var(--text);font-weight:600;}
    .cap-item-text em{color:var(--dim);font-style:normal;font-size:11.5px;}
    .commodity-strip{background:rgba(233,69,96,.04);border:1px solid rgba(233,69,96,.2);border-left:3px solid var(--red);border-radius:8px;padding:16px 20px;margin-bottom:0;}
    .commodity-label{font-size:10px;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:rgba(233,69,96,.7);margin-bottom:12px;}
    .commodity-items{display:flex;flex-wrap:wrap;gap:10px;}
    .commodity-item{display:flex;align-items:center;gap:8px;}
    .commodity-pill{font-size:10px;font-weight:700;padding:2px 8px;border-radius:4px;white-space:nowrap;flex-shrink:0;}
    .commodity-now{background:rgba(233,69,96,.12);color:var(--red);border:1px solid rgba(233,69,96,.3);}
    .commodity-soon{background:rgba(245,158,11,.10);color:var(--amber);border:1px solid rgba(245,158,11,.3);}
    .commodity-later{background:rgba(122,150,176,.08);color:var(--muted);border:1px solid var(--border);}
    .commodity-text{font-size:12.5px;color:var(--muted);}
    .moat-mini-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px;margin-bottom:24px;}
    .moat-mini{background:var(--navy2);border:1px solid var(--border);border-radius:10px;padding:18px 20px;position:relative;overflow:hidden;}
    .moat-mini::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;}
    .moat-mini-blue::before{background:var(--blue-lt);}
    .moat-mini-green::before{background:var(--green);}
    .moat-mini-teal::before{background:var(--teal);}
    .moat-mini-amber::before{background:var(--amber);}
    .moat-mini-purple::before{background:var(--purple);}
    .moat-mini-num{font-size:9.5px;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:var(--dim);margin-bottom:6px;font-family:var(--mono);}
    .moat-mini-title{font-size:13px;font-weight:700;color:var(--white);margin-bottom:8px;line-height:1.3;}
    .moat-mini-body{font-size:12px;color:var(--muted);line-height:1.6;}
    .moat-mini-body strong{color:var(--text);font-weight:600;}
    .moat-thesis{background:rgba(31,100,246,.05);border:1px solid rgba(31,100,246,.2);border-left:3px solid var(--blue);border-radius:8px;padding:18px 22px;}
    .moat-thesis-label{font-size:10px;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:var(--blue-lt);margin-bottom:10px;}
    .moat-thesis-items{display:flex;flex-direction:column;gap:6px;}
    .moat-thesis-item{font-size:12.5px;color:var(--muted);padding-left:14px;position:relative;line-height:1.5;}
    .moat-thesis-item::before{content:'→';position:absolute;left:0;color:var(--blue-lt);font-size:11px;top:1px;}
    .proof-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
    .proof-card{background:var(--navy2);border:1px solid var(--border);border-radius:10px;padding:18px 20px;}
    .proof-label{font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--dim);margin-bottom:8px;}
    .proof-title{font-size:13.5px;font-weight:700;color:var(--white);margin-bottom:6px;line-height:1.3;}
    .proof-desc{font-size:12px;color:var(--muted);line-height:1.55;}
    .proof-stat{display:inline-block;margin-top:10px;font-size:11.5px;font-weight:700;padding:3px 10px;border-radius:4px;}
    .proof-stat-green{color:var(--green);background:rgba(34,197,94,.08);border:1px solid rgba(34,197,94,.25);}
    .proof-stat-teal{color:var(--teal);background:rgba(14,165,233,.08);border:1px solid rgba(14,165,233,.25);}
    .proof-stat-purple{color:var(--purple);background:rgba(167,139,250,.08);border:1px solid rgba(167,139,250,.25);}
    .start-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
    .start-card{background:var(--navy2);border:1px solid var(--border);border-radius:10px;padding:18px 20px;}
    .start-num{font-size:1.6rem;font-weight:800;color:var(--blue-lt);line-height:1;margin-bottom:8px;letter-spacing:-0.04em;}
    .start-title{font-size:13px;font-weight:700;color:var(--white);margin-bottom:6px;}
    .start-desc{font-size:12.5px;color:var(--muted);line-height:1.55;}
    .cta-banner{background:linear-gradient(135deg,#071c2c 0%,#0d2640 40%,#071c2c 100%);border:1px solid rgba(31,100,246,.35);border-radius:14px;padding:40px 44px;position:relative;overflow:hidden;margin-bottom:0;}
    .cta-banner::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--blue) 0%,var(--teal) 50%,var(--green) 100%);}
    .cta-eyebrow{font-size:11px;font-weight:700;letter-spacing:0.14em;text-transform:uppercase;color:var(--blue-lt);display:flex;align-items:center;gap:10px;margin-bottom:16px;}
    .cta-eyebrow::after{content:'';flex:none;width:48px;height:1px;background:var(--blue);opacity:0.5;}
    .cta-title{font-size:clamp(1.3rem,3vw,1.8rem);font-weight:800;color:var(--white);letter-spacing:-0.025em;line-height:1.15;margin-bottom:14px;}
    .cta-title .accent{color:var(--green);}
    .cta-body{font-size:14px;color:var(--muted);line-height:1.7;max-width:680px;margin-bottom:28px;}
    .cta-body strong{color:var(--text);}
    .cta-steps{display:flex;flex-direction:column;gap:10px;margin-bottom:28px;}
    .cta-step{display:flex;gap:14px;align-items:flex-start;}
    .cta-step-num{width:26px;height:26px;border-radius:50%;background:var(--blue-dim);border:1px solid rgba(31,100,246,.4);display:flex;align-items:center;justify-content:center;font-size:11.5px;font-weight:700;color:var(--blue-lt);flex-shrink:0;margin-top:1px;}
    .cta-step-text{font-size:13.5px;color:var(--text);line-height:1.55;}
    .cta-step-text strong{color:var(--white);}
    .cta-step-text em{color:var(--dim);font-style:normal;font-size:12px;}
    .cta-prompt{background:rgba(31,100,246,.07);border:1px solid rgba(31,100,246,.25);border-radius:10px;padding:20px 24px;font-size:14px;color:var(--muted);line-height:1.65;}
    .cta-prompt strong{color:var(--white);font-size:15px;display:block;margin-bottom:8px;}
    .cta-examples{display:flex;flex-wrap:wrap;gap:8px;margin-top:14px;}
    .cta-ex{background:var(--navy3);border:1px solid var(--border);border-radius:4px;padding:4px 10px;font-size:11.5px;color:var(--dim);font-family:var(--mono);}
    footer{border-top:1px solid var(--border);padding:24px 56px;display:flex;align-items:center;justify-content:space-between;}
    .footer-note{font-size:11.5px;color:var(--dim);}
    @media(max-width:820px){
      .hero,.page,footer,.toc{padding-left:24px;padding-right:24px;}
      .cap-grid,.card-grid,.moat-mini-grid,.proof-grid,.start-grid{grid-template-columns:1fr;}
      h1{font-size:1.6rem;}
      .cta-banner{padding:28px 24px;}
    }
  </style>
</head>
<body>

<div class="hero">
  <svg class="hero-bg" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 576" aria-hidden="true">
    <circle cx="288" cy="288" r="220" fill="none" stroke="#1f64f6" stroke-width="0.5" opacity="0.4"/>
    <circle cx="288" cy="288" r="160" fill="none" stroke="#1f64f6" stroke-width="0.5" opacity="0.3"/>
    <circle cx="288" cy="288" r="100" fill="none" stroke="#1f64f6" stroke-width="0.5" opacity="0.2"/>
    <circle cx="288" cy="288" r="6" fill="#1f64f6"/>
    <circle cx="180" cy="180" r="4" fill="#4080ff"/><circle cx="396" cy="180" r="4" fill="#4080ff"/>
    <circle cx="420" cy="310" r="4" fill="#4080ff"/><circle cx="200" cy="380" r="4" fill="#4080ff"/>
    <circle cx="330" cy="420" r="4" fill="#4080ff"/>
    <line x1="288" y1="288" x2="180" y2="180" stroke="#1f64f6" stroke-width="0.7" opacity="0.5"/>
    <line x1="288" y1="288" x2="396" y2="180" stroke="#1f64f6" stroke-width="0.7" opacity="0.5"/>
    <line x1="288" y1="288" x2="420" y2="310" stroke="#1f64f6" stroke-width="0.7" opacity="0.5"/>
    <line x1="288" y1="288" x2="200" y2="380" stroke="#1f64f6" stroke-width="0.7" opacity="0.5"/>
    <line x1="288" y1="288" x2="330" y2="420" stroke="#1f64f6" stroke-width="0.7" opacity="0.5"/>
  </svg>

  <div class="hero-logo">
    <div class="hero-logo-mark">👥</div>
    <div class="hero-divider"></div>
    <span class="hero-label">People Team</span>
  </div>

  <div class="hero-eyebrow">AI Era · March 2026</div>
  <h1>AI can <span class="accent-green">10×</span> what you build.<br><span class="accent">Here's what that looks like for People.</span></h1>
  <p class="hero-sub">The tools exist today. The only question is whether we use them to attempt things that were previously impossible — or keep doing the same work, just a little faster. This is about the former.</p>
  <div class="hero-badges">
    <span class="badge badge-done"><span class="dot"></span>10× outcomes — already happening</span>
    <span class="badge badge-info"><span class="dot"></span>HR Ops, HRBP &amp; Recruiting examples inside</span>
    <span class="badge badge-purple"><span class="dot"></span>Action item at the end</span>
    <span class="badge badge-date">People Team · March 2026</span>
  </div>
</div>

<nav class="toc">
  <a href="#message">The Message</a>
  <a href="#moats">Why People Leads</a>
  <a href="#capabilities">Your Work, 10×</a>
  <a href="#proofpoints">Proof Points</a>
  <a href="#misogi">Your 2026 Misogi</a>
  <a href="#cta">Your Action Item</a>
</nav>

<div class="page">

<!-- MESSAGE -->
<div id="message" class="section">
  <div class="intro-box">
    <div class="intro-pill">⚡ The Core Message</div>
    <p class="intro-lead">
      AI does not replace what makes you valuable — <strong>your judgment, your empathy, your ability to read people and situations no model can fully grasp.</strong>
      What it eliminates is the toil between you and impact: the scheduling back-and-forth, the repetitive job description drafts, the reporting that takes hours because the data has to be pulled and formatted from scratch every time.
      <br><br>
      <strong>The new bar is not "use AI to do the same things faster."</strong>
      It is "use AI to attempt the things that were previously out of reach." The teams that get this right will hire better, support employees more proactively, and run more strategic HR operations — with the same headcount.
    </p>
  </div>

  <div class="card-grid">
    <div class="card card-blue">
      <h3><span class="card-dot"></span>What AI is good at in our domain</h3>
      <ul>
        <li>Generating the first 80% of any document, process, or analysis — the scaffolding you then refine</li>
        <li>Synthesizing large volumes of data — survey responses, performance reviews, headcount reports — faster than any analyst</li>
        <li>Drafting consistent, high-quality written content at scale: JDs, offer letters, policies, comms</li>
        <li>Answering repetitive employee and candidate questions with consistent, accurate information</li>
        <li>Connecting signals across disparate data: ATS, HRIS, engagement surveys, exit interviews</li>
      </ul>
    </div>
    <div class="card card-teal">
      <h3><span class="card-dot"></span>What stays yours</h3>
      <ul>
        <li><strong>Human judgment</strong> — knowing when the right answer isn't what the data says, and when a person needs a person</li>
        <li><strong>Relationship capital</strong> — the trust employees and candidates place in you cannot be automated</li>
        <li><strong>Culture stewardship</strong> — reading the room, navigating difficult conversations, shaping how the company feels</li>
        <li><strong>Strategic framing</strong> — deciding what problems to solve, what org design serves the business, what talent gaps matter most</li>
        <li><strong>Ethical discernment</strong> — ensuring AI outputs are fair, compliant, and aligned with our values</li>
      </ul>
    </div>
  </div>
</div>

<!-- WHY PEOPLE LEADS -->
<div id="moats" class="section">
  <div class="section-header">
    <h2>Why the People Team Has to Lead the Way</h2>
    <div class="section-rule"></div>
    <span class="section-tag">Our competitive advantages</span>
  </div>

  <div class="commodity-strip">
    <div class="commodity-label">Being commoditized by AI — no longer a differentiator</div>
    <div class="commodity-items">
      <div class="commodity-item"><span class="commodity-pill commodity-now">Now</span><span class="commodity-text">Job description drafting</span></div>
      <div class="commodity-item"><span class="commodity-pill commodity-now">Now</span><span class="commodity-text">Offer letter &amp; contract templates</span></div>
      <div class="commodity-item"><span class="commodity-pill commodity-now">Now</span><span class="commodity-text">FAQ responses to candidates &amp; employees</span></div>
      <div class="commodity-item"><span class="commodity-pill commodity-soon">12–18 mo</span><span class="commodity-text">First-pass resume screening</span></div>
      <div class="commodity-item"><span class="commodity-pill commodity-soon">12–18 mo</span><span class="commodity-text">Onboarding content &amp; workflows</span></div>
      <div class="commodity-item"><span class="commodity-pill commodity-later">2–3 yr</span><span class="commodity-text">Routine HR reporting &amp; dashboards</span></div>
    </div>
  </div>

  <div class="moat-mini-grid" style="margin-top:20px;">
    <div class="moat-mini moat-mini-blue">
      <div class="moat-mini-num">ADVANTAGE 01 · Stays Defensible</div>
      <div class="moat-mini-title">Institutional Context &amp; History</div>
      <div class="moat-mini-body">You understand the culture, the leadership dynamics, the unwritten rules, and the historical patterns that shaped the org. No external AI tool can replicate this. <strong>Use AI to surface and act on insights faster — grounded in context only you hold.</strong></div>
    </div>
    <div class="moat-mini moat-mini-teal">
      <div class="moat-mini-num">ADVANTAGE 02 · Stays Defensible</div>
      <div class="moat-mini-title">Trust &amp; Discretion</div>
      <div class="moat-mini-body">Employees share things with HR they won't share anywhere else. That trust is earned over time and held by people, not systems. <strong>Use AI to free up the time you currently spend on admin — so more of your time goes to the relationships that matter.</strong></div>
    </div>
    <div class="moat-mini moat-mini-amber">
      <div class="moat-mini-num">ADVANTAGE 03 · Must Be Built</div>
      <div class="moat-mini-title">The People Intelligence Layer</div>
      <div class="moat-mini-body">Talent trends, retention risk, engagement patterns, hiring velocity — this data exists but rarely gets synthesized into actionable intelligence. <strong>We build the people analytics layer. Leaders make decisions from it. That's how HR becomes strategic infrastructure.</strong></div>
    </div>
  </div>

  <div class="moat-thesis">
    <div class="moat-thesis-label">The Compounding Thesis</div>
    <div class="moat-thesis-items">
      <div class="moat-thesis-item">Every hour saved on admin → more time for strategic partnership → deeper credibility with the business → HR gets a seat at harder decisions → repeat</div>
      <div class="moat-thesis-item">Every new people data signal captured → better attrition prediction → proactive interventions → lower regrettable turnover → stronger talent moat</div>
      <div class="moat-thesis-item">Every AI tool that surfaces people insights → HR becomes the team that shapes strategy, not the team that processes paperwork</div>
    </div>
  </div>
</div>

<!-- CAPABILITIES -->
<div id="capabilities" class="section">
  <div class="section-header">
    <h2>Your Work, 10×</h2>
    <div class="section-rule"></div>
    <span class="section-tag">By function</span>
  </div>

  <div class="cap-callout">
    This is not about making your work a little bit faster. It is about making what we all thought was impossible — now possible. If we don't feel that we are attempting things that were out of reach before, we are not thinking ambitiously enough.
  </div>

  <div class="cap-grid">

    <!-- HR Operations -->
    <div class="cap-card">
      <div class="cap-header">
        <div class="cap-icon cap-icon-blue">⚙️</div>
        <div>
          <div class="cap-title">For HR Operations</div>
          <div class="cap-sub">Compliance · benefits · HRIS · employee lifecycle · reporting</div>
        </div>
      </div>
      <div class="cap-items">
        <div class="cap-item cap-item-blue">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>An AI-powered employee help desk</strong> — stop answering the same questions about PTO, benefits, leave, and policies over and over. Build an AI that handles every routine inquiry with accurate, up-to-date answers. You own the knowledge base; the AI handles the queue.</div>
        </div>
        <div class="cap-item cap-item-blue">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Onboarding that runs itself</strong> — personalized onboarding workflows, auto-generated welcome packages, pre-populated paperwork, and an AI guide that answers every "first week" question before it gets asked. New hire time-to-productivity improves. Your time spent per hire drops dramatically.</div>
        </div>
        <div class="cap-item cap-item-blue">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Instant policy &amp; compliance drafts</strong> — whether it's updating a leave policy, generating a compliant offer letter, or drafting a new procedure, AI produces a complete first draft in seconds. Your job becomes reviewing and approving, not writing from scratch.</div>
        </div>
        <div class="cap-item cap-item-blue">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Real-time headcount &amp; people reporting</strong> — connect your HRIS data to an AI layer that generates headcount reports, attrition analysis, and org summaries on demand. Any leader, any question, answered in minutes instead of days.</div>
        </div>
        <div class="cap-item cap-item-blue">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Automated offboarding workflows</strong> — from system access revocation checklists to exit interview scheduling to final documentation — AI orchestrates the process and surfaces what needs a human decision. Nothing falls through the cracks.</div>
        </div>
      </div>
      <div class="not-ambitious">
        <div class="not-ambitious-label">Not ambitious enough</div>
        <div class="na-items">
          <div class="na-item">Using AI to reformat a policy document you already wrote</div>
          <div class="na-item">Asking AI to proofread an email you drafted manually</div>
          <div class="na-item">Using ChatGPT to summarize a report you could read in 10 minutes</div>
          <div class="na-item">Having AI generate a slide you already knew the content of</div>
        </div>
      </div>
    </div>

    <!-- HRBPs -->
    <div class="cap-card">
      <div class="cap-header">
        <div class="cap-icon cap-icon-purple">🤝</div>
        <div>
          <div class="cap-title">For HRBPs</div>
          <div class="cap-sub">Strategic partnership · performance · engagement · org design · ER</div>
        </div>
      </div>
      <div class="cap-items">
        <div class="cap-item cap-item-purple">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Proactive retention risk signals</strong> — stop finding out people are unhappy when they resign. AI synthesizes engagement survey trends, tenure patterns, performance data, and internal mobility signals into an early-warning dashboard. You act before the attrition event, not after.</div>
        </div>
        <div class="cap-item cap-item-purple">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Business reviews that write themselves</strong> — drop in your people metrics and get a complete quarterly business review draft: headcount summary, attrition analysis, engagement highlights, and recommended focus areas. Your judgment shapes the narrative; AI does the assembly.</div>
        </div>
        <div class="cap-item cap-item-purple">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Performance cycle acceleration</strong> — AI synthesizes 360 feedback, self-assessments, and manager notes into structured summaries. Calibration prep drops from days to hours. Managers get better inputs. You have more time to coach the conversations that matter.</div>
        </div>
        <div class="cap-item cap-item-purple">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>ER case documentation &amp; coaching</strong> — AI drafts structured case notes, PIPs, and documentation from your inputs, ensuring consistency and compliance. You focus on the coaching relationship and the judgment calls; AI handles the paper trail.</div>
        </div>
        <div class="cap-item cap-item-purple">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Org design scenario modeling</strong> — describe a restructuring and get an instant analysis of span-of-control impacts, reporting line options, and headcount implications. Bring structured options to leadership conversations instead of building decks manually.</div>
        </div>
      </div>
      <div class="not-ambitious">
        <div class="not-ambitious-label">Not ambitious enough</div>
        <div class="na-items">
          <div class="na-item">Using AI to rewrite a manager email you already know what to say</div>
          <div class="na-item">Asking AI to summarize a meeting you were in</div>
          <div class="na-item">Using AI to translate your notes into a slide</div>
          <div class="na-item">Having AI draft a PIP template without connecting it to a real case</div>
        </div>
      </div>
    </div>

    <!-- Recruiting -->
    <div class="cap-card" style="grid-column:1/-1;">
      <div class="cap-header">
        <div class="cap-icon cap-icon-green">🎯</div>
        <div>
          <div class="cap-title">For Recruiting</div>
          <div class="cap-sub">Sourcing · screening · candidate experience · pipeline analytics · offer</div>
        </div>
      </div>
      <div class="cap-items" style="display:grid;grid-template-columns:1fr 1fr;gap:8px;">
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Sourcing that never sleeps</strong> — AI continuously scans LinkedIn, GitHub, portfolio sites, and conference speaker lists against your open roles and ideal candidate profiles, surfacing net-new talent before you ever open a req. Your pipeline builds itself; you evaluate and engage.</div>
        </div>
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Personalized outreach at scale</strong> — every candidate gets a tailored outreach message that references their specific background, not a generic template. AI generates them in bulk; you review and send. Response rates improve because candidates feel seen, not spammed.</div>
        </div>
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Interview prep packages on demand</strong> — drop a resume and a job description, get a complete interview guide: tailored competency questions, suggested scorecards, and red flags to probe. Every interviewer walks in prepared, not winging it.</div>
        </div>
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Debrief synthesis &amp; decision support</strong> — AI synthesizes interviewer feedback across the panel into a structured summary that surfaces consensus, disagreements, and gaps. Hiring decisions get faster and more consistent; bias blind spots become visible.</div>
        </div>
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Pipeline analytics that predict, not report</strong> — instead of telling you where your pipeline is today, AI models where it will be in 30, 60, 90 days based on current conversion rates, time-in-stage, and historical patterns. Hiring manager conversations shift from status to strategy.</div>
        </div>
        <div class="cap-item cap-item-green">
          <div class="cap-item-dot"></div>
          <div class="cap-item-text"><strong>Candidate experience, fully automated</strong> — every touchpoint — confirmation emails, interview reminders, status updates, rejection letters — is personalized, timely, and consistent. No candidate falls into a black hole. Your brand improves; your admin burden disappears.</div>
        </div>
      </div>
      <div class="not-ambitious">
        <div class="not-ambitious-label">Not ambitious enough</div>
        <div class="na-items">
          <div class="na-item">Using AI to write a job description you already know how to write</div>
          <div class="na-item">Asking AI to clean up a rejection email template</div>
          <div class="na-item">Using AI to convert a JD into a LinkedIn post</div>
          <div class="na-item">Having AI summarize a scorecard you already read</div>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- PROOF POINTS -->
<div id="proofpoints" class="section">
  <div class="section-header">
    <h2>This Is Already Happening</h2>
    <div class="section-rule"></div>
    <span class="section-tag">Not hypothetical — in market now</span>
  </div>

  <div class="proof-grid">
    <div class="proof-card">
      <div class="proof-label">Recruiting</div>
      <div class="proof-title">AI-Assisted Sourcing &amp; Screening</div>
      <div class="proof-desc">Teams using AI for sourcing and first-pass screening report dramatically shorter time-to-hire and higher quality-of-hire scores — recruiters shift from searching to evaluating.</div>
      <span class="proof-stat proof-stat-teal">40–60% reduction in time-to-screen</span>
    </div>
    <div class="proof-card">
      <div class="proof-label">HR Operations</div>
      <div class="proof-title">AI Employee Self-Service</div>
      <div class="proof-desc">Companies deploying AI HR chatbots see 50–70% of routine HR queries handled without human involvement — freeing ops teams from the inbox and into higher-value work.</div>
      <span class="proof-stat proof-stat-green">50–70% ticket deflection in pilots</span>
    </div>
    <div class="proof-card">
      <div class="proof-label">People Analytics</div>
      <div class="proof-title">Predictive Attrition Models</div>
      <div class="proof-desc">Leading People teams are using ML models to flag flight risk 60–90 days before resignation — giving HRBPs a window to intervene before regrettable attrition becomes a headline.</div>
      <span class="proof-stat proof-stat-purple">60–90 day early warning window</span>
    </div>
  </div>
</div>

<!-- MISOGI -->
<div id="misogi" class="section">
  <div class="section-header">
    <h2>Your 2026 Misogi</h2>
    <div class="section-rule"></div>
    <span class="section-tag">For everyone in People</span>
  </div>

  <div class="intro-box" style="margin-bottom:24px;">
    <div class="intro-pill">🏔 The Question to Ask Yourself</div>
    <p class="intro-lead">
      Your Misogi is supposed to be the one thing that, if you achieve it, makes everything else feel incremental by comparison. It should be ambitious enough that success isn't guaranteed.
      <br><br>
      <strong>So here's the question: is AI the cornerstone of how you get there?</strong> Not a tool you might use along the way — the actual engine that makes the goal possible. If the answer is yes, you're thinking at the right level. If the answer is no, or "I'm not sure," that's the conversation to have with your manager — now, not at mid-year.
    </p>
  </div>

  <div class="card-grid" style="margin-bottom:20px;">
    <div class="card card-green">
      <h3><span class="card-dot" style="background:var(--green);"></span>What it looks like when AI is the cornerstone</h3>
      <ul>
        <li>Your Misogi requires doing something at a scale or speed that was genuinely impossible without AI — not just "faster," but structurally different</li>
        <li>Removing AI from the plan would make the goal unreachable, not just harder</li>
        <li>The most ambitious version of your goal and the most ambitious use of AI are the same thing</li>
        <li>You can articulate specifically which AI capabilities unlock which parts of your Misogi</li>
      </ul>
    </div>
    <div class="card card-amber">
      <h3><span class="card-dot" style="background:var(--amber);"></span>Signs you might be thinking too small</h3>
      <ul>
        <li>AI appears as a footnote in your Misogi plan, not the foundation</li>
        <li>Your goal would look roughly the same if AI didn't exist</li>
        <li>You're using AI to do your current job faster — but your Misogi is still defined by the boundaries of your current job</li>
        <li>You haven't yet had a conversation with your manager about how AI changes what's possible for your goal</li>
      </ul>
    </div>
  </div>

  <div class="cta-prompt" style="background:rgba(167,139,250,.07);border-color:rgba(167,139,250,.25);">
    <strong style="color:var(--purple);">If AI isn't the cornerstone of your Misogi yet — put time on your manager's calendar this week.</strong>
    Come prepared with your current Misogi goal and an open question: <em style="color:var(--text);font-style:italic;">"How could AI make this goal 10× more ambitious, or make a completely different goal possible?"</em> That conversation is the starting point. Your manager will help you find the version of your Misogi that only makes sense in an AI-enabled world.
  </div>
</div>

<!-- CTA -->
<div id="cta" class="section">
  <div class="cta-banner">
    <div class="cta-eyebrow">Your Action Item</div>
    <h2 class="cta-title">At your H1 perf review, you will be asked:<br><span class="accent">"What were you able to make ~10× faster using AI? What did you fully delegate to AI?"</span></h2>
    <p class="cta-body">
      This is a real question in the H1 2026 performance review — for every IC and every manager.
      The people with the strongest answers will be the ones who started thinking about it now, not in June.
      <br><br>
      <strong>Your action item: draft your answer today.</strong> You don't need to have done it yet — you need to know what you're aiming for. Pick the one or two things in your current work where AI could have the biggest impact, and write what you want to be able to say at review time.
    </p>

    <div class="cta-steps">
      <div class="cta-step">
        <div class="cta-step-num">1</div>
        <div class="cta-step-text"><strong>Answer question A:</strong> What is one thing in your current work that takes significant time and AI could make 10× faster? <em>e.g. "Drafting interview guides for every panel — currently 45 min per role, could be 5 min with AI-generated competency questions from the JD."</em></div>
      </div>
      <div class="cta-step">
        <div class="cta-step-num">2</div>
        <div class="cta-step-text"><strong>Answer question B:</strong> What is one thing you currently own end-to-end that you could fully delegate to AI by H1 end? <em>e.g. "Answering routine benefits &amp; PTO questions — I currently field ~10 of these a week. An AI help-desk could handle 90% of them automatically."</em></div>
      </div>
      <div class="cta-step">
        <div class="cta-step-num">3</div>
        <div class="cta-step-text"><strong>Share it</strong> — bring your draft answers to your next 1:1. Your manager will help you make the target concrete and give you the space to pursue it.</div>
      </div>
    </div>

    <div class="cta-prompt">
      <strong>The exact perf review question (H1 2026):</strong>
      <br><br>
      <em style="color:var(--text);font-size:14px;font-style:italic;">"AI Outcomes: What were you able to make ~10x faster using AI? What were you able to fully delegate to AI that you previously spent a lot of time doing?"</em>
      <br><br>
      Draft your answer now. Use one of these as a starting point:
      <div class="cta-examples">
        <span class="cta-ex">Job description drafting</span>
        <span class="cta-ex">Interview guide generation</span>
        <span class="cta-ex">Candidate outreach</span>
        <span class="cta-ex">Offer letter creation</span>
        <span class="cta-ex">Policy Q&amp;A / help desk</span>
        <span class="cta-ex">Onboarding workflows</span>
        <span class="cta-ex">Attrition risk modeling</span>
        <span class="cta-ex">Headcount reporting</span>
        <span class="cta-ex">Performance review synthesis</span>
        <span class="cta-ex">Exit interview analysis</span>
        <span class="cta-ex">Sourcing &amp; screening</span>
        <span class="cta-ex">HRBP business reviews</span>
      </div>
    </div>
  </div>
</div>

</div>

<footer>
  <span style="font-size:16px;">👥</span>
  <span class="footer-note">People Team · AI Era · March 2026</span>
</footer>

</body>
</html>
