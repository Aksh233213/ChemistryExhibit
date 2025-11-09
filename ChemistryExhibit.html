<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Chemistry Exhibition 2025 — Dark Electric (Energy Edition)</title>
<script src="https://cdn.tailwindcss.com"></script>
<style>
  :root{
    --bg:#050714;
    --panel:#0c1320;
    --cyan:#00d8ff;
    --violet:#7c3aed;
    --muted:#9aa7b2;
    --glass: rgba(255,255,255,0.03);
    --btn-bg:#06b6d4;
    --btn-text:#021226;
  }
  html { scroll-behavior:smooth; }
  body{
    margin:0;
    font-family:Inter,ui-sans-serif,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
    background:
      radial-gradient(900px 420px at 8% 12%, rgba(124,58,237,0.03), transparent 6%),
      radial-gradient(700px 340px at 92% 88%, rgba(0,216,255,0.02), transparent 6%),
      var(--bg);
    color:#e6f7ff;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    min-height:100vh;
    overflow-x:hidden;
  }

  /* fixed nav */
  nav { position:fixed; top:16px; left:50%; transform:translateX(-50%); z-index:120; width:92%; max-width:1200px; }
  .navglass{ background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.03); backdrop-filter: blur(6px); border-radius:12px; padding:12px 18px; display:flex; align-items:center; justify-content:space-between; gap:12px; }
  .navglass a { color: rgba(230,247,255,0.9); text-decoration:none; font-weight:600; font-size:14px; }

  /* hero */
  .hero {
    background: linear-gradient(180deg, rgba(2,6,23,0.6), rgba(2,6,23,0.85)), url('https://images.unsplash.com/photo-1542534744-8c80a0a9a408?auto=format&fit=crop&w=2000&q=80');
    background-size:cover; background-position:center;
    min-height:88vh; display:flex; align-items:center; justify-content:center; text-align:center; padding:48px 20px; position:relative; overflow:hidden;
  }
  .hero h1 { font-size:clamp(34px,6vw,64px); line-height:1.02; font-weight:900; background: linear-gradient(90deg,var(--cyan),var(--violet)); -webkit-background-clip:text; -webkit-text-fill-color:transparent; letter-spacing:-0.02em; }

  /* canvas layers */
  #bg-canvas, #ripple-canvas { position:absolute; inset:0; z-index:0; pointer-events:none; }

  main { max-width:1200px; margin:56px auto 120px; padding:0 20px; position:relative; z-index:30; }

  /* panels and cards */
  .panel { background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.03); border-radius:12px; padding:16px; box-shadow: 0 22px 48px rgba(2,6,23,0.55); }
  .slider{ display:flex; gap:18px; overflow-x:auto; scroll-snap-type:x mandatory; padding:22px 4px; -webkit-overflow-scrolling:touch; }
  .slide{ min-width:72%; scroll-snap-align:center; border-radius:12px; overflow:hidden; transition:transform .25s ease, box-shadow .25s ease; background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.03); cursor:pointer; }
  .slide:hover{ transform:translateY(-10px); box-shadow: 0 32px 80px rgba(2,6,23,0.6); }
  .slide img{ width:100%; height:440px; object-fit:cover; display:block; filter: saturate(1.05) contrast(1.03); }

  @media (max-width:900px){ .slide{ min-width:92%; } .slide img{ height:260px; } }

  /* person cards clickable */
  .person { cursor:pointer; transition:transform .18s ease, box-shadow .18s ease; }
  .person:hover { transform:translateY(-6px); box-shadow: 0 20px 50px rgba(2,6,23,0.6); }

  /* buttons: toned-down solid */
  .btn { display:inline-block; padding:10px 14px; border-radius:999px; font-weight:700; cursor:pointer; border:none; }
  .btn-ghost { background:transparent; color:rgba(230,247,255,0.9); border:1px solid rgba(255,255,255,0.04); }
  .btn-primary { background:var(--btn-bg); color:var(--btn-text); box-shadow: 0 12px 30px rgba(0,188,212,0.08); transition:transform .15s ease, box-shadow .15s ease; }
  .btn-primary:hover{ transform:translateY(-3px); box-shadow: 0 18px 48px rgba(0,188,212,0.12); }

  /* small translucent bio window (faded) */
  .bio-overlay{ position:fixed; right:24px; bottom:24px; width:360px; max-width:calc(100% - 48px); z-index:160; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.04); padding:14px; border-radius:12px; box-shadow:0 30px 80px rgba(2,6,23,0.6); backdrop-filter: blur(6px); color:#e6f7ff; }

  /* reveal animations */
  .reveal { opacity:0; transform:translateY(18px); transition:opacity .6s ease, transform .6s ease; will-change:opacity, transform; }
  .reveal.show { opacity:1; transform:translateY(0); }

  /* heading shimmer */
  .shimmer { position:relative; overflow:hidden; display:inline-block; }
  .shimmer::after{ content:""; position:absolute; inset:0; left:-60%; width:60%; background:linear-gradient(90deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.18) 50%, rgba(255,255,255,0) 100%); transform:skewX(-18deg); animation: shimmer 3.8s linear infinite; pointer-events:none; opacity:0.5; }
  @keyframes shimmer { 0%{ left:-60% } 100%{ left:160% } }

  /* detail view container */
  #detailView { display:none; padding-top:120px; padding-bottom:80px; min-height:60vh; position:relative; z-index:40; }
  .detail-enter { animation: detailIn .42s cubic-bezier(.2,.9,.25,1) both; }
  @keyframes detailIn { from { opacity:0; transform:translateY(18px) scale(.996); } to { opacity:1; transform:translateY(0) scale(1);} }

  /* energy wave visual styles (for CSS fallback visuals) */
  .energy-attach { position:relative; overflow:visible; }

  /* footer small wave */
  footer { text-align:center; color:rgba(230,247,255,0.6); padding-bottom:40px; margin-top:28px; }

  .muted{ color:var(--muted); }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="navglass mx-auto" style="max-width:1200px;">
    <div style="display:flex;align-items:center;gap:12px;">
      <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(90deg,var(--cyan),var(--violet));display:flex;align-items:center;justify-content:center;font-weight:900;color:#021226">CE</div>
      <div>
        <div style="font-weight:900;color:#e6f7ff">Chemistry Exhibition</div>
        <div style="font-size:12px;color:rgba(230,247,255,0.65)">2025 — Department of Chemical Sciences</div>
      </div>
    </div>

    <div style="display:flex;gap:16px;align-items:center;">
      <a href="#" class="navlink" data-scroll="home">Home</a>
      <a href="#about" class="navlink" data-scroll="about">About</a>
      <a href="#team" class="navlink" data-scroll="team">Team</a>
      <a href="#teachers" class="navlink" data-scroll="teachers">Teachers</a>
      <a href="#exhibits" class="navlink" data-scroll="exhibits">Exhibits</a>
      <a href="#exchange" class="navlink" data-scroll="exchange">Exchange</a>
      <a href="#contact" class="navlink" data-scroll="contact">Contact</a>
    </div>
  </div>
</nav>

<!-- HERO -->
<header id="home" class="hero relative">
  <canvas id="bg-canvas"></canvas>
  <canvas id="ripple-canvas"></canvas>

  <div style="z-index:40; max-width:1100px; padding:28px;">
    <h1 class="shimmer">CHEMISTRY EXHIBITION <span style="display:block;font-size:18px;color:rgba(230,247,255,0.75);font-weight:700;margin-top:8px">2025 — From molecules to materials</span></h1>
    <p style="margin-top:18px;color:rgba(230,247,255,0.88);font-size:18px;max-width:840px;margin-left:auto;margin-right:auto;">
      A dynamic, high-energy showcase of experiments, research and global exchange. Click exhibits or exchange items to open their full in-site pages with energy wave transitions and immersive audio.
    </p>

    <div style="margin-top:24px;display:flex;gap:12px;justify-content:center;">
      <button class="btn btn-primary" id="exploreBtn">Explore Exhibits</button>
      <a href="#exchange" class="btn btn-ghost">See Exchange</a>
    </div>
  </div>
</header>

<main id="mainView">

  <!-- ABOUT -->
  <section id="about" class="mt-8 mb-8 reveal">
    <div style="display:grid;grid-template-columns:1fr 360px;gap:22px;align-items:start;">
      <div>
        <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">About the Exhibition</h2>
        <p class="muted" style="margin-top:10px;line-height:1.6">
          Chemistry Exhibition 2025 brings student research to the public and connects industry & international experiences with local learning. Expect exhibits on nanotechnology, green chemistry, space chemistry, forensic analysis, polymer innovations and exchange journeys to industry leaders and world labs.
        </p>
      </div>
      <div class="panel reveal">
        <div style="font-weight:800;color:var(--cyan)">Event snapshot</div>
        <ul style="margin-top:10px;color:rgba(230,247,255,0.9);line-height:1.6">
          <li><strong>When:</strong> Full-day event (see schedule)</li>
          <li><strong>Where:</strong> Main Hall & Research Labs</li>
          <li><strong>Audience:</strong> Students, educators, public visitors</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- TEAM -->
  <section id="team" class="mb-10 reveal">
    <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">Student Team</h2>
    <p class="muted" style="margin-top:8px">Core student organizers (exact names preserved).</p>

    <div style="margin-top:12px;display:grid;grid-template-columns:repeat(4,1fr);gap:14px;">
      <!-- Arjun -->
      <div class="panel person" tabindex="0" role="button" onclick="openBio('arjun')" onkeypress="if(event.key==='Enter') openBio('arjun')">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(90deg,var(--cyan),var(--violet));display:flex;align-items:center;justify-content:center;font-weight:900;color:#021226">A</div>
          <div>
            <div style="font-weight:900">Arjun Tosawad</div>
            <div class="muted">President</div>
          </div>
        </div>
        <p class="muted" style="margin-top:8px">Leads coordination, presentation, and safety for high-impact demonstrations (organic & public-safety focus).</p>
      </div>

      <!-- XXX -->
      <div class="panel person" tabindex="0" role="button" onclick="openBio('xxx')" onkeypress="if(event.key==='Enter') openBio('xxx')">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(90deg,#8b5cf6,#06b6d4);display:flex;align-items:center;justify-content:center;font-weight:900;color:#021226">X</div>
          <div>
            <div style="font-weight:900">XXX</div>
            <div class="muted">Secretary</div>
          </div>
        </div>
        <p class="muted" style="margin-top:8px">Documentation, scheduling and communications lead.</p>
      </div>

      <!-- YYY -->
      <div class="panel person" tabindex="0" role="button" onclick="openBio('yyy')" onkeypress="if(event.key==='Enter') openBio('yyy')">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(90deg,#00d8ff,#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:900;color:#021226">Y</div>
          <div>
            <div style="font-weight:900">YYY</div>
            <div class="muted">Vice President</div>
          </div>
        </div>
        <p class="muted" style="margin-top:8px">Oversees exhibit fabrication and safety systems; materials & scale-up focus.</p>
      </div>

      <!-- ZZZ -->
      <div class="panel person" tabindex="0" role="button" onclick="openBio('zzz')" onkeypress="if(event.key==='Enter') openBio('zzz')">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:56px;height:56px;border-radius:12px;background:linear-gradient(90deg,#7c3aed,#00d8ff);display:flex;align-items:center;justify-content:center;font-weight:900;color:#021226">Z</div>
          <div>
            <div style="font-weight:900">ZZZ</div>
            <div class="muted">IT & Tech Head</div>
          </div>
        </div>
        <p class="muted" style="margin-top:8px">Manages interactive displays, projection mapping and site tech.</p>
      </div>
    </div>
  </section>

  <!-- TEACHERS -->
  <section id="teachers" class="mb-12 reveal">
    <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">Faculty & Mentors</h2>
    <div style="margin-top:12px;display:grid;grid-template-columns:repeat(3,1fr);gap:14px;">
      <div class="panel person" tabindex="0" role="button" onclick="openBio('sankalp')" onkeypress="if(event.key==='Enter') openBio('sankalp')">
        <div style="font-weight:900;color:var(--cyan)">Mr. Sankalp Maheshwari</div>
        <div class="muted" style="margin-top:6px">Professor of Organic Chemistry</div>
        <p class="muted" style="margin-top:8px">Leads experimental design and pyrotechnics demonstrations; safety-first approach to dynamic displays and synthesis.</p>
      </div>

      <div class="panel person" tabindex="0" role="button" onclick="openBio('ankita')" onkeypress="if(event.key==='Enter') openBio('ankita')">
        <div style="font-weight:900;color:var(--cyan)">Mrs. Ankita Sharma</div>
        <div class="muted" style="margin-top:6px">Associate Professor — Materials & Nanotech</div>
        <p class="muted" style="margin-top:8px">Mentors nanotech exhibits and materials characterization workflows.</p>
      </div>

      <div class="panel person" tabindex="0" role="button" onclick="openBio('sudeep')" onkeypress="if(event.key==='Enter') openBio('sudeep')">
        <div style="font-weight:900;color:var(--cyan)">Mr. Sudeep XYZ</div>
        <div class="muted" style="margin-top:6px">Lecturer — Physical & Analytical Chemistry</div>
        <p class="muted" style="margin-top:8px">Leads forensic chemistry demos and spectroscopy workshops.</p>
      </div>
    </div>
  </section>

  <!-- EXHIBITS -->
  <section id="exhibits" class="mb-12 reveal">
    <div style="display:flex;justify-content:space-between;align-items:center">
      <div>
        <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">Featured Exhibits</h2>
        <div class="muted" style="margin-top:6px">Click or press Enter to open the exhibit page (same tab). Energy wave + audio will play during the transition.</div>
      </div>
      <div style="display:flex;gap:10px">
        <button onclick="scrollSlider(-1)" class="px-3 py-2 rounded bg-white/5">Prev</button>
        <button onclick="scrollSlider(1)" class="px-3 py-2 rounded" style="background:var(--btn-bg);color:var(--btn-text)">Next</button>
      </div>
    </div>

    <div class="slider mt-6" id="slider">
      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('chem-space')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('chem-space')">
        <img src="https://images.unsplash.com/photo-1581091870623-3f40b7b1c3a2?auto=format&fit=crop&w=1800&q=80" alt="Chemistry in space microgravity lab">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">Chemistry in Space</div>
          <div class="muted" style="margin-top:6px">Astrochemistry: microgravity reactions, propellants and life-support systems.</div>
        </div>
      </div>

      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('green-chemistry')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('green-chemistry')">
        <img src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?auto=format&fit=crop&w=1800&q=80" alt="green chemistry lab">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">Green Chemistry Revolution</div>
          <div class="muted" style="margin-top:6px">Sustainable syntheses, recyclable catalysts and biodegradable polymers.</div>
        </div>
      </div>

      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('nanotech')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('nanotech')">
        <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1800&q=80" alt="nanotechnology">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">Nanotechnology in Medicine</div>
          <div class="muted" style="margin-top:6px">Nanoparticles, targeted delivery and diagnostics.</div>
        </div>
      </div>

      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('forensic')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('forensic')">
        <img src="https://images.unsplash.com/photo-1602524815744-6e2b4d3df5aa?auto=format&fit=crop&w=1800&q=80" alt="forensic chemistry lab">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">Forensic & Analytical Chemistry</div>
          <div class="muted" style="margin-top:6px">Chromatography, mass spec and crime-scene simulation.</div>
        </div>
      </div>

      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('polymer')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('polymer')">
        <img src="https://images.unsplash.com/photo-1517976487492-0c3b6f8d8f2d?auto=format&fit=crop&w=1800&q=80" alt="polymers">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">Polymer Art & Smart Materials</div>
          <div class="muted" style="margin-top:6px">Shape-memory polymers and wearable chemistry.</div>
        </div>
      </div>

      <div class="slide" tabindex="0" role="button" onclick="triggerEnergyAndOpen('fireworks')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('fireworks')">
        <img src="https://images.unsplash.com/photo-1509395176047-4a66953fd231?auto=format&fit=crop&w=1800&q=80" alt="fireworks chemistry">
        <div style="padding:12px">
          <div style="font-weight:900;color:#e6f7ff">The Chemistry of Fireworks</div>
          <div class="muted" style="margin-top:6px">Metal salts and oxidizers for color (safety emphasized).</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EXCHANGE (new section) -->
  <section id="exchange" class="mb-12 reveal">
    <div style="display:flex;justify-content:space-between;align-items:center;">
      <div>
        <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">Exchange & Industry Visits</h2>
        <div class="muted" style="margin-top:6px">International and industrial experiences that inspired our exhibits — click to view full trip reports.</div>
      </div>
    </div>

    <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:12px;">
      <div class="panel person" tabindex="0" role="button" onclick="triggerEnergyAndOpen('marble-factory')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('marble-factory')">
        <h3 style="font-weight:900;color:#e6f7ff">Marble Factory Visit</h3>
        <p class="muted" style="margin-top:8px">An in-depth industrial visit to understand the chemistry of carbonate rocks and processing.</p>
      </div>

      <div class="panel person" tabindex="0" role="button" onclick="triggerEnergyAndOpen('spain-forensics')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('spain-forensics')">
        <h3 style="font-weight:900;color:#e6f7ff">Spain — Forensic Labs</h3>
        <p class="muted" style="margin-top:8px">Hands-on learning in Spanish forensic research centers and labs.</p>
      </div>

      <div class="panel person" tabindex="0" role="button" onclick="triggerEnergyAndOpen('cern')" onkeypress="if(event.key==='Enter') triggerEnergyAndOpen('cern')">
        <h3 style="font-weight:900;color:#e6f7ff">CERN, Switzerland</h3>
        <p class="muted" style="margin-top:8px">A technical visit to particle detection, materials under irradiation and analytical techniques.</p>
      </div>
    </div>
  </section>

  <!-- SCHEDULE -->
  <section id="schedule" class="mb-12 reveal">
    <h2 style="font-size:22px;font-weight:900;color:#e6f7ff">Event Schedule</h2>
    <div style="display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:12px">
      <div class="panel">9:00 AM — Opening Ceremony & Keynote</div>
      <div class="panel">10:00 AM — Guided Exhibit Walkthrough</div>
      <div class="panel">12:30 PM — Lunch & Poster Talks</div>
      <div class="panel">2:00 PM — Interactive Demonstrations (Hands-on)</div>
      <div class="panel">4:00 PM — Awards & Closing Remarks</div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="mb-24 reveal">
    <div style="display:flex;gap:18px;align-items:center;justify-content:space-between;">
      <div>
        <h3 style="font-weight:900;color:#e6f7ff">Contact & Inquiries</h3>
        <p class="muted" style="margin-top:8px">For collaborations, media requests, or participation contact:</p>
        <div style="margin-top:8px;color:var(--cyan);font-weight:800">chemexpo2025@school.edu</div>
      </div>
      <div class="panel">
        <div style="font-weight:900;color:var(--violet)">Venue</div>
        <div class="muted" style="margin-top:6px">Main campus — Exhibition Hall & Research Labs</div>
        <div style="font-weight:900;color:var(--violet);margin-top:12px">Organizers</div>
        <div class="muted" style="margin-top:6px">Department of Chemical Sciences</div>
      </div>
    </div>
  </section>

  <footer>© 2025 Chemistry Exhibition — Department of Chemical Sciences</footer>
</main>

<!-- DETAIL VIEW (single-file page content displayed here) -->
<section id="detailView" style="display:none; padding-top:120px; padding-bottom:80px; min-height:60vh; position:relative; z-index:50;">
  <div id="detailContent" style="max-width:1100px;margin:0 auto;padding:18px;"></div>
</section>

<!-- bio overlay (small faded window) -->
<div id="bioContainer" style="display:none;"></div>

<!-- modal (preview) -->
<div id="modal" style="display:none;position:fixed;inset:0;align-items:center;justify-content:center;background:rgba(2,6,23,0.75);z-index:180;padding:28px;">
  <div style="width:100%;max-width:880px;border-radius:12px;background:linear-gradient(180deg,#071022,#071426);border:1px solid rgba(255,255,255,0.04);padding:18px;color:#e6f7ff">
    <div style="display:flex;justify-content:space-between;align-items:center;">
      <div>
        <div id="modalTitle" style="font-weight:900;color:var(--cyan)"></div>
        <div id="modalSub" style="color:rgba(230,247,255,0.8);margin-top:6px">Quick preview</div>
      </div>
      <div><button onclick="closeModal()" style="padding:8px 10px;border-radius:8px;border:1px solid rgba(255,255,255,0.03);background:transparent;color:#e6f7ff">Close</button></div>
    </div>
    <div id="modalContent" style="margin-top:12px;color:rgba(230,247,255,0.9);line-height:1.6"></div>
  </div>
</div>

<script>
/* ----------------------------
  Particle background canvas
-----------------------------*/
(() => {
  const canvas = document.getElementById('bg-canvas');
  const dpr = Math.max(1, window.devicePixelRatio || 1);
  let w, h, ctx, particles = [];

  function resize() {
    w = canvas.width = Math.max(document.documentElement.clientWidth, window.innerWidth) * dpr;
    h = canvas.height = Math.max(document.documentElement.clientHeight, window.innerHeight) * dpr;
    canvas.style.width = (w / dpr) + 'px';
    canvas.style.height = (h / dpr) + 'px';
    if(!ctx) ctx = canvas.getContext('2d');
  }

  function rand(min, max) { return Math.random() * (max - min) + min; }

  function initParticles() {
    particles = [];
    const count = Math.round((w / dpr) * (h / dpr) / 75000); // denser for dynamic feel
    for(let i=0;i<count;i++){
      particles.push({
        x: Math.random() * w,
        y: Math.random() * h,
        r: rand(1.2, 3.6) * dpr,
        vx: rand(-0.35, 0.35) * dpr,
        vy: rand(-0.22, 0.22) * dpr,
        hue: rand(180, 270)
      });
    }
  }

  function draw() {
    ctx.clearRect(0,0,w,h);
    // faint gradient vignette
    const grad = ctx.createRadialGradient(w*0.2, h*0.12, 0, w*0.5, h*0.5, Math.max(w,h));
    grad.addColorStop(0, 'rgba(124,58,237,0.02)');
    grad.addColorStop(1, 'rgba(0,0,0,0)');
    ctx.fillStyle = grad;
    ctx.fillRect(0,0,w,h);

    // lines
    for(let i=0;i<particles.length;i++){
      const p = particles[i];
      for(let j=i+1;j<particles.length;j++){
        const q = particles[j];
        const dx = p.x - q.x, dy = p.y - q.y;
        const dist = Math.sqrt(dx*dx + dy*dy);
        if(dist < 120 * dpr){
          const alpha = 0.12 * (1 - dist / (120*dpr));
          ctx.strokeStyle = `rgba(120,80,255,${alpha})`;
          ctx.lineWidth = 0.5 * dpr;
          ctx.beginPath();
          ctx.moveTo(p.x, p.y);
          ctx.lineTo(q.x, q.y);
          ctx.stroke();
        }
      }
    }

    // particles
    for(const p of particles){
      ctx.beginPath();
      const g = ctx.createRadialGradient(p.x - 1*p.r, p.y - 1*p.r, 0, p.x, p.y, p.r*2);
      g.addColorStop(0, 'rgba(0,216,255,0.9)');
      g.addColorStop(0.5, 'rgba(124,58,237,0.8)');
      g.addColorStop(1, 'rgba(0,0,0,0)');
      ctx.fillStyle = g;
      ctx.arc(p.x, p.y, p.r, 0, Math.PI*2);
      ctx.fill();
    }
  }

  function step() {
    for(const p of particles){
      p.x += p.vx;
      p.y += p.vy;
      if(p.x < -20*dpr) p.x = w + 20*dpr;
      if(p.x > w + 20*dpr) p.x = -20*dpr;
      if(p.y < -20*dpr) p.y = h + 20*dpr;
      if(p.y > h + 20*dpr) p.y = -20*dpr;
    }
    draw();
    requestAnimationFrame(step);
  }

  function start() { resize(); initParticles(); step(); }

  window.addEventListener('resize', () => { resize(); initParticles(); });
  start();
})();

/* ----------------------------
  Ripple / energy wave canvas + WebAudio for sounds
-----------------------------*/
const rippleCanvas = document.getElementById('ripple-canvas');
const rc = rippleCanvas.getContext ? rippleCanvas.getContext('2d') : null;
const DPR = Math.max(1, window.devicePixelRatio || 1);
let rw, rh;
function resizeRipple(){
  if(!rippleCanvas) return;
  rw = rippleCanvas.width = Math.max(document.documentElement.clientWidth, window.innerWidth) * DPR;
  rh = rippleCanvas.height = Math.max(document.documentElement.clientHeight, window.innerHeight) * DPR;
  rippleCanvas.style.width = (rw / DPR) + 'px';
  rippleCanvas.style.height = (rh / DPR) + 'px';
}
resizeRipple();
window.addEventListener('resize', resizeRipple);

let ripples = [];
function createRipple(x, y, color='#66f0ff', maxR=700, duration=900){
  ripples.push({x:x*DPR, y:y*DPR, t:performance.now(), maxR, color, duration});
  // schedule cleanup
  setTimeout(()=> {
    // remove old ones in draw loop
  }, duration + 50);
}
function drawRipples(){
  if(!rc) return;
  rc.clearRect(0,0,rw,rh);
  const now = performance.now();
  for(let i=ripples.length-1;i>=0;i--){
    const r = ripples[i];
    const elapsed = now - r.t;
    const progress = Math.min(1, elapsed / r.duration);
    const radius = r.maxR * easeOutCubic(progress);
    const alpha = 0.85 * (1 - progress);
    // radial gradient stroke
    rc.beginPath();
    rc.lineWidth = 6 * (1 - progress) + 1;
    rc.strokeStyle = hexToRgba(r.color, alpha);
    rc.arc(r.x, r.y, radius, 0, Math.PI*2);
    rc.stroke();
    if(progress >= 1) ripples.splice(i,1);
  }
}
function loopRipples(){
  drawRipples();
  requestAnimationFrame(loopRipples);
}
loopRipples();

function easeOutCubic(t){ return 1 - Math.pow(1 - t, 3); }
function hexToRgba(hex, a){ 
  // accept #rrggbb or rgb values
  if(hex.startsWith('#')) {
    const bigint = parseInt(hex.slice(1),16);
    const r = (bigint>>16)&255, g=(bigint>>8)&255, b=bigint&255;
    return `rgba(${r},${g},${b},${a})`;
  }
  return hex;
}

/* WebAudio: small sonic palette for energy wave + hum */
const AudioCtx = window.AudioContext || window.webkitAudioContext;
let audioCtx = null;
function ensureAudio(){
  if(!audioCtx) audioCtx = new AudioCtx();
}
function playEnergySound(type='pulse'){
  ensureAudio();
  if(!audioCtx) return;
  const now = audioCtx.currentTime;
  // master gain
  const gain = audioCtx.createGain(); gain.connect(audioCtx.destination); gain.gain.value = 0.0001;
  // small fade-in to avoid clicks
  gain.gain.linearRampToValueAtTime(0.18, now + 0.01);
  // a short metallic chime + sub bass swoop
  if(type === 'pulse'){
    // metallic noise-ish with bandpass filter
    const o = audioCtx.createOscillator();
    o.type = 'triangle';
    o.frequency.setValueAtTime(520, now);
    const g2 = audioCtx.createGain(); g2.gain.value = 0.0;
    o.connect(g2);
    const hp = audioCtx.createBiquadFilter(); hp.type='highpass'; hp.frequency.value=220;
    g2.connect(hp); hp.connect(gain);
    o.start(now);
    // envelope
    g2.gain.setValueAtTime(0.0001, now);
    g2.gain.exponentialRampToValueAtTime(0.9, now + 0.02);
    g2.gain.exponentialRampToValueAtTime(0.001, now + 0.6);
    o.frequency.exponentialRampToValueAtTime(180, now + 0.6);
    o.stop(now + 0.9);
  }
  // sub-swoop
  const sub = audioCtx.createOscillator();
  sub.type = 'sine';
  sub.frequency.setValueAtTime(120, now);
  const subG = audioCtx.createGain(); subG.gain.value = 0.0;
  sub.connect(subG); subG.connect(gain);
  subG.gain.setValueAtTime(0.0001, now);
  subG.gain.exponentialRampToValueAtTime(0.12, now + 0.03);
  subG.gain.exponentialRampToValueAtTime(0.0001, now + 0.7);
  sub.frequency.exponentialRampToValueAtTime(60, now + 0.6);
  sub.start(now); sub.stop(now + 0.9);

  // final tiny click
  setTimeout(()=> { gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 0.02); }, 800);
}

/* ----------------------------
  SPA data for exhibits & exchange (detailed, "extreme")
-----------------------------*/
const PAGES = {
  // exhibits
  'chem-space': {
    title: 'Chemistry in Space',
    subtitle: 'Microgravity reactions, propellants, and life-support chemistry — deep field report',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">During this exhibit we present experiments and visual data exploring how gravity (or the lack of it) changes nucleation, crystal growth, diffusion-limited reactions and flame behavior. This page collects our experiment designs, raw imagery (placeholders), and stepwise analysis.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Experiment summaries</h4>
      <p class="muted">1) <strong>Crystallization under microgravity:</strong> comparative analysis with Earth-grown crystals. Observed: more isotropic morphologies, fewer defects for certain salts. Mechanistic notes on diffusion-limited aggregation and solvent transport.</p>
      <p class="muted">2) <strong>Combustion & flame chemistry:</strong> combustion in reduced convection — different soot formation routes, diffusion flame envelopes; implications for spacecraft fire safety and propellant engineering.</p>
      <p class="muted">3) <strong>Life-support chemistry:</strong> catalytic CO<sub>2</sub> scrubbing materials, water recovery sorbents and microbe-safe AEM membranes tested in bench-scale simulators.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Visuals & placeholders</h4>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Mission photo placeholder</div>
        <div class="panel photo-placeholder">Crystallization micrograph placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Takeaways</h4>
      <p class="muted">Microgravity offers unique parameter space: altered mass transport, suppressed convection, and novel nucleation pathways. For mission planning, this impacts propellant management, material synthesis and on-orbit manufacturing potential.</p>
    `
  },

  'green-chemistry': {
    title: 'Green Chemistry Revolution',
    subtitle: 'Low-waste syntheses, catalytic recycling, and life-cycle analysis (detailed field notes)',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">This exhibit documents multiple projects: solvent-free mechanochemical syntheses, recyclable heterogeneous catalysts, enzymatic cascade conversions, and cradle-to-gate life-cycle metrics comparing legacy versus green workflows.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Project highlights</h4>
      <p class="muted">• <strong>Mechanochemistry:</strong> ball-mill enabled couplings with near-zero solvent usage. Reaction profiles and energy consumption charts included as placeholders.</p>
      <p class="muted">• <strong>Biopolymer development:</strong> biodegradable polymer films from agricultural waste — tensile & thermal properties characterized.</p>
      <p class="muted">• <strong>Catalyst recovery:</strong> magnetic nanoparticle-supported catalysts enabling reuse with minimal leaching (ICP-MS checks).</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Visuals & data</h4>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Process schematic placeholder</div>
        <div class="panel photo-placeholder">Life-cycle chart placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Impact</h4>
      <p class="muted">Quantified reductions in solvent use and waste generation, with practical suggestions for laboratory adoption of green protocols.</p>
    `
  },

  'nanotech': {
    title: 'Nanotechnology in Medicine',
    subtitle: 'Synthesis, targeting, imaging — detailed experimental notes & characterization',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">Our nanotech exhibit focuses on nanoparticle design for targeted drug delivery, imaging contrast agents, and controlled release kinetics. Included: synthesis protocols, DLS/TEM micrographs (placeholders), and biodistribution modeling summaries.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Key experiments</h4>
      <p class="muted">• <strong>PEGylated liposomal systems:</strong> surface modification to extend circulation half-life; release profiles shown conceptually.</p>
      <p class="muted">• <strong>Targeting ligands:</strong> small molecule vs peptide-based targeting and their receptor-mediated uptake efficiencies in cell-line assays.</p>
      <p class="muted">• <strong>Characterization:</strong> TEM micrographs, size distributions (DLS), zeta-potential analysis and basic cytotoxicity panels.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">TEM micrograph placeholder</div>
        <div class="panel photo-placeholder">Particle size chart placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Clinical relevance</h4>
      <p class="muted">Design choices directly influence pharmacokinetics; ongoing studies emphasize safe-by-design approaches and translational pathways for clinical use.</p>
    `
  },

  'forensic': {
    title: 'Forensic & Analytical Chemistry',
    subtitle: 'Crime-scene simulation, chromatography, mass spec and data interpretation (field report)',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">This exhibit demonstrates modern analytical techniques used in forensics: gas chromatography–mass spectrometry (GC–MS), liquid chromatography–tandem mass spectrometry (LC–MS/MS), and spectroscopy-based methods for trace evidence.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Demonstrations</h4>
      <p class="muted">• <strong>Chromatography:</strong> simulated sample separation with visualization of retention differences for volatile substances.</p>
      <p class="muted">• <strong>Mass spec:</strong> concept demo showing fragmentation patterns and library matching used to identify unknowns.</p>
      <p class="muted">• <strong>Evidence workflow:</strong> simulated chain-of-custody procedures and contamination prevention checks.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Chromatogram placeholder</div>
        <div class="panel photo-placeholder">Instrument photo placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Field application</h4>
      <p class="muted">Visitors learn how analytical data supports investigations, and see the critical importance of sample handling, instrument calibration and interpretation rigor in forensic conclusions.</p>
    `
  },

  'polymer': {
    title: 'Polymer Art & Smart Materials',
    subtitle: 'Shape-memory systems, responsive polymers and wearable chemistry — demonstrated & documented',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">Interactive exhibits showing polymers that respond to heat, light or pH changes — shape-memory effects, soft robotics-inspired materials and interactive art pieces illustrating polymer chemistry.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Highlights</h4>
      <p class="muted">• <strong>Shape-memory demonstrations:</strong> programming & recovery cycles with temperature triggers.</p>
      <p class="muted">• <strong>Responsive hydrogels:</strong> swelling/deswelling visual demos and application notes for sensors.</p>
      <p class="muted">• <strong>Wearables:</strong> soft-conductive polymer leads for interactive garments (demo concept).</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Demo placeholder</div>
        <div class="panel photo-placeholder">Wearable sample placeholder</div>
      </div>
    `
  },

  'fireworks': {
    title: 'The Chemistry of Fireworks',
    subtitle: 'Pyrotechnic color chemistry — metal salts, oxidizers and safe demo design',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">Educational breakdown of how metal ions produce characteristic colors (Sr for red, Ba for green, Cu for blue, Na for yellow), and how oxidizers, binders and burn rates shape pyrotechnic performance. Safety and small-scale demonstration techniques are emphasized.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Ingredients & color mechanics</h4>
      <p class="muted">• <strong>Colorants:</strong> selective excitation & emission of metal cations in a hot flame environment; spectral explanation and demo spectra (placeholder).</p>
      <p class="muted">• <strong>Oxidizers & fuel balance:</strong> how oxidizer choices affect burn temperature & color purity.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Color sample placeholder</div>
        <div class="panel photo-placeholder">Demo setup placeholder</div>
      </div>
    `
  },

  // exchange items
  'marble-factory': {
    title: 'Marble Factory Visit — Industrial Materials Report',
    subtitle: 'From limestone geology to marble polishing: a detailed industrial account',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">The team visited a working marble extraction & processing plant to study the chemistry and engineering of carbonate rock processing. Our notes cover mineralogy, quarrying, cutting, polishing, fabrication chemistry and waste handling.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">What we observed</h4>
      <p class="muted"><strong>Geology:</strong> marble forms from metamorphism of limestone — primarily calcite (CaCO₃) — and often shows banding, recrystallization and impurity-driven coloration. We examined local strata and sampling protocols.</p>
      <p class="muted"><strong>Processing:</strong> block cutting uses diamond-wire saws; slurry containing fine CaCO₃ particulates is produced and must be treated. Polishing uses abrasive sequences and chemical sealants (polymeric sealants) to improve surface gloss and stain resistance.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Chemistry & environmental notes</h4>
      <p class="muted">Calcination (if practiced on-site for lime production) and slurry handling produce CO₂-related process streams; water recycling measures were discussed. Dust control (fine CaCO₃ particles) and occupational health practices were inspected.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Quarry/photo placeholder</div>
        <div class="panel photo-placeholder">Polishing/fabrication placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Conclusions</h4>
      <p class="muted">Industrial chemistry at scale emphasizes materials handling, worker safety and waste-water management. The visit informed our materials exhibit sections and polymer sealant choices for sample displays.</p>
    `
  },

  'spain-forensics': {
    title: 'Spain Forensic Labs — International Exchange Report',
    subtitle: 'Laboratory methods, case work, and collaborative learning in Spanish forensic centers',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">Our delegation visited Spanish forensic research centers to observe modern analytical pipelines. We documented lab workflows, mass spectrometry best practices, DNA analysis pipelines, and chain-of-custody protocols across multiple units.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Lab techniques observed</h4>
      <p class="muted">• <strong>GC–MS / LC–MS workflows:</strong> sample prep, instrument calibration, and interpretation sessions with real-case anonymized datasets.</p>
      <p class="muted">• <strong>DNA & sequencing:</strong> high-throughput extraction, library prep, and sequence matching discussion for forensic genetics.</p>
      <p class="muted">• <strong>Digital forensics integration:</strong> how chemical evidence integrates with digital timelines and metadata in modern casework.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Lab instrument photo placeholder</div>
        <div class="panel photo-placeholder">Chromatogram / data placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Reflections</h4>
      <p class="muted">International exchange highlighted protocol standardization, validation steps, and the role of cross-lab comparison studies. Students gained hands-on exposure to evidence workflows, instrument maintenance, and data integrity practices.</p>
    `
  },

  'cern': {
    title: 'CERN, Switzerland — Particle & Materials Interactions',
    subtitle: 'Detector materials, radiation chemistry and analytical detection — technical visit summary',
    content: `
      <h3 style="font-weight:800;color:var(--cyan)">Overview</h3>
      <p class="muted">At CERN we toured detector facilities and materials labs investigating how high-energy radiation interacts with materials. Focus areas included scintillator chemistry, radiation damage testing, and analytical detection of activation products.</p>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Highlights</h4>
      <p class="muted">• <strong>Detector materials:</strong> scintillators, silicon detectors and polymer substrates were examined. Chemistry of dopants and wavelength-shifters used in scintillation media was discussed.</p>
      <p class="muted">• <strong>Radiation effects:</strong> materials testing under controlled irradiation to observe embrittlement, discoloration and changes in electronic properties.</p>
      <p class="muted">• <strong>Radiochemistry:</strong> measurement of activation products and safe handling procedures; analytical techniques used to quantify induced radioisotopes.</p>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:8px">
        <div class="panel photo-placeholder">Detector lab placeholder</div>
        <div class="panel photo-placeholder">Material test placeholder</div>
      </div>

      <h4 style="margin-top:12px;font-weight:800;color:var(--violet)">Learning outcomes</h4>
      <p class="muted">Students learned real-world applications of chemistry at extreme conditions, and how materials chemistry supports particle physics instrumentation and long-term detector performance.</p>
    `
  }
};

/* ----------------------------
  SPA navigation & transitions
-----------------------------*/
const mainView = document.getElementById('mainView');
const detailView = document.getElementById('detailView');
const detailContent = document.getElementById('detailContent');

function renderPage(key){
  const page = PAGES[key];
  if(!page) return;
  // push history
  history.pushState({page:key}, '', `#${key}`);
  // swap views
  mainView.style.display = 'none';
  detailView.style.display = 'block';
  detailContent.innerHTML = `
    <div class="panel detail-enter">
      <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:18px">
        <div style="flex:1 1 64%">
          <h1 style="font-size:28px;font-weight:900;color:var(--cyan)">${page.title}</h1>
          <div style="margin-top:8px;color:rgba(230,247,255,0.88);font-weight:700">${page.subtitle}</div>
          <div style="margin-top:12px;color:rgba(230,247,255,0.92)">${page.content}</div>
        </div>
        <aside style="width:320px">
          <div class="panel">
            <div style="font-weight:900;color:var(--violet)">Quick Info</div>
            <div class="muted" style="margin-top:8px">Use the Back button to return to the main exhibit list. Media placeholders may be replaced later with high-resolution images.</div>
            <div style="margin-top:12px;display:flex;gap:8px;">
              <button class="btn btn-primary" onclick="playEnergySound();">Play energy</button>
              <button class="btn btn-ghost" onclick="goBack()">Back</button>
            </div>
          </div>
        </aside>
      </div>
    </div>
  `;
  // small entrance animation for placeholders (if any)
  detailView.scrollIntoView({behavior:'smooth', block:'start'});
}

function goBack(){
  history.pushState({page:'main'}, '', location.pathname);
  detailView.style.display = 'none';
  mainView.style.display = 'block';
  window.scrollTo({top:0, behavior:'smooth'});
}

// handle browser back/forward
window.addEventListener('popstate', (e) => {
  const st = e.state;
  if(!st || st.page === 'main'){
    detailView.style.display = 'none';
    mainView.style.display = 'block';
  } else {
    renderPage(st.page);
  }
});

/* triggerEnergyAndOpen: ripple + sound + render page after short delay */
function triggerEnergyAndOpen(key){
  // calculate center of viewport for ripple
  const x = window.innerWidth * 0.5;
  const y = window.innerHeight * 0.28;
  createRipple(x, y, '#66e7ff', 800, 1100);
  playEnergySound('pulse');
  setTimeout(()=> renderPage(key), 380);
}

/* showDetail wrapper for older handlers */
function openDetail(key){ triggerEnergyAndOpen(key); }

/* small slider helper */
const slider = document.getElementById('slider');
function scrollSlider(dir){
  if(!slider) return;
  const step = slider.clientWidth * 0.78;
  slider.scrollBy({left: dir * step, behavior:'smooth'});
}

/* ----------------------------
  Bio overlay (small faded window for person/teacher)
-----------------------------*/
const BIOS = {
  'arjun': {
    name: 'Arjun Tosawad',
    role: 'President',
    bio: 'Arjun coordinates presentations and safety for large demonstrations. Focus areas include organic synthesis, green chemistry demos, and public-safety training for live experiments.',
    fun: 'Fun fact: Arjun builds polymer models for interactive demos.'
  },
  'xxx': {
    name: 'XXX',
    role: 'Secretary',
    bio: 'XXX handles documentation, scheduling and communications. Special interest in analytical workflows and visitor engagement.',
    fun: 'Fun fact: XXX organizes data posters with clear visual storytelling.'
  },
  'yyy': {
    name: 'YYY',
    role: 'Vice President',
    bio: 'YYY oversees fabrication and safety systems, with a focus on material chemistry and large-format exhibit design.',
    fun: 'Fun fact: YYY prototypes 3D-printed reaction housings for demos.'
  },
  'zzz': {
    name: 'ZZZ',
    role: 'IT & Tech Head',
    bio: 'ZZZ manages interactive displays, projection mapping, and the technical stack for the exhibition web and on-site installations.',
    fun: 'Fun fact: ZZZ builds multi-projector mapping rigs for demos.'
  },
  'sankalp': {
    name: 'Mr. Sankalp Maheshwari',
    role: 'Professor of Organic Chemistry',
    bio: 'Mr. Maheshwari guides experimental design and safety protocols, with research in sustainable organic syntheses and color chemistry.',
    fun: 'Fun fact: Sankalp curated the fireworks color module for safe classroom demos.'
  },
  'ankita': {
    name: 'Mrs. Ankita Sharma',
    role: 'Associate Professor — Materials & Nanotechnology',
    bio: 'Mrs. Sharma mentors nanotech and materials exhibits; research includes nanoparticles for imaging and drug delivery.',
    fun: 'Fun fact: Ankita runs a microscopy club for undergraduates.'
  },
  'sudeep': {
    name: 'Mr. Sudeep XYZ',
    role: 'Lecturer — Physical & Analytical Chemistry',
    bio: 'Mr. Sudeep leads forensic demonstrations and spectroscopy workshops, with an emphasis on analytical rigor and hands-on data interpretation.',
    fun: 'Fun fact: Sudeep designs mini forensic puzzles for visitors.'
  }
};

const bioContainer = document.getElementById('bioContainer');

function openBio(key){
  const p = BIOS[key];
  if(!p) return;
  // remove existing
  bioContainer.innerHTML = '';
  bioContainer.style.display = 'block';
  const el = document.createElement('div');
  el.className = 'bio-overlay detail-enter';
  el.innerHTML = `
    <div style="display:flex;justify-content:space-between;align-items:start;gap:12px;">
      <div>
        <div style="font-weight:900;color:var(--cyan)">${escapeHtml(p.name)}</div>
        <div class="muted" style="margin-top:6px"><strong>${escapeHtml(p.role)}</strong></div>
        <p style="margin-top:10px;color:rgba(230,247,255,0.9)">${escapeHtml(p.bio)}</p>
        <div style="margin-top:8px;color:rgba(230,247,255,0.78);font-weight:700">${escapeHtml(p.fun)}</div>
      </div>
      <div style="display:flex;flex-direction:column;gap:8px;">
        <button class="btn btn-primary" onclick="playEnergySound()">Listen</button>
        <button class="btn btn-ghost" onclick="closeBio()">Close</button>
      </div>
    </div>
  `;
  bioContainer.appendChild(el);
  // small ripple from bottom-right
  const x = window.innerWidth - 120, y = window.innerHeight - 120;
  createRipple(x, y, '#b79bff', 420, 900);
  playEnergySound('pulse');
}

function closeBio(){
  bioContainer.innerHTML = '';
  bioContainer.style.display = 'none';
}

/* ----------------------------
  Modal preview
-----------------------------*/
function openModal(title, content){
  const modal = document.getElementById('modal');
  document.getElementById('modalTitle').textContent = title;
  document.getElementById('modalContent').innerHTML = content || '<p>No preview</p>';
  modal.style.display = 'flex';
}
function closeModal(){
  document.getElementById('modal').style.display = 'none';
}

/* ----------------------------
  small utility functions
-----------------------------*/
function escapeHtml(s){ return (s||'').toString().replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

/* playEnergySound triggers WebAudio; allowed without permission because on-user interaction */
function playEnergySound(){ playEnergySoundImpl(); }
function playEnergySoundImpl(){
  // call the earlier defined function in the outer scope
  if(typeof window !== 'undefined' && window && window.AudioContext) {
    try { playEnergySound('pulse'); } catch(e) { /* ignore if audio blocked */ }
  }
}

/* wire nav links to scroll (keyboard accessible) */
document.querySelectorAll('.navlink').forEach(a=>{
  a.addEventListener('click', (e)=>{
    e.preventDefault();
    const dest = a.getAttribute('data-scroll');
    if(dest === 'home') window.scrollTo({top:0,behavior:'smooth'});
    else {
      const el = document.getElementById(dest);
      if(el) el.scrollIntoView({behavior:'smooth', block:'start'});
    }
  });
});

/* Explore button scroll */
document.getElementById('exploreBtn').addEventListener('click', ()=> {
  const el = document.getElementById('exhibits');
  if(el) el.scrollIntoView({behavior:'smooth', block:'start'});
});

/* If loaded with hash for a page, open it on load */
window.addEventListener('DOMContentLoaded', ()=>{
  const hash = location.hash.replace('#','');
  if(hash && (hash in PAGES)){
    // open that page
    setTimeout(()=> {
      renderPage(hash);
    }, 200);
  } else {
    // reveal in sequence
    document.querySelectorAll('.reveal').forEach((el,i)=> setTimeout(()=> el.classList.add('show'), i*80));
  }
});

/* Ensure audio context created only on user gesture (some browsers block auto audio if not) */
document.addEventListener('click', function one(){ 
  if(!window.AudioContext && !window.webkitAudioContext) return;
  // create audio context lazily via a short oscillator and stop
  try{
    if(!window._audioPrimed){
      window._audioPrimed = true;
      if(!window.audioPrimedCtx) window.audioPrimedCtx = new (window.AudioContext || window.webkitAudioContext)();
      const ctx = window.audioPrimedCtx;
      const o = ctx.createOscillator(); const g = ctx.createGain();
      o.connect(g); g.connect(ctx.destination);
      g.gain.value = 0.00001; o.start(); g.gain.exponentialRampToValueAtTime(0.00001, ctx.currentTime + 0.01); o.stop(ctx.currentTime + 0.02);
    }
  }catch(e){}
  document.removeEventListener('click', one);
}, {once:true});

/* small safety: if location hash is a known page, replace state to use SPA */
window.addEventListener('load', ()=>{
  const h = location.hash.replace('#','');
  if(h && (h in PAGES)){
    history.replaceState({page:h}, '', `#${h}`);
  } else {
    history.replaceState({page:'main'}, '', location.pathname);
  }
});
</script>
</body>
</html>
