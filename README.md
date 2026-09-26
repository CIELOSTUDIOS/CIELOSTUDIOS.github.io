  # CIELOSTUDIOS.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Cielo Studios — We post. You grow.</title>
<meta name="description" content="Cielo Studios is a content studio in Belize. We plan, film, and post the content that grows your brand.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,400&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#241509;
    --espresso:#2b1810;
    --espresso-deep:#180d06;
    --cream:#f3e8d3;
    --parchment:#e9d7b3;
    --caramel:#b8874a;
    --gold:#d9b77c;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Fraunces',serif;
    background:var(--cream);
    color:var(--ink);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img{max-width:100%;display:block;}
  a{color:inherit;}
  .wrap{max-width:1080px;margin:0 auto;padding:0 28px;}
  h1,h2,h3{font-family:'Anton',sans-serif;font-weight:400;letter-spacing:0.01em;line-height:1.05;}

  /* grain texture, used on dark sections */
  .grain{position:relative;}
  .grain::before{
    content:"";position:absolute;inset:0;pointer-events:none;opacity:0.09;mix-blend-mode:overlay;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  }

  /* sprocket divider — nods to the film-reel mark */
  .sprockets{display:flex;justify-content:center;gap:14px;padding:22px 0;}
  .sprockets span{width:8px;height:8px;border-radius:50%;background:var(--caramel);opacity:0.55;}

  header{
    position:sticky;top:0;z-index:10;
    background:rgba(243,232,211,0.92);backdrop-filter:blur(6px);
    border-bottom:1px solid rgba(36,21,9,0.1);
  }
  .nav{display:flex;align-items:center;justify-content:space-between;padding:16px 28px;}
  .brand{display:flex;align-items:center;gap:10px;font-family:'Anton',sans-serif;font-size:1.05rem;letter-spacing:0.02em;}
  .brand img{height:34px;width:auto;}
  .nav a.cta{
    font-family:'Fraunces',serif;font-weight:600;font-size:0.92rem;
    background:var(--ink);color:var(--cream);padding:10px 18px;border-radius:999px;
    text-decoration:none;
  }

  /* HERO */
  .hero{background:var(--espresso);color:var(--cream);padding:96px 0 76px;overflow:hidden;}
  .hero .wrap{position:relative;z-index:1;}
  .hero .kicker{color:var(--gold);font-size:1.05rem;font-style:italic;margin-bottom:18px;}
  .hero h1{font-size:clamp(3rem,8vw,5.4rem);color:var(--cream);max-width:11ch;}
  .hero p{max-width:46ch;margin-top:26px;font-size:1.15rem;color:var(--parchment);}
  .hero .actions{display:flex;flex-wrap:wrap;gap:16px;margin-top:38px;}
  .btn{
    display:inline-block;font-family:'Fraunces',serif;font-weight:600;font-size:1rem;
    padding:14px 28px;border-radius:999px;text-decoration:none;border:1px solid transparent;
  }
  .btn-primary{background:var(--gold);color:var(--espresso-deep);}
  .btn-ghost{border-color:rgba(243,232,211,0.5);color:var(--cream);}
  .est{margin-top:52px;font-size:0.9rem;color:rgba(233,215,179,0.6);}

  /* ABOUT */
  .about{padding:88px 0;}
  .about .grid{display:grid;grid-template-columns:1.3fr 0.9fr;gap:64px;align-items:center;}
  .about h2{font-size:clamp(2.2rem,5vw,3.2rem);margin-bottom:22px;}
  .about p{font-size:1.08rem;max-width:52ch;}
  .about p + p{margin-top:16px;}
  .mark{
    width:220px;height:220px;border-radius:50%;background:var(--espresso);
    display:flex;align-items:center;justify-content:center;margin:0 auto;
    transform:rotate(-4deg);
  }
  .mark svg{width:70%;}

  /* SERVICES */
  .services{background:var(--parchment);padding:88px 0;}
  .services h2{font-size:clamp(2.2rem,5vw,3.2rem);margin-bottom:12px;}
  .services > .wrap > p{max-width:48ch;font-size:1.08rem;margin-bottom:48px;}
  .service-row{
    display:grid;grid-template-columns:60px 1fr;gap:24px;
    padding:28px 0;border-top:1px solid rgba(36,21,9,0.18);align-items:baseline;
  }
  .service-row:last-child{border-bottom:1px solid rgba(36,21,9,0.18);}
  .service-row .num{font-family:'Anton',sans-serif;font-size:1.4rem;color:var(--caramel);}
  .service-row h3{font-size:1.4rem;margin-bottom:6px;}
  .service-row p{max-width:52ch;}

  /* CONTACT */
  .contact{background:var(--espresso-deep);color:var(--cream);padding:100px 0;text-align:center;}
  .contact h2{font-size:clamp(2.6rem,8vw,4.6rem);color:var(--cream);}
  .contact p{max-width:44ch;margin:22px auto 0;color:var(--parchment);font-size:1.1rem;}
  .contact .actions{display:flex;justify-content:center;gap:16px;flex-wrap:wrap;margin-top:36px;}
  .contact .insta{display:block;margin-top:28px;color:var(--gold);text-decoration:none;font-style:italic;}

  footer{padding:32px 0;text-align:center;font-size:0.9rem;color:rgba(36,21,9,0.6);}

  @media(max-width:760px){
    .about .grid{grid-template-columns:1fr;}
    .mark{order:-1;width:160px;height:160px;}
    .nav a.cta{font-size:0.85rem;padding:9px 14px;}
  }
</style>
</head>
<body>

<header>
  <div class="nav wrap">
    <div class="brand"><img src="assets/logo.png" alt="Cielo Studios"> Cielo Studios</div>
    <a class="cta" href="https://wa.me/12133093160" target="_blank" rel="noopener">Say hello</a>
  </div>
</header>

<section class="hero grain">
  <div class="wrap">
    <div class="kicker">A content studio in Belize</div>
    <h1>We post.<br>You grow.</h1>
    <p>Cielo Studios plans, films, and posts the content that gets your brand seen — so you can stay focused on running the thing you built.</p>
    <div class="actions">
      <a class="btn btn-primary" href="https://wa.me/12133093160" target="_blank" rel="noopener">Message us on WhatsApp</a>
      <a class="btn btn-ghost" href="#services">See what we do</a>
    </div>
    <div class="est">Est. 2024 &nbsp;·&nbsp; @cielostudiosbz</div>
  </div>
</section>

<div class="sprockets"><span></span><span></span><span></span><span></span><span></span><span></span><span></span></div>

<section class="about">
  <div class="wrap grid">
    <div>
      <h2>Let's be better humans</h2>
      <p>That's less a slogan than a rule we hold ourselves to. We show up on time, we tell your story honestly, and we treat every client's community like our own.</p>
      <p>Good content isn't about chasing trends — it's about paying attention to what your people actually respond to, and doing that, consistently, week after week.</p>
    </div>
    <div class="mark">
      <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
        <circle cx="50" cy="50" r="46" fill="none" stroke="#f3e8d3" stroke-width="2"/>
        <line x1="50" y1="30" x2="50" y2="70" stroke="#f3e8d3" stroke-width="4" stroke-linecap="round"/>
        <line x1="34" y1="46" x2="66" y2="46" stroke="#f3e8d3" stroke-width="4" stroke-linecap="round"/>
      </svg>
    </div>
  </div>
</section>

<section class="services" id="services">
  <div class="wrap">
    <h2>What we do</h2>
    <p>One focus, done properly: content that's planned, shot, and posted so your account actually moves.</p>

    <div class="service-row">
      <div class="num">01</div>
      <div><h3>Content strategy</h3><p>We figure out what to post and why — a plan built around your brand, your audience, and what's actually working right now.</p></div>
    </div>
    <div class="service-row">
      <div class="num">02</div>
      <div><h3>Filming &amp; production</h3><p>Reels, photos, and short-form video, shot and edited to look like you — not like a template.</p></div>
    </div>
    <div class="service-row">
      <div class="num">03</div>
      <div><h3>Posting &amp; growth</h3><p>We publish on schedule and track what's landing, so the account keeps building instead of stalling out.</p></div>
    </div>
  </div>
</section>

<section class="contact grain">
  <div class="wrap">
    <h2>Think Cielo.</h2>
    <p>Ready to make content that actually works? Tell us about your brand and we'll take it from there.</p>
    <div class="actions">
      <a class="btn btn-primary" href="https://wa.me/12133093160" target="_blank" rel="noopener">Message us on WhatsApp</a>
    </div>
    <a class="insta" href="https://instagram.com/cielostudiosbz" target="_blank" rel="noopener">@cielostudiosbz</a>
  </div>
</section>

<footer>Cielo Studios © 2026 — Let's be better humans.</footer>

</body>
</html>
