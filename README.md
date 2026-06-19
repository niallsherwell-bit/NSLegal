<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Plain-English Legal Content Writer</title>

<!--
  ============================================================
  THINGS TO REPLACE BEFORE YOU SHARE THIS (search for [ ]):
   1. [YOUR NAME]        - appears in the wordmark, hero, footer
   2. [you@email.com]    - the contact email (2 places)
   3. [your-linkedin]    - your LinkedIn profile URL
   4. Sample links       - the href="#" on each work card -> link to the real article (Google Doc, PDF, Medium, etc.)
   5. Add your 2nd/3rd samples where marked "ADD SAMPLE"
  ============================================================
-->

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,600&family=Newsreader:opsz,wght@6..72,400;6..72,500&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
  :root{
    --paper:#FAF8F4;
    --paper-2:#F2EEE6;
    --ink:#1B2230;
    --ink-soft:#41485A;
    --ink-faint:#7C8294;
    --oxblood:#7E2230;
    --oxblood-bright:#A12E3C;
    --line:#E2DCD0;
    --line-strong:#CFC7B7;
    --display:"Fraunces", Georgia, serif;
    --body:"Newsreader", Georgia, serif;
    --mono:"JetBrains Mono", ui-monospace, monospace;
    --maxw:1080px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:var(--body);
    font-size:19px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    text-rendering:optimizeLegibility;
  }

  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 28px;}

  /* ---- eyebrow / mono labels ---- */
  .eyebrow{
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:.18em;
    text-transform:uppercase;
    color:var(--oxblood);
    font-weight:500;
    margin:0;
  }

  /* ---- header ---- */
  header.site{
    border-bottom:1px solid var(--line);
    position:sticky; top:0; z-index:10;
    background:rgba(250,248,244,.86);
    backdrop-filter:saturate(180%) blur(8px);
  }
  .site .wrap{display:flex; align-items:center; justify-content:space-between; height:64px;}
  .wordmark{
    font-family:var(--display);
    font-weight:600;
    font-size:19px;
    letter-spacing:-.01em;
    color:var(--ink);
    text-decoration:none;
  }
  .wordmark .dot{color:var(--oxblood);}
  nav.site-nav a{
    font-family:var(--mono);
    font-size:12.5px;
    letter-spacing:.08em;
    text-transform:uppercase;
    color:var(--ink-soft);
    text-decoration:none;
    margin-left:26px;
  }
  nav.site-nav a:hover{color:var(--oxblood);}
  @media(max-width:560px){ nav.site-nav a:first-child{display:none;} }

  /* ---- hero ---- */
  .hero{padding:84px 0 64px;}
  .hero h1{
    font-family:var(--display);
    font-weight:600;
    font-size:clamp(40px, 7vw, 76px);
    line-height:1.02;
    letter-spacing:-.02em;
    margin:20px 0 0;
    max-width:14ch;
  }
  .hero h1 em{font-style:italic; color:var(--oxblood);}
  .hero .lede{
    font-size:clamp(20px,2.4vw,23px);
    color:var(--ink-soft);
    max-width:48ch;
    margin:26px 0 0;
  }
  .hero .lede b{color:var(--ink); font-weight:500;}
  .cta-row{display:flex; flex-wrap:wrap; gap:14px; margin-top:36px;}
  .btn{
    font-family:var(--mono);
    font-size:13px;
    letter-spacing:.06em;
    text-transform:uppercase;
    text-decoration:none;
    padding:14px 22px;
    border-radius:2px;
    display:inline-block;
    transition:transform .15s ease, background .15s ease, color .15s ease;
  }
  .btn-primary{background:var(--ink); color:var(--paper);}
  .btn-primary:hover{background:var(--oxblood); transform:translateY(-1px);}
  .btn-ghost{border:1px solid var(--line-strong); color:var(--ink);}
  .btn-ghost:hover{border-color:var(--oxblood); color:var(--oxblood);}

  /* ---- signature: legalese -> plain english ---- */
  .redline{
    margin:72px 0 0;
    border:1px solid var(--line);
    border-radius:4px;
    background:#fff;
    overflow:hidden;
    display:grid;
    grid-template-columns:1fr 1fr;
  }
  @media(max-width:720px){ .redline{grid-template-columns:1fr;} }
  .redline .col{padding:30px 32px;}
  .redline .before{
    background:var(--paper-2);
    border-right:1px solid var(--line);
  }
  @media(max-width:720px){ .redline .before{border-right:none; border-bottom:1px solid var(--line);} }
  .redline .tag{
    font-family:var(--mono); font-size:11px; letter-spacing:.16em;
    text-transform:uppercase; margin:0 0 16px; color:var(--ink-faint);
  }
  .redline .before .tag{color:var(--ink-faint);}
  .redline .after .tag{color:var(--oxblood);}
  .redline p.spec{margin:0; font-size:17.5px; line-height:1.62;}
  .redline .before p.spec{color:var(--ink-soft);}
  .redline s{ text-decoration-color:var(--oxblood-bright); text-decoration-thickness:1.5px; color:var(--ink-faint);}
  .redline .after p.spec{color:var(--ink); font-size:18.5px;}
  .redline .after p.spec strong{color:var(--oxblood); font-weight:600;}

  /* ---- section scaffolding ---- */
  section{padding:76px 0;}
  .rule{border:none; border-top:1px solid var(--line); margin:0;}
  .sec-head{max-width:60ch;}
  .sec-head h2{
    font-family:var(--display);
    font-weight:500;
    font-size:clamp(28px,4vw,40px);
    line-height:1.1;
    letter-spacing:-.015em;
    margin:14px 0 0;
  }
  .sec-head p{color:var(--ink-soft); margin:18px 0 0; font-size:20px;}

  /* ---- why me: two failure modes ---- */
  .modes{display:grid; grid-template-columns:1fr 1fr; gap:24px; margin-top:44px;}
  @media(max-width:720px){ .modes{grid-template-columns:1fr;} }
  .mode{
    border-top:2px solid var(--line-strong);
    padding-top:22px;
  }
  .mode .n{font-family:var(--mono); font-size:12px; color:var(--ink-faint); letter-spacing:.1em;}
  .mode h3{font-family:var(--display); font-weight:500; font-size:22px; margin:10px 0 8px; letter-spacing:-.01em;}
  .mode p{margin:0; color:var(--ink-soft); font-size:17.5px;}
  .modes-foot{
    margin-top:36px; font-family:var(--display); font-style:italic;
    font-size:clamp(21px,2.6vw,26px); line-height:1.4; color:var(--ink); max-width:30ch;
  }
  .modes-foot b{color:var(--oxblood); font-style:normal; font-weight:600;}

  /* ---- work ---- */
  .work-grid{display:grid; grid-template-columns:repeat(2,1fr); gap:22px; margin-top:44px;}
  @media(max-width:720px){ .work-grid{grid-template-columns:1fr;} }
  .card{
    border:1px solid var(--line);
    border-radius:4px;
    background:#fff;
    padding:28px 28px 24px;
    display:flex; flex-direction:column;
    transition:border-color .18s ease, transform .18s ease;
    text-decoration:none; color:inherit;
  }
  .card:hover{border-color:var(--line-strong); transform:translateY(-2px);}
  .card .cat{font-family:var(--mono); font-size:11px; letter-spacing:.14em; text-transform:uppercase; color:var(--oxblood);}
  .card h3{font-family:var(--display); font-weight:600; font-size:23px; line-height:1.18; letter-spacing:-.01em; margin:14px 0 0;}
  .card p{color:var(--ink-soft); font-size:16.5px; margin:12px 0 22px;}
  .card .go{margin-top:auto; font-family:var(--mono); font-size:12.5px; letter-spacing:.04em; color:var(--ink); display:inline-flex; align-items:center; gap:7px;}
  .card:hover .go{color:var(--oxblood);}
  .card .go .arr{transition:transform .18s ease;}
  .card:hover .go .arr{transform:translateX(4px);}
  .card.placeholder{border-style:dashed; background:transparent;}
  .card.placeholder h3, .card.placeholder p{color:var(--ink-faint);}
  .card.placeholder .cat{color:var(--ink-faint);}

  /* ---- services strip ---- */
  .services{display:flex; flex-wrap:wrap; gap:10px; margin-top:40px;}
  .pill{
    font-family:var(--mono); font-size:12.5px; letter-spacing:.04em;
    border:1px solid var(--line-strong); border-radius:100px;
    padding:9px 16px; color:var(--ink-soft);
  }

  /* ---- contact ---- */
  .contact{background:var(--ink); color:var(--paper);}
  .contact .eyebrow{color:#E8A9B2;}
  .contact h2{font-family:var(--display); font-weight:500; font-size:clamp(30px,5vw,52px); letter-spacing:-.02em; line-height:1.06; margin:16px 0 0; max-width:18ch;}
  .contact h2 em{font-style:italic; color:#E8A9B2;}
  .contact p{color:#B7BCC8; font-size:20px; margin:22px 0 0; max-width:46ch;}
  .contact .cta-row{margin-top:40px;}
  .contact .btn-primary{background:var(--paper); color:var(--ink);}
  .contact .btn-primary:hover{background:var(--oxblood-bright); color:#fff;}
  .contact .btn-ghost{border-color:#3A4254; color:var(--paper);}
  .contact .btn-ghost:hover{border-color:#E8A9B2; color:#E8A9B2;}

  /* ---- footer ---- */
  footer.site{padding:34px 0; border-top:1px solid var(--line);}
  footer.site .wrap{display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;}
  footer .fm{font-family:var(--display); font-weight:600; font-size:16px;}
  footer .fm .dot{color:var(--oxblood);}
  footer small{font-family:var(--mono); font-size:11.5px; letter-spacing:.04em; color:var(--ink-faint);}

  /* ---- reveal ---- */
  .reveal{opacity:0; transform:translateY(14px); transition:opacity .6s ease, transform .6s ease;}
  .reveal.in{opacity:1; transform:none;}
  @media(prefers-reduced-motion:reduce){
    .reveal{opacity:1; transform:none; transition:none;}
    html{scroll-behavior:auto;}
    .btn,.card,.card .go .arr{transition:none;}
  }

  a:focus-visible, .btn:focus-visible, .card:focus-visible{
    outline:2px solid var(--oxblood-bright); outline-offset:3px;
  }
</style>
</head>
<body>

<header class="site">
  <div class="wrap">
    <a href="#top" class="wordmark">[YOUR NAME]<span class="dot">.</span></a>
    <nav class="site-nav">
      <a href="#work">Work</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <p class="eyebrow reveal">Plain-English legal content · England &amp; Wales</p>
      <h1 class="reveal">Accurate like a lawyer. <em>Readable</em> like a human.</h1>
      <p class="lede reveal">I'm <b>Niall Sherwell</b>, a law graduate who writes clear, correct content for law firms — the guides, articles, and explainers that turn searchers into the clients you actually want.</p>
      <div class="cta-row reveal">
        <a href="#work" class="btn btn-primary">See the writing</a>
        <a href="#contact" class="btn btn-ghost">Commission a piece</a>
      </div>

      <!-- SIGNATURE: legalese -> plain english -->
      <div class="redline reveal" aria-label="Example: dense legal writing rewritten in plain English">
        <div class="col before">
          <p class="tag">As most firms write it</p>
          <p class="spec">Notwithstanding the foregoing, the Company shall, <s>insofar as is reasonably practicable</s>, indemnify the Director <s>in respect of any and all liabilities incurred</s> in the proper discharge of their duties.</p>
        </div>
        <div class="col after">
          <p class="tag">As I'd write it</p>
          <p class="spec">If you're sued for doing your job properly, <strong>the company covers the cost</strong> — within the limits set out below.</p>
        </div>
      </div>
    </div>
  </section>

  <hr class="rule">

  <!-- WHY ME -->
  <section>
    <div class="wrap">
      <div class="sec-head reveal">
        <p class="eyebrow">Why this matters</p>
        <h2>Most legal content fails one of two ways.</h2>
      </div>
      <div class="modes">
        <div class="mode reveal">
          <span class="n">01</span>
          <h3>Writers who can't lawyer</h3>
          <p>Generalist copywriters are readable, but they get the law subtly wrong — and a single mistake on your blog makes the whole firm look careless.</p>
        </div>
        <div class="mode reveal">
          <span class="n">02</span>
          <h3>Lawyers who can't write</h3>
          <p>Accurate, but dense and joyless. The potential client clicks away before the second paragraph, and never makes the enquiry.</p>
        </div>
      </div>
      <p class="modes-foot reveal">I'm the rare overlap: writing that's <b>legally sound and genuinely good to read</b> — built for the client you want to attract.</p>
    </div>
  </section>

  <hr class="rule">

  <!-- WORK -->
  <section id="work">
    <div class="wrap">
      <div class="sec-head reveal">
        <p class="eyebrow">Selected writing</p>
        <h2>Samples.</h2>
        <p>Plain-English pieces on the questions real clients type into Google.</p>
      </div>

      <div class="work-grid">

        <!-- REAL SAMPLE 1 -->
        <a href="article-sole-trader.html" class="card reveal">
          <span class="cat">Company &amp; Tax</span>
          <h3>Sole trader or limited company — which should you choose?</h3>
          <p>A founder-facing guide to picking a business structure: liability, tax, and admin, explained without the jargon.</p>
          <span class="go">Read the piece <span class="arr">→</span></span>
        </a>

        <!-- ADD SAMPLE 2 — replace text + href, then delete the "placeholder" class -->
        <a href="#" class="card placeholder reveal">
          <span class="cat">Add area</span>
          <h3>Your second sample goes here</h3>
          <p>Pick a narrow question a client would Google, write 800–1,200 words, link it here.</p>
          <span class="go">Read the piece <span class="arr">→</span></span>
        </a>

        <!-- ADD SAMPLE 3 -->
        <a href="#" class="card placeholder reveal">
          <span class="cat">Add area</span>
          <h3>Your third sample goes here</h3>
          <p>Three or four strong samples across different practice areas is plenty to start pitching.</p>
          <span class="go">Read the piece <span class="arr">→</span></span>
        </a>

        <!-- ADD SAMPLE 4 -->
        <a href="#" class="card placeholder reveal">
          <span class="cat">Add area</span>
          <h3>Your fourth sample goes here</h3>
          <p>Optional. Once you have paid work, swap these spec pieces for real published ones.</p>
          <span class="go">Read the piece <span class="arr">→</span></span>
        </a>

      </div>

      <!-- WHAT I WRITE -->
      <div class="services reveal" aria-label="Types of writing offered">
        <span class="pill">Blog &amp; SEO articles</span>
        <span class="pill">Practice-area guides</span>
        <span class="pill">Website &amp; service-page copy</span>
        <span class="pill">Plain-English explainers</span>
        <span class="pill">Client newsletters</span>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">
    <div class="wrap">
      <p class="eyebrow reveal">Get in touch</p>
      <h2 class="reveal">Content your clients will <em>actually finish.</em></h2>
      <p class="reveal">Tell me the gap on your insights page and I'll send a sample on a topic your clients are already searching for. No obligation.</p>
      <div class="cta-row reveal">
        <a href="mailto:niallsherwell@gmail.com" class="btn btn-primary">[you@email.com]</a>
        <a href="https://www.linkedin.com/in/niall-sherwell-11b34322b/" class="btn btn-ghost">LinkedIn</a>
      </div>
    </div>
  </section>

</main>

<footer class="site">
  <div class="wrap">
    <span class="fm">NIALL SHERWELL<span class="dot">.</span></span>
    <small>Plain-English legal content · England &amp; Wales</small>
  </div>
</footer>

<script>
  (function(){
    var reduce = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
    var els = document.querySelectorAll('.reveal');
    if(reduce || !('IntersectionObserver' in window)){
      els.forEach(function(e){ e.classList.add('in'); });
      return;
    }
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(en){
        if(en.isIntersecting){ en.target.classList.add('in'); io.unobserve(en.target); }
      });
    }, {threshold:0.12, rootMargin:'0px 0px -40px 0px'});
    els.forEach(function(e){ io.observe(e); });
  })();
</script>

</body>
</html>
