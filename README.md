<Portfolio>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sethuli Sahasna — Biotechnology Portfolio</title>
<meta name="description" content="E-portfolio of Sethuli Sahasna, BSc (Hons) Biotechnology undergraduate at SLIIT.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
  :root{
    --ink:#12332C;
    --paper:#FAF9F4;
    --green:#1E7A54;
    --green-bright:#34B27C;
    --mint:#E8F1EB;
    --amber:#D98A32;
    --line:#DBE4DD;
    --muted:#566A61;
    --display:"Fraunces", Georgia, serif;
    --body:"Inter", system-ui, sans-serif;
    --mono:"IBM Plex Mono", ui-monospace, monospace;
  }

  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{
    font-family:var(--body);
    background:var(--paper);
    color:var(--ink);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  a{color:inherit;text-decoration:none}
  .wrap{width:min(1080px,92vw);margin:0 auto}

  .eyebrow{
    font-family:var(--mono);
    font-size:.72rem;
    letter-spacing:.22em;
    text-transform:uppercase;
    color:var(--green);
    display:inline-block;
    margin-bottom:1rem;
  }

  header.nav{
    position:sticky;top:0;z-index:50;
    background:rgba(250,249,244,.85);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{display:flex;align-items:center;justify-content:space-between;height:66px}
  .brand{display:flex;align-items:center;gap:.7rem;font-weight:600}
  .monogram{
    width:34px;height:34px;border-radius:50%;
    background:var(--ink);color:var(--paper);
    display:grid;place-items:center;
    font-family:var(--display);font-size:.95rem;
  }
  .nav-links{display:flex;align-items:center;gap:1.6rem}
  .nav-links a{font-size:.9rem;color:var(--muted);transition:color .2s}
  .nav-links a:hover{color:var(--ink)}
  .btn{
    font-family:var(--body);font-weight:500;font-size:.9rem;
    padding:.55rem 1.1rem;border-radius:999px;
    border:1px solid var(--ink);cursor:pointer;transition:all .2s;
    display:inline-flex;align-items:center;gap:.5rem;
  }
  .btn-solid{background:var(--ink);color:var(--paper)}
  .btn-solid:hover{background:var(--green)}
  .btn-ghost:hover{background:var(--ink);color:var(--paper)}
  .menu-toggle{display:none;background:none;border:none;cursor:pointer;font-size:1.5rem;color:var(--ink)}

  .hero{position:relative;overflow:hidden;padding:5rem 0 4.5rem}
  .helix{
    position:absolute;right:-40px;top:0;height:100%;width:340px;
    opacity:.16;pointer-events:none;z-index:0;
  }
  .hero-grid{
    position:relative;z-index:1;
    display:grid;grid-template-columns:1.35fr .9fr;
    gap:3.5rem;align-items:center;
  }
  .hero h1{
    font-family:var(--display);
    font-weight:500;
    font-size:clamp(2.8rem,7vw,4.9rem);
    line-height:1.02;
    letter-spacing:-.02em;
    margin:.2rem 0 1.1rem;
  }
  .hero .lede{font-size:1.12rem;color:var(--muted);max-width:46ch;margin-bottom:1.8rem}
  .hero-cta{display:flex;flex-wrap:wrap;gap:.8rem;margin-bottom:1.6rem}
  .chips{display:flex;flex-wrap:wrap;gap:.5rem}
  .chip{
    font-family:var(--mono);font-size:.76rem;
    padding:.35rem .8rem;border-radius:999px;
    background:var(--mint);color:var(--green);
  }

  .photo-frame{position:relative}
  .photo-frame::before{
    content:"";position:absolute;inset:-14px -14px 14px 14px;
    border:1.5px solid var(--green-bright);border-radius:20px;z-index:0;
  }
  .photo,.photo-fallback{
    position:relative;z-index:1;
    width:100%;aspect-ratio:4/5;border-radius:20px;
    object-fit:cover;display:block;
    box-shadow:0 18px 40px -22px rgba(18,51,44,.5);
  }
  .photo-fallback{
    display:none;place-items:center;
    background:var(--ink);color:var(--paper);
    font-family:var(--display);font-size:4rem;
  }

  section{padding:4.2rem 0;border-top:1px solid var(--line)}
  .sec-head{max-width:60ch;margin-bottom:2.4rem}
  .sec-head h2{
    font-family:var(--display);font-weight:500;
    font-size:clamp(1.8rem,4vw,2.6rem);letter-spacing:-.01em;
  }
  .sec-head p{color:var(--muted);margin-top:.6rem}

  .about-body{font-size:1.12rem;max-width:62ch;color:#2b463d}
  .about-body strong{color:var(--ink);font-weight:600}

  .timeline{display:grid;gap:1.4rem;max-width:760px}
  .tl-item{
    display:grid;grid-template-columns:120px 1fr;gap:1.4rem;
    padding:1.4rem 1.6rem;background:#fff;border:1px solid var(--line);
    border-radius:16px;transition:transform .2s,box-shadow .2s;
  }
  .tl-item:hover{transform:translateY(-3px);box-shadow:0 14px 30px -20px rgba(18,51,44,.35)}
  .tl-year{font-family:var(--mono);font-size:.82rem;color:var(--green);padding-top:.2rem}
  .tl-body h3{font-family:var(--display);font-weight:500;font-size:1.2rem}
  .tl-body .place{color:var(--muted);font-size:.92rem;margin:.15rem 0 .6rem}
  .tl-body ul{list-style:none;display:grid;gap:.25rem}
  .tl-body li{position:relative;padding-left:1.1rem;font-size:.95rem}
  .tl-body li::before{content:"";position:absolute;left:0;top:.65em;width:6px;height:6px;border-radius:50%;background:var(--green-bright)}

  .cols{display:grid;grid-template-columns:1fr 1fr;gap:2.5rem}
  .card-title{font-family:var(--mono);font-size:.78rem;letter-spacing:.14em;text-transform:uppercase;color:var(--green);margin-bottom:1rem}
  .list{list-style:none;display:grid;gap:.7rem}
  .list li{position:relative;padding-left:1.4rem}
  .list li::before{content:"→";position:absolute;left:0;color:var(--green-bright);font-family:var(--mono)}

  .act-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem}
  .act{
    padding:1.3rem 1.5rem;background:var(--mint);border-radius:14px;
    border:1px solid transparent;transition:border-color .2s;
  }
  .act:hover{border-color:var(--green-bright)}
  .act h4{font-weight:600;font-size:1.02rem;margin-bottom:.25rem}
  .act p{font-size:.9rem;color:var(--muted)}

  .hobby-row{display:flex;flex-wrap:wrap;gap:.7rem}
  .hobby{
    font-family:var(--mono);font-size:.85rem;
    padding:.5rem 1rem;border:1px solid var(--line);border-radius:999px;background:#fff;
  }

  .contact{background:var(--ink);color:var(--paper);border-radius:24px;padding:3rem clamp(1.5rem,5vw,3.5rem);margin-bottom:1rem}
  .contact .eyebrow{color:var(--green-bright)}
  .contact h2{font-family:var(--display);font-weight:500;font-size:clamp(1.8rem,4vw,2.6rem);margin-bottom:.6rem}
  .contact p{color:#c9d8d0;max-width:48ch;margin-bottom:1.8rem}
  .contact-grid{display:flex;flex-wrap:wrap;gap:2.2rem 3rem;align-items:flex-start}
  .cnt-item .k{font-family:var(--mono);font-size:.72rem;letter-spacing:.16em;text-transform:uppercase;color:var(--green-bright);margin-bottom:.35rem}
  .cnt-item .v{font-size:1.05rem}
  .cnt-item a:hover{color:var(--green-bright)}
  .contact .btn{border-color:var(--paper);color:var(--paper);margin-top:2rem}
  .contact .btn:hover{background:var(--paper);color:var(--ink)}

  footer{padding:2.4rem 0 3rem;text-align:center;color:var(--muted);font-size:.85rem}
  footer .id{font-family:var(--mono)}

  .reveal{opacity:0;transform:translateY(18px);transition:opacity .7s ease,transform .7s ease}
  .reveal.in{opacity:1;transform:none}

  @media(max-width:860px){
    .hero-grid{grid-template-columns:1fr;gap:2.5rem}
    .photo-frame{max-width:320px}
    .cols{grid-template-columns:1fr;gap:1.8rem}
    .act-grid{grid-template-columns:1fr}
    .nav-links{
      position:fixed;inset:66px 0 auto 0;flex-direction:column;
      background:var(--paper);border-bottom:1px solid var(--line);
      padding:1.2rem 6vw 1.6rem;gap:1.1rem;align-items:flex-start;
      display:none;
    }
    .nav-links.open{display:flex}
    .menu-toggle{display:block}
    .tl-item{grid-template-columns:1fr;gap:.5rem}
  }
  @media(prefers-reduced-motion:reduce){
    html{scroll-behavior:auto}
    .reveal{opacity:1;transform:none;transition:none}
  }
</style>
</head>
<body>

<header class="nav">
  <div class="wrap nav-inner">
    <a class="brand" href="#top">
      <span class="monogram">S</span>
      <span>Sethuli Sahasna</span>
    </a>
    <nav class="nav-links" id="navlinks">
      <a href="#about">About</a>
      <a href="#education">Education</a>
      <a href="#skills">Skills</a>
      <a href="#activities">Activities</a>
      <a href="#contact">Contact</a>
      <a class="btn btn-ghost" href="cv.pdf" download>Download CV</a>
    </nav>
    <button class="menu-toggle" id="menuToggle" aria-label="Menu">☰</button>
  </div>
</header>

<section class="hero" id="top">
  <svg class="helix" viewBox="0 0 200 600" fill="none" aria-hidden="true">
    <g stroke="#1E7A54" stroke-width="2">
      <path d="M40 0 C160 60 40 120 160 180 C40 240 160 300 40 360 C160 420 40 480 160 540 C90 570 90 570 100 600"/>
      <path d="M160 0 C40 60 160 120 40 180 C160 240 40 300 160 360 C40 420 160 480 40 540 C110 570 110 570 100 600"/>
    </g>
    <g stroke="#34B27C" stroke-width="1.5">
      <line x1="55" y1="30" x2="145" y2="30"/><line x1="70" y1="60" x2="130" y2="60"/>
      <line x1="55" y1="150" x2="145" y2="150"/><line x1="70" y1="120" x2="130" y2="120"/>
      <line x1="55" y1="210" x2="145" y2="210"/><line x1="70" y1="240" x2="130" y2="240"/>
      <line x1="55" y1="330" x2="145" y2="330"/><line x1="70" y1="300" x2="130" y2="300"/>
      <line x1="55" y1="390" x2="145" y2="390"/><line x1="70" y1="420" x2="130" y2="420"/>
      <line x1="55" y1="510" x2="145" y2="510"/><line x1="70" y1="480" x2="130" y2="480"/>
    </g>
  </svg>

  <div class="wrap hero-grid">
    <div class="reveal in">
      <span class="eyebrow">Biotechnology Undergraduate · SLIIT</span>
      <h1>Sethuli<br>Sahasna</h1>
      <p class="lede">Curious about what happens at the bench. I'm building hands-on lab experience and looking for a molecular biology or biochemistry internship where I can learn fast and contribute.</p>
      <div class="hero-cta">
        <a class="btn btn-solid" href="cv.pdf" download>↓ Download my CV</a>
        <a class="btn btn-ghost" href="#contact">Get in touch</a>
      </div>
      <div class="chips">
        <span class="chip">Laboratory work</span>
        <span class="chip">Molecular biology</span>
        <span class="chip">Fast learner</span>
        <span class="chip">Team player</span>
      </div>
    </div>

    <div class="photo-frame reveal in">
      <img src="photo.jpg" alt="Portrait of Sethuli Sahasna" class="photo"
           onerror="this.style.display='none';document.getElementById('pf').style.display='grid';">
      <div class="photo-fallback" id="pf">SS</div>
    </div>
  </div>
</section>

<section id="about">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">01 — About me</span>
      <h2>Who I am</h2>
    </div>
    <p class="about-body reveal">
      I'm an undergraduate reading for a <strong>BSc (Hons) in Biotechnology</strong> at SLIIT.
      I like the practical side of science — handling lab work, understanding how systems and
      processes fit together, and figuring out problems quickly. Right now I'm looking for an
      <strong>internship in a molecular biology or biochemistry setting</strong>, ideally in a
      fast-paced clinical or diagnostics lab, where I can turn what I've learned into real
      experience. As a former <strong>Air Scout</strong> and an active <strong>Gavel Club</strong>
      member, I bring strong communication, teamwork and time-management skills to everything I take on.
    </p>
  </div>
</section>

<section id="education">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">02 — Education</span>
      <h2>Academic background</h2>
      <p>My path from secondary school through to my degree.</p>
    </div>
    <div class="timeline">
      <div class="tl-item reveal">
        <div class="tl-year">2025 — Present</div>
        <div class="tl-body">
          <h3>BSc (Hons) in Biotechnology</h3>
          <p class="place">Sri Lanka Institute of Information Technology (SLIIT)</p>
          <ul>
            <li>Undergraduate degree currently in progress (Year 1)</li>
            <li>Coursework across biological sciences, laboratory safety and IT fundamentals</li>
          </ul>
        </div>
      </div>
      <div class="tl-item reveal">
        <div class="tl-year">2024</div>
        <div class="tl-body">
          <h3>G.C.E. Advanced Level — Bio Science stream</h3>
          <p class="place">Chemistry · Physics · Biology</p>
          <ul>
            <li>Three "C" passes across Chemistry, Physics and Biology</li>
          </ul>
        </div>
      </div>
      <div class="tl-item reveal">
        <div class="tl-year">2020</div>
        <div class="tl-body">
          <h3>G.C.E. Ordinary Level</h3>
          <p class="place">Secondary education</p>
          <ul>
            <li>6 "A" passes in the main subjects</li>
            <li>A — Tamil Language &nbsp;·&nbsp; A — Information &amp; Communication Technology</li>
            <li>B — English Literature</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">03 — Skills</span>
      <h2>What I bring</h2>
    </div>
    <div class="cols">
      <div class="reveal">
        <p class="card-title">Core skills</p>
        <ul class="list">
          <li>Handling laboratory work and procedures</li>
          <li>Quickly learning new systems and processes to solve problems</li>
          <li>Microsoft Word, PowerPoint and Excel</li>
          <li>Time management and organisation</li>
        </ul>
      </div>
      <div class="reveal">
        <p class="card-title">Languages</p>
        <ul class="list">
          <li>English — fluent</li>
          <li>Tamil — fluent comprehension, basic speaking</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="activities">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">04 — Activities &amp; leadership</span>
      <h2>Beyond the classroom</h2>
      <p>Where I've built communication, teamwork and discipline.</p>
    </div>
    <div class="act-grid">
      <div class="act reveal">
        <h4>Air Scouts</h4>
        <p>Member — developed teamwork, leadership, discipline and communication.</p>
      </div>
      <div class="act reveal">
        <h4>Gavel Club, SLIIT</h4>
        <p>Member of the SLIIT community club, focused on public speaking.</p>
      </div>
      <div class="act reveal">
        <h4>School Red Cross Society</h4>
        <p>Member — emergency response and first-aid awareness.</p>
      </div>
      <div class="act reveal">
        <h4>Prefect Board</h4>
        <p>School prefect — responsibility, leadership and organisation.</p>
      </div>
      <div class="act reveal">
        <h4>Traditional Kandyan Dancing</h4>
        <p>Graduate in traditional Kandyan dance.</p>
      </div>
    </div>
  </div>
</section>

<section id="hobbies">
  <div class="wrap">
    <div class="sec-head reveal">
      <span class="eyebrow">05 — Hobbies</span>
      <h2>Off the clock</h2>
    </div>
    <div class="hobby-row reveal">
      <span class="hobby">Kandyan dancing</span>
      <span class="hobby">Public speaking</span>
      <span class="hobby">Volunteering</span>
      <span class="hobby">Scouting</span>
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="contact reveal">
      <span class="eyebrow">06 — Contact</span>
      <h2>Let's talk</h2>
      <p>Open to internship opportunities in molecular biology, biochemistry and diagnostics. The quickest way to reach me is email.</p>
      <div class="contact-grid">
        <div class="cnt-item">
          <div class="k">Email</div>
          <div class="v"><a href="mailto:Sethuli987@gmail.com">Sethuli987@gmail.com</a></div>
        </div>
        <div class="cnt-item">
          <div class="k">Phone</div>
          <div class="v"><a href="tel:+94776970982">077 697 0982</a></div>
        </div>
        <div class="cnt-item">
          <div class="k">Location</div>
          <div class="v">Wathugedara, Sri Lanka</div>
        </div>
      </div>
      <a class="btn" href="cv.pdf" download>↓ Download my resume (PDF)</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <p>© <span id="year"></span> Sethuli Sahasna · Biotechnology E-Portfolio</p>
    <p class="id">SC1172 — Introduction to Information Technology · HS26510010</p>
  </div>
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  var toggle = document.getElementById('menuToggle');
  var links = document.getElementById('navlinks');
  toggle.addEventListener('click', function(){ links.classList.toggle('open'); });
  links.querySelectorAll('a').forEach(function(a){
    a.addEventListener('click', function(){ links.classList.remove('open'); });
  });

  var io = new IntersectionObserver(function(entries){
    entries.forEach(function(e){ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target);} });
  }, {threshold:.14});
  document.querySelectorAll('.reveal').forEach(function(el){ io.observe(el); });
</script>
</body>
</html>
