<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0"/>
<title>Digital Marketing Proposal — Baggbee</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}

:root{
  --ink:#0D1117;
  --ink-mid:#3A4A5C;
  --ink-soft:#6B7A8D;
  --gold:#C8963A;
  --gold-lt:#F7EDD8;
  --cream:#FAFAF7;
  --white:#FFFFFF;
  --rule:#E2E6EA;
  --chip:#EFF3F6;
}

html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}

body{
  font-family:'Inter',sans-serif;
  background:var(--cream);
  color:var(--ink);
  line-height:1.6;
  overflow-x:hidden;
}

/* ── NAV ── */
nav{
  position:fixed;top:0;left:0;right:0;z-index:999;
  background:rgba(13,17,23,0.97);
  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 5vw;height:56px;
  border-bottom:1px solid rgba(200,150,58,0.2);
}
.nav-logo{
  font-family:'JetBrains Mono',monospace;
  font-size:12px;color:var(--gold);letter-spacing:2px;
  white-space:nowrap;
}
.nav-links{display:flex;gap:clamp(16px,3vw,32px)}
.nav-links a{
  font-size:11px;font-weight:500;color:rgba(255,255,255,0.45);
  text-decoration:none;letter-spacing:0.5px;text-transform:uppercase;
  transition:color 0.2s;white-space:nowrap;
}
.nav-links a:hover{color:var(--gold)}
@media(max-width:600px){.nav-links{display:none}}

/* ── HERO ── */
.hero{
  min-height:100svh;
  background:var(--ink);
  display:flex;flex-direction:column;justify-content:flex-end;
  padding:calc(56px + 6vw) 6vw 6vw;
  position:relative;overflow:hidden;
}
.hero-grid{
  position:absolute;inset:0;
  background-image:
    linear-gradient(rgba(200,150,58,0.04) 1px,transparent 1px),
    linear-gradient(90deg,rgba(200,150,58,0.04) 1px,transparent 1px);
  background-size:48px 48px;
  pointer-events:none;
}
.hero-glow{
  position:absolute;top:-20%;right:-10%;
  width:min(600px,80vw);height:min(600px,80vw);border-radius:50%;
  background:radial-gradient(circle,rgba(200,150,58,0.12) 0%,transparent 70%);
  pointer-events:none;
}
.hero-tag{
  font-family:'JetBrains Mono',monospace;
  font-size:11px;color:var(--gold);letter-spacing:3px;
  text-transform:uppercase;margin-bottom:clamp(16px,3vw,28px);
  display:flex;align-items:center;gap:12px;
}
.hero-tag::before{content:'';display:block;width:28px;height:1px;background:var(--gold)}
.hero-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(44px,10vw,96px);
  font-weight:900;line-height:0.95;
  color:var(--white);margin-bottom:clamp(24px,4vw,36px);
}
.hero-title span{color:var(--gold)}
.hero-meta{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(120px,1fr));
  gap:clamp(16px,3vw,32px);
  border-top:1px solid rgba(255,255,255,0.08);
  padding-top:clamp(20px,3vw,32px);
}
.hero-meta-item label{
  display:block;font-size:10px;letter-spacing:2px;
  text-transform:uppercase;color:rgba(255,255,255,0.3);
  margin-bottom:4px;
}
.hero-meta-item p{font-size:clamp(13px,1.5vw,15px);font-weight:600;color:var(--white)}

/* ── SECTIONS ── */
.section{padding:clamp(56px,8vw,96px) clamp(20px,6vw,80px)}
.section.alt{background:var(--white)}
.eyebrow{
  font-family:'JetBrains Mono',monospace;
  font-size:10px;letter-spacing:3px;text-transform:uppercase;
  color:var(--gold);margin-bottom:14px;
  display:flex;align-items:center;gap:10px;
}
.eyebrow::after{content:'';flex:1;max-width:40px;height:1px;background:var(--gold);opacity:0.4}
.section-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(26px,4vw,42px);font-weight:700;
  color:var(--ink);margin-bottom:clamp(32px,5vw,52px);line-height:1.2;
}

/* ── ABOUT ── */
.about-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:clamp(32px,5vw,64px);
  align-items:start;
}
@media(max-width:700px){.about-grid{grid-template-columns:1fr}}
.about-body{font-size:clamp(14px,1.5vw,16px);color:var(--ink-mid);line-height:1.85}
.stats{display:grid;grid-template-columns:1fr 1fr;gap:2px}
.stat{background:var(--ink);padding:clamp(20px,3vw,32px) clamp(16px,2.5vw,28px);position:relative;overflow:hidden}
.stat::before{content:'';position:absolute;top:0;left:0;width:3px;height:100%;background:var(--gold)}
.stat.accent{grid-column:1/-1;background:var(--gold)}
.stat.accent .snum{color:var(--ink)}
.stat.accent .slbl{color:rgba(13,17,23,0.65)}
.snum{font-family:'Playfair Display',serif;font-size:clamp(26px,4vw,36px);font-weight:900;color:var(--white);line-height:1;margin-bottom:5px}
.slbl{font-size:10px;letter-spacing:1px;text-transform:uppercase;color:rgba(255,255,255,0.45);font-weight:500}

/* ── PHASES ── */
.phases{display:flex;flex-direction:column;gap:2px}
.phase{border:1px solid var(--rule);background:var(--white);transition:border-color 0.2s}
.phase:hover{border-color:var(--gold)}
.phase-hd{display:flex;align-items:center;flex-wrap:wrap;gap:12px;padding:clamp(18px,2.5vw,28px) clamp(16px,2.5vw,32px)}
.pnum{font-family:'JetBrains Mono',monospace;font-size:10px;font-weight:600;color:var(--gold);background:var(--gold-lt);padding:4px 10px;border-radius:4px;flex-shrink:0}
.pname{font-size:clamp(13px,1.5vw,16px);font-weight:600;color:var(--ink);flex:1;min-width:140px}
.pbadge{font-size:11px;font-weight:500;color:var(--ink-soft);background:var(--chip);padding:4px 12px;border-radius:20px;white-space:nowrap}
.phase-bd{padding:0 clamp(16px,2.5vw,32px) clamp(18px,2.5vw,28px) clamp(52px,7vw,80px)}
.plist{list-style:none;display:flex;flex-direction:column;gap:8px}
.plist li{font-size:clamp(13px,1.4vw,14px);color:var(--ink-mid);padding-left:20px;position:relative}
.plist li::before{content:'→';position:absolute;left:0;color:var(--gold);font-size:12px}
.pnote{margin-top:14px;padding:12px 16px;background:var(--gold-lt);border-left:3px solid var(--gold);font-size:12px;color:var(--ink-mid);line-height:1.6}

/* ── ROADMAP ── */
.roadmap{position:relative;padding-left:clamp(20px,4vw,0px)}
.rm-track{position:absolute;left:clamp(90px,12vw,100px);top:24px;bottom:24px;width:1px;background:var(--rule)}
@media(max-width:600px){.rm-track{left:16px}}
.rm-item{
  display:grid;
  grid-template-columns:clamp(90px,15vw,200px) 1fr;
  gap:clamp(16px,3vw,32px);
  align-items:start;
  padding:clamp(20px,3vw,32px) 0;
  border-bottom:1px solid var(--rule);
  position:relative;
}
.rm-item:last-child{border-bottom:none}
.rm-item::before{
  content:'';position:absolute;
  left:calc(clamp(90px,15vw,200px) - 4px);
  top:clamp(26px,4vw,40px);
  width:9px;height:9px;border-radius:50%;
  background:var(--gold);border:2px solid var(--cream);
  box-shadow:0 0 0 3px var(--gold-lt);
}
@media(max-width:600px){
  .rm-item{grid-template-columns:1fr;padding-left:36px}
  .rm-item::before{left:8px;top:20px}
  .rm-track{display:none}
}
.rm-label{padding-top:4px;text-align:right;padding-right:clamp(24px,4vw,48px)}
@media(max-width:600px){.rm-label{text-align:left;padding-right:0;padding-left:0}}
.rm-month{font-family:'Playfair Display',serif;font-size:clamp(18px,2.5vw,22px);font-weight:700;color:var(--ink);display:block;margin-bottom:4px}
.rm-focus{font-size:10px;font-weight:600;letter-spacing:1.5px;text-transform:uppercase;color:var(--gold)}
.rm-content h4{font-size:clamp(13px,1.4vw,15px);font-weight:600;color:var(--ink);margin-bottom:12px}
.tags{display:flex;flex-wrap:wrap;gap:8px}
.tag{font-size:11px;padding:5px 10px;border-radius:4px;background:var(--chip);color:var(--ink-mid);font-weight:500}
.tag.g{background:var(--gold-lt);color:var(--gold)}

/* ── WORK ── */
.work-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,280px),1fr));gap:2px}
.wcard{background:var(--white);border:1px solid var(--rule);padding:clamp(24px,3vw,32px);position:relative;overflow:hidden;transition:border-color 0.2s}
.wcard:hover{border-color:var(--gold)}
.wcard.dark{background:var(--ink)}
.wcard::before{content:'';position:absolute;top:0;left:0;width:100%;height:3px;background:var(--gold)}
.wcard-eye{font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:8px}
.wcard-title{font-family:'Playfair Display',serif;font-size:clamp(17px,2vw,20px);font-weight:700;color:var(--ink);margin-bottom:4px}
.wcard.dark .wcard-title{color:var(--white)}
.wcard-sub{font-size:12px;color:var(--ink-soft);margin-bottom:18px}
.wcard.dark .wcard-sub{color:rgba(255,255,255,0.35)}
.wstats{display:flex;gap:16px;margin-bottom:18px;flex-wrap:wrap}
.wstat-num{font-family:'Playfair Display',serif;font-size:clamp(22px,3vw,28px);font-weight:900;color:var(--gold);line-height:1;margin-bottom:4px}
.wstat-lbl{font-size:10px;color:var(--ink-mid);font-weight:600;line-height:1.3}
.wcard.dark .wstat-lbl{color:rgba(255,255,255,0.5)}
.wbody{font-size:clamp(12px,1.3vw,13px);color:var(--ink-mid);line-height:1.75;margin-bottom:16px}
.wcard.dark .wbody{color:rgba(255,255,255,0.6)}
.chips{display:flex;gap:6px;flex-wrap:wrap}
.chip{font-size:11px;padding:4px 10px;background:var(--chip);color:var(--ink-mid);border-radius:4px}
.chip.g{background:rgba(200,150,58,0.15);color:var(--gold)}
.edu-bar{margin-top:2px;background:var(--gold-lt);border:1px solid var(--gold);padding:clamp(16px,2.5vw,24px) clamp(20px,3vw,28px);display:flex;gap:16px;align-items:center}
.edu-bar-icon{font-size:24px;flex-shrink:0}
.edu-bar-title{font-size:11px;font-weight:700;letter-spacing:1px;text-transform:uppercase;color:var(--ink);margin-bottom:4px}
.edu-bar-body{font-size:12px;color:var(--ink-mid);line-height:1.6}

/* ── BUDGET ── */
.budget-hero{
  background:var(--ink);border-radius:4px;
  padding:clamp(28px,4vw,48px);margin-bottom:2px;
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:24px;
  position:relative;overflow:hidden;
}
.budget-hero::after{content:'';position:absolute;right:-40px;top:-40px;width:200px;height:200px;border-radius:50%;background:radial-gradient(circle,rgba(200,150,58,0.15),transparent 70%);pointer-events:none}
.bh-label{font-size:12px;font-weight:400;color:rgba(255,255,255,0.35);letter-spacing:2px;text-transform:uppercase;margin-bottom:8px}
.bh-total{font-family:'Playfair Display',serif;font-size:clamp(44px,8vw,64px);font-weight:900;color:var(--white);line-height:1}
.bh-total sup{color:var(--gold);font-size:0.5em;vertical-align:super}
.bh-right{text-align:right}
@media(max-width:500px){.bh-right{text-align:left}}
.bh-right p{font-size:12px;color:rgba(255,255,255,0.35);margin-bottom:3px}
.bh-right strong{font-size:clamp(15px,2vw,18px);color:var(--gold);display:block}
.bmonths{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,220px),1fr));gap:2px;margin-bottom:clamp(28px,4vw,48px)}
.bm{background:var(--white);border:1px solid var(--rule);padding:clamp(20px,3vw,28px);display:flex;flex-direction:column;transition:border-color 0.2s,transform 0.2s}
.bm:hover{border-color:var(--gold);transform:translateY(-2px)}
.bm-eye{font-family:'JetBrains Mono',monospace;font-size:10px;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:10px}
.bm-scope{font-size:clamp(12px,1.3vw,13px);color:var(--ink-mid);line-height:1.6;margin-bottom:16px;flex:1}
.bm-amt{font-family:'Playfair Display',serif;font-size:clamp(22px,3vw,28px);font-weight:700;color:var(--ink);border-top:1px solid var(--rule);padding-top:14px}

/* ── PAYMENT ── */
.pay-track{position:relative;padding-left:40px}
.pay-track::before{content:'';position:absolute;left:8px;top:12px;bottom:12px;width:1px;background:var(--rule)}
.pay-step{position:relative;padding-bottom:clamp(24px,4vw,40px)}
.pay-step:last-child{padding-bottom:0}
.pay-step::before{content:'';position:absolute;left:-32px;top:4px;width:16px;height:16px;border-radius:50%;background:var(--gold-lt);border:2px solid var(--gold)}
.ps-lbl{font-size:10px;font-weight:600;letter-spacing:2px;text-transform:uppercase;color:var(--ink-soft);margin-bottom:4px}
.ps-amt{font-family:'Playfair Display',serif;font-size:clamp(26px,4vw,32px);font-weight:700;color:var(--ink);margin-bottom:4px}
.ps-when{font-size:clamp(12px,1.3vw,13px);color:var(--ink-mid)}
.excl{margin-top:clamp(28px,4vw,48px);padding:clamp(16px,2.5vw,24px) clamp(18px,3vw,28px);border:1px solid var(--rule);background:var(--chip);display:flex;gap:14px;align-items:flex-start}
.excl-icon{font-size:18px;flex-shrink:0;margin-top:2px}
.excl-title{font-size:11px;font-weight:700;letter-spacing:1px;text-transform:uppercase;color:var(--ink);margin-bottom:5px}
.excl-body{font-size:clamp(12px,1.3vw,13px);color:var(--ink-mid);line-height:1.6}

/* ── EXPECTATIONS ── */
.exp-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,220px),1fr));gap:2px}
.ecard{padding:clamp(24px,3vw,36px);background:var(--white);border:1px solid var(--rule);position:relative;overflow:hidden}
.ecard::before{content:attr(data-m);position:absolute;top:16px;right:20px;font-family:'Playfair Display',serif;font-size:64px;font-weight:900;color:var(--rule);line-height:1;pointer-events:none}
.ecard h4{font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--gold);margin-bottom:10px;position:relative}
.ecard p{font-size:clamp(12px,1.3vw,14px);color:var(--ink-mid);line-height:1.75;position:relative}

/* ── FOOTER ── */
footer{
  background:var(--ink);padding:clamp(40px,6vw,64px) clamp(20px,6vw,80px);
  display:flex;align-items:center;justify-content:space-between;
  flex-wrap:wrap;gap:24px;
  border-top:1px solid rgba(200,150,58,0.2);
}
.ft-title{font-family:'Playfair Display',serif;font-size:clamp(18px,2.5vw,24px);color:var(--white);margin-bottom:5px}
.ft-sub{font-size:12px;color:rgba(255,255,255,0.3)}
.ft-right{font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--gold);letter-spacing:2px;line-height:2.2;text-align:right}
@media(max-width:500px){.ft-right{text-align:left}}

/* ── FADE IN ── */
.fi{opacity:0;transform:translateY(18px);transition:opacity 0.5s ease,transform 0.5s ease}
.fi.on{opacity:1;transform:none}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">BAGGBEE · PROPOSAL</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#roadmap">Roadmap</a>
    <a href="#work">Our Work</a>
    <a href="#budget">Budget</a>
    <a href="#expectations">Expectations</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-tag">Project Proposal — 2026</div>
  <h1 class="hero-title">Digital<br/><span>Marketing</span><br/>Proposal</h1>
  <div class="hero-meta">
    <div class="hero-meta-item">
      <label>Prepared for</label>
      <p>Baggbee, Chennai</p>
    </div>
    <div class="hero-meta-item">
      <label>Prepared by</label>
      <p>Divya &amp; Punam</p>
    </div>
    <div class="hero-meta-item">
      <label>Engagement</label>
      <p>3-Month Plan A</p>
    </div>
    <div class="hero-meta-item">
      <label>Date</label>
      <p>June 2026</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="section alt" id="about">
  <div class="eyebrow">Who we are</div>
  <h2 class="section-title">A team built for brands<br/>starting from zero.</h2>
  <div class="about-grid fi">
    <div>
      <p class="about-body">We are a 2-member digital marketing team — Divya &amp; Punam — specialising in building brands online from scratch. We handle everything end-to-end: strategy, content writing, shooting, editing, posting, and management.<br/><br/>In case of additional shoot requirements, we bring in a freelance shoot specialist on a need basis — only when required. No bloated team. No unnecessary overhead. Just focused, high-quality work.</p>
    </div>
    <div class="stats">
      <div class="stat accent">
        <div class="snum">3-Month</div>
        <div class="slbl">Focused Engagement</div>
      </div>
      <div class="stat">
        <div class="snum">3×</div>
        <div class="slbl">Posts per Week</div>
      </div>
      <div class="stat">
        <div class="snum">E2E</div>
        <div class="slbl">Full Management</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="section" id="services">
  <div class="eyebrow">What we deliver</div>
  <h2 class="section-title">Three phases.<br/>One complete strategy.</h2>
  <div class="phases fi">
    <div class="phase">
      <div class="phase-hd">
        <span class="pnum">PHASE 01</span>
        <span class="pname">Content &amp; Instagram Management</span>
        <span class="pbadge">Month 1 onwards</span>
      </div>
      <div class="phase-bd">
        <ul class="plist">
          <li>Content strategy and planning</li>
          <li>Content writing, shooting, and editing</li>
          <li>3 posts per week — reels, carousels, static posts</li>
          <li>Weekly visit to location for content shoot (twice if needed)</li>
          <li>Posting and account management</li>
          <li>Competitor research and market analysis</li>
          <li>Monthly content calendar</li>
        </ul>
      </div>
    </div>
    <div class="phase">
      <div class="phase-hd">
        <span class="pnum">PHASE 02</span>
        <span class="pname">Amazon Setup &amp; Management</span>
        <span class="pbadge">Month 2 onwards</span>
      </div>
      <div class="phase-bd">
        <ul class="plist">
          <li>Amazon seller account setup</li>
          <li>Product listing creation with descriptions and photos</li>
          <li>Ongoing Amazon account management</li>
        </ul>
        <div class="pnote">All Amazon ad spend and platform fees are paid directly by the client — not included in our fees.</div>
      </div>
    </div>
    <div class="phase">
      <div class="phase-hd">
        <span class="pnum">PHASE 03</span>
        <span class="pname">Meta Ads Management</span>
        <span class="pbadge">Month 3</span>
      </div>
      <div class="phase-bd">
        <ul class="plist">
          <li>Ad strategy and creatives</li>
          <li>Campaign setup, monitoring, and optimisation</li>
          <li>Performance reporting</li>
        </ul>
        <div class="pnote">All Meta ad spend budget is paid directly by the client — not included in our fees.</div>
      </div>
    </div>
  </div>
</section>

<!-- ROADMAP -->
<section class="section alt" id="roadmap">
  <div class="eyebrow">The plan</div>
  <h2 class="section-title">3-Month content roadmap.</h2>
  <div class="roadmap fi">
    <div class="rm-track"></div>
    <div class="rm-item">
      <div class="rm-label">
        <span class="rm-month">Month 1</span>
        <span class="rm-focus">Brand Identity</span>
      </div>
      <div class="rm-content">
        <h4>Establishing who you are before you sell anything.</h4>
        <div class="tags">
          <span class="tag">Company intro (3–4 posts)</span>
          <span class="tag">Product showcase</span>
          <span class="tag g">Legacy story — 40+ years</span>
          <span class="tag">Milestones &amp; achievements</span>
          <span class="tag">80,000 schoolbags milestone</span>
        </div>
      </div>
    </div>
    <div class="rm-item">
      <div class="rm-label">
        <span class="rm-month">Month 2</span>
        <span class="rm-focus">Trust &amp; Engagement</span>
      </div>
      <div class="rm-content">
        <h4>Building an audience that actually cares.</h4>
        <div class="tags">
          <span class="tag">Trending reels</span>
          <span class="tag">Interactive content</span>
          <span class="tag g">Amazon setup begins</span>
          <span class="tag">Brand goals &amp; upcoming plans</span>
          <span class="tag">Customisation offering content</span>
        </div>
      </div>
    </div>
    <div class="rm-item">
      <div class="rm-label">
        <span class="rm-month">Month 3</span>
        <span class="rm-focus">Growth &amp; Revenue</span>
      </div>
      <div class="rm-content">
        <h4>Converting reach into real revenue.</h4>
        <div class="tags">
          <span class="tag g">Meta ads launch</span>
          <span class="tag">Influencer collabs</span>
          <span class="tag g">Amazon retail live</span>
          <span class="tag">Corporate gifting push</span>
          <span class="tag">Wedding customisation</span>
        </div>
      </div>
    </div>
  </div>
  <p style="margin-top:28px;font-size:12px;color:var(--ink-soft);">↗ Throughout all 3 months: trending content, audience engagement, and content calendar run simultaneously.</p>
</section>

<!-- PREVIOUS WORK -->
<section class="section" id="work">
  <div class="eyebrow">Our Work</div>
  <h2 class="section-title">Proven results.<br/>Real brands.</h2>
  <div class="work-grid fi">

    <div class="wcard">
      <div class="wcard-eye">Social Media Management</div>
      <div class="wcard-title">Stalk Marketing &amp; Events</div>
      <div class="wcard-sub">Chennai · 2025–2026 · Divya</div>
      <div class="wstats">
        <div>
          <div class="wstat-num">↑</div>
          <div class="wstat-lbl">Significant Profile<br/>View Growth</div>
        </div>
        <div>
          <div class="wstat-num">AI</div>
          <div class="wstat-lbl">Object-Talking Video<br/>Strategy Adopted</div>
        </div>
      </div>
      <p class="wbody">Managed social media end-to-end for a marketing &amp; events firm. Developed an AI object-talking video content format that the client adopted as a recurring strategy. Drove measurable growth in profile reach and engagement.</p>
      <div class="chips">
        <span class="chip">Content Strategy</span>
        <span class="chip">AI Video</span>
        <span class="chip">Account Management</span>
      </div>
    </div>

    <div class="wcard">
      <div class="wcard-eye">Social Media Research &amp; Strategy</div>
      <div class="wcard-title">Uzi World Digital</div>
      <div class="wcard-sub">Chennai · 2025 · Divya</div>
      <div class="wstats">
        <div>
          <div class="wstat-num">Strat</div>
          <div class="wstat-lbl">Multi-Platform<br/>Strategy</div>
        </div>
        <div>
          <div class="wstat-num">R&amp;D</div>
          <div class="wstat-lbl">Deep Market<br/>Research</div>
        </div>
      </div>
      <p class="wbody">Conducted in-depth social media research and developed platform strategies for a digital marketing agency. Built content frameworks aligned with brand goals and audience behaviour across multiple platforms.</p>
      <div class="chips">
        <span class="chip">Market Research</span>
        <span class="chip">Content Frameworks</span>
        <span class="chip">Multi-Platform</span>
      </div>
    </div>

    <div class="wcard">
      <div class="wcard-eye">Instagram Page Management</div>
      <div class="wcard-title">Empire Weekly <span style="font-size:12px;font-weight:400;color:var(--ink-soft);">by Uzi World Digital</span></div>
      <div class="wcard-sub">Chennai · 2026 · Punam</div>
      <div class="wstats">
        <div>
          <div class="wstat-num">2M</div>
          <div class="wstat-lbl">Months of Full<br/>Page Ownership</div>
        </div>
        <div>
          <div class="wstat-num">E2E</div>
          <div class="wstat-lbl">End-to-End<br/>Management</div>
        </div>
      </div>
      <p class="wbody">Empire Weekly is a worldwide entertainment news page under Uzi World Digital. Punam independently manages the entire Instagram handle — writing captions, designing and editing posts in Canva, and publishing content consistently. Content includes edited story posts covering global entertainment updates.</p>
      <div class="chips">
        <span class="chip">Caption Writing</span>
        <span class="chip">Canva Editing</span>
        <span class="chip">Story Posts</span>
        <span class="chip">Instagram Posting</span>
      </div>
    </div>

    <div class="wcard dark">
      <div class="wcard-eye">A Key Differentiator</div>
      <div class="wcard-title">On-Camera &amp; MC Presence</div>
      <div class="wcard-sub">Live Events · College Audiences · Brand Content</div>
      <p class="wbody">Hosted events for large college audiences and appeared in department Instagram content. In an era where most marketers work only behind the screen — our ability to be on-camera means your brand gets a face, a voice, and energy that audiences connect with.</p>
      <div class="chips">
        <span class="chip g">Event Hosting</span>
        <span class="chip g">Reels &amp; Video</span>
        <span class="chip g">Brand Storytelling</span>
      </div>
    </div>

  </div>
  <div class="edu-bar fi">
    <div class="edu-bar-icon">🎓</div>
    <div>
      <div class="edu-bar-title">Academic &amp; Certification Background</div>
      <div class="edu-bar-body">B.Com Marketing Management · Dwarka Doss Goverdhan Doss Vaishnav College, Chennai (graduating 2027) &nbsp;·&nbsp; Design Thinking Certified &nbsp;·&nbsp; Marketing strategy coursework applied directly to client work.</div>
    </div>
  </div>
</section>

<!-- BUDGET -->
<section class="section alt" id="budget">
  <div class="eyebrow">Investment</div>
  <h2 class="section-title">Transparent pricing.<br/>No surprises.</h2>
  <div class="budget-hero fi">
    <div>
      <div class="bh-label">3-Month Package</div>
      <div class="bh-total"><sup>₹</sup>1,10,000</div>
    </div>
    <div class="bh-right">
      <p>Standard price</p>
      <strong>₹1,35,000</strong>
      <p style="margin-top:10px">You save</p>
      <strong>₹25,000</strong>
    </div>
  </div>
  <div class="bmonths fi">
    <div class="bm">
      <div class="bm-eye">Month 01</div>
      <div class="bm-scope">Instagram Management<br/>Content strategy, writing, shooting, editing &amp; posting — 3 posts/week</div>
      <div class="bm-amt">₹25,000</div>
    </div>
    <div class="bm">
      <div class="bm-eye">Month 02</div>
      <div class="bm-scope">Instagram Management<br/>+ Amazon Setup &amp; Management</div>
      <div class="bm-amt">₹35,000</div>
    </div>
    <div class="bm">
      <div class="bm-eye">Month 03</div>
      <div class="bm-scope">Instagram Management<br/>+ Amazon Management<br/>+ Meta Ads Management</div>
      <div class="bm-amt">₹50,000</div>
    </div>
  </div>

  <h3 style="font-family:'Playfair Display',serif;font-size:clamp(18px,2.5vw,22px);margin-bottom:clamp(20px,3vw,32px);">Payment Schedule</h3>
  <div class="pay-track fi">
    <div class="pay-step">
      <div class="ps-lbl">1st Payment — Advance</div>
      <div class="ps-amt">₹30,000</div>
      <div class="ps-when">Due before the project begins</div>
    </div>
    <div class="pay-step">
      <div class="ps-lbl">2nd Payment</div>
      <div class="ps-amt">₹40,000</div>
      <div class="ps-when">Due mid of Month 2</div>
    </div>
    <div class="pay-step">
      <div class="ps-lbl">3rd &amp; Final Payment</div>
      <div class="ps-amt">₹40,000</div>
      <div class="ps-when">Due after completion of Month 3</div>
    </div>
  </div>
  <div class="excl fi">
    <div class="excl-icon">⚡</div>
    <div>
      <div class="excl-title">Not included in our fees — paid directly by client</div>
      <div class="excl-body">Meta Ads spend budget &nbsp;·&nbsp; Amazon Ads &amp; platform fees &nbsp;·&nbsp; Any additional production costs outside the agreed scope</div>
    </div>
  </div>
</section>

<!-- EXPECTATIONS -->
<section class="section" id="expectations">
  <div class="eyebrow">What to expect</div>
  <h2 class="section-title">Social media is a process,<br/>not an overnight result.</h2>
  <div class="exp-grid fi">
    <div class="ecard" data-m="1">
      <h4>Month 1 — Awareness</h4>
      <p>We focus purely on building awareness. Views and interactions matter more than follower count at this stage. The goal is to make people stop and notice.</p>
    </div>
    <div class="ecard" data-m="2">
      <h4>Month 2 — Audience</h4>
      <p>We focus on growing a real, engaged audience. Followers who care about the brand, not just numbers on a screen. Amazon goes live in parallel.</p>
    </div>
    <div class="ecard" data-m="3">
      <h4>Month 3 — Revenue</h4>
      <p>We start driving actual customer enquiries and revenue. Ads amplify what's already working organically. Performance data shared every month — full transparency.</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div>
    <div class="ft-title">Let's build something great.</div>
    <div class="ft-sub">Divya &amp; Punam · Chennai · June 2026</div>
  </div>
  <div class="ft-right">
    PLAN A · 3 MONTHS<br/>
    ₹1,10,000 PACKAGE<br/>
    INSTAGRAM · AMAZON · META ADS
  </div>
</footer>

<script>
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('on') });
}, {threshold:0.08});
document.querySelectorAll('.fi').forEach(el => obs.observe(el));
</script>
</body>
</html>
