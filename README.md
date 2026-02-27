<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bhanu Ayurveda — Pure. Potent. Natural.</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,700;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root {
  --forest: #1e3a2f;
  --forest-mid: #2e5e45;
  --sage: #5c8a6e;
  --sage-light: #8fb89e;
  --cream: #f7f2e9;
  --cream-warm: #efe8d6;
  --amber: #c49a2c;
  --amber-light: #e8c96a;
  --terracotta: #c4734a;
  --text: #1a2e22;
  --text-muted: #56725f;
  --white: #ffffff;
}
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { font-family: 'DM Sans', sans-serif; background: var(--cream); color: var(--text); overflow-x: hidden; }

/* ─── ANNOUNCEMENT BAR ─── */
.announcement {
  background: var(--forest);
  color: rgba(247,242,233,0.9);
  text-align: center;
  padding: 0.55rem 1rem;
  font-size: 0.8rem;
  letter-spacing: 0.05em;
}
.announcement span { color: var(--amber-light); font-weight: 500; }

/* ─── NAV ─── */
nav {
  position: sticky; top: 0; z-index: 200;
  background: rgba(247,242,233,0.96);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(30,58,47,0.1);
  padding: 0 5rem;
  display: flex; align-items: center; justify-content: space-between;
  height: 68px;
}
.nav-logo {
  font-family: 'Playfair Display', serif;
  font-size: 1.55rem; color: var(--forest);
  display: flex; align-items: center; gap: 0.5rem;
}
.nav-logo-leaf { font-size: 1.2rem; }
.nav-logo em { color: var(--amber); font-style: italic; }
.nav-links { display: flex; gap: 2.2rem; list-style: none; }
.nav-links a { text-decoration: none; color: var(--text-muted); font-size: 0.85rem; font-weight: 400; letter-spacing: 0.04em; transition: color 0.25s; }
.nav-links a:hover { color: var(--forest); }
.nav-cta {
  background: var(--forest); color: var(--cream);
  padding: 0.6rem 1.5rem; border: none; cursor: pointer;
  font-family: 'DM Sans', sans-serif; font-size: 0.82rem; font-weight: 500;
  letter-spacing: 0.06em; text-transform: uppercase;
  transition: background 0.3s;
  text-decoration: none; display: inline-block;
}
.nav-cta:hover { background: var(--forest-mid); }

/* ─── HERO ─── */
#hero {
  min-height: calc(100vh - 103px);
  display: grid; grid-template-columns: 55% 45%;
  background: var(--forest);
  overflow: hidden; position: relative;
}
/* Decorative botanical SVG lines */
#hero::before {
  content: '';
  position: absolute; inset: 0; pointer-events: none;
  background-image:
    radial-gradient(circle at 20% 80%, rgba(92,138,110,0.15) 0%, transparent 40%),
    radial-gradient(circle at 80% 20%, rgba(196,154,44,0.08) 0%, transparent 35%);
}
.hero-content {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; justify-content: center;
  padding: 5rem 4rem 5rem 6rem;
}
.hero-tag {
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: rgba(196,154,44,0.15);
  border: 1px solid rgba(196,154,44,0.35);
  color: var(--amber-light);
  padding: 0.4rem 1rem; border-radius: 100px;
  font-size: 0.75rem; letter-spacing: 0.12em; text-transform: uppercase;
  width: fit-content; margin-bottom: 2rem;
}
.hero-h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(3.2rem, 5vw, 5rem);
  font-weight: 400; color: var(--cream);
  line-height: 1.08; margin-bottom: 1.6rem;
  letter-spacing: -0.01em;
}
.hero-h1 em { color: var(--amber-light); font-style: italic; }
.hero-h1 .line-green { color: var(--sage-light); }
.hero-sub {
  color: rgba(247,242,233,0.6);
  font-size: 1rem; line-height: 1.8; font-weight: 300;
  max-width: 420px; margin-bottom: 2.5rem;
}
.hero-actions { display: flex; gap: 1rem; align-items: center; margin-bottom: 3rem; }
.btn-primary {
  background: var(--amber); color: var(--forest);
  padding: 0.85rem 2rem; font-size: 0.85rem;
  font-weight: 600; letter-spacing: 0.05em; text-transform: uppercase;
  border: none; cursor: pointer; text-decoration: none;
  transition: background 0.3s, transform 0.2s;
  display: inline-block;
}
.btn-primary:hover { background: var(--amber-light); transform: translateY(-2px); }
.btn-ghost {
  color: rgba(247,242,233,0.7); font-size: 0.85rem;
  text-decoration: underline; text-underline-offset: 3px;
  letter-spacing: 0.03em; transition: color 0.3s;
}
.btn-ghost:hover { color: var(--cream); }
.hero-trust {
  display: flex; gap: 2rem;
  padding-top: 2rem; border-top: 1px solid rgba(247,242,233,0.1);
}
.trust-item { display: flex; align-items: center; gap: 0.6rem; }
.trust-icon { font-size: 1.1rem; }
.trust-text { font-size: 0.8rem; color: rgba(247,242,233,0.55); line-height: 1.3; }
.trust-text strong { display: block; color: rgba(247,242,233,0.9); font-weight: 500; }

/* Hero right — product showcase */
.hero-visual {
  position: relative; overflow: hidden;
  background: linear-gradient(160deg, #2a5040 0%, #1a3028 100%);
  display: flex; align-items: center; justify-content: center;
}
.hero-visual::before {
  content: '';
  position: absolute; top: -50%; left: -50%;
  width: 200%; height: 200%;
  background: radial-gradient(circle at 60% 50%, rgba(196,154,44,0.1) 0%, transparent 50%);
}
.product-showcase {
  position: relative; z-index: 2;
  display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;
  padding: 3rem 2.5rem;
  width: 100%;
}
.product-card {
  background: rgba(247,242,233,0.06);
  border: 1px solid rgba(247,242,233,0.08);
  border-radius: 4px; padding: 1.5rem 1.2rem;
  transition: background 0.3s, transform 0.3s;
  cursor: default;
}
.product-card:hover { background: rgba(247,242,233,0.1); transform: translateY(-3px); }
.product-card.featured {
  grid-column: 1 / -1;
  background: rgba(196,154,44,0.12);
  border-color: rgba(196,154,44,0.25);
  display: flex; align-items: center; gap: 1.5rem;
  padding: 1.5rem 1.8rem;
}
.pc-icon { font-size: 2.2rem; margin-bottom: 0.8rem; line-height: 1; }
.pc-icon-lg { font-size: 3rem; flex-shrink: 0; }
.pc-label {
  font-size: 0.68rem; letter-spacing: 0.14em; text-transform: uppercase;
  color: var(--amber-light); margin-bottom: 0.3rem;
}
.pc-name {
  font-family: 'Playfair Display', serif;
  font-size: 1.05rem; color: var(--cream); font-weight: 400;
  margin-bottom: 0.4rem;
}
.pc-desc { font-size: 0.78rem; color: rgba(247,242,233,0.5); line-height: 1.5; }
.pc-price { font-size: 1.1rem; color: var(--amber-light); font-weight: 500; margin-top: 0.4rem; }
.pc-featured-info { flex: 1; }
.pc-badge {
  background: var(--amber); color: var(--forest);
  font-size: 0.68rem; font-weight: 700; letter-spacing: 0.08em;
  text-transform: uppercase; padding: 0.25rem 0.7rem;
  border-radius: 100px; margin-top: 0.5rem; display: inline-block;
}

/* ─── MARQUEE ─── */
.marquee-wrap {
  background: var(--amber);
  padding: 0.7rem 0; overflow: hidden;
}
.marquee-track {
  display: flex; gap: 3rem;
  animation: marquee 22s linear infinite;
  width: max-content;
}
.marquee-track span {
  font-size: 0.8rem; font-weight: 600; letter-spacing: 0.1em;
  text-transform: uppercase; color: var(--forest);
  white-space: nowrap;
}
.marquee-track span.dot { color: var(--forest-mid); opacity: 0.5; }
@keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

/* ─── INGREDIENTS STRIP ─── */
#ingredients {
  background: var(--cream-warm);
  padding: 5rem 6rem;
}
.section-header { margin-bottom: 3.5rem; }
.section-label {
  font-size: 0.72rem; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--sage); margin-bottom: 0.6rem;
}
.section-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.9rem, 3vw, 2.8rem); font-weight: 400;
  color: var(--forest); line-height: 1.2;
}
.section-title em { font-style: italic; color: var(--forest-mid); }
.ingredients-grid {
  display: grid; grid-template-columns: repeat(6, 1fr); gap: 1.2rem;
}
.ing-card {
  background: var(--cream);
  border: 1px solid rgba(30,58,47,0.07);
  padding: 1.8rem 1.2rem;
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: default;
}
.ing-card:hover { transform: translateY(-4px); box-shadow: 0 12px 30px rgba(30,58,47,0.08); }
.ing-emoji { font-size: 2.4rem; margin-bottom: 0.8rem; }
.ing-name { font-family: 'Playfair Display', serif; font-size: 0.95rem; color: var(--forest); margin-bottom: 0.3rem; }
.ing-benefit { font-size: 0.75rem; color: var(--text-muted); line-height: 1.4; }

/* ─── ABOUT (BENTO) ─── */
#about {
  padding: 6rem 6rem;
  background: var(--cream);
}
.bento-grid {
  display: grid;
  grid-template-columns: 1.3fr 1fr 1fr;
  grid-template-rows: auto auto;
  gap: 1.2rem;
  margin-top: 3rem;
}
.bento-card {
  background: var(--cream-warm);
  border: 1px solid rgba(30,58,47,0.07);
  padding: 2.5rem;
  position: relative; overflow: hidden;
  transition: box-shadow 0.3s;
}
.bento-card:hover { box-shadow: 0 8px 30px rgba(30,58,47,0.07); }
.bento-card.tall { grid-row: 1 / 3; background: var(--forest); }
.bento-card.amber-bg { background: var(--amber); }
.bento-card.wide { grid-column: 2 / 4; }
.bento-icon { font-size: 2.5rem; margin-bottom: 1rem; }
.bento-stat {
  font-family: 'Playfair Display', serif;
  font-size: 3.5rem; font-weight: 400; color: var(--forest);
  line-height: 1;
}
.bento-card.amber-bg .bento-stat { color: var(--forest); }
.bento-card.tall .bento-stat { color: var(--amber-light); }
.bento-stat-label { font-size: 0.82rem; color: var(--text-muted); margin-top: 0.4rem; font-weight: 400; }
.bento-card.tall .bento-stat-label { color: rgba(247,242,233,0.6); }
.bento-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.5rem; color: var(--cream); margin-bottom: 1rem;
}
.bento-text { color: rgba(247,242,233,0.65); font-size: 0.9rem; line-height: 1.8; font-weight: 300; }
.bento-list { list-style: none; margin-top: 1.2rem; display: flex; flex-direction: column; gap: 0.6rem; }
.bento-list li {
  display: flex; align-items: center; gap: 0.6rem;
  color: rgba(247,242,233,0.75); font-size: 0.85rem;
}
.bento-list li::before { content: '✓'; color: var(--amber-light); font-size: 0.75rem; }
.bento-card.amber-bg .bento-stat-label { color: rgba(30,58,47,0.7); }
.bento-card.amber-bg .bento-icon { font-size: 2rem; margin-bottom: 0.6rem; }

/* ─── PRODUCTS ─── */
#products {
  background: var(--forest);
  padding: 6rem 6rem;
}
#products .section-label { color: rgba(196,154,44,0.7); }
#products .section-title { color: var(--cream); }
.products-grid {
  display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
  margin-top: 3rem;
}
.prod-card {
  background: rgba(247,242,233,0.04);
  border: 1px solid rgba(247,242,233,0.07);
  overflow: hidden;
  transition: background 0.3s, transform 0.3s;
  cursor: default;
}
.prod-card:hover { background: rgba(247,242,233,0.08); transform: translateY(-3px); }
.prod-img {
  height: 180px;
  display: flex; align-items: center; justify-content: center;
  font-size: 4rem;
  background: rgba(247,242,233,0.05);
  border-bottom: 1px solid rgba(247,242,233,0.06);
  position: relative; overflow: hidden;
}
.prod-img::before {
  content: '';
  position: absolute; inset: 0;
  background: radial-gradient(circle at 50% 60%, rgba(196,154,44,0.07) 0%, transparent 70%);
}
.prod-body { padding: 1.5rem; }
.prod-cat { font-size: 0.7rem; letter-spacing: 0.14em; text-transform: uppercase; color: var(--sage-light); margin-bottom: 0.5rem; }
.prod-name { font-family: 'Playfair Display', serif; font-size: 1.2rem; color: var(--cream); margin-bottom: 0.6rem; }
.prod-desc { font-size: 0.82rem; color: rgba(247,242,233,0.5); line-height: 1.7; margin-bottom: 1rem; font-weight: 300; }
.prod-footer { display: flex; align-items: center; justify-content: space-between; }
.prod-tags { display: flex; gap: 0.4rem; flex-wrap: wrap; }
.prod-tag {
  background: rgba(92,138,110,0.2);
  color: var(--sage-light); font-size: 0.68rem;
  padding: 0.25rem 0.6rem; border-radius: 2px; letter-spacing: 0.05em;
}
.prod-arrow {
  width: 32px; height: 32px;
  border: 1px solid rgba(247,242,233,0.15);
  display: flex; align-items: center; justify-content: center;
  color: rgba(247,242,233,0.4); font-size: 0.85rem;
  transition: border-color 0.3s, color 0.3s;
}
.prod-card:hover .prod-arrow { border-color: var(--amber); color: var(--amber); }

/* ─── WHY US ─── */
#why {
  padding: 6rem 6rem;
  background: var(--cream-warm);
  display: grid; grid-template-columns: 1fr 1fr; gap: 6rem; align-items: center;
}
.why-features { display: flex; flex-direction: column; gap: 1.8rem; margin-top: 2.5rem; }
.why-feat {
  display: flex; gap: 1.2rem; align-items: flex-start;
  padding-bottom: 1.8rem;
  border-bottom: 1px solid rgba(30,58,47,0.08);
}
.why-feat:last-child { border-bottom: none; padding-bottom: 0; }
.why-feat-icon {
  width: 48px; height: 48px; flex-shrink: 0;
  background: var(--forest);
  display: flex; align-items: center; justify-content: center;
  font-size: 1.2rem;
}
.why-feat-title { font-size: 0.95rem; font-weight: 500; color: var(--forest); margin-bottom: 0.3rem; }
.why-feat-desc { font-size: 0.85rem; color: var(--text-muted); line-height: 1.7; font-weight: 300; }
.why-visual {
  position: relative; display: flex; flex-direction: column; gap: 1rem;
}
.why-img-main {
  background: linear-gradient(135deg, var(--forest) 0%, var(--forest-mid) 100%);
  aspect-ratio: 4/3; border-radius: 2px;
  display: flex; align-items: center; justify-content: center;
  font-size: 6rem; color: rgba(247,242,233,0.15);
  position: relative; overflow: hidden;
}
.why-img-main::after {
  content: '🌿';
  position: absolute; font-size: 8rem;
  opacity: 0.15;
  right: -1rem; bottom: -1rem;
  transform: rotate(-20deg);
}
.why-callout {
  background: var(--amber);
  padding: 1.5rem 2rem;
  display: flex; align-items: center; gap: 1.5rem;
}
.why-callout-num {
  font-family: 'Playfair Display', serif;
  font-size: 2.5rem; color: var(--forest); font-weight: 400; line-height: 1;
}
.why-callout-text { font-size: 0.85rem; color: rgba(30,58,47,0.75); line-height: 1.5; }
.why-callout-text strong { display: block; color: var(--forest); font-size: 0.92rem; }

/* ─── TESTIMONIALS ─── */
#testimonials {
  padding: 6rem 6rem;
  background: var(--cream);
}
.testi-grid {
  display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1.5rem;
  margin-top: 3rem;
}
.testi-card {
  padding: 2rem;
  border: 1px solid rgba(30,58,47,0.1);
  background: var(--cream-warm);
  position: relative;
  transition: box-shadow 0.3s;
}
.testi-card:hover { box-shadow: 0 8px 30px rgba(30,58,47,0.07); }
.testi-card.highlight {
  background: var(--forest); border-color: var(--forest);
}
.testi-stars { color: var(--amber); font-size: 0.85rem; margin-bottom: 1rem; }
.testi-card.highlight .testi-stars { color: var(--amber-light); }
.testi-text {
  font-family: 'Playfair Display', serif;
  font-style: italic; font-size: 1rem;
  color: var(--text); line-height: 1.75;
  margin-bottom: 1.5rem;
}
.testi-card.highlight .testi-text { color: rgba(247,242,233,0.85); }
.testi-author { display: flex; align-items: center; gap: 0.8rem; }
.testi-avatar {
  width: 38px; height: 38px; border-radius: 50%;
  background: var(--sage); color: var(--cream);
  display: flex; align-items: center; justify-content: center;
  font-family: 'Playfair Display', serif; font-size: 0.95rem;
}
.testi-card.highlight .testi-avatar { background: rgba(247,242,233,0.15); }
.testi-name { font-size: 0.85rem; font-weight: 500; color: var(--text); }
.testi-card.highlight .testi-name { color: var(--cream); }
.testi-city { font-size: 0.75rem; color: var(--text-muted); }
.testi-card.highlight .testi-city { color: rgba(247,242,233,0.45); }
.testi-quote-mark {
  position: absolute; top: 1rem; right: 1.5rem;
  font-family: 'Playfair Display', serif; font-size: 4rem;
  color: rgba(196,154,44,0.12); line-height: 1; pointer-events: none;
}
.testi-card.highlight .testi-quote-mark { color: rgba(247,242,233,0.05); }

/* ─── CONTACT ─── */
#contact {
  background: var(--cream-warm);
  padding: 6rem 6rem;
  display: grid; grid-template-columns: 1fr 1.1fr; gap: 6rem;
}
.contact-eyebrow { margin-bottom: 3rem; }
.contact-items { display: flex; flex-direction: column; gap: 1.4rem; margin-top: 2rem; }
.contact-item { display: flex; gap: 1rem; align-items: flex-start; }
.contact-item-icon {
  width: 44px; height: 44px; background: var(--forest);
  display: flex; align-items: center; justify-content: center;
  font-size: 1rem; flex-shrink: 0;
}
.contact-item-title { font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--sage); margin-bottom: 0.2rem; }
.contact-item-val { font-size: 0.92rem; color: var(--text); font-weight: 400; }
.form { display: flex; flex-direction: column; gap: 1.1rem; }
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1.1rem; }
.form-group { display: flex; flex-direction: column; gap: 0.35rem; }
.form-group label { font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--text-muted); font-weight: 500; }
.form-group input, .form-group textarea, .form-group select {
  padding: 0.8rem 1rem;
  border: 1px solid rgba(30,58,47,0.15);
  background: var(--white); color: var(--text);
  font-family: 'DM Sans', sans-serif; font-size: 0.92rem;
  outline: none; transition: border-color 0.25s;
  -webkit-appearance: none;
}
.form-group input:focus, .form-group textarea:focus, .form-group select:focus { border-color: var(--sage); }
.form-group textarea { min-height: 100px; resize: vertical; }
.form-btn {
  background: var(--forest); color: var(--cream);
  border: none; padding: 0.9rem;
  font-family: 'DM Sans', sans-serif; font-size: 0.82rem;
  letter-spacing: 0.14em; text-transform: uppercase; font-weight: 500;
  cursor: pointer; transition: background 0.3s;
  margin-top: 0.3rem;
}
.form-btn:hover { background: var(--forest-mid); }

/* ─── FOOTER ─── */
footer {
  background: #111e17;
  padding: 3.5rem 6rem;
}
.footer-top {
  display: grid; grid-template-columns: 1.5fr 1fr 1fr 1fr;
  gap: 3rem; margin-bottom: 3rem;
  padding-bottom: 3rem;
  border-bottom: 1px solid rgba(247,242,233,0.07);
}
.footer-brand p {
  color: rgba(247,242,233,0.4); font-size: 0.85rem;
  line-height: 1.8; margin-top: 1rem; max-width: 240px;
  font-weight: 300;
}
.footer-logo {
  font-family: 'Playfair Display', serif;
  font-size: 1.4rem; color: var(--cream);
  display: flex; align-items: center; gap: 0.4rem;
}
.footer-logo em { color: var(--amber); font-style: italic; }
.footer-col-title {
  font-size: 0.72rem; letter-spacing: 0.14em; text-transform: uppercase;
  color: rgba(247,242,233,0.4); margin-bottom: 1.2rem; font-weight: 500;
}
.footer-links { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
.footer-links a {
  color: rgba(247,242,233,0.55); font-size: 0.85rem;
  text-decoration: none; transition: color 0.25s;
}
.footer-links a:hover { color: var(--amber-light); }
.footer-bottom { display: flex; align-items: center; justify-content: space-between; }
.footer-bottom p { color: rgba(247,242,233,0.3); font-size: 0.78rem; }
.footer-socials { display: flex; gap: 0.8rem; }
.social-link {
  width: 34px; height: 34px;
  border: 1px solid rgba(247,242,233,0.12);
  display: flex; align-items: center; justify-content: center;
  color: rgba(247,242,233,0.5); font-size: 0.85rem;
  text-decoration: none; transition: border-color 0.3s, color 0.3s;
}
.social-link:hover { border-color: var(--amber); color: var(--amber); }

/* ─── FADE ANIMATIONS ─── */
.fade-up { opacity: 0; transform: translateY(28px); transition: opacity 0.75s ease, transform 0.75s ease; }
.fade-up.visible { opacity: 1; transform: translateY(0); }
.fade-up-delay-1 { transition-delay: 0.1s; }
.fade-up-delay-2 { transition-delay: 0.2s; }
.fade-up-delay-3 { transition-delay: 0.3s; }

/* ─── RESPONSIVE ─── */
@media (max-width: 1024px) {
  nav { padding: 0 2.5rem; }
  #hero { grid-template-columns: 1fr; }
  .hero-content { padding: 4rem 2.5rem; }
  .hero-visual { min-height:
