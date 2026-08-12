<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Neeraj Singh — Cloud & DevOps Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#eaf4f4;
    --paper-2:#f5faf9;
    --card:#ffffff;
    --line:#bcd8d4;
    --line-soft:#d7e9e6;
    --ink:#0f3b3a;
    --ink-2:#3c6360;
    --ink-muted:#6f8f8c;
    --blue:#1f6fb2;
    --blue-deep:#124b7a;
    --green:#2f9e63;
    --green-deep:#1f7248;
    --amber:#c07d16;
    --radius:3px;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--paper);
    color:var(--ink);
    font-family:'Inter', system-ui, sans-serif;
    line-height:1.6;
    background-image:
      linear-gradient(var(--line-soft) 1px, transparent 1px),
      linear-gradient(90deg, var(--line-soft) 1px, transparent 1px);
    background-size: 28px 28px;
  }
  .display{font-family:'Space Grotesk', sans-serif;}
  .mono{font-family:'IBM Plex Mono', ui-monospace, monospace;}
  a{color:inherit;}
  .wrap{max-width:1040px;margin:0 auto;padding:0 30px;}

  .title-block{
    position:fixed; bottom:18px; right:18px; z-index:60;
    background:var(--card); border:1.5px solid var(--ink); border-radius:var(--radius);
    box-shadow:3px 3px 0 var(--line);
    font-family:'IBM Plex Mono',monospace; font-size:10.5px; color:var(--ink-2);
    width:220px; overflow:hidden;
  }
  .title-block .tb-row{display:flex; border-top:1px solid var(--line); }
  .title-block .tb-row:first-child{border-top:none;}
  .title-block .tb-cell{padding:6px 8px; flex:1;}
  .title-block .tb-cell + .tb-cell{border-left:1px solid var(--line);}
  .title-block .tb-label{color:var(--ink-muted); font-size:9px; text-transform:uppercase; letter-spacing:0.06em; display:block;}
  .title-block .tb-value{color:var(--ink); font-weight:500;}
  @media (max-width:760px){ .title-block{display:none;} }

  .topbar{
    position:sticky; top:0; z-index:50;
    background:rgba(234,244,244,0.9); backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  .topbar .wrap{display:flex;align-items:center;justify-content:space-between;height:58px;}
  .brand{font-family:'Space Grotesk',sans-serif;font-weight:700;font-size:15px;color:var(--ink);display:flex;align-items:center;gap:8px;}
  .brand .crosshair{width:16px;height:16px;position:relative;flex:none;}
  .brand .crosshair::before,.brand .crosshair::after{content:"";position:absolute;background:var(--blue);}
  .brand .crosshair::before{width:100%;height:1.5px;top:50%;transform:translateY(-50%);}
  .brand .crosshair::after{height:100%;width:1.5px;left:50%;transform:translateX(-50%);}
  .navlinks{display:flex;gap:24px;font-family:'IBM Plex Mono',monospace;font-size:11.5px;text-transform:uppercase;letter-spacing:0.07em;}
  .navlinks a{color:var(--ink-2);text-decoration:none;transition:color .2s;}
  .navlinks a:hover{color:var(--blue);}
  @media (max-width:720px){ .navlinks{display:none;} }

  .hero{padding:80px 0 56px;}
  .callout{
    display:inline-flex; align-items:center; gap:8px; font-family:'IBM Plex Mono',monospace;
    font-size:11px; letter-spacing:0.1em; text-transform:uppercase; color:var(--blue-deep);
    background:var(--card); border:1px solid var(--blue); border-radius:20px; padding:6px 14px; margin-bottom:22px;
  }
  .callout .pulse{width:6px;height:6px;border-radius:50%;background:var(--green);}
  h1{
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:clamp(36px,5.5vw,58px);
    letter-spacing:-0.01em; line-height:1.08; color:var(--ink); max-width:780px; margin-bottom:18px;
  }
  h1 .underline-blue{ text-decoration:underline; text-decoration-color:var(--blue); text-decoration-thickness:3px; text-underline-offset:6px;}
  .subhead{font-size:16px; color:var(--ink-2); max-width:600px; margin-bottom:30px;}
  .subhead b{color:var(--ink); font-weight:600;}

  .hero-cta{display:flex;gap:14px;margin-bottom:44px;flex-wrap:wrap;}
  .btn{
    font-family:'IBM Plex Mono',monospace; font-size:12.5px; letter-spacing:0.02em;
    padding:12px 20px; border-radius:var(--radius); text-decoration:none;
    border:1.5px solid var(--ink); color:var(--ink); transition:all .15s; background:var(--card);
  }
  .btn.primary{background:var(--blue); color:#fff; border-color:var(--blue-deep);}
  .btn.primary:hover{background:var(--blue-deep);}
  .btn:not(.primary):hover{background:var(--ink); color:#fff;}

  .dim{display:flex; align-items:center; gap:10px; margin:0 0 40px;}
  .dim .dl{flex:1; height:1px; background:var(--line); position:relative;}
  .dim .dl::before,.dim .dl::after{content:"";position:absolute;top:-4px;width:1px;height:9px;background:var(--line);}
  .dim .dl::before{left:0;} .dim .dl::after{right:0;}
  .dim span{font-family:'IBM Plex Mono',monospace; font-size:10.5px; color:var(--ink-muted); letter-spacing:0.06em; white-space:nowrap;}

  section{padding:60px 0;}
  .section-tag{
    display:flex; align-items:center; gap:10px; margin-bottom:8px;
    font-family:'IBM Plex Mono',monospace; font-size:11px; color:var(--blue-deep); letter-spacing:0.08em; text-transform:uppercase;
  }
  .section-tag .sq{width:8px;height:8px;border:1.5px solid var(--blue);flex:none;}
  h2{font-family:'Space Grotesk',sans-serif; font-size:clamp(22px,3vw,29px); font-weight:600; color:var(--ink); margin-bottom:34px;}

  .schematic{
    display:grid; grid-template-columns:1fr auto 1fr; gap:0; align-items:center; margin-bottom:40px;
  }
  @media (max-width:720px){ .schematic{grid-template-columns:1fr; gap:20px;} .schematic .arrow-col{display:none;} }
  .schem-box{
    background:var(--card); border:1.5px solid var(--ink); border-radius:var(--radius); padding:24px;
    position:relative;
  }
  .schem-box .tag{
    position:absolute; top:-11px; left:16px; background:var(--paper-2); padding:0 8px;
    font-family:'IBM Plex Mono',monospace; font-size:10px; letter-spacing:0.08em; text-transform:uppercase;
  }
  .schem-box.from .tag{color:var(--ink-muted);}
  .schem-box.to .tag{color:var(--green-deep);}
  .schem-box h3{font-family:'Space Grotesk',sans-serif; font-size:18px; margin-bottom:10px; color:var(--ink);}
  .schem-box p{font-size:13.5px; color:var(--ink-2);}
  .arrow-col{display:flex; flex-direction:column; align-items:center; padding:0 18px; color:var(--blue);}
  .arrow-col svg{width:44px;height:20px;}
  .arrow-col span{font-family:'IBM Plex Mono',monospace; font-size:9.5px; color:var(--ink-muted); margin-top:4px; white-space:nowrap;}

  .about-copy{color:var(--ink-2); max-width:74ch; margin-bottom:26px;}
  .about-copy b{color:var(--ink); font-weight:600;}
  .about-list{display:grid; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); gap:12px;}
  .about-item{
    display:flex; gap:10px; background:var(--card); border:1px solid var(--line); border-radius:var(--radius); padding:14px 16px;
  }
  .about-item .marker{color:var(--blue); font-family:'IBM Plex Mono',monospace; font-size:12px; font-weight:600; flex:none;}
  .about-item p{font-size:13.5px; color:var(--ink-2);}
  .about-item b{color:var(--ink);}

  .skill-groups{display:grid; grid-template-columns:repeat(auto-fit,minmax(240px,1fr)); gap:18px;}
  .skill-card{background:var(--card); border:1px solid var(--line); border-radius:var(--radius); padding:20px;}
  .skill-card .head{display:flex; justify-content:space-between; align-items:baseline; margin-bottom:14px;}
  .skill-card h3{font-family:'Space Grotesk',sans-serif; font-size:14px; color:var(--ink);}
  .skill-card .count{font-family:'IBM Plex Mono',monospace; font-size:10px; color:var(--ink-muted);}
  .parts{display:flex; flex-direction:column; gap:8px;}
  .part{display:flex; align-items:center; gap:10px; font-size:13px;}
  .part .ref{
    font-family:'IBM Plex Mono',monospace; font-size:10px; color:var(--blue-deep); background:#e6f1fb;
    border-radius:20px; padding:2px 7px; flex:none; min-width:38px; text-align:center;
  }
  .part.learning .ref{color:var(--amber); background:#faeeda;}
  .part .name{color:var(--ink-2);}
  .part.learning .name::after{content:" — learning"; color:var(--amber); font-size:11px;}

  .projects{display:grid; grid-template-columns:repeat(auto-fit,minmax(270px,1fr)); gap:20px;}
  .sheet{
    background:var(--card); border:1.5px solid var(--ink); border-radius:var(--radius); padding:22px;
    position:relative;
  }
  .sheet-head{display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:12px;}
  .sheet-num{font-family:'IBM Plex Mono',monospace; font-size:10px; color:var(--ink-muted);}
  .stamp{
    font-family:'IBM Plex Mono',monospace; font-size:9.5px; letter-spacing:0.06em; text-transform:uppercase;
    border:1.5px solid; border-radius:20px; padding:3px 9px; transform:rotate(-3deg);
  }
  .stamp.active{color:var(--green-deep); border-color:var(--green);}
  .stamp.planned{color:var(--ink-muted); border-color:var(--line);}
  .sheet h3{font-family:'Space Grotesk',sans-serif; font-size:16px; margin-bottom:8px; color:var(--ink);}
  .sheet p{font-size:13px; color:var(--ink-2); margin-bottom:14px;}
  .sheet-tags{display:flex; flex-wrap:wrap; gap:6px;}
  .sheet-tags span{font-family:'IBM Plex Mono',monospace; font-size:10px; color:var(--blue-deep); background:#e6f1fb; padding:3px 8px; border-radius:20px;}

  .ruler{position:relative; padding:30px 0 10px; margin-bottom:10px;}
  .ruler-line{position:relative; height:2px; background:var(--ink); margin:0 6px;}
  .ruler-pts{display:flex; justify-content:space-between; position:relative;}
  .ruler-pt{position:relative; text-align:center; flex:1;}
  .ruler-pt::before{content:""; position:absolute; top:-31px; left:50%; transform:translateX(-50%); width:2px; height:12px; background:var(--ink);}
  .ruler-pt .dot{width:11px;height:11px;border-radius:50%;background:var(--blue);border:2px solid var(--card);box-shadow:0 0 0 1.5px var(--ink);margin:0 auto -22px;position:relative;top:-6px;}
  .ruler-pt .date{font-family:'IBM Plex Mono',monospace; font-size:10px; color:var(--ink-muted); margin-bottom:6px;}
  .ruler-pt .title{font-weight:600; font-size:13.5px; color:var(--ink); margin-bottom:4px; padding:0 6px;}
  .ruler-pt .desc{font-size:12px; color:var(--ink-2); padding:0 8px;}
  @media (max-width:760px){
    .ruler-pts{flex-direction:column; gap:26px;}
    .ruler-line{display:none;}
    .ruler-pt::before{display:none;}
    .ruler-pt{text-align:left; display:flex; gap:14px; align-items:flex-start;}
    .ruler-pt .dot{margin:2px 0 0;}
  }

  .contact{
    border:1.5px solid var(--ink); border-radius:var(--radius); padding:44px; text-align:center; background:var(--card);
  }
  .contact h2{margin-bottom:10px;}
  .contact p{color:var(--ink-2); max-width:52ch; margin:0 auto 26px;}
  .contact-links{display:flex; justify-content:center; gap:14px; flex-wrap:wrap;}
  footer{padding:34px 0 100px; text-align:center; font-family:'IBM Plex Mono',monospace; font-size:11px; color:var(--ink-muted);}

  .reveal{opacity:0; transform:translateY(14px); transition:opacity .6s ease, transform .6s ease;}
  .reveal.in{opacity:1; transform:translateY(0);}
  @media (prefers-reduced-motion: reduce){ .reveal{opacity:1; transform:none; transition:none;} }
</style>
</head>
<body>

<div class="title-block">
  <div class="tb-row">
    <div class="tb-cell" style="flex:2;">
      <span class="tb-label">Name</span>
      <span class="tb-value">Neeraj Singh</span>
    </div>
  </div>
  <div class="tb-row">
    <div class="tb-cell">
      <span class="tb-label">Discipline</span>
      <span class="tb-value">Cloud / DevOps</span>
    </div>
    <div class="tb-cell">
      <span class="tb-label">Rev</span>
      <span class="tb-value">In progress</span>
    </div>
  </div>
  <div class="tb-row">
    <div class="tb-cell">
      <span class="tb-label">Location</span>
      <span class="tb-value">Uttar Pradesh, IN</span>
    </div>
    <div class="tb-cell">
      <span class="tb-label">Status</span>
      <span class="tb-value">Open to work</span>
    </div>
  </div>
</div>

<div class="topbar">
  <div class="wrap">
    <div class="brand"><span class="crosshair"></span>Neeraj Singh</div>
    <nav class="navlinks">
      <a href="#about">about</a>
      <a href="#skills">skills</a>
      <a href="#projects">projects</a>
      <a href="#journey">journey</a>
      <a href="#contact">contact</a>
    </nav>
  </div>
</div>

<header class="hero">
  <div class="wrap">
    <div class="callout"><span class="pulse"></span>Open to DevOps / Cloud Engineer roles — NCR</div>
    <h1>Building cloud infrastructure with the <span class="underline-blue">precision of a closed ledger.</span></h1>
    <p class="subhead">
      I'm <b>Neeraj Singh</b>, a Cloud &amp; DevOps engineer in training — hands-on with <b>Azure</b> and
      <b>Terraform</b> through a structured DevOps internship, backed by 5+ years of controls-driven
      finance operations experience.
    </p>
    <div class="hero-cta">
      <a class="btn primary" href="https://github.com/nraajsingh55-dot" target="_blank" rel="noopener">View GitHub →</a>
      <a class="btn" href="#projects">See projects</a>
      <a class="btn" href="#contact">Get in touch</a>
    </div>
    <div class="dim"><div class="dl"></div><span>SCOPE OF WORK — SCROLL TO EXPLORE</span><div class="dl"></div></div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-tag reveal"><span class="sq"></span>01 — about</div>
    <h2 class="reveal">Two disciplines, one build</h2>

    <div class="schematic reveal">
      <div class="schem-box from">
        <span class="tag">Origin</span>
        <h3>Finance Operations</h3>
        <p>5+ years in Record-to-Report — reconciliation, JD Edwards, AS400, Advanced Excel and Power Query. Precision and traceability, non-negotiable.</p>
      </div>
      <div class="arrow-col">
        <svg viewBox="0 0 44 20" fill="none"><path d="M0 10H38M38 10L30 3M38 10L30 17" stroke="#1f6fb2" stroke-width="2"/></svg>
        <span>in transition</span>
      </div>
      <div class="schem-box to">
        <span class="tag">Destination</span>
        <h3>Cloud &amp; DevOps</h3>
        <p>Azure infrastructure, Terraform modules, Linux fundamentals — applying the same controls-first discipline to infrastructure as code.</p>
      </div>
    </div>

    <p class="about-copy reveal">
      I'm building hands-on expertise in <b>Cloud &amp; DevOps engineering</b> — working through real Azure
      infrastructure, Terraform modules, and Linux fundamentals via a structured, hands-on internship. That sits
      on top of a <b>detail-first, controls-driven mindset from 5+ years in finance operations</b>, which I'm now
      applying to building reliable, well-documented infrastructure.
    </p>

    <div class="about-list reveal">
      <div class="about-item"><span class="marker">01</span><p><b>DevOps internship</b> — Azure networking, load balancers, NAT Gateway, Azure Bastion.</p></div>
      <div class="about-item"><span class="marker">02</span><p><b>Terraform</b> — modules, <code>for_each</code>, remote backends.</p></div>
      <div class="about-item"><span class="marker">03</span><p>Currently deepening <b>Docker</b> and <b>Kubernetes</b>.</p></div>
      <div class="about-item"><span class="marker">04</span><p><b>Finance operations</b> — R2R / reconciliation across JD Edwards and AS400.</p></div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-tag reveal"><span class="sq"></span>02 — skills</div>
    <h2 class="reveal">Toolset, by component</h2>
    <div class="skill-groups reveal">
      <div class="skill-card">
        <div class="head"><h3>Cloud &amp; IaC</h3><span class="count">05 parts</span></div>
        <div class="parts">
          <div class="part"><span class="ref">AZ-01</span><span class="name">Microsoft Azure</span></div>
          <div class="part"><span class="ref">TF-01</span><span class="name">Terraform</span></div>
          <div class="part"><span class="ref">AZ-02</span><span class="name">Azure Load Balancer</span></div>
          <div class="part"><span class="ref">AZ-03</span><span class="name">NAT Gateway</span></div>
          <div class="part"><span class="ref">AZ-04</span><span class="name">Azure Bastion</span></div>
        </div>
      </div>
      <div class="skill-card">
        <div class="head"><h3>Containers</h3><span class="count">02 parts</span></div>
        <div class="parts">
          <div class="part learning"><span class="ref">DK-01</span><span class="name">Docker</span></div>
          <div class="part learning"><span class="ref">K8-01</span><span class="name">Kubernetes</span></div>
        </div>
      </div>
      <div class="skill-card">
        <div class="head"><h3>Version control &amp; CI/CD</h3><span class="count">03 parts</span></div>
        <div class="parts">
          <div class="part"><span class="ref">GT-01</span><span class="name">Git</span></div>
          <div class="part"><span class="ref">GH-01</span><span class="name">GitHub</span></div>
          <div class="part"><span class="ref">CI-01</span><span class="name">CI/CD pipelines</span></div>
        </div>
      </div>
      <div class="skill-card">
        <div class="head"><h3>Finance &amp; reconciliation</h3><span class="count">04 parts</span></div>
        <div class="parts">
          <div class="part"><span class="ref">FX-01</span><span class="name">Advanced Excel</span></div>
          <div class="part"><span class="ref">FX-02</span><span class="name">Power Query</span></div>
          <div class="part"><span class="ref">FX-03</span><span class="name">JD Edwards</span></div>
          <div class="part"><span class="ref">FX-04</span><span class="name">AS400</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-tag reveal"><span class="sq"></span>03 — projects</div>
    <h2 class="reveal">Build sheets</h2>
    <div class="projects reveal">
      <div class="sheet">
        <div class="sheet-head"><span class="sheet-num">SHEET 01 / 04</span><span class="stamp active">In progress</span></div>
        <h3>Azure load-balanced web tier</h3>
        <p>Two-VM setup behind an Azure Load Balancer, provisioned end-to-end with Terraform.</p>
        <div class="sheet-tags"><span>Azure</span><span>Terraform</span><span>Load Balancer</span></div>
      </div>
      <div class="sheet">
        <div class="sheet-head"><span class="sheet-num">SHEET 02 / 04</span><span class="stamp planned">Planned</span></div>
        <h3>Secure Bastion access module</h3>
        <p>Reusable Terraform module for Azure Bastion + NAT Gateway, replacing public IP exposure with a locked-down jump host.</p>
        <div class="sheet-tags"><span>Terraform</span><span>Azure Bastion</span><span>Security</span></div>
      </div>
      <div class="sheet">
        <div class="sheet-head"><span class="sheet-num">SHEET 03 / 04</span><span class="stamp planned">Planned</span></div>
        <h3>Containerized app on Kubernetes</h3>
        <p>First end-to-end deployment: a Dockerized app shipped to a Kubernetes cluster via a basic CI/CD pipeline.</p>
        <div class="sheet-tags"><span>Docker</span><span>Kubernetes</span><span>CI/CD</span></div>
      </div>
      <div class="sheet">
        <div class="sheet-head"><span class="sheet-num">SHEET 04 / 04</span><span class="stamp planned">Idea</span></div>
        <h3>Recon-to-cloud automation</h3>
        <p>A personal project bridging both worlds — using Azure Functions to reduce manual steps in a recurring reconciliation workflow.</p>
        <div class="sheet-tags"><span>Azure Functions</span><span>Automation</span></div>
      </div>
    </div>
  </div>
</section>

<section id="journey">
  <div class="wrap">
    <div class="section-tag reveal"><span class="sq"></span>04 — journey</div>
    <h2 class="reveal">Progress, measured</h2>
    <div class="ruler reveal">
      <div class="ruler-pts">
        <div class="ruler-pt">
          <div class="dot"></div>
          <div class="date">Ongoing</div>
          <div class="title">Finance operations</div>
          <div class="desc">R2R reconciliation across JD Edwards and AS400.</div>
        </div>
        <div class="ruler-pt">
          <div class="dot"></div>
          <div class="date">Hands-on</div>
          <div class="title">DevOps internship</div>
          <div class="desc">Azure networking, load balancing, Terraform labs.</div>
        </div>
        <div class="ruler-pt">
          <div class="dot"></div>
          <div class="date">Next</div>
          <div class="title">Docker, Kubernetes &amp; CI/CD</div>
          <div class="desc">Completing the container and pipeline skill set.</div>
        </div>
        <div class="ruler-pt">
          <div class="dot"></div>
          <div class="date">Goal</div>
          <div class="title">Full-time DevOps role</div>
          <div class="desc">Targeting NCR — Delhi, Gurgaon, Noida.</div>
        </div>
      </div>
      <div class="ruler-line"></div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="contact reveal">
      <h2>Let's connect</h2>
      <p>Open to DevOps and Cloud Engineer opportunities — happy to talk infrastructure, reconciliation-grade rigor, or both.</p>
      <div class="contact-links">
        <a class="btn primary" href="https://github.com/nraajsingh55-dot" target="_blank" rel="noopener">GitHub</a>
        <a class="btn" href="https://www.linkedin.com/in/neeraj-singh-b86424178" target="_blank" rel="noopener">LinkedIn</a>
        <a class="btn" href="mailto:Nraajsingh55@gmail.com">Email</a>
      </div>
    </div>
  </div>
</section>

<footer>
  © <span id="year"></span> Neeraj Singh — drawn to scale, built to spec.
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();
  const els = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window) {
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } });
    }, { threshold: 0.12 });
    els.forEach(el => io.observe(el));
  } else {
    els.forEach(el => el.classList.add('in'));
  }
</script>

</body>
</html>
