<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Souhail Lissaneddine</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

:root{
–bg: #060d18;
–bg2: #0a1525;
–bg3: #0f1e35;
–card: #0d1b30;
–border: #162840;
–blue: #0ea5e9;
–blue2: #38bdf8;
–teal: #00d4b4;
–gold: #f5a623;
–green: #22c55e;
–red: #ef4444;
–white: #f0f8ff;
–dim: #6a8faf;
–muted: #2a4a6a;
}

body{
background:var(–bg);
color:var(–white);
font-family:‘DM Sans’,sans-serif;
font-weight:300;
line-height:1.6;
overflow-x:hidden;
}

/* grid lines bg */
body::before{
content:’’;position:fixed;inset:0;z-index:0;
background-image:
linear-gradient(rgba(14,165,233,0.04) 1px,transparent 1px),
linear-gradient(90deg,rgba(14,165,233,0.04) 1px,transparent 1px);
background-size:48px 48px;
pointer-events:none;
}

.wrap{position:relative;z-index:1;max-width:1100px;margin:0 auto;padding:0 24px 80px}

/* ── HERO ───────────────────────────────────────────────── */
.hero{
padding:80px 0 60px;
display:grid;
grid-template-columns:1fr auto;
gap:40px;
align-items:center;
border-bottom:1px solid var(–border);
margin-bottom:60px;
}
@media(max-width:700px){.hero{grid-template-columns:1fr;}.hero-right{display:none}}

.hero-badge{
display:inline-flex;align-items:center;gap:8px;
background:rgba(14,165,233,0.1);
border:1px solid rgba(14,165,233,0.25);
border-radius:20px;padding:5px 16px;
font-size:11px;font-weight:500;letter-spacing:2px;
color:var(–blue2);text-transform:uppercase;
margin-bottom:20px;
}
.hero-badge::before{
content:’’;width:7px;height:7px;border-radius:50%;
background:var(–teal);animation:pulse 2s infinite;
}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.3;transform:scale(1.5)}}

.hero h1{
font-family:‘Bebas Neue’,sans-serif;
font-size:clamp(48px,7vw,88px);
line-height:.95;
letter-spacing:2px;
background:linear-gradient(135deg,var(–white) 0%,var(–blue2) 60%,var(–teal) 100%);
-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
margin-bottom:16px;
}
.hero-role{font-size:18px;color:var(–dim);font-weight:400;margin-bottom:24px}
.hero-role span{color:var(–teal);font-weight:500}

.hero-tags{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:32px}
.tag{
padding:5px 14px;border-radius:6px;font-size:11px;
font-weight:500;letter-spacing:.8px;text-transform:uppercase;
}
.tb{background:rgba(14,165,233,0.1);color:var(–blue2);border:1px solid rgba(14,165,233,0.2)}
.tt{background:rgba(0,212,180,0.1);color:var(–teal);border:1px solid rgba(0,212,180,0.2)}
.tg{background:rgba(245,166,35,0.1);color:var(–gold);border:1px solid rgba(245,166,35,0.2)}

.hero-links{display:flex;gap:12px;flex-wrap:wrap}
.btn{
padding:10px 22px;border-radius:8px;font-size:13px;font-weight:500;
text-decoration:none;transition:all .2s;display:inline-flex;align-items:center;gap:8px;
}
.btn-primary{background:var(–blue);color:#fff}
.btn-primary:hover{background:var(–blue2);transform:translateY(-2px)}
.btn-outline{border:1px solid var(–border);color:var(–dim)}
.btn-outline:hover{border-color:var(–blue);color:var(–blue);transform:translateY(-2px)}

.hero-right{text-align:center}
.years-num{
font-family:‘Bebas Neue’,sans-serif;font-size:110px;line-height:1;
color:var(–blue);text-shadow:0 0 60px rgba(14,165,233,0.4);
}
.years-lbl{font-size:12px;letter-spacing:3px;color:var(–dim);text-transform:uppercase}

/* ── SECTION LABEL ──────────────────────────────────────── */
.sec-lbl{
font-size:11px;font-weight:600;letter-spacing:3px;
text-transform:uppercase;color:var(–teal);
margin-bottom:20px;display:flex;align-items:center;gap:12px;
}
.sec-lbl::after{content:’’;flex:1;height:1px;background:linear-gradient(90deg,var(–border),transparent)}

/* ── KPI STRIP ──────────────────────────────────────────── */
.kpi-grid{
display:grid;
grid-template-columns:repeat(6,1fr);
gap:12px;margin-bottom:60px;
}
@media(max-width:900px){.kpi-grid{grid-template-columns:repeat(3,1fr)}}
@media(max-width:500px){.kpi-grid{grid-template-columns:repeat(2,1fr)}}

.kpi{
background:var(–card);border:1px solid var(–border);
border-radius:12px;padding:20px 14px;text-align:center;
position:relative;overflow:hidden;
transition:transform .2s,border-color .2s;
}
.kpi:hover{transform:translateY(-4px)}
.kpi::before{content:’’;position:absolute;top:0;left:0;right:0;height:2px}
.kpi.b::before{background:linear-gradient(90deg,var(–blue),var(–teal))}
.kpi.t::before{background:linear-gradient(90deg,var(–teal),var(–blue))}
.kpi.g::before{background:linear-gradient(90deg,var(–gold),#f97316)}
.kpi.gr::before{background:linear-gradient(90deg,var(–green),var(–teal))}
.kpi.r::before{background:linear-gradient(90deg,var(–red),var(–gold))}
.kpi:hover{border-color:var(–blue)}

.kpi-num{
font-family:‘Bebas Neue’,sans-serif;
font-size:40px;line-height:1;margin-bottom:6px;
}
.kpi.b .kpi-num{color:var(–blue2)}
.kpi.t .kpi-num{color:var(–teal)}
.kpi.g .kpi-num{color:var(–gold)}
.kpi.gr .kpi-num{color:var(–green)}
.kpi.r .kpi-num{color:var(–red)}

.kpi-lbl{font-size:10px;color:var(–dim);line-height:1.3;letter-spacing:.3px}
.kpi-sub{font-size:9px;color:var(–muted);margin-top:4px;font-style:italic}

/* ── CARDS ──────────────────────────────────────────────── */
.card{
background:var(–card);border:1px solid var(–border);
border-radius:14px;padding:28px;margin-bottom:16px;
}
.card-title{
font-size:11px;font-weight:600;letter-spacing:2px;
text-transform:uppercase;color:var(–dim);
margin-bottom:20px;display:flex;align-items:center;gap:8px;
}
.card-title span{color:var(–blue)}

/* ── TIMELINE ───────────────────────────────────────────── */
.timeline{display:flex;flex-direction:column;gap:0}
.tl-item{
display:grid;grid-template-columns:90px 16px 1fr;
gap:0 20px;position:relative;
}
.tl-item:not(:last-child)::after{
content:’’;position:absolute;
left:98px;top:22px;bottom:-6px;
width:2px;background:linear-gradient(180deg,var(–border),transparent);
}
.tl-date{font-size:10px;color:var(–muted);text-align:right;padding-top:4px;line-height:1.5}
.tl-dot{
width:12px;height:12px;border-radius:50%;
margin-top:6px;flex-shrink:0;position:relative;z-index:1;
}
.tl-dot.b{background:var(–blue);box-shadow:0 0 10px var(–blue)}
.tl-dot.t{background:var(–teal);box-shadow:0 0 10px var(–teal)}
.tl-dot.g{background:var(–gold);box-shadow:0 0 10px var(–gold)}
.tl-dot.gr{background:var(–green);box-shadow:0 0 10px var(–green)}
.tl-dot.r{background:var(–red);box-shadow:0 0 10px var(–red)}

.tl-body{padding:0 0 28px}
.tl-co{font-family:‘Bebas Neue’,sans-serif;font-size:20px;letter-spacing:1px}
.tl-co.b{color:var(–blue2)}
.tl-co.t{color:var(–teal)}
.tl-co.g{color:var(–gold)}
.tl-co.gr{color:var(–green)}
.tl-co.r{color:var(–red)}

.tl-role{font-size:12px;color:var(–dim);margin:3px 0 10px}
.tl-stats{display:flex;flex-wrap:wrap;gap:6px}
.tl-stat{
font-size:10px;padding:3px 10px;border-radius:4px;
background:rgba(14,165,233,0.08);
border:1px solid rgba(14,165,233,0.15);color:var(–blue2);
}
.tl-stat.t{background:rgba(0,212,180,0.08);border-color:rgba(0,212,180,0.15);color:var(–teal)}
.tl-stat.g{background:rgba(245,166,35,0.08);border-color:rgba(245,166,35,0.15);color:var(–gold)}
.tl-stat.gr{background:rgba(34,197,94,0.08);border-color:rgba(34,197,94,0.15);color:var(–green)}

/* ── SKILL BARS ─────────────────────────────────────────── */
.skill{margin-bottom:16px}
.skill-hdr{display:flex;justify-content:space-between;margin-bottom:6px}
.skill-name{font-size:12px;color:var(–white)}
.skill-pct{font-family:‘Bebas Neue’,sans-serif;font-size:16px;color:var(–dim)}
.skill-track{height:5px;border-radius:3px;background:var(–bg3);overflow:hidden}
.skill-fill{
height:100%;border-radius:3px;width:0;
transition:width 1.6s cubic-bezier(.4,0,.2,1);
}
.sf-b{background:linear-gradient(90deg,var(–blue),var(–teal))}
.sf-g{background:linear-gradient(90deg,var(–gold),#f97316)}
.sf-gr{background:linear-gradient(90deg,var(–green),var(–teal))}

/* ── TOOLS ──────────────────────────────────────────────── */
.tools{display:flex;flex-wrap:wrap;gap:10px}
.tool{
display:flex;align-items:center;gap:10px;
padding:10px 16px;border-radius:8px;
background:var(–bg3);border:1px solid var(–border);
transition:border-color .2s,transform .2s;
cursor:default;
}
.tool:hover{border-color:var(–blue);transform:translateY(-2px)}
.tool-ico{font-size:18px}
.tool-info .tool-name{font-size:12px;font-weight:500}
.tool-info .tool-lvl{font-size:10px;color:var(–dim)}

/* ── ACHIEVEMENTS ───────────────────────────────────────── */
.ach-list{display:flex;flex-direction:column;gap:10px}
.ach{
display:flex;align-items:flex-start;gap:14px;
padding:14px 16px;border-radius:8px;
background:var(–bg3);
border-left:3px solid var(–blue);
transition:background .2s;
}
.ach:hover{background:var(–bg2)}
.ach.t{border-left-color:var(–teal)}
.ach.g{border-left-color:var(–gold)}
.ach.gr{border-left-color:var(–green)}
.ach-ico{font-size:20px;flex-shrink:0;margin-top:1px}
.ach-txt{flex:1}
.ach-title{font-size:12px;font-weight:500;margin-bottom:3px}
.ach-desc{font-size:11px;color:var(–dim);line-height:1.5}
.ach-num{
font-family:‘Bebas Neue’,sans-serif;
font-size:24px;color:var(–blue2);flex-shrink:0;
}
.ach.t .ach-num{color:var(–teal)}
.ach.g .ach-num{color:var(–gold)}
.ach.gr .ach-num{color:var(–green)}

/* ── QUOTE ──────────────────────────────────────────────── */
.quote{
background:linear-gradient(135deg,var(–bg2),var(–bg3));
border:1px solid var(–border);
border-left:4px solid var(–teal);
border-radius:12px;padding:28px 32px;
margin:60px 0;position:relative;
}
.quote::before{
content:‘❝’;position:absolute;top:10px;right:24px;
font-size:70px;color:var(–border);line-height:1;font-family:serif;
}
.quote-text{font-size:16px;line-height:1.8;font-weight:300}
.quote-attr{font-size:12px;color:var(–teal);margin-top:12px;font-weight:500}

/* ── LANG DOTS ──────────────────────────────────────────── */
.lang-row{
display:flex;align-items:center;justify-content:space-between;
padding:12px 0;border-bottom:1px solid var(–border);
}
.lang-row:last-child{border:none}
.lang-name{font-size:13px;font-weight:500}
.lang-sub{font-size:11px;color:var(–dim)}
.dots{display:flex;gap:5px}
.dot{width:8px;height:8px;border-radius:50%;background:var(–muted)}
.dot.on{background:var(–teal);box-shadow:0 0 6px var(–teal)}

/* ── GRID LAYOUTS ───────────────────────────────────────── */
.g2{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-bottom:60px}
.g21{display:grid;grid-template-columns:2fr 1fr;gap:20px;margin-bottom:60px}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:20px;margin-bottom:60px}
@media(max-width:860px){.g2,.g21,.g3{grid-template-columns:1fr}}

/* ── CONTACT BAR ────────────────────────────────────────── */
.contact{
border-top:1px solid var(–border);
padding-top:40px;margin-top:40px;
display:flex;flex-wrap:wrap;gap:20px;justify-content:center;
text-align:center;
}
.contact a{
color:var(–blue2);text-decoration:none;font-size:13px;
letter-spacing:.5px;transition:color .2s;
}
.contact a:hover{color:var(–teal)}

/* ── FADE ANIMATION ─────────────────────────────────────── */
.fade{opacity:0;transform:translateY(24px);animation:fu .6s ease forwards}
@keyframes fu{to{opacity:1;transform:translateY(0)}}
.fade:nth-child(1){animation-delay:.05s}
.fade:nth-child(2){animation-delay:.12s}
.fade:nth-child(3){animation-delay:.19s}
.fade:nth-child(4){animation-delay:.26s}
.fade:nth-child(5){animation-delay:.33s}
.fade:nth-child(6){animation-delay:.40s}
</style>

</head>
<body>
<div class="wrap">

<!-- ══ HERO ══════════════════════════════════════════════════ -->

<div class="hero">
<div>
<div class="hero-badge">Operations Analytics Portfolio</div>
<h1>Souhail<br>Lissaneddine</h1>
<p class="hero-role">Supply Chain & Logistics Manager · <span>Casablanca, Morocco</span></p>
<div class="hero-tags">
<span class="tag tb">Last Mile Ops</span>
<span class="tag tt">Supply Chain</span>
<span class="tag tg">Procurement</span>
<span class="tag tb">Warehouse Mgt</span>
<span class="tag tt">S&OP Planning</span>
<span class="tag tg">KPI Analytics</span>
</div>
<div class="hero-links">
<a href="mailto:souhail.lissaneddine@gmail.com" class="btn btn-primary">✉ Contact Me</a>
<a href="https://www.linkedin.com/in/souhail-lissan-eddine-7253a1192" target="_blank" class="btn btn-outline">LinkedIn →</a>
</div>
</div>
<div class="hero-right">
<div class="years-num" id="yrs">0</div>
<div class="years-lbl">Years Experience</div>
</div>
</div>

<!-- ══ KPIs ═══════════════════════════════════════════════════ -->

<div class="sec-lbl">Core Performance Metrics</div>
<div class="kpi-grid">
<div class="kpi b fade"><div class="kpi-num"><span class="cnt" data-t="9000" data-s="+">0</span></div><div class="kpi-lbl">Orders Per Day</div><div class="kpi-sub">Jumia Group peak</div></div>
<div class="kpi t fade"><div class="kpi-num"><span class="cnt" data-t="98" data-s="%+">0</span></div><div class="kpi-lbl">On-Time Delivery</div><div class="kpi-sub">OTIF rate achieved</div></div>
<div class="kpi g fade"><div class="kpi-num"><span class="cnt" data-t="40" data-s="T+">0</span></div><div class="kpi-lbl">Tonnes / Day</div><div class="kpi-sub">Fresh produce managed</div></div>
<div class="kpi gr fade"><div class="kpi-num"><span class="cnt" data-t="30" data-s="%">0</span></div><div class="kpi-lbl">Revenue Growth</div><div class="kpi-sub">B2C e-com launch Y1</div></div>
<div class="kpi b fade"><div class="kpi-num"><span class="cnt" data-t="99" data-s="%">0</span></div><div class="kpi-lbl">Stock Accuracy</div><div class="kpi-sub">Inventory precision</div></div>
<div class="kpi r fade"><div class="kpi-num"><span class="cnt" data-t="47" data-s="">0</span></div><div class="kpi-lbl">Max Team Size</div><div class="kpi-sub">People led directly</div></div>
</div>

<!-- ══ TIMELINE + RADAR ═══════════════════════════════════════ -->

<div class="sec-lbl">Career Timeline</div>
<div class="g21">
<div class="card">
<div class="card-title"><span>◈</span> 5 Companies · 8+ Years · 3 Sectors</div>
<div class="timeline">

```
<div class="tl-item">
<div class="tl-date">Apr 2017<br>Mar 2019</div>
<div class="tl-dot b"></div>
<div class="tl-body">
<div class="tl-co b">Jumia Group</div>
<div class="tl-role">Outbound Logistics Supervisor — Casablanca</div>
<div class="tl-stats">
<span class="tl-stat">9,000 orders/day</span>
<span class="tl-stat t">98% OTIF</span>
<span class="tl-stat gr">+20% productivity</span>
<span class="tl-stat g">Africa #1 e-com</span>
</div>
</div>
</div>

<div class="tl-item">
<div class="tl-date">Mar 2019<br>Jan 2022</div>
<div class="tl-dot g"></div>
<div class="tl-body">
<div class="tl-co g">Gamma Coffee Group</div>
<div class="tl-role">Procurement & Logistics Manager — Casablanca</div>
<div class="tl-stats">
<span class="tl-stat g">+30% revenue Y1</span>
<span class="tl-stat t">-20% supplier costs</span>
<span class="tl-stat">B2C e-com launch</span>
<span class="tl-stat gr">99% accuracy</span>
</div>
</div>
</div>

<div class="tl-item">
<div class="tl-date">Feb 2022<br>Jul 2023</div>
<div class="tl-dot t"></div>
<div class="tl-body">
<div class="tl-co t">SENDIT</div>
<div class="tl-role">Last Mile Operations Manager — Casablanca</div>
<div class="tl-stats">
<span class="tl-stat">5,000 parcels/day</span>
<span class="tl-stat t">98%+ OTIF</span>
<span class="tl-stat g">-15% transport cost</span>
<span class="tl-stat gr">44 staff</span>
</div>
</div>
</div>

<div class="tl-item">
<div class="tl-date">Jul 2023<br>Jul 2024</div>
<div class="tl-dot gr"></div>
<div class="tl-body">
<div class="tl-co gr">Yola Fresh</div>
<div class="tl-role">Warehouse Manager — Agadir</div>
<div class="tl-stats">
<span class="tl-stat gr">40T+/day perishables</span>
<span class="tl-stat t">95% OTIF</span>
<span class="tl-stat">99% stock accuracy</span>
<span class="tl-stat g">37 staff</span>
</div>
</div>
</div>

<div class="tl-item">
<div class="tl-date">Jul 2024<br>Mar 2025</div>
<div class="tl-dot r"></div>
<div class="tl-body">
<div class="tl-co" style="color:#ef4444">ERIS</div>
<div class="tl-role">Logistics Operations Manager — Casablanca</div>
<div class="tl-stats">
<span class="tl-stat t">100% on-time</span>
<span class="tl-stat gr">-25% shortages</span>
<span class="tl-stat g">+18% efficiency</span>
</div>
</div>
</div>

</div>
```

</div>

<!-- Skills card -->

<div style="display:flex;flex-direction:column;gap:16px">
<div class="card">
<div class="card-title"><span>◈</span> Competencies</div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">Last Mile & Delivery Ops</span><span class="skill-pct">98%</span></div><div class="skill-track"><div class="skill-fill sf-b" data-w="98"></div></div></div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">Warehouse & WMS</span><span class="skill-pct">95%</span></div><div class="skill-track"><div class="skill-fill sf-b" data-w="95"></div></div></div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">Inventory Control</span><span class="skill-pct">99%</span></div><div class="skill-track"><div class="skill-fill sf-b" data-w="99"></div></div></div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">Team Leadership</span><span class="skill-pct">92%</span></div><div class="skill-track"><div class="skill-fill sf-b" data-w="92"></div></div></div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">Procurement & Sourcing</span><span class="skill-pct">88%</span></div><div class="skill-track"><div class="skill-fill sf-g" data-w="88"></div></div></div>
<div class="skill"><div class="skill-hdr"><span class="skill-name">S&OP & Forecasting</span><span class="skill-pct">85%</span></div><div class="skill-track"><div class="skill-fill sf-gr" data-w="85"></div></div></div>
</div>
<div class="card">
<div class="card-title"><span>◈</span> Languages</div>
<div class="lang-row"><div><div class="lang-name">Arabic</div><div class="lang-sub">Native</div></div><div class="dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
<div class="lang-row"><div><div class="lang-name">French</div><div class="lang-sub">Full Professional</div></div><div class="dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
<div class="lang-row"><div><div class="lang-name">English</div><div class="lang-sub">Bilingual</div></div><div class="dots"><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div></div></div>
</div>
</div>
</div>

<!-- ══ ACHIEVEMENTS ════════════════════════════════════════════ -->

<div class="sec-lbl">Signature Achievements by Company</div>
<div class="g3">
<div class="card fade">
<div class="card-title"><span>◈</span> SENDIT</div>
<div class="ach-list">
<div class="ach"><span class="ach-ico">🚀</span><div class="ach-txt"><div class="ach-title">Built ops from scratch</div><div class="ach-desc">5,000 parcels/day national — full infrastructure in weeks</div></div><div class="ach-num">5K</div></div>
<div class="ach t"><span class="ach-ico">📉</span><div class="ach-txt"><div class="ach-title">Transport cost cut</div><div class="ach-desc">Route optimization — no headcount reduction</div></div><div class="ach-num">-15%</div></div>
<div class="ach gr"><span class="ach-ico">📈</span><div class="ach-txt"><div class="ach-title">Team productivity</div><div class="ach-desc">44-person team in under 6 months</div></div><div class="ach-num">+25%</div></div>
</div>
</div>
<div class="card fade">
<div class="card-title"><span>◈</span> Yola Fresh</div>
<div class="ach-list">
<div class="ach g"><span class="ach-ico">❄️</span><div class="ach-txt"><div class="ach-title">Zero cold chain incidents</div><div class="ach-desc">40T+ daily perishables — 12 months zero breach</div></div><div class="ach-num">0</div></div>
<div class="ach t"><span class="ach-ico">✅</span><div class="ach-txt"><div class="ach-title">Inventory accuracy</div><div class="ach-desc">FIFO/FEFO discipline across 37-person team</div></div><div class="ach-num">99%</div></div>
<div class="ach gr"><span class="ach-ico">👥</span><div class="ach-txt"><div class="ach-title">Productivity gain</div><div class="ach-desc">3-level structure built from zero</div></div><div class="ach-num">+20%</div></div>
</div>
</div>
<div class="card fade">
<div class="card-title"><span>◈</span> Gamma Coffee</div>
<div class="ach-list">
<div class="ach"><span class="ach-ico">🛒</span><div class="ach-txt"><div class="ach-title">B2C e-commerce launch</div><div class="ach-desc">Morocco's first DTC coffee platform built from scratch</div></div><div class="ach-num">+30%</div></div>
<div class="ach g"><span class="ach-ico">🤝</span><div class="ach-txt"><div class="ach-title">Supplier savings</div><div class="ach-desc">International sourcing — contract renegotiation</div></div><div class="ach-num">-20%</div></div>
<div class="ach t"><span class="ach-ico">📦</span><div class="ach-txt"><div class="ach-title">Stockout reduction</div><div class="ach-desc">Demand planning + supplier alignment</div></div><div class="ach-num">-25%</div></div>
</div>
</div>
</div>

<!-- ══ TOOLS ═══════════════════════════════════════════════════ -->

<div class="sec-lbl">Tools & Technologies</div>
<div class="card" style="margin-bottom:60px">
<div class="tools">
<div class="tool"><span class="tool-ico">📊</span><div class="tool-info"><div class="tool-name">Excel Advanced</div><div class="tool-lvl">Pivot · VLOOKUP · Dashboards</div></div></div>
<div class="tool"><span class="tool-ico">🏭</span><div class="tool-info"><div class="tool-name">WMS Systems</div><div class="tool-lvl">Stock · Movements · Traceability</div></div></div>
<div class="tool"><span class="tool-ico">🗄️</span><div class="tool-info"><div class="tool-name">ERP / SAP</div><div class="tool-lvl">MM · WM Modules</div></div></div>
<div class="tool"><span class="tool-ico">📈</span><div class="tool-info"><div class="tool-name">Power BI</div><div class="tool-lvl">Dashboards · DAX</div></div></div>
<div class="tool"><span class="tool-ico">🗃️</span><div class="tool-info"><div class="tool-name">SQL / Data</div><div class="tool-lvl">Queries · Reporting</div></div></div>
<div class="tool"><span class="tool-ico">📦</span><div class="tool-info"><div class="tool-name">Route Optimization</div><div class="tool-lvl">Zone planning · Load balancing</div></div></div>
<div class="tool"><span class="tool-ico">🔄</span><div class="tool-info"><div class="tool-name">Lean / FIFO / FEFO</div><div class="tool-lvl">Process improvement</div></div></div>
<div class="tool"><span class="tool-ico">📋</span><div class="tool-info"><div class="tool-name">KPI Frameworks</div><div class="tool-lvl">OTIF · DIFOT · Balanced Scorecard</div></div></div>
</div>
</div>

<!-- ══ QUOTE ════════════════════════════════════════════════════ -->

<div class="quote">
<p class="quote-text">"Logistics performance is 20% tools and 80% discipline. I have spent 8 years building operations that work without me being in the room — through systems, accountability, and teams that own their numbers."</p>
<p class="quote-attr">— Souhail Lissaneddine · Supply Chain & Logistics Manager</p>
</div>

<!-- ══ CONTACT ══════════════════════════════════════════════════ -->

<div class="contact">
<a href="mailto:souhail.lissaneddine@gmail.com">✉ souhail.lissaneddine@gmail.com</a>
<a href="tel:+212632570273">📞 +212 632 570 273</a>
<a href="https://www.linkedin.com/in/souhail-lissan-eddine-7253a1192" target="_blank">🔗 LinkedIn Profile</a>
<span style="color:var(--dim);font-size:13px">📍 Casablanca, Morocco · Open to relocation</span>
</div>

</div><!-- /wrap -->

<script>
// Counter animation
function animateCounters(){
document.querySelectorAll('.cnt').forEach(el=>{
const target=parseInt(el.dataset.t);
const suffix=el.dataset.s||'';
const dur=2000; const start=performance.now();
function upd(now){
const p=Math.min((now-start)/dur,1);
const ease=1-Math.pow(1-p,3);
el.textContent=Math.round(ease*target).toLocaleString()+suffix;
if(p<1)requestAnimationFrame(upd);
}
requestAnimationFrame(upd);
});
// years
const yr=document.getElementById('yrs');
const yrDur=1500; const yrStart=performance.now();
function yrUpd(now){
const p=Math.min((now-yrStart)/yrDur,1);
yr.textContent=Math.round(p*8)+'+';
if(p<1)requestAnimationFrame(yrUpd);
}
requestAnimationFrame(yrUpd);
}

// Skill bars
function animateBars(){
document.querySelectorAll('.skill-fill').forEach(el=>{
el.style.width=el.dataset.w+'%';
});
}

window.addEventListener('load',()=>{
setTimeout(animateCounters,200);
setTimeout(animateBars,300);
});
</script>

</body>
</html>
