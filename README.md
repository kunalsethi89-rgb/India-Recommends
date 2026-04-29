[index (13).html](https://github.com/user-attachments/files/27194424/index.13.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>India Recommends — Udaipur</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,600&family=Cinzel:wght@400;500;600&family=Lato:wght@300;400&display=swap" rel="stylesheet">
<style>

/* ─────────────────────────────────────
   TOKENS
───────────────────────────────────── */
:root {
  --bone:       #F5F0E8;
  --bone-dk:    #EDE5D8;
  --parchment:  #E8DEC8;
  --ink:        #1A1410;
  --ink70:      rgba(26,20,16,.7);
  --ink60:      rgba(26,20,16,.6);
  --ink30:      rgba(26,20,16,.3);
  --ink10:      rgba(26,20,16,.1);
  --gold:       #B8922C;
  --gold-lt:    #D4AE58;
  --gold-dk:    #8A6A18;
  --gold-pale:  rgba(184,146,44,.1);
  --crimson:    #8B1A1A;
  --teal:       #1A4A4A;
  --rule:       rgba(184,146,44,.25);
  --f-serif:    'Cormorant Garamond', Georgia, serif;
  --f-caps:     'Cinzel', serif;
  --f-body:     'Lato', sans-serif;
  --ease:       cubic-bezier(.22,1,.36,1);
}

*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
html{font-size:16px;scroll-behavior:smooth}
body{background:var(--bone);color:var(--ink);font-family:var(--f-body);font-weight:300;overflow-x:hidden;-webkit-font-smoothing:antialiased}
a{text-decoration:none;color:inherit}
button{font:inherit;cursor:pointer;border:none;background:none}
img{display:block;max-width:100%;height:100%;object-fit:cover}

/* Paper texture */
body::after{content:'';position:fixed;inset:0;z-index:9000;pointer-events:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='300' height='300' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");opacity:.7;mix-blend-mode:multiply}

/* ─────────────────────────────────────
   IMAGE PLACEHOLDER SYSTEM
───────────────────────────────────── */
/*
  HOW TO REPLACE PLACEHOLDERS WITH REAL PHOTOS:
  Each .img-slot has a data-slot attribute.
  Replace the background gradient with:
  background-image: url('your-photo.jpg');
  Or add an <img> tag inside the slot.
*/
.img-slot {
  position: relative;
  overflow: hidden;
  background-color: #2A2018;
}
.img-slot img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 6s var(--ease);
}
.img-slot:hover img { transform: scale(1.03); }

/* Placeholder gradient fills — remove when adding real photos */
.img-slot:not(:has(img))::before {
  content: '';
  position: absolute;
  inset: 0;
}
.img-slot[data-slot="hero"]::before         { background: linear-gradient(160deg,#1A2230 0%,#2A1808 60%,#1A1010 100%); }
.img-slot[data-slot="pichola"]::before      { background: linear-gradient(180deg,#0A1020 0%,#1A2835 40%,#0A1818 100%); }
.img-slot[data-slot="city-palace"]::before  { background: linear-gradient(160deg,#201808 0%,#301A08 60%,#1A1208 100%); }
.img-slot[data-slot="havelis"]::before      { background: linear-gradient(135deg,#180A08 0%,#2A1008 60%,#180808 100%); }
.img-slot[data-slot="culture"]::before      { background: linear-gradient(180deg,#100818 0%,#1A0A28 60%,#0A0818 100%); }
.img-slot[data-slot="ghoomar"]::before      { background: linear-gradient(135deg,#200818 0%,#2A0828 70%,#100818 100%); }
.img-slot[data-slot="miniature"]::before    { background: linear-gradient(160deg,#180808 0%,#2A1008 60%,#180808 100%); }
.img-slot[data-slot="laal-maas"]::before    { background: linear-gradient(180deg,#200808 0%,#301010 60%,#180808 100%); }
.img-slot[data-slot="dal-baati"]::before    { background: linear-gradient(160deg,#201408 0%,#302008 60%,#201408 100%); }
.img-slot[data-slot="thali"]::before        { background: linear-gradient(135deg,#181008 0%,#281808 60%,#181008 100%); }
.img-slot[data-slot="kachori"]::before      { background: linear-gradient(180deg,#1A1008 0%,#2A1808 60%,#1A0808 100%); }
.img-slot[data-slot="gangaur"]::before      { background: linear-gradient(160deg,#180818 0%,#280828 60%,#180818 100%); }
.img-slot[data-slot="diwali"]::before       { background: linear-gradient(180deg,#080808 0%,#1A1008 60%,#080808 100%); }
.img-slot[data-slot="monsoon"]::before      { background: linear-gradient(135deg,#080818 0%,#081828 70%,#080818 100%); }
.img-slot[data-slot="craft"]::before        { background: linear-gradient(160deg,#180808 0%,#281408 60%,#180808 100%); }

/* Photo label overlay — shows slot name, remove when adding real photos */
.img-slot[data-slot]::after {
  content: attr(data-label);
  position: absolute;
  bottom: 0; left: 0; right: 0;
  padding: 10px 14px;
  font-family: var(--f-caps);
  font-size: 8px;
  letter-spacing: .18em;
  color: rgba(245,240,232,.4);
  background: linear-gradient(to top, rgba(26,20,16,.7), transparent);
  pointer-events: none;
  z-index: 2;
}
.img-slot img + .img-caption { display: block; }
.img-slot:not(:has(img))::after { display: block; }

/* Photo icon in centre of empty slots */
.img-placeholder-icon {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%,-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  pointer-events: none;
  z-index: 1;
}
.img-placeholder-icon svg {
  opacity: .18;
}
.img-placeholder-icon span {
  font-family: var(--f-caps);
  font-size: 8px;
  letter-spacing: .18em;
  color: rgba(245,240,232,.25);
  text-align: center;
  max-width: 140px;
  line-height: 1.6;
}

/* ─────────────────────────────────────
   LAYOUT
───────────────────────────────────── */
.wrap    { max-width:1200px; margin:0 auto; padding:0 56px; }
.wrap-sm { max-width:780px;  margin:0 auto; padding:0 56px; }
.wrap-xs { max-width:620px;  margin:0 auto; padding:0 56px; }
.section { padding:120px 0; }

/* ─────────────────────────────────────
   TYPOGRAPHY
───────────────────────────────────── */
.sec-eyebrow { font-family:var(--f-caps); font-size:9px; font-weight:400; letter-spacing:.26em; text-transform:uppercase; color:var(--gold-dk); margin-bottom:14px; }
.sec-title   { font-family:var(--f-serif); font-size:clamp(36px,4.5vw,66px); font-weight:300; letter-spacing:-.01em; line-height:1.1; color:var(--ink); }
.sec-title em{ font-style:italic; color:var(--gold-dk); }
.sec-subtitle{ font-family:var(--f-serif); font-size:20px; font-weight:300; color:var(--ink60); line-height:1.7; margin-top:18px; max-width:560px; margin-left:auto; margin-right:auto; }
.sec-header  { text-align:center; margin-bottom:72px; }
.u-serif     { font-family:var(--f-serif); font-weight:300; }
.gold-rule   { display:block; width:40px; height:1px; background:var(--gold); margin:20px auto; }
.gold-rule-l { display:block; width:40px; height:1px; background:var(--gold); margin:18px 0; }
.ornament    { display:block; text-align:center; color:var(--gold); font-size:18px; letter-spacing:.3em; opacity:.6; margin:12px 0; }

/* ─────────────────────────────────────
   ANIMATIONS
───────────────────────────────────── */
@keyframes fadeUp    { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:none} }
@keyframes fadeIn    { from{opacity:0} to{opacity:1} }
@keyframes ticker    { from{transform:translateX(0)} to{transform:translateX(-50%)} }
@keyframes float     { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-8px)} }
@keyframes rotateCW  { from{transform:rotate(0)} to{transform:rotate(360deg)} }
@keyframes parallaxY { from{transform:translateY(-5%)} to{transform:translateY(5%)} }
@keyframes shimmer   { 0%{opacity:.3} 50%{opacity:.6} 100%{opacity:.3} }

.reveal   { opacity:0; transform:translateY(22px); transition:opacity .9s var(--ease),transform .9s var(--ease); }
.reveal.in{ opacity:1; transform:none; }
.reveal-l { opacity:0; transform:translateX(-18px); transition:opacity .9s var(--ease),transform .9s var(--ease); }
.reveal-l.in{ opacity:1; transform:none; }
.reveal-r { opacity:0; transform:translateX(18px); transition:opacity .9s var(--ease),transform .9s var(--ease); }
.reveal-r.in{ opacity:1; transform:none; }

/* ─────────────────────────────────────
   NAV
───────────────────────────────────── */
.nav {
  position:fixed; top:0; left:0; right:0; z-index:800;
  height:64px; display:flex; align-items:center; justify-content:space-between;
  padding:0 48px;
  background:rgba(245,240,232,.94);
  backdrop-filter:blur(16px) saturate(160%);
  border-bottom:1px solid var(--rule);
  transition:box-shadow .4s;
  animation:fadeIn .6s both;
}
.nav.scrolled { box-shadow:0 2px 32px rgba(26,20,16,.06); }
.nav-logo { font-family:var(--f-caps); font-size:15px; font-weight:600; letter-spacing:.15em; color:var(--ink); }
.nav-links { display:flex; gap:36px; list-style:none; position:absolute; left:50%; transform:translateX(-50%); }
.nav-links a { font-family:var(--f-caps); font-size:9px; letter-spacing:.18em; color:var(--ink60); transition:color .2s; position:relative; padding-bottom:3px; }
.nav-links a::after { content:''; position:absolute; bottom:0; left:0; width:0; height:1px; background:var(--gold); transition:width .3s var(--ease); }
.nav-links a:hover { color:var(--gold-dk); }
.nav-links a:hover::after { width:100%; }
.nav-right { display:flex; align-items:center; gap:20px; }
.nav-admin-link { font-family:var(--f-caps); font-size:9px; letter-spacing:.18em; color:var(--gold-dk); border-bottom:1px solid var(--rule); padding-bottom:2px; cursor:pointer; transition:color .2s,border-color .2s; }
.nav-admin-link:hover { color:var(--gold); border-color:var(--gold); }
.nav-hamburger { display:none; flex-direction:column; gap:6px; padding:4px; }
.nav-hamburger span { display:block; width:22px; height:1px; background:var(--ink); transition:.3s; }
.drawer { position:fixed; inset:0; z-index:790; background:var(--bone); display:flex; flex-direction:column; align-items:center; justify-content:center; gap:32px; transform:translateY(-100%); transition:transform .5s var(--ease); }
.drawer.open { transform:none; }
.drawer-link { font-family:var(--f-caps); font-size:clamp(18px,4vw,28px); letter-spacing:.12em; color:var(--ink30); transition:color .2s; }
.drawer-link:hover { color:var(--ink); }

/* ─────────────────────────────────────
   BUTTONS
───────────────────────────────────── */
.btn { display:inline-flex; align-items:center; gap:10px; font-family:var(--f-caps); font-size:10px; font-weight:500; letter-spacing:.2em; padding:14px 30px; cursor:pointer; transition:all .3s var(--ease); border:none; }
.btn-gold { background:var(--gold-dk); color:var(--bone); }
.btn-gold:hover { background:var(--gold); transform:translateY(-1px); box-shadow:0 8px 24px rgba(184,146,44,.25); }
.btn-outline { background:transparent; color:var(--ink); border:1px solid var(--ink10); }
.btn-outline:hover { border-color:var(--gold-dk); color:var(--gold-dk); }
.btn-sm { padding:9px 18px; font-size:9px; }

/* ─────────────────────────────────────
   HERO — FULL BLEED CINEMATIC
───────────────────────────────────── */
.hero {
  height: 100vh; min-height: 700px;
  position: relative; overflow: hidden;
  display: flex; align-items: flex-end;
}

/* Hero image — replace gradient with real photo */
.hero-bg {
  position: absolute; inset: 0;
}
.hero-bg::before {
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(160deg, #1A2230 0%, #2A1808 50%, #0A0808 100%);
  z-index: 0;
}
/* Replace this comment block with:
   <img src="your-udaipur-photo.jpg" alt="Udaipur Lake Palace at dusk">
   inside .hero-bg
*/
.hero-bg img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover;
  opacity: .65;
}
/* Dark gradient overlay so text reads */
.hero-overlay {
  position: absolute; inset: 0; z-index: 1;
  background: linear-gradient(
    to top,
    rgba(26,20,16,.92) 0%,
    rgba(26,20,16,.45) 45%,
    rgba(26,20,16,.15) 75%,
    transparent 100%
  );
}
.hero-content {
  position: relative; z-index: 2;
  width: 100%; padding: 0 56px 72px;
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 64px; align-items: end;
}
.hero-left {}
.hero-eyebrow {
  font-family: var(--f-caps); font-size: 9px;
  letter-spacing: .3em; color: var(--gold);
  margin-bottom: 20px; animation: fadeUp .8s .1s both;
}
.hero-h1 {
  font-family: var(--f-serif);
  font-size: clamp(48px,7vw,100px);
  font-weight: 300; letter-spacing: -.02em;
  line-height: .97; color: var(--bone);
  margin-bottom: 24px; animation: fadeUp .9s .22s both;
}
.hero-h1 em { font-style: italic; color: var(--gold-lt); }
.hero-tagline {
  font-family: var(--f-serif); font-size: 18px;
  font-style: italic; font-weight: 300;
  color: rgba(245,240,232,.6);
  animation: fadeUp .9s .38s both; margin-bottom: 36px;
}
.hero-btns { display:flex; gap:14px; flex-wrap:wrap; animation:fadeUp .9s .52s both; }

.hero-right { text-align: right; animation: fadeUp .9s .4s both; }
.hero-stats { display: flex; flex-direction: column; gap: 20px; align-items: flex-end; }
.hstat {}
.hstat-n {
  font-family: var(--f-serif); font-size: 40px;
  font-weight: 300; letter-spacing: -.02em;
  color: var(--gold-lt); line-height: 1;
}
.hstat-l {
  font-family: var(--f-caps); font-size: 8px;
  letter-spacing: .18em; color: rgba(245,240,232,.35);
  margin-top: 5px;
}
.hero-scroll {
  position: absolute; bottom: 28px; left: 50%;
  transform: translateX(-50%); z-index: 3;
  display: flex; flex-direction: column; align-items: center; gap: 8px;
  animation: fadeIn .8s 1.4s both;
}
.hero-scroll-label { font-family:var(--f-caps); font-size:8px; letter-spacing:.2em; color:rgba(245,240,232,.3); }
.hero-scroll-line { width:1px; height:32px; background:linear-gradient(to bottom,var(--gold),transparent); animation:float 2s ease-in-out infinite; }

/* Photo swap helper for hero */
.hero-photo-hint {
  position: absolute; top: 20px; left: 50%;
  transform: translateX(-50%); z-index: 5;
  background: rgba(26,20,16,.8); backdrop-filter: blur(8px);
  border: 1px solid var(--rule); padding: 10px 20px;
  font-family: var(--f-caps); font-size: 8px;
  letter-spacing: .14em; color: var(--gold);
  white-space: nowrap; pointer-events: none;
}

/* ─────────────────────────────────────
   TICKER
───────────────────────────────────── */
.ticker { background:var(--ink); padding:12px 0; overflow:hidden; white-space:nowrap; }
.ticker-track { display:inline-flex; animation:ticker 30s linear infinite; }
.ticker-item  { font-family:var(--f-serif); font-size:14px; font-style:italic; color:rgba(245,240,232,.55); padding:0 36px; letter-spacing:.04em; }
.ticker-sep   { color:var(--gold); opacity:.5; }

/* ─────────────────────────────────────
   CINEMATIC STRIP — Udaipur vignettes
───────────────────────────────────── */
.cinematic-strip {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  grid-template-rows: 480px;
  gap: 3px;
}
.cinematic-strip .img-slot { height: 100%; }
.cinematic-strip .img-slot.tall { grid-row: span 1; }

.cine-caption {
  position: absolute; bottom: 0; left: 0; right: 0;
  padding: 40px 28px 24px;
  background: linear-gradient(to top, rgba(26,20,16,.85), transparent);
  z-index: 3;
}
.cine-caption-eye {
  font-family: var(--f-caps); font-size: 8px;
  letter-spacing: .2em; color: var(--gold); margin-bottom: 6px;
}
.cine-caption-title {
  font-family: var(--f-serif); font-size: 22px;
  font-weight: 300; color: var(--bone); line-height: 1.2;
}

/* ─────────────────────────────────────
   THE GAP / VS
───────────────────────────────────── */
.gap-section { background:var(--bone); }
.vs-wrap { display:grid; grid-template-columns:1fr 1px 1fr; gap:0; margin-top:64px; border:1px solid var(--rule); }
.vs-col  { padding:48px 44px; }
.vs-col.them { background:var(--bone-dk); }
.vs-col.us   { background:var(--ink); }
.vs-divider  { background:var(--rule); display:flex; align-items:center; justify-content:center; }
.vs-or { width:36px; height:36px; border:1px solid var(--rule); background:var(--bone); display:flex; align-items:center; justify-content:center; font-family:var(--f-serif); font-size:14px; font-style:italic; color:var(--ink60); }
.vs-label { font-family:var(--f-caps); font-size:9px; letter-spacing:.2em; margin-bottom:28px; }
.vs-col.them .vs-label { color:var(--ink30); }
.vs-col.us   .vs-label { color:var(--gold); }
.vs-item { display:flex; gap:14px; margin-bottom:18px; align-items:flex-start; }
.vs-mark { flex-shrink:0; margin-top:4px; font-size:12px; }
.vs-text { font-family:var(--f-serif); font-size:17px; font-weight:300; line-height:1.5; }
.vs-col.them .vs-text { color:var(--ink30); }
.vs-col.us   .vs-text { color:rgba(245,240,232,.75); }
.vs-col.us   .vs-text strong { color:var(--gold-lt); font-weight:400; }

/* ─────────────────────────────────────
   IR MATCH
───────────────────────────────────── */
.match-section { background:var(--bone-dk); }
.match-layout  { display:grid; grid-template-columns:1fr 1fr; gap:80px; align-items:start; margin-top:64px; }
.match-steps   { display:flex; flex-direction:column; gap:36px; }
.mstep         { display:flex; gap:20px; }
.mstep-n       { width:38px; height:38px; border:1px solid var(--rule); display:flex; align-items:center; justify-content:center; font-family:var(--f-serif); font-size:18px; font-weight:300; color:var(--gold-dk); flex-shrink:0; }
.mstep-title   { font-family:var(--f-serif); font-size:20px; font-weight:400; color:var(--ink); margin-bottom:6px; }
.mstep-desc    { font-family:var(--f-serif); font-size:16px; font-weight:300; color:var(--ink60); line-height:1.6; }
.quiz-shell    { background:var(--ink); border:1px solid rgba(184,146,44,.2); }
.quiz-head     { padding:18px 24px; border-bottom:1px solid rgba(184,146,44,.15); display:flex; align-items:center; justify-content:space-between; }
.quiz-head-title { font-family:var(--f-caps); font-size:9px; letter-spacing:.2em; color:var(--gold); }
.quiz-dots     { display:flex; gap:6px; }
.quiz-dot      { width:8px; height:8px; border-radius:50%; }
.quiz-body     { padding:28px 24px; }
.q-row         { margin-bottom:22px; }
.q-label       { font-family:var(--f-caps); font-size:8px; letter-spacing:.18em; color:rgba(245,240,232,.3); margin-bottom:10px; }
.q-opts        { display:flex; flex-wrap:wrap; gap:7px; }
.qopt          { font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; padding:8px 16px; border:1px solid rgba(184,146,44,.2); color:rgba(245,240,232,.4); cursor:pointer; transition:all .2s; user-select:none; }
.qopt:hover    { border-color:var(--gold); color:var(--gold); }
.qopt.on       { background:var(--gold-dk); border-color:var(--gold-dk); color:var(--bone); }
.quiz-cta      { width:100%; margin-top:8px; padding:14px; background:var(--gold-dk); color:var(--bone); font-family:var(--f-caps); font-size:10px; letter-spacing:.2em; transition:all .25s; }
.quiz-cta:hover{ background:var(--gold); }
.result-shell  { background:var(--ink); margin-top:14px; border:1px solid rgba(184,146,44,.2); display:none; }
.result-shell.show { display:block; animation:fadeUp .5s var(--ease) both; }
.result-head   { padding:22px 24px 18px; border-bottom:2px solid var(--gold-dk); background:linear-gradient(135deg,rgba(26,48,26,.8) 0%,rgba(26,20,16,1) 100%); }
.result-tag    { font-family:var(--f-caps); font-size:8px; letter-spacing:.18em; color:var(--gold); margin-bottom:8px; }
.result-name   { font-family:var(--f-serif); font-size:26px; font-weight:400; color:var(--bone); margin-bottom:10px; }
.result-pill   { display:inline-block; background:var(--gold-dk); color:var(--bone); font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; padding:4px 12px; }
.result-row    { display:grid; grid-template-columns:80px 1fr; border-bottom:1px solid rgba(255,255,255,.05); }
.result-row:last-child { border:none; }
.result-lbl    { padding:12px 12px 12px 16px; font-family:var(--f-caps); font-size:7px; letter-spacing:.14em; color:rgba(245,240,232,.25); border-right:1px solid rgba(255,255,255,.05); }
.result-val    { padding:11px 14px; font-family:var(--f-serif); font-size:15px; font-weight:300; color:rgba(245,240,232,.7); line-height:1.5; }
.result-val strong { color:var(--gold-lt); font-weight:400; }

/* ─────────────────────────────────────
   PILLARS
───────────────────────────────────── */
.pillars-section { background:var(--ink); }
.pillars-section .sec-title { color:var(--bone); }
.pillars-section .sec-eyebrow { color:var(--gold); }
.pillars-section .sec-subtitle { color:rgba(245,240,232,.5); }
.pillars-grid { display:grid; grid-template-columns:repeat(5,1fr); gap:1px; margin-top:64px; background:rgba(255,255,255,.05); border:1px solid rgba(255,255,255,.05); }
.pillar { background:rgba(26,20,16,.95); padding:36px 26px; text-align:center; position:relative; transition:background .3s; cursor:default; }
.pillar::after { content:''; position:absolute; bottom:0; left:0; right:0; height:1px; background:var(--gold); transform:scaleX(0); transition:transform .35s var(--ease); }
.pillar:hover { background:rgba(40,30,20,.9); }
.pillar:hover::after { transform:scaleX(1); }
.pillar-glyph { font-size:26px; margin-bottom:16px; display:block; opacity:.8; }
.pillar-name  { font-family:var(--f-caps); font-size:10px; letter-spacing:.18em; color:var(--bone); margin-bottom:10px; }
.pillar-desc  { font-family:var(--f-serif); font-size:14px; font-weight:300; color:rgba(245,240,232,.4); line-height:1.6; }

/* ─────────────────────────────────────
   SEAL
───────────────────────────────────── */
.seal-section { background:var(--bone-dk); }
.seal-layout  { display:grid; grid-template-columns:1fr 1fr; gap:88px; align-items:center; margin-top:64px; }
.seal-visual  { display:flex; align-items:center; justify-content:center; position:relative; padding:48px; }
.seal-outer-ring,.seal-inner-ring { position:absolute; border-radius:50%; border:1px solid rgba(184,146,44,.2); }
.seal-outer-ring { inset:0; animation:rotateCW 40s linear infinite; }
.seal-inner-ring { inset:28px; border-style:dashed; animation:rotateCW 28s linear infinite reverse; }
.seal-medallion  { width:200px; height:200px; border-radius:50%; border:2px solid rgba(184,146,44,.4); background:radial-gradient(circle,rgba(184,146,44,.06) 0%,transparent 70%); display:flex; flex-direction:column; align-items:center; justify-content:center; box-shadow:0 0 0 10px rgba(184,146,44,.06),0 0 0 20px rgba(184,146,44,.03); position:relative; z-index:1; animation:float 5s ease-in-out infinite; }
.seal-ir   { font-family:var(--f-serif); font-size:56px; font-weight:300; font-style:italic; color:var(--gold-dk); line-height:1; }
.seal-word { font-family:var(--f-caps); font-size:7px; letter-spacing:.3em; color:var(--ink30); margin-top:6px; }
.seal-stars{ color:var(--gold); font-size:12px; margin-top:8px; letter-spacing:4px; }
.seal-promise { font-family:var(--f-serif); font-size:clamp(26px,3vw,42px); font-weight:300; font-style:italic; color:var(--ink); line-height:1.25; margin-bottom:20px; }
.seal-promise strong { font-style:normal; font-weight:400; color:var(--gold-dk); }
.seal-body    { font-family:var(--f-serif); font-size:18px; font-weight:300; color:var(--ink60); line-height:1.75; margin-bottom:36px; }
.seal-nums    { display:flex; gap:36px; margin-bottom:32px; }
.sn-n { font-family:var(--f-serif); font-size:44px; font-weight:300; color:var(--gold-dk); line-height:1; }
.sn-l { font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; color:var(--ink30); margin-top:4px; }
.seal-steps { display:flex; flex-direction:column; gap:16px; }
.ss   { display:flex; gap:14px; align-items:flex-start; }
.ss-n { width:24px; height:24px; border:1px solid var(--rule); flex-shrink:0; display:flex; align-items:center; justify-content:center; font-family:var(--f-caps); font-size:8px; color:var(--gold-dk); margin-top:2px; }
.ss-t { font-family:var(--f-serif); font-size:16px; font-weight:300; color:var(--ink60); line-height:1.5; }
.ss-t strong { color:var(--ink); font-weight:400; }

/* ─────────────────────────────────────
   UDAIPUR BAND — cinematic opener
───────────────────────────────────── */
.udaipur-band { position:relative; min-height:80vh; display:flex; align-items:center; justify-content:center; text-align:center; overflow:hidden; }
.udaipur-band-bg { position:absolute; inset:0; }
.udaipur-band-bg::before { content:''; position:absolute; inset:0; background:linear-gradient(160deg,#0A1020 0%,#1A2835 40%,#0A1010 100%); }
.udaipur-band-bg img { position:absolute; inset:0; width:100%; height:100%; object-fit:cover; opacity:.55; }
.udaipur-band-overlay { position:absolute; inset:0; background:rgba(26,20,16,.55); }
.udaipur-band-content { position:relative; z-index:2; padding:0 24px; }
.udaipur-kicker { display:flex; align-items:center; justify-content:center; gap:16px; font-family:var(--f-caps); font-size:9px; letter-spacing:.28em; color:var(--gold); margin-bottom:24px; }
.udaipur-kicker::before,.udaipur-kicker::after { content:''; width:32px; height:1px; background:rgba(184,146,44,.4); }
.udaipur-main-title { font-family:var(--f-serif); font-size:clamp(56px,11vw,140px); font-weight:300; font-style:italic; letter-spacing:-.02em; line-height:.95; color:var(--bone); margin-bottom:4px; }
.udaipur-sub-title  { font-family:var(--f-caps); font-size:clamp(11px,1.2vw,15px); letter-spacing:.3em; color:rgba(245,240,232,.25); margin-bottom:28px; }
.udaipur-desc  { font-family:var(--f-serif); font-size:18px; font-weight:300; font-style:italic; color:rgba(245,240,232,.55); max-width:540px; margin:0 auto 44px; line-height:1.7; }
.udaipur-chips { display:flex; flex-wrap:wrap; justify-content:center; gap:10px; }
.uchip { font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; padding:8px 18px; border:1px solid rgba(184,146,44,.2); color:rgba(245,240,232,.4); cursor:default; transition:all .25s; }
.uchip:hover { border-color:var(--gold); color:var(--gold); }
.uchip span  { color:var(--gold); margin-right:4px; }

/* ─────────────────────────────────────
   HISTORY
───────────────────────────────────── */
.history-section { background:var(--bone); }
.history-layout  { display:grid; grid-template-columns:1fr 1fr; gap:88px; align-items:start; margin-top:64px; }
.palace-frame    { position:relative; aspect-ratio:4/5; overflow:hidden; border:1px solid var(--rule); }
.palace-frame .img-slot { position:absolute; inset:0; }
.palace-frame .img-slot::before { background:linear-gradient(160deg,#201808 0%,#301A08 60%,#1A1208 100%); }
.palace-overlay  { position:absolute; inset:0; z-index:2; background:linear-gradient(to top,rgba(26,20,16,.7) 0%,transparent 50%); }
.palace-year     { position:absolute; top:20px; right:20px; z-index:3; background:var(--gold-dk); color:var(--bone); font-family:var(--f-serif); font-size:15px; font-style:italic; font-weight:300; padding:8px 16px; }
.palace-quote    { position:absolute; bottom:20px; left:20px; right:20px; z-index:3; background:rgba(26,20,16,.82); backdrop-filter:blur(8px); border:1px solid rgba(184,146,44,.2); padding:16px 18px; }
.palace-quote-text { font-family:var(--f-serif); font-size:14px; font-style:italic; color:rgba(245,240,232,.75); line-height:1.5; margin-bottom:6px; }
.palace-quote-attr { font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; color:var(--gold); }
.timeline  { display:flex; flex-direction:column; gap:0; }
.tl-item   { display:flex; gap:20px; padding-bottom:32px; position:relative; }
.tl-item:last-child { padding-bottom:0; }
.tl-left   { display:flex; flex-direction:column; align-items:center; flex-shrink:0; }
.tl-dot    { width:36px; height:36px; border:1px solid var(--rule); background:var(--bone-dk); display:flex; align-items:center; justify-content:center; font-size:14px; transition:all .3s; }
.tl-item:hover .tl-dot { border-color:var(--gold); background:var(--gold-pale); }
.tl-line   { width:1px; flex:1; background:var(--rule); margin-top:8px; }
.tl-year   { font-family:var(--f-serif); font-size:14px; font-style:italic; color:var(--gold-dk); margin-bottom:4px; }
.tl-title  { font-family:var(--f-serif); font-size:20px; font-weight:400; color:var(--ink); margin-bottom:6px; }
.tl-desc   { font-family:var(--f-serif); font-size:15px; font-weight:300; color:var(--ink60); line-height:1.65; }

/* ─────────────────────────────────────
   CULTURE
───────────────────────────────────── */
.culture-section { background:var(--bone-dk); }

/* Culture photo row — 3 images side by side */
.culture-photo-row {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 3px;
  height: 380px;
  margin-bottom: 3px;
}
.culture-photo-row .img-slot { height: 100%; position: relative; }

.culture-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:var(--rule); border:1px solid var(--rule); margin-top:3px; }
.cult-card { background:var(--bone); padding:36px 30px; position:relative; overflow:hidden; cursor:default; transition:background .3s; }
.cult-card.wide { grid-column:1/-1; display:grid; grid-template-columns:1fr 1fr; gap:48px; align-items:center; padding:40px; }
.cult-card:hover { background:var(--parchment); }
.cult-card::after { content:''; position:absolute; top:0; left:0; right:0; height:1px; background:var(--gold); transform:scaleX(0); transition:transform .35s var(--ease); }
.cult-card:hover::after { transform:scaleX(1); }
.cult-bg-char { position:absolute; font-family:var(--f-serif); font-size:120px; font-style:italic; color:rgba(26,20,16,.03); right:10px; top:0; line-height:1; pointer-events:none; }
.cult-icon  { font-size:28px; margin-bottom:18px; display:block; }
.cult-cat   { font-family:var(--f-caps); font-size:8px; letter-spacing:.2em; color:var(--gold-dk); margin-bottom:10px; }
.cult-title { font-family:var(--f-serif); font-size:22px; font-weight:400; color:var(--ink); margin-bottom:10px; }
.cult-desc  { font-family:var(--f-serif); font-size:15px; font-weight:300; color:var(--ink60); line-height:1.7; }
.cult-tags  { display:flex; flex-wrap:wrap; gap:7px; margin-top:14px; }
.cult-tag   { font-family:var(--f-caps); font-size:7px; letter-spacing:.1em; color:var(--ink30); border:1px solid var(--rule); padding:4px 10px; }

/* ─────────────────────────────────────
   FOOD — full photo treatment
───────────────────────────────────── */
.food-section { background:var(--ink); }
.food-section .sec-title    { color:var(--bone); }
.food-section .sec-eyebrow  { color:var(--gold); }
.food-section .sec-subtitle { color:rgba(245,240,232,.45); }
.food-header-layout { display:grid; grid-template-columns:1fr 1fr; gap:64px; align-items:end; margin-bottom:56px; }
.food-intro { font-family:var(--f-serif); font-size:17px; font-weight:300; color:rgba(245,240,232,.5); line-height:1.8; }

/* Food photo bento */
.food-bento {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 320px 240px;
  gap: 3px;
}
.food-bento-item {
  position: relative;
  overflow: hidden;
}
.food-bento-item.span2 { grid-column: span 2; }
.food-bento-item .img-slot { position:absolute; inset:0; height:100%; }
.food-bento-overlay {
  position: absolute; inset: 0; z-index: 2;
  background: linear-gradient(to top, rgba(26,20,16,.88) 0%, rgba(26,20,16,.2) 60%, transparent 100%);
}
.food-bento-label {
  position: absolute; bottom: 0; left: 0; right: 0;
  padding: 28px 22px 20px; z-index: 3;
}
.food-bento-cat  { font-family:var(--f-caps); font-size:8px; letter-spacing:.18em; color:var(--gold); margin-bottom:5px; }
.food-bento-name { font-family:var(--f-serif); font-size:22px; font-weight:300; color:var(--bone); margin-bottom:5px; }
.food-bento-desc { font-family:var(--f-serif); font-size:14px; font-style:italic; font-weight:300; color:rgba(245,240,232,.55); line-height:1.4; }
.food-heat-row   { display:flex; align-items:center; gap:3px; margin-top:8px; }
.fheat { width:6px; height:6px; border-radius:50%; background:rgba(255,255,255,.15); }
.fheat.on { background:var(--gold-lt); }

/* Thali feature */
.food-feature {
  margin-top: 3px;
  background: rgba(184,146,44,.06);
  border: 1px solid rgba(184,146,44,.15);
  padding: 40px;
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 48px; align-items: center;
}
.food-feat-num   { font-family:var(--f-serif); font-size:100px; font-weight:300; font-style:italic; color:rgba(184,146,44,.12); text-align:center; line-height:1; }
.food-feat-title { font-family:var(--f-serif); font-size:24px; font-weight:400; color:var(--bone); margin-bottom:10px; }
.food-feat-desc  { font-family:var(--f-serif); font-size:15px; font-weight:300; color:rgba(245,240,232,.5); line-height:1.75; }
.food-must       { display:flex; flex-wrap:wrap; gap:7px; margin-top:16px; }
.food-must-item  { font-family:var(--f-caps); font-size:7px; letter-spacing:.1em; color:var(--gold); border:1px solid rgba(184,146,44,.25); padding:5px 13px; }

/* ─────────────────────────────────────
   TRADITION
───────────────────────────────────── */
.tradition-section { background:var(--bone); }
.tradition-intro-txt { font-family:var(--f-serif); font-size:18px; font-weight:300; color:var(--ink60); line-height:1.75; text-align:center; max-width:580px; margin:16px auto 0; }

/* Festival photo grid */
.festival-photo-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 340px 240px;
  gap: 3px;
  margin-bottom: 48px;
}
.festival-photo-grid .img-slot { height:100%; }
.festival-photo-grid .img-slot.tall { grid-row:span 2; }

/* Horizontal scroll strip */
.strip-outer { overflow:hidden; margin:0 -56px; padding:0 56px; }
.strip        { display:flex; gap:14px; overflow-x:auto; padding-bottom:20px; scroll-snap-type:x mandatory; -webkit-overflow-scrolling:touch; scrollbar-width:thin; scrollbar-color:var(--rule) transparent; }
.strip::-webkit-scrollbar { height:3px; }
.strip::-webkit-scrollbar-thumb { background:var(--rule); }
.fest-card    { min-width:280px; background:var(--bone-dk); border:1px solid var(--rule); padding:28px 24px; flex-shrink:0; scroll-snap-align:start; transition:border-color .3s,transform .3s; cursor:default; position:relative; }
.fest-card::after { content:''; position:absolute; bottom:0; left:0; right:0; height:1px; background:var(--gold); transform:scaleX(0); transition:transform .3s var(--ease); }
.fest-card:hover { border-color:var(--gold-dk); transform:translateY(-3px); }
.fest-card:hover::after { transform:scaleX(1); }
.fest-icon    { font-size:36px; margin-bottom:14px; display:block; }
.fest-season  { font-family:var(--f-caps); font-size:8px; letter-spacing:.18em; color:var(--gold-dk); margin-bottom:8px; }
.fest-name    { font-family:var(--f-serif); font-size:20px; font-weight:400; color:var(--ink); margin-bottom:8px; }
.fest-desc    { font-family:var(--f-serif); font-size:14px; font-weight:300; color:var(--ink60); line-height:1.6; margin-bottom:14px; }
.fest-when    { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; color:var(--ink30); display:flex; align-items:center; gap:6px; }
.fest-when::before { content:''; width:5px; height:5px; border-radius:50%; background:var(--gold); flex-shrink:0; }
.strip-dots   { display:flex; justify-content:center; gap:7px; margin-top:20px; }
.sdot         { width:6px; height:6px; border-radius:50%; background:var(--rule); cursor:pointer; transition:all .2s; }
.sdot.active  { background:var(--gold); width:20px; border-radius:3px; }

/* Crafts */
.crafts-grid  { display:grid; grid-template-columns:repeat(6,1fr); gap:1px; margin-top:48px; background:var(--rule); border:1px solid var(--rule); }
.craft-cell   { background:var(--bone-dk); padding:24px 16px; text-align:center; transition:background .3s; }
.craft-cell:hover { background:var(--parchment); }
.craft-emoji  { font-size:26px; margin-bottom:10px; display:block; }
.craft-name   { font-family:var(--f-serif); font-size:14px; font-weight:400; color:var(--ink); margin-bottom:4px; }
.craft-note   { font-family:var(--f-caps); font-size:7px; letter-spacing:.1em; color:var(--ink30); }

/* ─────────────────────────────────────
   GUIDE
───────────────────────────────────── */
.guide-section { background:var(--bone-dk); }
.guide-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1px; margin-top:64px; background:var(--rule); border:1px solid var(--rule); }
.g-card     { background:var(--bone); padding:30px 26px; position:relative; transition:background .3s; cursor:default; }
.g-card:hover { background:var(--parchment); }
.g-card::after { content:''; position:absolute; top:0; left:0; right:0; height:1px; background:var(--gold); transform:scaleX(0); transition:transform .35s var(--ease); }
.g-card:hover::after { transform:scaleX(1); }
.g-seal-mark { position:absolute; top:16px; right:16px; font-family:var(--f-serif); font-size:11px; font-style:italic; color:var(--gold-dk); border:1px solid var(--rule); padding:3px 9px; }
.g-cat    { font-family:var(--f-caps); font-size:8px; letter-spacing:.2em; color:var(--gold-dk); margin-bottom:8px; }
.g-name   { font-family:var(--f-serif); font-size:22px; font-weight:400; color:var(--ink); margin-bottom:8px; }
.g-desc   { font-family:var(--f-serif); font-size:15px; font-weight:300; color:var(--ink60); line-height:1.6; margin-bottom:18px; }
.g-meta   { display:flex; align-items:center; justify-content:space-between; }
.g-score  { font-family:var(--f-serif); font-size:14px; color:var(--gold-dk); display:flex; align-items:center; gap:8px; }
.g-bar    { width:48px; height:2px; background:var(--rule); overflow:hidden; }
.g-bar-fill { height:100%; background:var(--gold); }
.g-tag    { font-family:var(--f-caps); font-size:8px; letter-spacing:.08em; color:var(--ink30); }
.g-cta-card  { background:var(--ink); cursor:pointer; display:flex; flex-direction:column; justify-content:center; }
.g-cta-card:hover { background:rgba(40,30,20,.95); }
.g-cta-cat   { font-family:var(--f-caps); font-size:8px; letter-spacing:.2em; color:var(--gold); margin-bottom:12px; }
.g-cta-title { font-family:var(--f-serif); font-size:24px; font-weight:300; font-style:italic; color:var(--bone); line-height:1.2; margin-bottom:14px; }
.g-cta-sub   { font-family:var(--f-serif); font-size:14px; font-weight:300; color:rgba(245,240,232,.4); line-height:1.5; }

/* ─────────────────────────────────────
   MANIFESTO
───────────────────────────────────── */
.manifesto-section { background:var(--gold-dk); padding:120px 0; text-align:center; position:relative; overflow:hidden; }
.manifesto-section::before { content:'IR'; position:absolute; font-family:var(--f-serif); font-size:clamp(180px,28vw,340px); font-style:italic; font-weight:300; color:rgba(26,20,16,.06); top:50%; left:50%; transform:translate(-50%,-50%); pointer-events:none; line-height:1; }
.manifesto-quote { font-family:var(--f-serif); font-size:clamp(20px,3vw,44px); font-weight:300; font-style:italic; color:rgba(245,240,232,.92); line-height:1.3; max-width:860px; margin:0 auto 20px; position:relative; }
.manifesto-attr  { font-family:var(--f-caps); font-size:9px; letter-spacing:.24em; color:rgba(245,240,232,.45); position:relative; }

/* ─────────────────────────────────────
   PARTNER
───────────────────────────────────── */
.partner-section { background:var(--bone); }
.partner-layout  { display:grid; grid-template-columns:1fr 1fr; gap:64px; align-items:start; margin-top:64px; }
.partner-intro   { font-family:var(--f-serif); font-size:17px; font-weight:300; color:var(--ink60); line-height:1.8; margin-bottom:24px; }
.partner-perks   { display:flex; flex-direction:column; gap:13px; }
.perk      { display:flex; gap:12px; align-items:flex-start; }
.perk-mark { width:16px; height:16px; flex-shrink:0; border:1px solid var(--rule); display:flex; align-items:center; justify-content:center; font-size:8px; color:var(--gold-dk); margin-top:3px; }
.perk-text { font-family:var(--f-serif); font-size:16px; font-weight:300; color:var(--ink60); line-height:1.5; }
.partner-form { border:1px solid var(--rule); padding:36px; background:var(--bone-dk); }
.form-title   { font-family:var(--f-serif); font-size:24px; font-weight:400; color:var(--ink); margin-bottom:28px; }
.fl { display:block; font-family:var(--f-caps); font-size:8px; letter-spacing:.16em; color:var(--ink30); margin-bottom:7px; }
.fi,.fs { width:100%; background:var(--bone); border:1px solid var(--rule); color:var(--ink); font-family:var(--f-serif); font-size:15px; font-weight:300; padding:11px 13px; outline:none; margin-bottom:16px; transition:border-color .2s; }
.fi::placeholder { color:var(--ink30); }
.fi:focus,.fs:focus { border-color:var(--gold-dk); }
.fs { cursor:pointer; }

/* ─────────────────────────────────────
   FOOTER
───────────────────────────────────── */
.footer { background:var(--ink); padding:72px 56px 44px; }
.footer-grid { display:grid; grid-template-columns:2fr 1fr 1fr 1fr; gap:48px; max-width:1200px; margin:0 auto; padding-bottom:48px; border-bottom:1px solid rgba(255,255,255,.07); margin-bottom:28px; }
.f-logo     { font-family:var(--f-caps); font-size:14px; letter-spacing:.16em; color:var(--bone); margin-bottom:12px; }
.f-tagline  { font-family:var(--f-serif); font-size:15px; font-style:italic; color:rgba(245,240,232,.3); line-height:1.6; max-width:240px; }
.f-col-title{ font-family:var(--f-caps); font-size:8px; letter-spacing:.22em; color:var(--gold); margin-bottom:18px; }
.f-links    { list-style:none; display:flex; flex-direction:column; gap:9px; }
.f-links a  { font-family:var(--f-serif); font-size:14px; font-weight:300; color:rgba(245,240,232,.3); transition:color .2s; }
.f-links a:hover { color:var(--bone); }
.footer-bottom { max-width:1200px; margin:0 auto; display:flex; align-items:center; justify-content:space-between; }
.f-copy { font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; color:rgba(245,240,232,.18); }
.f-made { font-family:var(--f-serif); font-size:13px; font-style:italic; color:rgba(184,146,44,.4); }

/* ─────────────────────────────────────
   PHOTO GUIDE PANEL
───────────────────────────────────── */
.photo-guide {
  position: fixed;
  top: 80px; right: 20px;
  z-index: 700;
  width: 260px;
  background: rgba(26,20,16,.96);
  backdrop-filter: blur(12px);
  border: 1px solid var(--rule);
  padding: 0;
  transform: translateX(290px);
  transition: transform .4s var(--ease);
  font-family: var(--f-caps);
}
.photo-guide.open { transform: none; }
.photo-guide-head {
  padding: 14px 18px;
  border-bottom: 1px solid rgba(184,146,44,.15);
  display: flex; align-items: center; justify-content: space-between;
}
.photo-guide-title { font-size: 9px; letter-spacing: .18em; color: var(--gold); }
.photo-guide-close { font-size: 14px; color: rgba(245,240,232,.3); cursor: pointer; transition: color .2s; }
.photo-guide-close:hover { color: var(--bone); }
.photo-guide-body { padding: 16px 18px; }
.photo-guide-intro { font-family: var(--f-serif); font-size: 13px; font-style: italic; color: rgba(245,240,232,.4); line-height: 1.5; margin-bottom: 14px; }
.photo-slot-list { display: flex; flex-direction: column; gap: 8px; }
.photo-slot-item { display: flex; gap: 10px; align-items: center; }
.photo-slot-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--gold-dk); flex-shrink: 0; }
.photo-slot-name { font-size: 8px; letter-spacing: .12em; color: rgba(245,240,232,.4); }
.photo-guide-toggle {
  position: fixed;
  top: 80px; right: 20px; z-index: 701;
  background: var(--gold-dk);
  color: var(--bone);
  font-family: var(--f-caps); font-size: 8px;
  letter-spacing: .14em; padding: 8px 14px;
  cursor: pointer; transition: all .2s;
  border: none;
  display: flex; align-items: center; gap: 6px;
}
.photo-guide-toggle:hover { background: var(--gold); }

/* ─────────────────────────────────────
   ADMIN GATE
───────────────────────────────────── */
.gate { position:fixed; inset:0; z-index:9500; background:rgba(26,20,16,.96); backdrop-filter:blur(20px); display:flex; align-items:center; justify-content:center; opacity:0; pointer-events:none; transition:opacity .35s var(--ease); }
.gate.open { opacity:1; pointer-events:all; }
.gate-card { background:var(--bone); border:1px solid var(--rule); padding:52px 56px; width:100%; max-width:420px; text-align:center; transform:translateY(12px); transition:transform .4s var(--ease); }
.gate.open .gate-card { transform:none; }
.gate-logo { font-family:var(--f-caps); font-size:14px; letter-spacing:.2em; color:var(--ink); margin-bottom:4px; }
.gate-sub  { font-family:var(--f-serif); font-size:14px; font-style:italic; color:var(--ink30); margin-bottom:36px; }
.gate-input{ width:100%; background:var(--bone-dk); border:1px solid var(--rule); color:var(--ink); font-family:var(--f-serif); font-size:16px; font-weight:300; padding:13px 16px; outline:none; margin-bottom:14px; text-align:center; letter-spacing:.12em; transition:border-color .2s; }
.gate-input:focus { border-color:var(--gold-dk); }
.gate-error{ font-family:var(--f-serif); font-size:13px; font-style:italic; color:var(--crimson); opacity:0; transition:opacity .2s; min-height:18px; margin-top:8px; }
.gate-error.show { opacity:1; }
.gate-hint { font-family:var(--f-serif); font-size:13px; font-style:italic; color:var(--ink30); margin-top:14px; }

/* ─────────────────────────────────────
   ADMIN SHELL
───────────────────────────────────── */
#admShell { position:fixed; inset:0; z-index:9400; background:var(--bone); display:none; }
#admShell.open { display:flex; animation:fadeIn .3s both; }
.adm-sb { width:236px; flex-shrink:0; background:var(--ink); border-right:1px solid rgba(255,255,255,.07); display:flex; flex-direction:column; overflow-y:auto; }
.adm-sb-logo { padding:24px 22px 20px; border-bottom:1px solid rgba(255,255,255,.07); }
.adm-sb-logo-name { font-family:var(--f-caps); font-size:13px; letter-spacing:.2em; color:var(--bone); }
.adm-sb-logo-sub  { font-family:var(--f-serif); font-size:12px; font-style:italic; color:rgba(245,240,232,.25); margin-top:4px; }
.adm-nav    { padding:14px 0; flex:1; }
.adm-sec-label { font-family:var(--f-caps); font-size:7px; letter-spacing:.22em; color:rgba(245,240,232,.2); padding:10px 20px 6px; }
.adm-ni     { display:flex; align-items:center; gap:10px; padding:10px 20px; font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; color:rgba(245,240,232,.4); cursor:pointer; transition:all .2s; border-left:1px solid transparent; user-select:none; }
.adm-ni:hover { color:var(--bone); background:rgba(255,255,255,.03); }
.adm-ni.active{ color:var(--bone); background:rgba(255,255,255,.05); border-left-color:var(--gold); }
.adm-ni-ico { font-size:13px; width:17px; text-align:center; flex-shrink:0; }
.adm-badge  { margin-left:auto; background:var(--gold-dk); color:var(--bone); font-size:9px; font-weight:700; padding:2px 7px; }
.adm-sb-foot { padding:18px 20px; border-top:1px solid rgba(255,255,255,.07); display:flex; align-items:center; gap:10px; }
.adm-avatar  { width:28px; height:28px; border:1px solid rgba(184,146,44,.3); display:flex; align-items:center; justify-content:center; font-family:var(--f-serif); font-size:12px; font-style:italic; color:var(--gold); flex-shrink:0; }
.adm-user-name { font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; color:rgba(245,240,232,.5); }
.adm-user-role { font-family:var(--f-serif); font-size:11px; font-style:italic; color:rgba(245,240,232,.25); margin-top:2px; }
.adm-exit-btn  { margin-left:auto; font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; color:rgba(245,240,232,.25); cursor:pointer; transition:color .2s; }
.adm-exit-btn:hover { color:var(--bone); }
.adm-main    { flex:1; display:flex; flex-direction:column; overflow:hidden; }
.adm-topbar  { height:56px; background:var(--bone-dk); border-bottom:1px solid var(--rule); display:flex; align-items:center; padding:0 28px; gap:14px; flex-shrink:0; }
.adm-topbar-title { font-family:var(--f-serif); font-size:18px; font-weight:400; font-style:italic; color:var(--ink); }
.adm-topbar-city  { font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; color:var(--ink30); border:1px solid var(--rule); padding:4px 12px; }
.adm-topbar-actions { margin-left:auto; display:flex; gap:8px; }
.adm-content { flex:1; overflow-y:auto; padding:28px; background:var(--bone); }
.adm-stats   { display:grid; grid-template-columns:repeat(5,1fr); gap:10px; margin-bottom:22px; }
.adm-stat    { background:var(--bone-dk); border:1px solid var(--rule); padding:16px 18px; transition:border-color .2s; }
.adm-stat:hover { border-color:var(--gold); }
.adm-stat-n  { font-family:var(--f-serif); font-size:30px; font-weight:300; line-height:1; color:var(--ink); }
.adm-stat-n.gold  { color:var(--gold-dk); }
.adm-stat-n.teal  { color:var(--teal); }
.adm-stat-n.muted { color:var(--ink30); }
.adm-stat-l  { font-family:var(--f-caps); font-size:8px; letter-spacing:.12em; color:var(--ink30); margin-top:6px; }
.adm-panel   { background:var(--bone-dk); border:1px solid var(--rule); overflow:hidden; margin-bottom:18px; }
.adm-ph      { padding:14px 20px; border-bottom:1px solid var(--rule); display:flex; align-items:center; gap:12px; }
.adm-ph-title{ font-family:var(--f-serif); font-size:16px; font-weight:400; font-style:italic; color:var(--ink); }
.adm-ph-sub  { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; color:var(--ink30); }
.adm-ph-actions { margin-left:auto; display:flex; gap:7px; }
.adm-view    { display:none; }
.adm-view.active { display:block; }
.adm-tbl     { width:100%; border-collapse:collapse; }
.adm-tbl th  { font-family:var(--f-caps); font-size:8px; letter-spacing:.16em; color:var(--ink30); text-align:left; padding:11px 14px; border-bottom:1px solid var(--rule); background:var(--bone); }
.adm-tbl td  { padding:12px 14px; border-bottom:1px solid rgba(26,20,16,.05); vertical-align:middle; }
.adm-tbl tr:last-child td { border:none; }
.adm-tbl tr:hover td { background:var(--bone); }
.tp-name { font-family:var(--f-serif); font-size:15px; font-weight:400; color:var(--ink); }
.tp-cat  { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; color:var(--ink30); margin-top:2px; }
.t-trust { display:flex; align-items:center; gap:8px; }
.t-trust-n   { font-family:var(--f-serif); font-size:14px; width:24px; }
.t-trust-bar { width:60px; height:2px; background:var(--rule); overflow:hidden; }
.t-trust-fill{ height:100%; background:var(--gold); }
.tag-seal-y  { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; border:1px solid rgba(184,146,44,.3); color:var(--gold-dk); padding:3px 8px; }
.tag-seal-n  { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; color:var(--ink30); border:1px solid var(--rule); padding:3px 8px; }
.st-live     { font-family:var(--f-caps); font-size:8px; letter-spacing:.08em; color:var(--teal); border:1px solid rgba(26,74,74,.2); padding:3px 8px; }
.st-draft    { font-family:var(--f-caps); font-size:8px; letter-spacing:.08em; color:var(--gold-dk); border:1px solid var(--rule); padding:3px 8px; }
.tbl-acts    { display:flex; gap:5px; }
.tbl-btn     { width:26px; height:26px; border:1px solid var(--rule); background:transparent; color:var(--ink30); display:flex; align-items:center; justify-content:center; font-size:11px; cursor:pointer; transition:all .18s; }
.tbl-btn:hover     { border-color:var(--gold-dk); color:var(--gold-dk); }
.tbl-btn.del:hover { border-color:var(--crimson); color:var(--crimson); }
.empty-state { text-align:center; padding:52px 24px; font-family:var(--f-serif); font-style:italic; font-size:18px; color:var(--ink30); }
.adm-search  { display:flex; align-items:center; gap:8px; background:var(--bone); border:1px solid var(--rule); padding:7px 12px; transition:border-color .2s; }
.adm-search:focus-within { border-color:var(--gold-dk); }
.adm-si      { background:none; border:none; outline:none; font-family:var(--f-serif); font-size:14px; font-weight:300; color:var(--ink); width:160px; }
.adm-si::placeholder { color:var(--ink30); }
.form-cols   { display:grid; grid-template-columns:1fr 1fr; }
.form-col    { padding:26px 28px; border-right:1px solid var(--rule); }
.form-col:last-child { border:none; }
.fs-title    { font-family:var(--f-caps); font-size:8px; letter-spacing:.2em; color:var(--gold-dk); margin-bottom:16px; display:flex; align-items:center; gap:10px; }
.fs-title::after { content:''; flex:1; height:1px; background:var(--rule); }
.frow        { margin-bottom:14px; }
.f-lbl       { display:block; font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; color:var(--ink30); margin-bottom:6px; }
.f-lbl .req  { color:var(--gold-dk); }
.f-in,.f-sel,.f-ta { width:100%; background:var(--bone); border:1px solid var(--rule); color:var(--ink); font-family:var(--f-serif); font-size:14px; font-weight:300; padding:9px 12px; outline:none; transition:border-color .2s; }
.f-in::placeholder,.f-ta::placeholder { color:var(--ink30); }
.f-in:focus,.f-sel:focus,.f-ta:focus { border-color:var(--gold-dk); }
.f-ta  { resize:vertical; min-height:68px; line-height:1.5; }
.f-sel { cursor:pointer; }
.tog-grid { display:grid; grid-template-columns:1fr 1fr; gap:7px; }
.tog  { display:flex; align-items:center; gap:8px; padding:8px 10px; border:1px solid var(--rule); cursor:pointer; transition:all .18s; user-select:none; background:var(--bone-dk); }
.tog.on { background:var(--gold-pale); border-color:rgba(184,146,44,.3); }
.tog-tr { width:24px; height:13px; background:var(--rule); position:relative; transition:background .18s; flex-shrink:0; }
.tog-tr::after { content:''; position:absolute; width:9px; height:9px; background:rgba(26,20,16,.3); top:2px; left:2px; transition:all .18s; }
.tog.on .tog-tr { background:var(--gold-dk); }
.tog.on .tog-tr::after { left:13px; background:var(--bone); }
.tog-l { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; color:var(--ink60); }
.tog.on .tog-l { color:var(--gold-dk); }
.sl-row { display:flex; align-items:center; gap:11px; margin-bottom:10px; }
.sl-l   { font-family:var(--f-serif); font-size:13px; font-weight:300; color:var(--ink60); width:95px; flex-shrink:0; }
.f-sl   { flex:1; -webkit-appearance:none; height:2px; background:var(--rule); outline:none; cursor:pointer; }
.f-sl::-webkit-slider-thumb { -webkit-appearance:none; width:13px; height:13px; background:var(--gold-dk); cursor:pointer; transition:transform .15s; }
.f-sl::-webkit-slider-thumb:hover { transform:scale(1.3); }
.sl-v   { font-family:var(--f-serif); font-size:13px; color:var(--ink); width:18px; text-align:right; }
.trust-disp { text-align:center; padding:20px; border:1px solid var(--rule); background:var(--bone); margin-bottom:14px; }
.trust-disp svg { display:block; margin:0 auto 6px; }
.trust-lbl  { font-family:var(--f-caps); font-size:8px; letter-spacing:.14em; color:var(--ink30); }
.prev-wrap  { padding:22px; }
.prev-card  { background:var(--ink); border:1px solid rgba(184,146,44,.2); }
.prev-head  { padding:18px 20px 14px; border-bottom:2px solid var(--gold-dk); background:linear-gradient(135deg,rgba(26,48,26,.8) 0%,rgba(26,20,16,1) 100%); }
.prev-tag   { font-family:var(--f-caps); font-size:8px; letter-spacing:.18em; color:var(--gold); margin-bottom:6px; }
.prev-name  { font-family:var(--f-serif); font-size:20px; font-weight:400; color:var(--bone); margin-bottom:8px; }
.prev-pill  { font-family:var(--f-caps); font-size:8px; letter-spacing:.1em; background:var(--gold-dk); color:var(--bone); padding:3px 10px; }
.prev-row   { display:grid; grid-template-columns:75px 1fr; border-bottom:1px solid rgba(255,255,255,.05); }
.prev-row:last-child { border:none; }
.prev-lbl   { padding:10px 10px 10px 14px; font-family:var(--f-caps); font-size:7px; letter-spacing:.12em; color:rgba(245,240,232,.25); border-right:1px solid rgba(255,255,255,.05); }
.prev-val   { padding:10px 13px; font-family:var(--f-serif); font-size:14px; font-weight:300; color:rgba(245,240,232,.6); line-height:1.45; }
.form-actions { padding:16px 28px; border-top:1px solid var(--rule); display:flex; align-items:center; gap:10px; background:var(--bone-dk); }
.form-hint    { font-family:var(--f-serif); font-size:12px; font-style:italic; color:var(--ink30); margin-left:auto; }
.sim-grid   { display:grid; grid-template-columns:1fr 1fr; gap:18px; align-items:start; }
.toast      { position:fixed; bottom:24px; right:24px; z-index:9999; background:var(--bone-dk); color:var(--ink); border:1px solid var(--rule); padding:12px 18px; font-family:var(--f-serif); font-size:14px; font-weight:300; display:flex; align-items:center; gap:9px; box-shadow:0 8px 32px rgba(26,20,16,.12); transform:translateY(72px); opacity:0; transition:all .4s var(--ease); }
.toast.show { transform:none; opacity:1; }
.toast-dot  { width:6px; height:6px; flex-shrink:0; }

/* ─────────────────────────────────────
   RESPONSIVE
───────────────────────────────────── */
@media(max-width:1024px) {
  .nav { padding:0 24px; }
  .nav-links { display:none; }
  .nav-hamburger { display:flex; }
  .wrap,.wrap-sm,.wrap-xs { padding:0 28px; }
  .footer { padding:56px 28px 40px; }
  .hero-content { grid-template-columns:1fr; gap:32px; padding:0 28px 60px; }
  .hero-right { display:none; }
  .match-layout,.seal-layout,.history-layout,.partner-layout { grid-template-columns:1fr; gap:48px; }
  .seal-visual { display:none; }
  .pillars-grid { grid-template-columns:1fr 1fr; }
  .culture-photo-row { grid-template-columns:1fr 1fr; height:280px; }
  .culture-grid { grid-template-columns:1fr 1fr; }
  .cult-card.wide { grid-column:1/-1; grid-template-columns:1fr; gap:24px; }
  .food-header-layout { grid-template-columns:1fr; gap:24px; }
  .food-bento { grid-template-columns:1fr 1fr; grid-template-rows:260px 200px; }
  .food-bento-item.span2 { grid-column:span 2; }
  .food-feature { grid-template-columns:1fr; }
  .festival-photo-grid { grid-template-columns:1fr 1fr; grid-template-rows:240px 180px; }
  .festival-photo-grid .img-slot.tall { grid-row:span 1; }
  .guide-grid { grid-template-columns:1fr 1fr; }
  .footer-grid { grid-template-columns:1fr 1fr; gap:32px; }
  .adm-stats { grid-template-columns:repeat(3,1fr); }
  .form-cols { grid-template-columns:1fr; }
  .sim-grid  { grid-template-columns:1fr; }
  .vs-wrap   { grid-template-columns:1fr; }
  .vs-divider { display:none; }
  .cinematic-strip { grid-template-columns:1fr 1fr; }
  .crafts-grid { grid-template-columns:repeat(3,1fr); }
  .photo-guide,.photo-guide-toggle { display:none; }
}
@media(max-width:640px) {
  .wrap,.wrap-sm,.wrap-xs { padding:0 18px; }
  .culture-photo-row { grid-template-columns:1fr; height:220px; }
  .culture-grid { grid-template-columns:1fr; }
  .food-bento { grid-template-columns:1fr; grid-template-rows:none; }
  .food-bento-item { height:240px; }
  .food-bento-item.span2 { grid-column:span 1; }
  .food-feature { padding:24px; }
  .festival-photo-grid { grid-template-columns:1fr; grid-template-rows:none; }
  .festival-photo-grid .img-slot { height:220px; }
  .guide-grid { grid-template-columns:1fr; }
  .pillars-grid { grid-template-columns:1fr; }
  .footer-grid { grid-template-columns:1fr; }
  .footer-bottom { flex-direction:column; gap:8px; text-align:center; }
  .adm-stats { grid-template-columns:1fr 1fr; }
  .crafts-grid { grid-template-columns:repeat(2,1fr); }
  .cinematic-strip { grid-template-columns:1fr; height:auto; }
  .cinematic-strip .img-slot { height:260px; }
  .strip-outer { margin:0 -18px; padding:0 18px; }
  .footer { padding:48px 18px 32px; }
  .adm-sb { display:none; }
}


/* ── Real photo display fix ──────────────────── */
.img-slot img {
  position: absolute;
  inset: 0; width: 100%; height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 6s cubic-bezier(.22,1,.36,1);
}
.img-slot:hover img { transform: scale(1.04); }
.hero-bg img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover; object-position: center 40%;
}
.udaipur-band-bg img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover; object-position: center 60%;
}
.palace-frame .img-slot img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover; object-position: center top;
}
/* food bento images */
.food-bento-item .img-slot img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover; object-position: center;
}
/* festival grid */
.festival-photo-grid .img-slot img {
  position: absolute; inset: 0;
  width: 100%; height: 100%;
  object-fit: cover;
}
</style>
</head>
<body>

<!-- Photo Guide Toggle (hidden – images are live) -->
<button class="photo-guide-toggle" id="pgToggle" onclick="togglePhotoGuide()" style="display:none">
  📸 Photo Guide
</button>

<!-- Photo Guide Panel -->
<div class="photo-guide" id="photoGuide">
  <div class="photo-guide-head">
    <div class="photo-guide-title">Photo Slots</div>
    <span class="photo-guide-close" onclick="togglePhotoGuide()">✕</span>
  </div>
  <div class="photo-guide-body">
    <div class="photo-guide-intro">Replace each slot with your Unsplash or own image. Add an &lt;img src="..."&gt; inside each .img-slot div.</div>
    <div class="photo-slot-list">
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">HERO — Lake Palace at dusk</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">PICHOLA — Lake wide shot</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">CITY-PALACE — Palace exterior</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">HAVELIS — Old city streets</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">CULTURE — Ghoomar dancer</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">GHOOMAR — Performance</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">MINIATURE — Painting detail</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">LAAL-MAAS — The dish</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">DAL-BAATI — Plated dish</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">THALI — Full spread</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">KACHORI — Close up</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">GANGAUR — Festival scene</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">DIWALI — Lake lights</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">MONSOON — Aravalli green</div></div>
      <div class="photo-slot-item"><div class="photo-slot-dot"></div><div class="photo-slot-name">CRAFT — Block printing</div></div>
    </div>
  </div>
</div>

<!-- Admin Gate -->
<div class="gate" id="gate">
  <div class="gate-card">
    <div class="gate-logo">India Recommends</div>
    <div class="gate-sub">Editorial Administration</div>
    <input class="gate-input" type="password" id="gpass" placeholder="Enter password">
    <button class="btn btn-gold" style="width:100%;justify-content:center" onclick="checkGate()">Enter</button>
    <div class="gate-error" id="gerr">Incorrect password. Please try again.</div>
    <div class="gate-hint">Password: ir2026</div>
  </div>
</div>

<!-- Admin Shell -->
<div id="admShell">
  <aside class="adm-sb">
    <div class="adm-sb-logo"><div class="adm-sb-logo-name">India Recommends</div><div class="adm-sb-logo-sub">Editorial Administration</div></div>
    <nav class="adm-nav">
      <div class="adm-sec-label">Overview</div>
      <div class="adm-ni active" onclick="admView('dashboard',this)"><span class="adm-ni-ico">◈</span>Dashboard</div>
      <div class="adm-ni" onclick="admView('places',this)"><span class="adm-ni-ico">◉</span>All Places<span class="adm-badge" id="bdg-places">0</span></div>
      <div class="adm-ni" onclick="admView('add',this)"><span class="adm-ni-ico">✦</span>Add New Place</div>
      <div class="adm-sec-label" style="margin-top:8px">IR Match</div>
      <div class="adm-ni" onclick="admView('preview',this)"><span class="adm-ni-ico">◎</span>Simulator</div>
      <div class="adm-ni" onclick="admView('scores',this)"><span class="adm-ni-ico">◆</span>Score Manager</div>
      <div class="adm-sec-label" style="margin-top:8px">Programme</div>
      <div class="adm-ni" onclick="admView('seal',this)"><span class="adm-ni-ico">★</span>IR Seal Awards</div>
      <div class="adm-ni" onclick="admView('partners',this)"><span class="adm-ni-ico">◇</span>Partner Requests<span class="adm-badge" style="background:var(--teal)" id="bdg-partners">0</span></div>
    </nav>
    <div class="adm-sb-foot">
      <div class="adm-avatar">IR</div>
      <div><div class="adm-user-name">Chief Editor</div><div class="adm-user-role">Udaipur, 2026</div></div>
      <div class="adm-exit-btn" onclick="exitAdm()">Exit</div>
    </div>
  </aside>
  <div class="adm-main">
    <div class="adm-topbar">
      <div class="adm-topbar-title" id="adm-ttl">Dashboard</div>
      <div class="adm-topbar-city">Udaipur</div>
      <div class="adm-topbar-actions">
        <button class="btn btn-outline btn-sm" onclick="admView('preview',null)">Preview</button>
        <button class="btn btn-gold btn-sm" onclick="admView('add',null)">Add Place</button>
      </div>
    </div>
    <div class="adm-content">
      <!-- DASHBOARD -->
      <div class="adm-view active" id="adm-dashboard">
        <div class="adm-stats">
          <div class="adm-stat"><div class="adm-stat-n" id="s-total">0</div><div class="adm-stat-l">Total Places</div></div>
          <div class="adm-stat"><div class="adm-stat-n teal" id="s-live">0</div><div class="adm-stat-l">Live in IR Match</div></div>
          <div class="adm-stat"><div class="adm-stat-n gold" id="s-seal">0</div><div class="adm-stat-l">IR Seal</div></div>
          <div class="adm-stat"><div class="adm-stat-n gold" id="s-avg">—</div><div class="adm-stat-l">Avg Trust Score</div></div>
          <div class="adm-stat"><div class="adm-stat-n muted" id="s-draft">0</div><div class="adm-stat-l">Drafts</div></div>
        </div>
        <div class="adm-panel">
          <div class="adm-ph"><div><div class="adm-ph-title">Recent Places</div><div class="adm-ph-sub">Last editorial additions</div></div><div class="adm-ph-actions"><button class="btn btn-gold btn-sm" onclick="admView('add',null)">Add Place</button></div></div>
          <div id="dash-tbl"></div>
        </div>
      </div>
      <!-- ALL PLACES -->
      <div class="adm-view" id="adm-places">
        <div class="adm-panel">
          <div class="adm-ph"><div><div class="adm-ph-title">All Places</div><div class="adm-ph-sub">Complete editorial database</div></div><div class="adm-ph-actions"><div class="adm-search"><span style="font-size:12px;color:var(--ink30)">⌕</span><input class="adm-si" placeholder="Search…" oninput="filterTbl(this.value)"></div><button class="btn btn-gold btn-sm" onclick="admView('add',null)">Add</button></div></div>
          <div id="places-tbl"></div>
        </div>
      </div>
      <!-- ADD / EDIT -->
      <div class="adm-view" id="adm-add">
        <div class="adm-panel">
          <div class="adm-ph"><div><div class="adm-ph-title" id="form-ttl">Add New Place</div><div class="adm-ph-sub">From your editorial visit</div></div><div class="adm-ph-actions"><button class="btn btn-outline btn-sm" onclick="resetForm()">Clear</button></div></div>
          <div class="form-cols">
            <div class="form-col">
              <div class="fs-title">Basic Information</div>
              <div class="frow"><label class="f-lbl">Name <span class="req">*</span></label><input class="f-in" id="fn" placeholder="e.g. Ambrai Restaurant" oninput="prevUpdate()"></div>
              <div class="frow"><label class="f-lbl">City</label><select class="f-sel" id="fcity"><option value="udaipur">Udaipur</option><option value="jaipur">Jaipur</option><option value="jodhpur">Jodhpur</option></select></div>
              <div class="frow"><label class="f-lbl">Category <span class="req">*</span></label><select class="f-sel" id="fcat"><option value="">Select…</option><option value="dining">Dining</option><option value="street_food">Street Food</option><option value="cafe">Café</option><option value="stay">Stay</option><option value="experience">Experience</option><option value="craft">Craft</option></select></div>
              <div class="frow"><label class="f-lbl">Description</label><textarea class="f-ta" id="fdesc" placeholder="2–3 lines in your editorial voice…" oninput="prevUpdate()"></textarea></div>
              <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px"><div class="frow"><label class="f-lbl">Address</label><input class="f-in" id="faddr" placeholder="Location"></div><div class="frow"><label class="f-lbl">Price ₹</label><input class="f-in" id="fprice" type="number" placeholder="1200"></div></div>
              <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px"><div class="frow"><label class="f-lbl">Visit Date <span class="req">*</span></label><input class="f-in" id="fvisit" type="date"></div><div class="frow"><label class="f-lbl">Status</label><select class="f-sel" id="fstatus"><option value="live">Live</option><option value="draft">Draft</option></select></div></div>
              <div class="fs-title" style="margin-top:16px">Who It Is For</div>
              <div class="tog-grid">
                <div class="tog on" onclick="this.classList.toggle('on')" data-k="solo"><div class="tog-tr"></div><span class="tog-l">Solo</span></div>
                <div class="tog on" onclick="this.classList.toggle('on')" data-k="couple"><div class="tog-tr"></div><span class="tog-l">Couple</span></div>
                <div class="tog" onclick="this.classList.toggle('on')" data-k="family"><div class="tog-tr"></div><span class="tog-l">Family</span></div>
                <div class="tog on" onclick="this.classList.toggle('on')" data-k="friends"><div class="tog-tr"></div><span class="tog-l">Friends</span></div>
              </div>
              <div class="fs-title" style="margin-top:16px">Budget</div>
              <div class="tog-grid">
                <div class="tog" onclick="this.classList.toggle('on')" data-k="bgt_low"><div class="tog-tr"></div><span class="tog-l">Under 500</span></div>
                <div class="tog on" onclick="this.classList.toggle('on')" data-k="bgt_mid"><div class="tog-tr"></div><span class="tog-l">500–1500</span></div>
                <div class="tog" onclick="this.classList.toggle('on')" data-k="bgt_high"><div class="tog-tr"></div><span class="tog-l">Splurge</span></div>
              </div>
              <div class="fs-title" style="margin-top:16px">Time Required</div>
              <div class="tog-grid">
                <div class="tog" onclick="this.classList.toggle('on')" data-k="t45"><div class="tog-tr"></div><span class="tog-l">45 min</span></div>
                <div class="tog on" onclick="this.classList.toggle('on')" data-k="t2hr"><div class="tog-tr"></div><span class="tog-l">2 Hours</span></div>
                <div class="tog" onclick="this.classList.toggle('on')" data-k="thalf"><div class="tog-tr"></div><span class="tog-l">Half Day</span></div>
              </div>
            </div>
            <div class="form-col">
              <div class="fs-title">IR Trust Score</div>
              <div class="trust-disp"><svg width="80" height="80" viewBox="0 0 80 80"><circle cx="40" cy="40" r="33" fill="none" stroke="var(--rule)" stroke-width="5"/><circle cx="40" cy="40" r="33" fill="none" stroke="var(--gold-dk)" stroke-width="5" stroke-dasharray="207" id="tarc" stroke-dashoffset="52" stroke-linecap="round" transform="rotate(-90 40 40)"/></svg><div style="font-family:var(--f-serif);font-size:20px;font-weight:300;color:var(--gold-dk)" id="tdisp">75</div><div class="trust-lbl">Trust Score / 100</div></div>
              <div class="sl-row"><span class="sl-l">Trust Score</span><input type="range" class="f-sl" id="ftrust" min="0" max="100" value="75" oninput="syncTrust(this.value);prevUpdate()"><div class="sl-v" id="tv">75</div></div>
              <div class="frow" style="margin-top:10px"><div class="tog" id="seal-tog" onclick="this.classList.toggle('on')" style="width:fit-content;gap:12px"><div class="tog-tr"></div><span class="tog-l">Award IR Seal</span></div></div>
              <div class="fs-title" style="margin-top:20px">Mood Scores (1–10)</div>
              <div class="sl-row"><span class="sl-l">Romantic</span><input type="range" class="f-sl" id="mr" min="1" max="10" value="8" oninput="sv(this)"><div class="sl-v" id="v-mr">8</div></div>
              <div class="sl-row"><span class="sl-l">Local</span><input type="range" class="f-sl" id="ml" min="1" max="10" value="6" oninput="sv(this)"><div class="sl-v" id="v-ml">6</div></div>
              <div class="sl-row"><span class="sl-l">Quiet</span><input type="range" class="f-sl" id="mq" min="1" max="10" value="7" oninput="sv(this)"><div class="sl-v" id="v-mq">7</div></div>
              <div class="sl-row"><span class="sl-l">Celebratory</span><input type="range" class="f-sl" id="mc" min="1" max="10" value="6" oninput="sv(this)"><div class="sl-v" id="v-mc">6</div></div>
              <div class="sl-row"><span class="sl-l">Hidden Gem</span><input type="range" class="f-sl" id="mh" min="1" max="10" value="5" oninput="sv(this)"><div class="sl-v" id="v-mh">5</div></div>
              <div class="fs-title" style="margin-top:18px">Priority Scores (1–10)</div>
              <div class="sl-row"><span class="sl-l">Food</span><input type="range" class="f-sl" id="pf" min="1" max="10" value="8" oninput="sv(this)"><div class="sl-v" id="v-pf">8</div></div>
              <div class="sl-row"><span class="sl-l">View</span><input type="range" class="f-sl" id="pv" min="1" max="10" value="10" oninput="sv(this)"><div class="sl-v" id="v-pv">10</div></div>
              <div class="sl-row"><span class="sl-l">Authentic</span><input type="range" class="f-sl" id="pa" min="1" max="10" value="6" oninput="sv(this)"><div class="sl-v" id="v-pa">6</div></div>
              <div class="sl-row"><span class="sl-l">Comfort</span><input type="range" class="f-sl" id="pc" min="1" max="10" value="8" oninput="sv(this)"><div class="sl-v" id="v-pc">8</div></div>
              <div class="sl-row"><span class="sl-l">Photo</span><input type="range" class="f-sl" id="pp" min="1" max="10" value="9" oninput="sv(this)"><div class="sl-v" id="v-pp">9</div></div>
              <div class="fs-title" style="margin-top:18px">IR Match Fields</div>
              <div class="frow"><label class="f-lbl">Why Now <span class="req">*</span></label><textarea class="f-ta" id="fwhy" placeholder="Specific timing, vibe, seasonal note…" oninput="prevUpdate()"></textarea></div>
              <div class="frow"><label class="f-lbl">Best Time <span class="req">*</span></label><input class="f-in" id="ftime" placeholder="e.g. 6:15pm — last lake table 7:30pm" oninput="prevUpdate()"></div>
              <div class="frow"><label class="f-lbl">Order / Do <span class="req">*</span></label><textarea class="f-ta" id="forder" placeholder="Specific dish, price, table." style="min-height:52px" oninput="prevUpdate()"></textarea></div>
              <div class="frow"><label class="f-lbl">Avoid <span class="req">*</span></label><input class="f-in" id="favoid" placeholder="Honest editorial warning…" oninput="prevUpdate()"></div>
            </div>
          </div>
          <div class="form-actions"><button class="btn btn-outline btn-sm" onclick="saveDraft()">Draft</button><button class="btn btn-gold btn-sm" onclick="savePlace()">Publish to IR Match</button><div class="form-hint">Fields marked <span style="color:var(--gold-dk)">*</span> required</div></div>
        </div>
        <div class="adm-panel" style="margin-top:16px">
          <div class="adm-ph"><div class="adm-ph-title">Live IR Match Preview</div><div class="adm-ph-sub">Exactly what travelers see</div></div>
          <div class="prev-wrap"><div class="prev-card"><div class="prev-head"><div class="prev-tag">IR Match — Pick 1 of 3</div><div class="prev-name" id="pv-name">Start filling the form…</div><span class="prev-pill" id="pv-trust">Trust Score: 75 / 100</span></div><div class="prev-row"><div class="prev-lbl">Why Now</div><div class="prev-val" id="pv-why" style="font-style:italic;opacity:.4">Your text appears here</div></div><div class="prev-row"><div class="prev-lbl">Best Time</div><div class="prev-val" id="pv-time" style="font-style:italic;opacity:.4">Best time here</div></div><div class="prev-row"><div class="prev-lbl">Order</div><div class="prev-val" id="pv-order" style="font-style:italic;opacity:.4">Order details here</div></div><div class="prev-row"><div class="prev-lbl">Avoid</div><div class="prev-val" id="pv-avoid" style="font-style:italic;opacity:.4">What to avoid here</div></div></div></div>
        </div>
      </div>
      <!-- SIMULATOR -->
      <div class="adm-view" id="adm-preview">
        <div class="sim-grid">
          <div class="adm-panel">
            <div class="adm-ph"><div class="adm-ph-title">IR Match Simulator</div><div class="adm-ph-sub">Test your database</div></div>
            <div style="padding:22px">
              <div class="frow"><label class="f-lbl">Mood</label><select class="f-sel" id="sm-mood" onchange="runSim()"><option value="r">Romantic</option><option value="l">Local</option><option value="q" selected>Quiet</option><option value="c">Celebratory</option><option value="h">Hidden Gem</option></select></div>
              <div class="frow"><label class="f-lbl">Budget</label><select class="f-sel" id="sm-budget" onchange="runSim()"><option value="bgt_low">Under 500</option><option value="bgt_mid" selected>500–1500</option><option value="bgt_high">Splurge</option></select></div>
              <div class="frow"><label class="f-lbl">Group</label><select class="f-sel" id="sm-group" onchange="runSim()"><option value="solo">Solo</option><option value="couple" selected>Couple</option><option value="family">Family</option><option value="friends">Friends</option></select></div>
              <div class="frow"><label class="f-lbl">Priority</label><select class="f-sel" id="sm-priority" onchange="runSim()"><option value="f">Food</option><option value="v" selected>View</option><option value="a">Authentic</option><option value="c2">Comfort</option><option value="p">Photo</option></select></div>
              <button class="btn btn-gold" style="width:100%;justify-content:center;margin-top:4px" onclick="runSim()">Run IR Match</button>
            </div>
          </div>
          <div id="sim-out"><div class="adm-panel"><div class="empty-state">Run the simulator to see results</div></div></div>
        </div>
      </div>
      <!-- SEAL -->
      <div class="adm-view" id="adm-seal">
        <div class="adm-panel"><div class="adm-ph"><div class="adm-ph-title">IR Seal Awards</div><div class="adm-ph-sub">Places carrying the Seal of Trust</div></div><div id="seal-tbl"></div></div>
      </div>
      <!-- SCORES -->
      <div class="adm-view" id="adm-scores">
        <div class="adm-panel"><div class="adm-ph"><div class="adm-ph-title">Score Manager</div><div class="adm-ph-sub">Update scores after revisits</div></div><div id="scores-tbl"></div></div>
      </div>
      <!-- PARTNERS -->
      <div class="adm-view" id="adm-partners">
        <div class="adm-panel"><div class="adm-ph"><div class="adm-ph-title">Partner Requests</div><div class="adm-ph-sub">Expressions of interest</div></div><div style="padding:16px"><div style="border:1px solid var(--rule);padding:14px;margin-bottom:16px;font-family:var(--f-serif);font-size:14px;font-style:italic;color:var(--ink60)">Partner interest forms from the website appear here. Editorial independence is absolute.</div><div id="partners-tbl"><div class="empty-state">No partner requests yet</div></div></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════
     PUBLIC WEBSITE
═══════════════════════════════════════ -->
<div id="pub">

<!-- NAV -->
<nav class="nav" id="nav">
  <a href="#" class="nav-logo">India Recommends</a>
  <ul class="nav-links">
    <li><a href="#match">IR Match</a></li>
    <li><a href="#seal">IR Seal</a></li>
    <li><a href="#udaipur-band">Udaipur</a></li>
    <li><a href="#guide">The Edit</a></li>
    <li><a href="#partner">Partner</a></li>
  </ul>
  <div class="nav-right">
    <button class="nav-admin-link" onclick="openGate()">Admin</button>
    <button class="nav-hamburger" id="burg"><span></span><span></span><span></span></button>
  </div>
</nav>
<div class="drawer" id="drawer">
  <a href="#match"        class="drawer-link" onclick="closeDr()">IR Match</a>
  <a href="#seal"         class="drawer-link" onclick="closeDr()">IR Seal</a>
  <a href="#udaipur-band" class="drawer-link" onclick="closeDr()">Udaipur</a>
  <a href="#guide"        class="drawer-link" onclick="closeDr()">The Edit</a>
  <a href="#partner"      class="drawer-link" onclick="closeDr()">Partner With Us</a>
</div>

<!-- ─── HERO ─────────────────────────────────── -->
<section class="hero">
  <!-- PHOTO SLOT: Hero background
       Replace with: background photo of Udaipur Lake Palace at golden hour
       Recommended search: "Udaipur Lake Palace sunset" on Unsplash
       Add <img src="YOUR-PHOTO.jpg" alt="Lake Palace Udaipur"> inside .hero-bg -->
  <div class="hero-bg" data-slot="hero">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/Udaipur-citypalace.jpg/1280px-Udaipur-citypalace.jpg" alt="City Palace Udaipur Lake" style="width:100%;height:100%;object-fit:cover;opacity:.65">
  </div>
  <div class="hero-overlay"></div>


  <div class="hero-content">
    <div class="hero-left">
      <div class="hero-eyebrow">Udaipur &middot; Rajasthan &middot; India &middot; Est. 2026</div>
      <h1 class="hero-h1">For you.<br><em>Right now.</em></h1>
      <div class="hero-tagline">The Venice of the East, curated with editorial precision</div>
      <div class="hero-btns">
        <a href="#match" class="btn btn-gold">Try IR Match</a>
        <a href="#gap"   class="btn btn-outline" style="border-color:rgba(245,240,232,.2);color:rgba(245,240,232,.7)">Why We Are Different</a>
      </div>
    </div>
  </div>

  <div class="hero-scroll">
    <div class="hero-scroll-label">Scroll</div>
    <div class="hero-scroll-line"></div>
  </div>
</section>

<!-- ─── CINEMATIC STRIP ──────────────────────── -->
<!-- PHOTO SLOTS: Three panoramic city views
     slot="pichola"     → Lake Pichola wide shot
     slot="city-palace" → City Palace exterior
     slot="havelis"     → Old city, havelis, narrow lanes -->
<div class="cinematic-strip">
  <div class="img-slot" data-slot="pichola" data-label="Lake Pichola — wide shot">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/India_-_Udaipur_-_001_-_Udaipur_Palace_panorama_from_the_lake_%281038245526%29.jpg/1280px-India_-_Udaipur_-_001_-_Udaipur_Palace_panorama_from_the_lake_%281038245526%29.jpg" alt="Lake Pichola Udaipur" loading="lazy">
    <!-- replaced -->
    <div class="img-placeholder-icon">
      <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,1)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
      <span>Lake Pichola<br>wide shot</span>
    </div>
    <div class="cine-caption">
      <div class="cine-caption-eye">Lake Pichola</div>
      <div class="cine-caption-title">Where Rajputana meets the water</div>
    </div>
  </div>
  <div class="img-slot" data-slot="city-palace" data-label="City Palace exterior">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/Udaipur-citypalace.jpg/1280px-Udaipur-citypalace.jpg" alt="City Palace Udaipur" loading="lazy">
    <!-- replaced -->
    <div class="img-placeholder-icon">
      <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,1)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
      <span>City Palace<br>exterior</span>
    </div>
    <div class="cine-caption">
      <div class="cine-caption-eye">City Palace</div>
      <div class="cine-caption-title">400 years of Mewar ambition</div>
    </div>
  </div>
  <div class="img-slot" data-slot="havelis" data-label="Old city streets &amp; havelis">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Bagore-ki-Haveli%2C_Udaipur.jpg/1280px-Bagore-ki-Haveli%2C_Udaipur.jpg" alt="Bagore Ki Haveli Udaipur" loading="lazy">
    <!-- replaced -->
    <div class="img-placeholder-icon">
      <svg width="36" height="36" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,1)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
      <span>Old city<br>havelis &amp; lanes</span>
    </div>
    <div class="cine-caption">
      <div class="cine-caption-eye">The Old City</div>
      <div class="cine-caption-title">Marble lanes that never changed</div>
    </div>
  </div>
</div>

<!-- TICKER -->
<div class="ticker" aria-hidden="true">
  <div class="ticker-track">
    <span class="ticker-item">Editorial Trust <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Hyperlocal Depth <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">IR Trust Score <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Never Pay-to-Feature <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">The IR Seal <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">For You, Right Now <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Udaipur&rsquo;s Trusted Guide <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Editorial Trust <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Hyperlocal Depth <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">IR Trust Score <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Never Pay-to-Feature <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">The IR Seal <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">For You, Right Now <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
    <span class="ticker-item">Udaipur&rsquo;s Trusted Guide <span class="ticker-sep">&nbsp;&#9670;&nbsp;</span></span>
  </div>
</div>

<!-- ─── THE GAP ───────────────────────────────── -->
<section class="section gap-section" id="gap">
  <div class="wrap">
    <div class="sec-header reveal">
      <div class="sec-eyebrow">The Gap We Fill</div>
      <span class="gold-rule"></span>
      <h2 class="sec-title">Why neither TripAdvisor<br>nor Cond&eacute; Nast is <em>enough</em></h2>
    </div>
    <div class="vs-wrap reveal">
      <div class="vs-col them">
        <div class="vs-label">TripAdvisor &amp; Cond&eacute; Nast</div>
        <div class="vs-item"><span class="vs-mark">&#10007;</span><span class="vs-text">Crowd-sourced reviews with zero editorial accountability</span></div>
        <div class="vs-item"><span class="vs-mark">&#10007;</span><span class="vs-text">Beautiful aspiration &mdash; no help deciding right now</span></div>
        <div class="vs-item"><span class="vs-mark">&#10007;</span><span class="vs-text">No hyperlocal Udaipur depth &mdash; no timing or specific tables</span></div>
        <div class="vs-item"><span class="vs-mark">&#10007;</span><span class="vs-text">Pay-to-feature placements dressed as genuine recommendations</span></div>
        <div class="vs-item"><span class="vs-mark">&#10007;</span><span class="vs-text">Same generic list for everyone &mdash; zero context for your moment</span></div>
      </div>
      <div class="vs-divider"><div class="vs-or">vs</div></div>
      <div class="vs-col us">
        <div class="vs-label">India Recommends</div>
        <div class="vs-item"><span class="vs-mark">&#10003;</span><span class="vs-text">Every pick <strong>editor-verified in person.</strong> Full price paid. Always.</span></div>
        <div class="vs-item"><span class="vs-mark">&#10003;</span><span class="vs-text"><strong>IR Match</strong> tells you where to go for <strong>your exact mood, tonight</strong></span></div>
        <div class="vs-item"><span class="vs-mark">&#10003;</span><span class="vs-text">Specific tables, dishes, timing &mdash; <strong>the insider level, always</strong></span></div>
        <div class="vs-item"><span class="vs-mark">&#10003;</span><span class="vs-text">100% independent. The IR Seal is <strong>earned, never purchased</strong></span></div>
        <div class="vs-item"><span class="vs-mark">&#10003;</span><span class="vs-text">Mood &middot; Budget &middot; Group &middot; Time &mdash; <strong>matched precisely to you</strong></span></div>
      </div>
    </div>
  </div>
</section>

<!-- ─── IR MATCH ──────────────────────────────── -->
<section class="section match-section" id="match">
  <div class="wrap">
    <div class="sec-header reveal">
      <div class="sec-eyebrow">IR Match</div>
      <span class="gold-rule"></span>
      <h2 class="sec-title">The smart <em>concierge</em><br>in your pocket</h2>
      <p class="sec-subtitle">Tell us five things. Receive three perfect answers. Every answer backed by an editor who actually went.</p>
    </div>
    <div class="match-layout">
      <div class="match-steps reveal-l">
        <div class="mstep"><div class="mstep-n">1</div><div><div class="mstep-title">Tell us your moment</div><div class="mstep-desc">Mood, budget, time available, group type, priority. Thirty seconds. No account required.</div></div></div>
        <div class="mstep"><div class="mstep-n">2</div><div><div class="mstep-title">We score verified picks</div><div class="mstep-desc">Every place in our database was personally visited, scored on six dimensions, and assigned an IR Trust Score by our editorial team.</div></div></div>
        <div class="mstep"><div class="mstep-n">3</div><div><div class="mstep-title">Three picks. Specific. Honest.</div><div class="mstep-desc">Not two hundred listings &mdash; three perfect fits with Trust Scores, exact notes, timing, and a backup if your first choice is crowded.</div></div></div>
      </div>
      <div class="quiz-shell reveal-r">
        <div class="quiz-head"><div class="quiz-head-title">IR Match &mdash; Try It Now</div><div class="quiz-dots"><div class="quiz-dot" style="background:#B85550"></div><div class="quiz-dot" style="background:var(--gold-dk);margin-left:5px"></div><div class="quiz-dot" style="background:var(--teal);margin-left:5px"></div></div></div>
        <div class="quiz-body">
          <div class="q-row"><div class="q-label">Your mood?</div><div class="q-opts" data-g="mood"><span class="qopt on" onclick="pickQ(this)">Quiet &amp; Calm</span><span class="qopt" onclick="pickQ(this)">Romantic</span><span class="qopt" onclick="pickQ(this)">Local &amp; Authentic</span><span class="qopt" onclick="pickQ(this)">Celebratory</span><span class="qopt" onclick="pickQ(this)">Hidden Gem</span></div></div>
          <div class="q-row"><div class="q-label">Budget per person?</div><div class="q-opts" data-g="budget"><span class="qopt" onclick="pickQ(this)">Under &#8377;500</span><span class="qopt on" onclick="pickQ(this)">&#8377;500 &ndash; 1,500</span><span class="qopt" onclick="pickQ(this)">Splurge</span></div></div>
          <div class="q-row"><div class="q-label">Time available?</div><div class="q-opts" data-g="time"><span class="qopt" onclick="pickQ(this)">45 minutes</span><span class="qopt on" onclick="pickQ(this)">2 hours</span><span class="qopt" onclick="pickQ(this)">Half day</span></div></div>
          <div class="q-row"><div class="q-label">Who are you with?</div><div class="q-opts" data-g="group"><span class="qopt" onclick="pickQ(this)">Solo</span><span class="qopt on" onclick="pickQ(this)">Couple</span><span class="qopt" onclick="pickQ(this)">Family</span><span class="qopt" onclick="pickQ(this)">Friends</span></div></div>
          <div class="q-row"><div class="q-label">What matters most?</div><div class="q-opts" data-g="priority"><span class="qopt on" onclick="pickQ(this)">View &amp; Atmosphere</span><span class="qopt" onclick="pickQ(this)">Food Quality</span><span class="qopt" onclick="pickQ(this)">Authenticity</span><span class="qopt" onclick="pickQ(this)">Photo-worthy</span></div></div>
          <button class="quiz-cta" id="qbtn" onclick="runMatch()">Find My Match</button>
          <div class="result-shell" id="qresult">
            <div class="result-head"><div class="result-tag">IR Match &mdash; Pick 1 of 3</div><div class="result-name" id="qr-name">Ambrai Restaurant</div><span class="result-pill" id="qr-trust">Trust Score 91 / 100</span></div>
            <div class="result-row"><div class="result-lbl">Why Now</div><div class="result-val" id="qr-why">Quiet Tuesday. City Palace faces west &mdash; <strong>golden light at 6:40pm tonight.</strong></div></div>
            <div class="result-row"><div class="result-lbl">Best Time</div><div class="result-val" id="qr-time">Arrive <strong>6:15pm.</strong> Last lake-view table: 7:30pm.</div></div>
            <div class="result-row"><div class="result-lbl">Order</div><div class="result-val" id="qr-order"><strong>Laal Maas &#8377;650</strong> + Malai Kofta &#8377;480. Ask for the lakeside corner table.</div></div>
            <div class="result-row"><div class="result-lbl">Avoid</div><div class="result-val" id="qr-avoid">Continental menu. Weekends &mdash; crowds remove the intimacy.</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── PILLARS ───────────────────────────────── -->
<section class="section pillars-section">
  <div class="wrap">
    <div class="sec-header reveal"><div class="sec-eyebrow">Our Foundation</div><span class="gold-rule"></span><h2 class="sec-title" style="color:var(--bone)">Five pillars.<br><em>Zero compromises.</em></h2></div>
    <div class="pillars-grid reveal">
      <div class="pillar"><span class="pillar-glyph">&#9650;</span><div class="pillar-name">Honest</div><div class="pillar-desc">Never pay-to-feature. Every recommendation earned through editorial standards, not a transfer.</div></div>
      <div class="pillar"><span class="pillar-glyph">&#9830;</span><div class="pillar-name">Curated</div><div class="pillar-desc">Fifty perfect picks beat five thousand mediocre ones. We choose deliberately.</div></div>
      <div class="pillar"><span class="pillar-glyph">&#9733;</span><div class="pillar-name">Experiential</div><div class="pillar-desc">The full on-ground story &mdash; atmosphere, real timing, what actually matters about a place.</div></div>
      <div class="pillar"><span class="pillar-glyph">&#9679;</span><div class="pillar-name">Aspirational</div><div class="pillar-desc">India&rsquo;s best, told with pride. Premium editorial voice. No compromise on quality.</div></div>
      <div class="pillar"><span class="pillar-glyph">&#9670;</span><div class="pillar-name">Hyperlocal</div><div class="pillar-desc">Which table. Which time. Which dish. The level only genuine local knowledge produces.</div></div>
    </div>
  </div>
</section>

<!-- ─── SEAL ──────────────────────────────────── -->
<section class="section seal-section" id="seal">
  <div class="wrap">
    <div class="seal-layout">
      <div class="seal-visual reveal-l"><div class="seal-outer-ring"></div><div class="seal-inner-ring"></div><div class="seal-medallion"><div class="seal-ir">IR</div><div class="seal-word">Seal of Trust</div><div class="seal-stars">&#9733; &#9733; &#9733;</div></div></div>
      <div class="reveal-r">
        <div class="sec-eyebrow">The India Recommends Seal</div>
        <span class="gold-rule-l"></span>
        <p class="seal-promise">The badge that is <strong>earned</strong>. Not purchased.</p>
        <p class="seal-body">Our editorial team visits every business anonymously, pays full price, and scores the experience across six dimensions. A business does not apply for the IR Seal &mdash; they are chosen. That is what makes it defensible. That is what makes it mean something.</p>
        <div class="seal-nums"><div><div class="sn-n">8.0+</div><div class="sn-l">Score to qualify</div></div><div><div class="sn-n">6</div><div class="sn-l">Judging criteria</div></div><div><div class="sn-n">100%</div><div class="sn-l">Anonymous visits</div></div></div>
        <div class="seal-steps">
          <div class="ss"><div class="ss-n">1</div><div class="ss-t"><strong>Anonymous visit</strong> &mdash; no disclosure, full price paid</div></div>
          <div class="ss"><div class="ss-n">2</div><div class="ss-t"><strong>Score six dimensions</strong> &mdash; quality, consistency, experience, value, hospitality, authenticity</div></div>
          <div class="ss"><div class="ss-n">3</div><div class="ss-t"><strong>Invitation only</strong> &mdash; businesses do not apply. They are chosen.</div></div>
          <div class="ss"><div class="ss-n">4</div><div class="ss-t"><strong>Annual review</strong> &mdash; the Seal can be removed. Trust is maintained, never assumed.</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── UDAIPUR BAND ──────────────────────────── -->
<!-- PHOTO SLOT: Panoramic Udaipur / Pichola at dusk
     Search "Udaipur panorama" or "Pichola lake aerial" on Unsplash -->
<div class="udaipur-band" id="udaipur-band">
  <div class="udaipur-band-bg" data-slot="pichola" data-label="Replace: Pichola Lake panorama">
    <!-- <img src="pichola-panorama.jpg" alt="Udaipur Pichola Lake"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Jag_Mandir_%28Worldminister%29_Water_palace_on_lake_at_Udaipur%2C_Mewar.jpg/1280px-Jag_Mandir_%28Worldminister%29_Water_palace_on_lake_at_Udaipur%2C_Mewar.jpg" alt="Jag Mandir Water Palace Lake Pichola Udaipur" loading="lazy">
  </div>
  <div class="udaipur-band-overlay"></div>
  <div class="udaipur-band-content">
    <div class="udaipur-kicker reveal">City of Lakes &middot; Rajasthan &middot; India</div>
    <div class="udaipur-main-title reveal">Udaipur</div>
    <div class="udaipur-sub-title reveal">The Venice of the East</div>
    <p class="udaipur-desc reveal">A city so beautiful it once made a Mughal emperor weep. Marble palaces rising from silver lakes. A living culture that has never stopped dancing.</p>
    <div class="udaipur-chips reveal">
      <div class="uchip"><span>1559</span>Year Founded</div>
      <div class="uchip"><span>4</span>Natural Lakes</div>
      <div class="uchip"><span>20M+</span>Annual Visitors</div>
      <div class="uchip"><span>1,300m</span>Altitude</div>
      <div class="uchip"><span>No.1</span>Most Romantic in Asia</div>
    </div>
  </div>
</div>

<!-- ─── HISTORY ───────────────────────────────── -->
<section class="section history-section" id="udaipur-history">
  <div class="wrap">
    <div class="sec-header reveal"><div class="sec-eyebrow">History &amp; Heritage</div><span class="gold-rule"></span><h2 class="sec-title">Five centuries of<br><em>Rajput glory</em></h2></div>
    <div class="history-layout">
      <!-- PHOTO SLOT: City Palace close-up -->
      <div class="palace-frame reveal-l">
        <div class="img-slot" data-slot="city-palace" data-label="City Palace — close-up detail">
          <!-- <img src="city-palace-detail.jpg" alt="City Palace Udaipur"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Statue_of_Maharana_Pratap_of_Mewar%2C_commemorating_the_Battle_of_Haldighati%2C_City_Palace%2C_Udaipur.jpg/800px-Statue_of_Maharana_Pratap_of_Mewar%2C_commemorating_the_Battle_of_Haldighati%2C_City_Palace%2C_Udaipur.jpg" alt="Maharana Pratap statue City Palace Udaipur" loading="lazy">
          <div class="img-placeholder-icon">
            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.6)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>City Palace<br>close-up photo</span>
          </div>
        </div>
        <div class="palace-overlay"></div>
        <div class="palace-year">Est. 1559</div>
        <div class="palace-quote">
          <div class="palace-quote-text">&ldquo;If on Earth there be a paradise of bliss, it is this, it is this, it is this.&rdquo;</div>
          <div class="palace-quote-attr">Mughal poet on seeing Udaipur, 17th century</div>
        </div>
      </div>

      <div class="reveal-r">
        <div class="sec-eyebrow" style="margin-bottom:8px">A Living Dynasty</div>
        <p class="u-serif" style="font-size:16px;color:var(--ink60);margin-bottom:32px">The Mewar dynasty claims the longest unbroken royal lineage in the world. Seventy-six successive rulers. Fourteen hundred years. Their legacy is written in marble, lake and song.</p>
        <div class="timeline">
          <div class="tl-item reveal"><div class="tl-left"><div class="tl-dot">&#127963;</div><div class="tl-line"></div></div><div><div class="tl-year">1559</div><div class="tl-title">The City Is Born</div><div class="tl-desc">Maharana Udai Singh II discovers a sage meditating by Pichola Lake. Udaipur is founded &mdash; a new capital hidden from Mughal reach.</div></div></div>
          <div class="tl-item reveal" style="transition-delay:.1s"><div class="tl-left"><div class="tl-dot">&#9876;&#65039;</div><div class="tl-line"></div></div><div><div class="tl-year">1576</div><div class="tl-title">The Battle of Haldighati</div><div class="tl-desc">Maharana Pratap faces Emperor Akbar&rsquo;s vast army. Though outnumbered, he becomes India&rsquo;s greatest symbol of resistance &mdash; his legend still sung in every Rajasthani home.</div></div></div>
          <div class="tl-item reveal" style="transition-delay:.2s"><div class="tl-left"><div class="tl-dot">&#127963;</div><div class="tl-line"></div></div><div><div class="tl-year">1620&ndash;1800</div><div class="tl-title">Age of Palaces</div><div class="tl-desc">Over two centuries, successive Maharanas build the City Palace &mdash; eleven stories of mirrored rooms, stained glass, and intricate Rajput&ndash;Mughal architecture.</div></div></div>
          <div class="tl-item reveal" style="transition-delay:.3s"><div class="tl-left"><div class="tl-dot">&#127909;</div></div><div><div class="tl-year">1983 &rarr; Today</div><div class="tl-title">The World Discovers Udaipur</div><div class="tl-desc">James Bond films Octopussy here. Over twenty million visitors a year come to see what many call the most romantic city in Asia &mdash; and find it hauntingly, stubbornly itself.</div></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── CULTURE ───────────────────────────────── -->
<section class="section culture-section" id="udaipur-culture">
  <div class="wrap">
    <div class="sec-header reveal"><div class="sec-eyebrow">Culture &amp; Arts</div><span class="gold-rule"></span><h2 class="sec-title">A city that never<br><em>stopped creating</em></h2></div>

    <!-- PHOTO ROW: 3 culture images side by side -->
    <!-- slot="culture"    → Ghoomar dancer in full costume
         slot="ghoomar"   → Performance close-up
         slot="miniature" → Miniature painting detail / artisan hand -->
    <div class="culture-photo-row reveal">
      <div class="img-slot" data-slot="culture" data-label="Ghoomar dancer — full costume">
        <!-- <img src="ghoomar.jpg" alt="Ghoomar dancer"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Ghoomar_dance_Jaipur.jpg/1280px-Ghoomar_dance_Jaipur.jpg" alt="Ghoomar dance Rajasthan" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Ghoomar dancer<br>full costume</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Performing Arts</div><div class="cine-caption-title">Ghoomar</div></div>
      </div>
      <div class="img-slot" data-slot="ghoomar" data-label="Kathputli puppet performance">
        <!-- <img src="kathputli.jpg" alt="Kathputli puppets"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/67/Kathputli_puppets_Rajasthan.jpg/1280px-Kathputli_puppets_Rajasthan.jpg" alt="Kathputli puppets Rajasthan" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Kathputli<br>puppet performance</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Folk Tradition</div><div class="cine-caption-title">Kathputli</div></div>
      </div>
      <div class="img-slot" data-slot="miniature" data-label="Miniature painting artisan">
        <!-- <img src="miniature-art.jpg" alt="Miniature painting"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Rajput_painting.jpg/800px-Rajput_painting.jpg" alt="Rajput miniature painting" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Miniature painting<br>artisan at work</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Visual Arts</div><div class="cine-caption-title">Miniature Painting</div></div>
      </div>
    </div>

    <div class="culture-grid reveal">
      <div class="cult-card"><div class="cult-bg-char">Art</div><span class="cult-icon">&#127912;</span><div class="cult-cat">Visual Arts</div><div class="cult-title">Pichwai &amp; Miniature Painting</div><div class="cult-desc">Udaipur is the undisputed home of the Mewar School of Miniature Painting. Pichwai paintings, some taking months to complete, hang in palaces and galleries worldwide. The best artists still live in the old city.</div><div class="cult-tags"><span class="cult-tag">Miniature</span><span class="cult-tag">Pichwai</span><span class="cult-tag">Mewar School</span></div></div>
      <div class="cult-card"><div class="cult-bg-char">Dance</div><span class="cult-icon">&#128131;</span><div class="cult-cat">Performing Arts</div><div class="cult-title">Ghoomar &amp; Kathputli</div><div class="cult-desc">Ghoomar &mdash; the swirling skirt dance of Rajasthan &mdash; was born in Mewar courts. Watch it performed at Bagore Ki Haveli every evening. Kathputli puppet theatre tells epic tales through cloth and colour.</div><div class="cult-tags"><span class="cult-tag">Ghoomar</span><span class="cult-tag">Puppetry</span><span class="cult-tag">Folk Music</span></div></div>
      <div class="cult-card"><div class="cult-bg-char">Craft</div><span class="cult-icon">&#127963;</span><div class="cult-cat">Craft Traditions</div><div class="cult-title">Block Printing &amp; Blue Pottery</div><div class="cult-desc">Udaipur&rsquo;s artisans practice wood block printing that predates the Mughals. Blue pottery &mdash; a Persian technique adopted by Rajput craftsmen &mdash; produces the vivid azure vessels found in every market.</div><div class="cult-tags"><span class="cult-tag">Block Print</span><span class="cult-tag">Blue Pottery</span><span class="cult-tag">Leheriya</span></div></div>
      <div class="cult-card"><div class="cult-bg-char">Music</div><span class="cult-icon">&#127925;</span><div class="cult-cat">Music</div><div class="cult-title">Langas &amp; Manganiyars</div><div class="cult-desc">The Langa and Manganiyar communities are hereditary musicians &mdash; their knowledge passed father to son for seven hundred years. Hearing a Manganiyar at sunset, his voice carrying over the lake, is transcendent.</div><div class="cult-tags"><span class="cult-tag">Langas</span><span class="cult-tag">Manganiyar</span><span class="cult-tag">Sufi</span></div></div>
      <div class="cult-card"><div class="cult-bg-char">Text</div><span class="cult-icon">&#128218;</span><div class="cult-cat">Literary Heritage</div><div class="cult-title">Bards &amp; Living Epics</div><div class="cult-desc">The Charans &mdash; hereditary bards &mdash; memorised entire genealogies and battle sagas. Their oral literature kept the history of Mewar alive through centuries without a single written word.</div><div class="cult-tags"><span class="cult-tag">Charans</span><span class="cult-tag">Oral Tradition</span><span class="cult-tag">Epic Poetry</span></div></div>
      <div class="cult-card wide"><div><span class="cult-icon">&#127963;</span><div class="cult-cat">Architecture</div><div class="cult-title">Where Stone Becomes Poetry</div><div class="cult-desc">Udaipur&rsquo;s architecture is a dialogue between Rajput bravado and Mughal refinement. Jharokhas let royal women observe the world unseen. Jali screens cast kaleidoscopic shadows. And everywhere: white marble from Makrana, the same stone that built the Taj Mahal.</div></div><div><div class="cult-tags" style="margin-top:0;margin-bottom:16px"><span class="cult-tag">City Palace</span><span class="cult-tag">Jag Mandir</span><span class="cult-tag">Monsoon Palace</span><span class="cult-tag">Jagdish Temple</span></div><p class="u-serif" style="font-size:15px;color:var(--ink60)">The City Palace alone took four hundred years to complete &mdash; each Maharana adding his own wing, courtyard and tower. Walk its corridors and you walk through four centuries of Mewar artistic ambition.</p></div></div>
    </div>
  </div>
</section>

<!-- ─── FOOD ──────────────────────────────────── -->
<section class="section food-section" id="udaipur-food">
  <div class="wrap">
    <div class="food-header-layout">
      <div class="reveal"><div class="sec-eyebrow">Food &amp; Flavour</div><span class="gold-rule-l"></span><h2 class="sec-title" style="color:var(--bone)">A kitchen that<br>survived <em>empires</em></h2></div>
      <p class="food-intro reveal">Rajasthani cuisine was born of scarcity &mdash; desert terrain, scarce water, months of travel. The result is food so deeply flavoured that it became one of India&rsquo;s greatest culinary traditions. In Udaipur, you eat like a Maharana.</p>
    </div>

    <!-- FOOD BENTO — 4 photo slots
         slot="laal-maas"  → Laal Maas in a clay pot, rich red
         slot="dal-baati"  → Dal Baati Churma plated
         slot="thali"      → Full Rajasthani thali spread
         slot="kachori"    → Mawa Kachori close-up -->
    <div class="food-bento reveal">
      <!-- Large hero food image — Laal Maas -->
      <div class="food-bento-item span2">
        <div class="img-slot" data-slot="laal-maas" data-label="Laal Maas — clay pot, rich red colour">
          <!-- <img src="laal-maas.jpg" alt="Laal Maas"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Laal_Maas.jpg/1280px-Laal_Maas.jpg" alt="Laal Maas Rajasthani curry" loading="lazy">
          <div class="img-placeholder-icon">
            <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Laal Maas<br>clay pot · rich red</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">Meat &middot; Royal Rajasthani</div>
          <div class="food-bento-name">Laal Maas</div>
          <div class="food-bento-desc">Lamb slow-cooked in Mathania chillies &mdash; the only chilli native to Rajasthan. Rich, complex, unforgettably red.</div>
          <div class="food-heat-row"><div class="fheat on"></div><div class="fheat on"></div><div class="fheat on"></div><div class="fheat on"></div><div class="fheat"></div></div>
        </div>
      </div>
      <!-- Dal Baati -->
      <div class="food-bento-item">
        <div class="img-slot" data-slot="dal-baati" data-label="Dal Baati Churma — plated dish">
          <!-- <img src="dal-baati.jpg" alt="Dal Baati Churma"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c0/Dal_Bati_Churma.jpg/1280px-Dal_Bati_Churma.jpg" alt="Dal Bati Churma Rajasthani food" loading="lazy">
          <div class="img-placeholder-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Dal Baati Churma</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">Vegetarian &middot; Staple</div>
          <div class="food-bento-name">Dal Baati Churma</div>
          <div class="food-bento-desc">The holy trinity of Rajasthani cooking.</div>
          <div class="food-heat-row"><div class="fheat on"></div><div class="fheat on"></div><div class="fheat"></div><div class="fheat"></div><div class="fheat"></div></div>
        </div>
      </div>
      <!-- Kachori -->
      <div class="food-bento-item">
        <div class="img-slot" data-slot="kachori" data-label="Mawa Kachori — close-up golden">
          <!-- <img src="kachori.jpg" alt="Mawa Kachori"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Kachori.jpg/1280px-Kachori.jpg" alt="Kachori Indian snack" loading="lazy">
          <div class="img-placeholder-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Mawa Kachori<br>golden &amp; sweet</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">Sweet &middot; Morning</div>
          <div class="food-bento-name">Mawa Kachori</div>
          <div class="food-bento-desc">Finest breakfast in Rajasthan.</div>
          <div class="food-heat-row"><div class="fheat"></div><div class="fheat"></div><div class="fheat"></div><div class="fheat"></div><div class="fheat"></div></div>
        </div>
      </div>
      <!-- Thali — full width bottom -->
      <div class="food-bento-item span2">
        <div class="img-slot" data-slot="thali" data-label="Full Rajasthani thali — overhead shot">
          <!-- <img src="rajasthani-thali.jpg" alt="Rajasthani Thali"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/Rajasthani_Thali.jpg/1280px-Rajasthani_Thali.jpg" alt="Rajasthani Thali full spread" loading="lazy">
          <div class="img-placeholder-icon">
            <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Rajasthani Thali<br>full spread · overhead</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">The Complete Experience</div>
          <div class="food-bento-name">Rajasthani Thali</div>
          <div class="food-bento-desc">Not a meal. A philosophy. Twelve to sixteen preparations, refilled endlessly. Abundance as hospitality.</div>
        </div>
      </div>
      <!-- Gatte ki sabzi -->
      <div class="food-bento-item">
        <div class="img-slot" data-slot="dal-baati" data-label="Gatte Ki Sabzi — gram dumplings">
          <!-- <img src="gatte.jpg" alt="Gatte Ki Sabzi"> -->
          <div class="img-placeholder-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Gatte Ki Sabzi</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">Vegetarian &middot; Classic</div>
          <div class="food-bento-name">Gatte Ki Sabzi</div>
          <div class="food-bento-desc">Better than most dishes made with vegetables.</div>
          <div class="food-heat-row"><div class="fheat on"></div><div class="fheat on"></div><div class="fheat on"></div><div class="fheat"></div><div class="fheat"></div></div>
        </div>
      </div>
      <!-- Street food -->
      <div class="food-bento-item">
        <div class="img-slot" data-slot="kachori" data-label="Udaipur street food — vendor scene">
          <!-- <img src="street-food.jpg" alt="Street food vendor"> -->
          <div class="img-placeholder-icon">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            <span>Street food<br>vendor scene</span>
          </div>
        </div>
        <div class="food-bento-overlay"></div>
        <div class="food-bento-label">
          <div class="food-bento-cat">Street &middot; Old City</div>
          <div class="food-bento-name">The Street Edit</div>
          <div class="food-bento-desc">Kachori, pyaaz ki kachori, mirchi vada.</div>
        </div>
      </div>
    </div>

    <div class="food-feature">
      <div class="food-feat-num">1</div>
      <div class="food-feat-content">
        <div class="food-feat-title">The Rajasthani Thali &mdash; A Meal Philosophy</div>
        <div class="food-feat-desc">A Rajasthani thali is not a meal &mdash; it is a statement. It says: you are a guest, and a guest must not leave hungry. Twelve to sixteen individual preparations arrive simultaneously, refilled endlessly. It is abundance as hospitality. The custom of <em>atithi devo bhava</em> &mdash; the guest is God &mdash; made edible.</div>
        <div class="food-must"><span class="food-must-item">Ker Sangri</span><span class="food-must-item">Bajre Ki Roti</span><span class="food-must-item">Mohan Maas</span><span class="food-must-item">Raab</span><span class="food-must-item">Ghewar</span><span class="food-must-item">Choorma Ladoo</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ─── TRADITION ─────────────────────────────── -->
<section class="section tradition-section" id="udaipur-tradition">
  <div class="wrap">
    <div class="sec-header reveal">
      <div class="sec-eyebrow">Festivals &amp; Tradition</div>
      <span class="gold-rule"></span>
      <h2 class="sec-title">The calendar here<br>is a <em>ceremony</em></h2>
      <p class="tradition-intro-txt">Udaipur does not celebrate festivals &mdash; it inhabits them. Every month brings a ritual, a colour, a sound practised for centuries without interruption.</p>
    </div>

    <!-- FESTIVAL PHOTO GRID
         slot="gangaur"  → Gangaur procession, women in colour
         slot="diwali"   → Diwali lights on lake / palace
         slot="monsoon"  → Aravalli hills green, monsoon mood
         slot="craft"    → Shilpgram craft fair, artisans -->
    <div class="festival-photo-grid reveal">
      <div class="img-slot tall" data-slot="gangaur" data-label="Gangaur — women in procession, colour">
        <!-- <img src="gangaur.jpg" alt="Gangaur Festival"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/Gangaur_procession_Udaipur.jpg/1280px-Gangaur_procession_Udaipur.jpg" alt="Gangaur festival procession Udaipur" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Gangaur Festival<br>procession &amp; colour</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Spring &middot; March</div><div class="cine-caption-title">Gangaur</div></div>
      </div>
      <div class="img-slot" data-slot="diwali" data-label="Diwali lights on Pichola Lake">
        <!-- <img src="diwali-udaipur.jpg" alt="Diwali Udaipur"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Diwali_2012_Kolkata.jpg/1280px-Diwali_2012_Kolkata.jpg" alt="Diwali festival lights" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Diwali lights<br>on Pichola</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Autumn &middot; October</div><div class="cine-caption-title">Diwali on the Lake</div></div>
      </div>
      <div class="img-slot" data-slot="monsoon" data-label="Monsoon Aravalli hills — lush green">
        <!-- <img src="monsoon-aravalli.jpg" alt="Monsoon Udaipur"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Sajjangarh_Monsoon_Palace_Udaipur_Rajasthan.jpg/1280px-Sajjangarh_Monsoon_Palace_Udaipur_Rajasthan.jpg" alt="Sajjangarh Monsoon Palace Udaipur" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Monsoon Aravalli<br>lush green hills</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Monsoon &middot; July</div><div class="cine-caption-title">Hariyali Amavasya</div></div>
      </div>
      <div class="img-slot" data-slot="craft" data-label="Shilpgram craft fair — artisans at work">
        <!-- <img src="shilpgram.jpg" alt="Shilpgram Craft Fair"> -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Shilpgram_craftsmen.jpg/1280px-Shilpgram_craftsmen.jpg" alt="Shilpgram craft artisans Udaipur" loading="lazy">
        <div class="img-placeholder-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="rgba(245,240,232,.5)" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="1"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          <span>Shilpgram<br>artisans at work</span>
        </div>
        <div class="cine-caption"><div class="cine-caption-eye">Winter &middot; December</div><div class="cine-caption-title">Shilpgram Utsav</div></div>
      </div>
    </div>

    <!-- Festival scroll strip -->
    <div class="strip-outer" style="margin-top:48px">
      <div class="strip" id="festStrip">
        <div class="fest-card reveal"><span class="fest-icon">&#128293;</span><div class="fest-season">Winter &middot; December</div><div class="fest-name">Shilpgram Utsav</div><div class="fest-desc">The largest crafts fair in western India. Artisans from five states gather for ten days. Weaving, pottery, puppet shows, Ghoomar performances and folk music from dawn to midnight.</div><div class="fest-when">21&ndash;30 December &middot; Annual</div></div>
        <div class="fest-card reveal" style="transition-delay:.07s"><span class="fest-icon">&#127800;</span><div class="fest-season">Spring &middot; March</div><div class="fest-name">Gangaur Festival</div><div class="fest-desc">18 days celebrating the goddess Gauri. Women dress in their finest, paint their hands with mehndi, and carry clay idols to the lake in elaborate processions.</div><div class="fest-when">March&ndash;April &middot; 18 days</div></div>
        <div class="fest-card reveal" style="transition-delay:.14s"><span class="fest-icon">&#128300;</span><div class="fest-season">Autumn &middot; October</div><div class="fest-name">Diwali on Pichola</div><div class="fest-desc">Nowhere in India does Diwali burn like Udaipur. Every palace, every ghats, every boat on the lake carries diyas. City Palace is lit from base to battlement.</div><div class="fest-when">October&ndash;November &middot; 5 nights</div></div>
        <div class="fest-card reveal" style="transition-delay:.21s"><span class="fest-icon">&#127777;&#65039;</span><div class="fest-season">Spring &middot; March</div><div class="fest-name">Mewar Festival</div><div class="fest-desc">Udaipur&rsquo;s own spring festival. Colourful processions of women, folk dances on the ghats, and the burning of effigy Holika at Manek Chowk. Three nights without sleep.</div><div class="fest-when">3 days before Holi &middot; Annual</div></div>
        <div class="fest-card reveal" style="transition-delay:.28s"><span class="fest-icon">&#127754;</span><div class="fest-season">Monsoon &middot; July</div><div class="fest-name">Hariyali Amavasya</div><div class="fest-desc">On the new moon of Shravan, the Aravalli hills turn completely green. Locals picnic on hillsides, swing on jhulas and sing the rain songs of Rajasthan. The least touristy festival of the year.</div><div class="fest-when">July&ndash;August &middot; Shravan new moon</div></div>
        <div class="fest-card reveal" style="transition-delay:.35s"><span class="fest-icon">&#127908;</span><div class="fest-season">Winter &middot; November</div><div class="fest-name">World Music Festival</div><div class="fest-desc">Three nights of world-class music on stages across the City Palace complex and the lake shore. International artists alongside Rajasthani folk legends.</div><div class="fest-when">November &middot; 3 nights &middot; Annual</div></div>
      </div>
    </div>
    <div class="strip-dots" id="festDots">
      <div class="sdot active"></div><div class="sdot"></div><div class="sdot"></div><div class="sdot"></div><div class="sdot"></div><div class="sdot"></div>
    </div>

    <div style="margin-top:64px" class="reveal">
      <div class="sec-eyebrow" style="text-align:center;margin-bottom:12px">Living Crafts of Udaipur</div>
      <span class="gold-rule"></span>
    </div>
    <div class="crafts-grid reveal">
      <div class="craft-cell"><span class="craft-emoji">&#128424;&#65039;</span><div class="craft-name">Block Printing</div><div class="craft-note">Since 12th century</div></div>
      <div class="craft-cell"><span class="craft-emoji">&#127994;</span><div class="craft-name">Blue Pottery</div><div class="craft-note">Persian origin, Rajput soul</div></div>
      <div class="craft-cell"><span class="craft-emoji">&#127912;</span><div class="craft-name">Miniature Painting</div><div class="craft-note">Mewar School, 16th c.</div></div>
      <div class="craft-cell"><span class="craft-emoji">&#128142;</span><div class="craft-name">Kundan Jewellery</div><div class="craft-note">Royal court craft</div></div>
      <div class="craft-cell"><span class="craft-emoji">&#129525;</span><div class="craft-name">Leheriya Tie-Dye</div><div class="craft-note">Wave pattern dyeing</div></div>
      <div class="craft-cell"><span class="craft-emoji">&#129334;</span><div class="craft-name">Kathputli Puppets</div><div class="craft-note">1,000-year tradition</div></div>
    </div>
  </div>
</section>

<!-- ─── GUIDE ─────────────────────────────────── -->
<section class="section guide-section" id="guide">
  <div class="wrap">
    <div class="sec-header reveal"><div class="sec-eyebrow">The Udaipur Edit</div><span class="gold-rule"></span><h2 class="sec-title">Editor&rsquo;s picks.<br><em>Right now.</em></h2><p class="sec-subtitle">Every place below was visited anonymously. Every score was earned. Nothing was paid for.</p></div>
    <div class="guide-grid" id="pub-grid"></div>
  </div>
</section>

<!-- ─── MANIFESTO ─────────────────────────────── -->
<div class="manifesto-section">
  <div class="wrap-xs">
    <div class="ornament reveal">&#9670; &#9670; &#9670;</div>
    <p class="manifesto-quote reveal">&ldquo;We are the only travel platform that gives context-aware, editor-verified recommendations for what suits you right now.&rdquo;</p>
    <span class="gold-rule"></span>
    <div class="manifesto-attr reveal">India Recommends &middot; Udaipur &middot; 2026</div>
  </div>
</div>

<!-- ─── PARTNER ───────────────────────────────── -->
<section class="section partner-section" id="partner">
  <div class="wrap">
    <div class="sec-header reveal"><div class="sec-eyebrow">For Businesses</div><span class="gold-rule"></span><h2 class="sec-title">Become a<br><em>founding partner</em></h2></div>
    <div class="partner-layout">
      <div class="reveal-l">
        <p class="partner-intro">We are selecting the first twenty Udaipur businesses to feature in India Recommends &mdash; at no cost &mdash; in exchange for editorial access and Seal consideration.</p>
        <div class="partner-perks">
          <div class="perk"><div class="perk-mark">&#10003;</div><div class="perk-text">Full editorial feature &mdash; reviewed, photographed, mapped</div></div>
          <div class="perk"><div class="perk-mark">&#10003;</div><div class="perk-text">Priority consideration for the inaugural IR Seal</div></div>
          <div class="perk"><div class="perk-mark">&#10003;</div><div class="perk-text">Trust Score feeds directly into IR Match results</div></div>
          <div class="perk"><div class="perk-mark">&#10003;</div><div class="perk-text">Featured in launch campaign to 50,000+ travelers</div></div>
          <div class="perk"><div class="perk-mark">&#10003;</div><div class="perk-text">Complete editorial independence &mdash; never pay-to-feature</div></div>
        </div>
      </div>
      <div class="partner-form reveal-r">
        <div class="form-title">Express Interest</div>
        <label class="fl">Your Name</label><input class="fi" placeholder="Arjun Sharma" id="pname">
        <label class="fl">Business Name</label><input class="fi" placeholder="Restaurant or Experience" id="pbiz">
        <label class="fl">Category</label><select class="fs" id="pcat"><option>Restaurant / Caf&eacute;</option><option>Heritage Stay</option><option>Experience / Activity</option><option>Craft / Shopping</option></select>
        <label class="fl">Email</label><input class="fi" type="email" placeholder="you@yourbusiness.com" id="pemail">
        <button class="btn btn-gold" style="width:100%;justify-content:center;margin-top:4px" onclick="submitPartner()">Submit Expression of Interest</button>
      </div>
    </div>
  </div>
</section>

<!-- ─── FOOTER ────────────────────────────────── -->
<footer class="footer">
  <div class="footer-grid">
    <div><div class="f-logo">India Recommends</div><div class="f-tagline">Not the best places in the city. The best place for you, in this moment, verified by our standards.</div></div>
    <div><div class="f-col-title">Platform</div><ul class="f-links"><li><a href="#match">IR Match</a></li><li><a href="#seal">IR Seal</a></li><li><a href="#guide">Udaipur Guide</a></li><li><a href="#partner">Partner With Us</a></li></ul></div>
    <div><div class="f-col-title">Company</div><ul class="f-links"><li><a href="#">About</a></li><li><a href="#">Editorial Standards</a></li><li><a href="#">Press</a></li><li><a href="#">Investors</a></li></ul></div>
    <div><div class="f-col-title">Connect</div><ul class="f-links"><li><a href="#">Instagram</a></li><li><a href="#">YouTube</a></li><li><a href="#">Newsletter</a></li><li><a href="#">hello@indiarecommends.com</a></li></ul></div>
  </div>
  <div class="footer-bottom"><div class="f-copy">&copy; 2026 India Recommends. All rights reserved.</div><div class="f-made">Made with love in Udaipur.</div></div>
</footer>

</div><!-- end pub -->

<div class="toast" id="toast"><div class="toast-dot" id="tdot"></div><span id="tmsg"></span></div>

<script>
var DB=JSON.parse(localStorage.getItem('ir_db')||'[]');
var editId=null;
var PASS='ir2026';
function persist(){localStorage.setItem('ir_db',JSON.stringify(DB));updateBadges();renderPubGuide();updatePubStats();}
if(!DB.length){DB.push({id:'s1',name:'Ambrai Restaurant',city:'udaipur',category:'dining',description:'The only table where City Palace turns gold as you eat. Go at 6:15pm on a weeknight. The Laal Maas is extraordinary.',address:'Amet Haveli, Hanuman Ghat',price:1200,visitDate:'2026-01-15',status:'live',sealAwarded:true,trustScore:91,solo:false,couple:true,family:true,friends:true,bgt_low:false,bgt_mid:true,bgt_high:true,t45:false,t2hr:true,thalf:true,mr:9,ml:6,mq:8,mc:7,mh:4,pf:8,pv:10,pa:6,pc:8,pp:9,whyNow:'City Palace faces directly west — golden light hits at 6:40pm tonight. Quiet on weeknights.',bestTime:'6:15pm — last entry for lake view table: 7:30pm.',order:'Laal Maas (\u20B9650) + Malai Kofta (\u20B9480). Request the lakeside corner table specifically.',avoid:'Continental menu. Weekends — crowds remove the intimacy completely.',createdAt:new Date().toISOString()});persist();}

function togglePhotoGuide(){var g=document.getElementById('photoGuide');var t=document.getElementById('pgToggle');var isOpen=g.classList.toggle('open');t.textContent=isOpen?'✕ Close Guide':'📸 Photo Guide';}
function openGate(){document.getElementById('gate').classList.add('open');setTimeout(function(){document.getElementById('gpass').focus();},250);}
function checkGate(){if(document.getElementById('gpass').value===PASS){document.getElementById('gate').classList.remove('open');document.getElementById('admShell').classList.add('open');document.getElementById('pub').style.display='none';document.getElementById('gpass').value='';document.getElementById('gerr').classList.remove('show');renderDash();}else{document.getElementById('gerr').classList.add('show');document.getElementById('gpass').select();}}
document.getElementById('gpass').addEventListener('keydown',function(e){if(e.key==='Enter')checkGate();});
document.getElementById('gate').addEventListener('click',function(e){if(e.target===document.getElementById('gate'))document.getElementById('gate').classList.remove('open');});
function exitAdm(){document.getElementById('admShell').classList.remove('open');document.getElementById('pub').style.display='';}
var admTitles={dashboard:'Dashboard',places:'All Places',add:'Add New Place',preview:'Simulator',scores:'Score Manager',seal:'IR Seal Awards',partners:'Partner Requests'};
function admView(id,el){document.querySelectorAll('.adm-view').forEach(function(v){v.classList.remove('active');});document.getElementById('adm-'+id).classList.add('active');document.querySelectorAll('.adm-ni').forEach(function(n){n.classList.remove('active');});if(el)el.classList.add('active');document.getElementById('adm-ttl').textContent=admTitles[id]||id;if(id==='dashboard')renderDash();if(id==='places')renderTbl();if(id==='add'){if(!editId)resetForm();prevUpdate();}if(id==='preview')runSim();if(id==='seal')renderSealTbl();if(id==='scores')renderScoresTbl();}
function updateBadges(){document.getElementById('bdg-places').textContent=DB.filter(function(p){return!p.isPartner;}).length;document.getElementById('bdg-partners').textContent=DB.filter(function(p){return p.isPartner;}).length;}
function tc(s){return s>=85?'var(--teal)':s>=70?'var(--gold-dk)':'var(--crimson)';}
function getT(k){var el=document.querySelector('[data-k="'+k+'"]');return el?el.classList.contains('on'):false;}
function setT(k,v){var el=document.querySelector('[data-k="'+k+'"]');if(el)el.classList.toggle('on',!!v);}
function sv(el){document.getElementById('v-'+el.id).textContent=el.value;}
function syncTrust(v){v=parseInt(v);document.getElementById('tv').textContent=v;document.getElementById('tdisp').textContent=v;var arc=document.getElementById('tarc');arc.setAttribute('stroke-dashoffset',207-(207*v/100));arc.style.stroke=tc(v);document.getElementById('tdisp').style.color=tc(v);}
function toast(msg,col){col=col||'var(--teal)';var t=document.getElementById('toast');document.getElementById('tmsg').textContent=msg;document.getElementById('tdot').style.background=col;t.classList.add('show');clearTimeout(window._tt);window._tt=setTimeout(function(){t.classList.remove('show');},3500);}
function renderStats(){var real=DB.filter(function(p){return!p.isPartner;});document.getElementById('s-total').textContent=real.length;document.getElementById('s-live').textContent=real.filter(function(p){return p.status==='live';}).length;document.getElementById('s-seal').textContent=real.filter(function(p){return p.sealAwarded;}).length;var avg=real.length?Math.round(real.reduce(function(s,p){return s+p.trustScore;},0)/real.length):0;document.getElementById('s-avg').textContent=real.length?avg:'\u2014';document.getElementById('s-draft').textContent=real.filter(function(p){return p.status==='draft';}).length;}
function pRow(p){return '<tr><td><div class="tp-name">'+p.name+'</div><div class="tp-cat">'+(p.category||'')+' \u00b7 '+p.city+'</div></td><td><div class="t-trust"><span class="t-trust-n" style="color:'+tc(p.trustScore)+'">'+p.trustScore+'</span><div class="t-trust-bar"><div class="t-trust-fill" style="width:'+p.trustScore+'%;background:'+tc(p.trustScore)+'"></div></div></div></td><td><span class="'+(p.sealAwarded?'tag-seal-y':'tag-seal-n')+'">'+(p.sealAwarded?'\u2605 Seal':'\u2014')+'</span></td><td><span class="st-'+p.status+'">'+p.status+'</span></td><td style="font-family:var(--f-caps);font-size:9px;color:var(--ink30)">'+(p.visitDate||'\u2014')+'</td><td><div class="tbl-acts"><button class="tbl-btn" onclick="editPlace(\''+p.id+'\')">&#9998;</button><button class="tbl-btn del" onclick="delPlace(\''+p.id+'\')">&#10005;</button></div></td></tr>';}
function makeTbl(rows){if(!rows.length)return'<div class="empty-state">No places yet \u2014 add your first editorial entry</div>';return'<table class="adm-tbl"><thead><tr><th>Place</th><th>Trust</th><th>Seal</th><th>Status</th><th>Visit</th><th>Actions</th></tr></thead><tbody>'+rows.join('')+'</tbody></table>';}
function renderDash(){renderStats();document.getElementById('dash-tbl').innerHTML=makeTbl(DB.filter(function(p){return!p.isPartner;}).slice(0,6).map(pRow));}
function renderTbl(f){f=f||'';var rows=DB.filter(function(p){return!p.isPartner&&(p.name.toLowerCase().indexOf(f.toLowerCase())>-1||(p.category||'').toLowerCase().indexOf(f.toLowerCase())>-1);}).map(pRow);document.getElementById('places-tbl').innerHTML=makeTbl(rows);}
function filterTbl(v){renderTbl(v);}
function renderSealTbl(){var sealed=DB.filter(function(p){return!p.isPartner&&p.sealAwarded;});document.getElementById('seal-tbl').innerHTML=sealed.length?'<table class="adm-tbl"><thead><tr><th>Place</th><th>Trust</th><th>City</th><th>Visit</th><th>Edit</th></tr></thead><tbody>'+sealed.map(function(p){return'<tr><td><div class="tp-name">\u2605 '+p.name+'</div></td><td style="color:'+tc(p.trustScore)+'">'+p.trustScore+'/100</td><td style="font-family:var(--f-caps);font-size:9px;color:var(--ink60)">'+p.city+'</td><td style="font-family:var(--f-caps);font-size:9px;color:var(--ink30)">'+(p.visitDate||'\u2014')+'</td><td><button class="tbl-btn" onclick="editPlace(\''+p.id+'\')">&#9998;</button></td></tr>';}).join('')+'</tbody></table>':'<div class="empty-state">No Seals awarded yet</div>';}
function renderScoresTbl(){var real=DB.filter(function(p){return!p.isPartner;});document.getElementById('scores-tbl').innerHTML=real.length?'<table class="adm-tbl"><thead><tr><th>Place</th><th>Trust</th><th>Romantic</th><th>Quiet</th><th>View</th><th>Food</th><th>Visit</th><th>Edit</th></tr></thead><tbody>'+real.map(function(p){return'<tr><td><div class="tp-name">'+p.name+'</div></td><td style="color:'+tc(p.trustScore)+'">'+p.trustScore+'</td><td>'+(p.mr||'\u2014')+'</td><td>'+(p.mq||'\u2014')+'</td><td>'+(p.pv||'\u2014')+'</td><td>'+(p.pf||'\u2014')+'</td><td style="font-family:var(--f-caps);font-size:9px;color:var(--ink30)">'+(p.visitDate||'\u2014')+'</td><td><button class="tbl-btn" onclick="editPlace(\''+p.id+'\')">&#9998;</button></td></tr>';}).join('')+'</tbody></table>':'<div class="empty-state">No places yet</div>';}
function prevUpdate(){var n=document.getElementById('fn').value||'Your Place Name';var t=document.getElementById('ftrust').value;var w=document.getElementById('fwhy').value;var tm=document.getElementById('ftime').value;var o=document.getElementById('forder').value;var av=document.getElementById('favoid').value;document.getElementById('pv-name').textContent=n;document.getElementById('pv-trust').textContent='Trust Score: '+t+' / 100';function set(id,v,ph){var el=document.getElementById(id);el.textContent=v||ph;el.style.opacity=v?'':'0.4';el.style.fontStyle=v?'':'italic';}set('pv-why',w,'Your "Why Now" appears here');set('pv-time',tm,'Best time here');set('pv-order',o,'Order details here');set('pv-avoid',av,'What to avoid here');}
function readForm(status){var n=document.getElementById('fn').value.trim();if(!n){toast('Place name is required','var(--crimson)');return null;}return{id:editId||Date.now().toString(),name:n,city:document.getElementById('fcity').value,category:document.getElementById('fcat').value,description:document.getElementById('fdesc').value.trim(),address:document.getElementById('faddr').value.trim(),price:document.getElementById('fprice').value,visitDate:document.getElementById('fvisit').value,status:status||document.getElementById('fstatus').value,sealAwarded:document.getElementById('seal-tog').classList.contains('on'),trustScore:parseInt(document.getElementById('ftrust').value),solo:getT('solo'),couple:getT('couple'),family:getT('family'),friends:getT('friends'),bgt_low:getT('bgt_low'),bgt_mid:getT('bgt_mid'),bgt_high:getT('bgt_high'),t45:getT('t45'),t2hr:getT('t2hr'),thalf:getT('thalf'),mr:parseInt(document.getElementById('mr').value),ml:parseInt(document.getElementById('ml').value),mq:parseInt(document.getElementById('mq').value),mc:parseInt(document.getElementById('mc').value),mh:parseInt(document.getElementById('mh').value),pf:parseInt(document.getElementById('pf').value),pv:parseInt(document.getElementById('pv').value),pa:parseInt(document.getElementById('pa').value),pc:parseInt(document.getElementById('pc').value),pp:parseInt(document.getElementById('pp').value),whyNow:document.getElementById('fwhy').value.trim(),bestTime:document.getElementById('ftime').value.trim(),order:document.getElementById('forder').value.trim(),avoid:document.getElementById('favoid').value.trim(),createdAt:new Date().toISOString()};}
function savePlace(){var p=readForm('live');if(!p)return;if(editId){var i=DB.findIndex(function(x){return x.id===editId;});if(i>-1)DB[i]=p;}else DB.unshift(p);persist();resetForm();admView('places',document.querySelectorAll('.adm-ni')[1]);toast(p.name+' is now live in IR Match');}
function saveDraft(){var p=readForm('draft');if(!p)return;if(editId){var i=DB.findIndex(function(x){return x.id===editId;});if(i>-1)DB[i]=p;}else DB.unshift(p);persist();resetForm();admView('places',document.querySelectorAll('.adm-ni')[1]);toast('Saved as draft','var(--gold-dk)');}
function editPlace(id){var p=DB.find(function(x){return x.id===id;});if(!p)return;editId=id;admView('add',document.querySelectorAll('.adm-ni')[2]);document.getElementById('form-ttl').textContent='Editing: '+p.name;var map={fn:'name',fcity:'city',fcat:'category',fdesc:'description',faddr:'address',fprice:'price',fvisit:'visitDate',fstatus:'status',fwhy:'whyNow',ftime:'bestTime',forder:'order',favoid:'avoid'};Object.keys(map).forEach(function(fid){var el=document.getElementById(fid);if(el)el.value=p[map[fid]]||'';});document.getElementById('ftrust').value=p.trustScore;syncTrust(p.trustScore);document.getElementById('seal-tog').classList.toggle('on',!!p.sealAwarded);['solo','couple','family','friends','bgt_low','bgt_mid','bgt_high','t45','t2hr','thalf'].forEach(function(k){setT(k,p[k]);});var smap={mr:p.mr,ml:p.ml,mq:p.mq,mc:p.mc,mh:p.mh,pf:p.pf,pv:p.pv,pa:p.pa,pc:p.pc,pp:p.pp};Object.keys(smap).forEach(function(id){var el=document.getElementById(id);if(!el)return;el.value=smap[id]||7;document.getElementById('v-'+id).textContent=smap[id]||7;});prevUpdate();}
function delPlace(id){var p=DB.find(function(x){return x.id===id;});if(!p)return;if(!confirm('Remove "'+p.name+'"?'))return;DB=DB.filter(function(x){return x.id!==id;});persist();renderTbl();toast('"'+p.name+'" removed','var(--crimson)');}
function resetForm(){editId=null;document.getElementById('form-ttl').textContent='Add New Place';['fn','fdesc','faddr','fprice','fwhy','ftime','forder','favoid'].forEach(function(id){var el=document.getElementById(id);if(el)el.value='';});document.getElementById('fvisit').value=new Date().toISOString().split('T')[0];document.getElementById('fstatus').value='live';document.getElementById('ftrust').value=75;syncTrust(75);document.getElementById('seal-tog').classList.remove('on');var defs={mr:8,ml:6,mq:7,mc:6,mh:5,pf:8,pv:10,pa:6,pc:8,pp:9};Object.keys(defs).forEach(function(id){var el=document.getElementById(id);if(!el)return;el.value=defs[id];document.getElementById('v-'+id).textContent=defs[id];});var onK=['solo','couple','friends','bgt_mid','t2hr'];document.querySelectorAll('[data-k]').forEach(function(el){el.classList.toggle('on',onK.indexOf(el.dataset.k)>-1);});prevUpdate();}
function runSim(){var mood=document.getElementById('sm-mood').value;var budget=document.getElementById('sm-budget').value;var group=document.getElementById('sm-group').value;var priority=document.getElementById('sm-priority').value;var mKey='m'+mood;var pKey='p'+priority;var cands=DB.filter(function(p){return!p.isPartner&&p.status==='live'&&p[budget]&&p[group]&&p.trustScore>=70;});var scored=cands.map(function(p){var ms=((p[mKey]||5)/10)*0.4;var ps=((p[pKey]||5)/10)*0.4;var ts=(p.trustScore/100)*0.2;return Object.assign({},p,{_s:ms+ps+ts});}).sort(function(a,b){return b._s-a._s;}).slice(0,3);var el=document.getElementById('sim-out');if(!scored.length){el.innerHTML='<div class="adm-panel"><div class="empty-state">No matches \u2014 add more places or adjust filters</div></div>';return;}el.innerHTML=scored.map(function(p,i){return'<div style="background:var(--ink);border:1px solid rgba(184,146,44,.2);overflow:hidden;margin-bottom:12px"><div style="padding:16px 20px 12px;background:linear-gradient(135deg,rgba(26,48,26,.8) 0%,rgba(26,20,16,1) 100%);border-bottom:2px solid var(--gold-dk)"><div style="font-family:var(--f-caps);font-size:8px;letter-spacing:.18em;color:var(--gold);margin-bottom:6px">Pick '+(i+1)+' \u00b7 Match '+(p._s*100).toFixed(0)+'%</div><div style="font-family:var(--f-serif);font-size:20px;color:var(--bone)">'+p.name+'</div><span style="display:inline-block;background:var(--gold-dk);color:var(--bone);font-family:var(--f-caps);font-size:8px;letter-spacing:.1em;padding:3px 10px;margin-top:7px">Trust Score '+p.trustScore+'/100'+(p.sealAwarded?' \u2605 Seal':'')+' </span></div>'+(p.whyNow?'<div style="display:grid;grid-template-columns:72px 1fr;border-bottom:1px solid rgba(255,255,255,.05)"><div style="padding:10px 10px 10px 14px;font-family:var(--f-caps);font-size:7px;letter-spacing:.12em;color:rgba(245,240,232,.25);border-right:1px solid rgba(255,255,255,.05)">Why Now</div><div style="padding:10px 13px;font-family:var(--f-serif);font-size:14px;color:rgba(245,240,232,.65)">'+p.whyNow+'</div></div>':'')+(p.bestTime?'<div style="display:grid;grid-template-columns:72px 1fr"><div style="padding:10px 10px 10px 14px;font-family:var(--f-caps);font-size:7px;letter-spacing:.12em;color:rgba(245,240,232,.25);border-right:1px solid rgba(255,255,255,.05)">Best Time</div><div style="padding:10px 13px;font-family:var(--f-serif);font-size:14px;color:rgba(245,240,232,.65)">'+p.bestTime+'</div></div>':'')+'</div>';}).join('');}
function pickQ(el){el.closest('.q-opts').querySelectorAll('.qopt').forEach(function(s){s.classList.remove('on');});el.classList.add('on');}
function runMatch(){var btn=document.getElementById('qbtn');var card=document.getElementById('qresult');var moodTxt=(document.querySelector('[data-g="mood"] .qopt.on')||{}).textContent||'';var grpTxt=(document.querySelector('[data-g="group"] .qopt.on')||{}).textContent||'';var bdgTxt=(document.querySelector('[data-g="budget"] .qopt.on')||{}).textContent||'';var bdg=bdgTxt.indexOf('500')===0?'bgt_low':bdgTxt.indexOf('Splurge')>-1?'bgt_high':'bgt_mid';var grp=grpTxt.toLowerCase().indexOf('couple')>-1?'couple':grpTxt.toLowerCase().indexOf('family')>-1?'family':grpTxt.toLowerCase().indexOf('friends')>-1?'friends':'solo';var mood=moodTxt.toLowerCase().indexOf('romantic')>-1?'mr':moodTxt.toLowerCase().indexOf('local')>-1?'ml':moodTxt.toLowerCase().indexOf('celebr')>-1?'mc':moodTxt.toLowerCase().indexOf('hidden')>-1?'mh':'mq';var cands=DB.filter(function(p){return!p.isPartner&&p.status==='live'&&p[bdg]&&p[grp]&&p.trustScore>=70;});var top=cands.sort(function(a,b){return(b[mood]||0)-(a[mood]||0);})[0];btn.textContent='Finding your match\u2026';btn.style.background='var(--ink)';btn.style.color='var(--bone)';btn.style.pointerEvents='none';setTimeout(function(){if(top){document.getElementById('qr-name').textContent=top.name;document.getElementById('qr-trust').textContent='Trust Score '+top.trustScore+' / 100';document.getElementById('qr-why').innerHTML=top.whyNow||'\u2014';document.getElementById('qr-time').innerHTML=top.bestTime||'\u2014';document.getElementById('qr-order').innerHTML=top.order||'\u2014';document.getElementById('qr-avoid').innerHTML=top.avoid||'\u2014';}card.classList.add('show');btn.textContent='Match found \u2014 see below';btn.style.background='var(--teal)';btn.style.pointerEvents='';card.scrollIntoView({behavior:'smooth',block:'nearest'});},1400);}
function renderPubGuide(){var live=DB.filter(function(p){return!p.isPartner&&p.status==='live';}).slice(0,5);var grid=document.getElementById('pub-grid');if(!grid)return;grid.innerHTML=live.map(function(p){return'<div class="g-card">'+(p.sealAwarded?'<div class="g-seal-mark">IR Seal</div>':'')+'<div class="g-cat">'+(p.category||'Place')+' \u00b7 '+p.city+'</div><div class="g-name">'+p.name+'</div><div class="g-desc">'+(p.description||'')+'</div><div class="g-meta"><div class="g-score">'+p.trustScore+'<div class="g-bar"><div class="g-bar-fill" style="width:'+p.trustScore+'%"></div></div></div><div class="g-tag">'+(p.bgt_mid?'\u20B9\u20B9':'\u20B9')+' \u00b7 '+(p.couple?'Couple':p.solo?'Solo':'Any')+'</div></div></div>';}).join('')+'<div class="g-card g-cta-card" onclick="document.getElementById(\'match\').scrollIntoView({behavior:\'smooth\'})" role="button"><div class="g-cta-cat">Use IR Match</div><div class="g-cta-title">Find your perfect place,<br>right now \u2192</div><div class="g-cta-sub">Tell us your mood. Thirty seconds.</div></div>';grid.querySelectorAll('.g-card').forEach(function(el,i){el.style.transitionDelay=(i*0.07)+'s';el.classList.add('reveal');revealObs.observe(el);});}
function updatePubStats(){var real=DB.filter(function(p){return!p.isPartner;});var avg=real.length?Math.round(real.reduce(function(s,p){return s+p.trustScore;},0)/real.length):91;var el=document.getElementById('pub-avg');if(el)el.textContent=avg;}
function submitPartner(){var n=document.getElementById('pname').value.trim();var b=document.getElementById('pbiz').value.trim();var e=document.getElementById('pemail').value.trim();if(!n||!b||!e){toast('Please fill in all fields','var(--crimson)');return;}DB.push({id:Date.now().toString(),name:b,isPartner:true,partnerName:n,partnerEmail:e,status:'pending',trustScore:0,createdAt:new Date().toISOString()});persist();toast('Received, '+n.split(' ')[0]+'. We will be in touch within 48 hours.');['pname','pbiz','pemail'].forEach(function(id){document.getElementById(id).value='';});}
var revealObs=new IntersectionObserver(function(entries){entries.forEach(function(e){if(e.isIntersecting)e.target.classList.add('in');});},{threshold:0.1});
document.querySelectorAll('.reveal,.reveal-l,.reveal-r').forEach(function(el){revealObs.observe(el);});
['.pillars-grid','.culture-grid','.crafts-grid'].forEach(function(sel){document.querySelectorAll(sel).forEach(function(grid){Array.prototype.slice.call(grid.children).forEach(function(c,i){c.style.transitionDelay=(i*0.06)+'s';if(!c.classList.contains('reveal')){c.classList.add('reveal');revealObs.observe(c);}});});});
var navEl=document.getElementById('nav');
window.addEventListener('scroll',function(){navEl.classList.toggle('scrolled',window.scrollY>20);},{passive:true});
var burg=document.getElementById('burg');var drawer=document.getElementById('drawer');var drOpen=false;
burg.addEventListener('click',function(){drOpen=!drOpen;drawer.classList.toggle('open',drOpen);var s=burg.querySelectorAll('span');if(drOpen){s[0].style.transform='rotate(45deg) translate(5px,5px)';s[1].style.opacity='0';s[2].style.transform='rotate(-45deg) translate(5px,-5px)';}else s.forEach(function(x){x.style.transform='';x.style.opacity='';});});
function closeDr(){drOpen=false;drawer.classList.remove('open');burg.querySelectorAll('span').forEach(function(x){x.style.transform='';x.style.opacity='';});}
var strip=document.getElementById('festStrip');var sdots=document.querySelectorAll('.sdot');
if(strip){strip.addEventListener('scroll',function(){var idx=Math.round(strip.scrollLeft/294);sdots.forEach(function(d,i){d.classList.toggle('active',i===idx);});},{passive:true});sdots.forEach(function(d,i){d.addEventListener('click',function(){strip.scrollTo({left:i*294,behavior:'smooth'});});});}
document.getElementById('fvisit').value=new Date().toISOString().split('T')[0];
syncTrust(75);updateBadges();renderPubGuide();updatePubStats();
</script>
</body>
</html>
