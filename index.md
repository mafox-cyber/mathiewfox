---
layout: none
---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Re-writing History for Eden & Michael</title>
  <style>
    :root{
      --text:#fff;
      --muted:rgba(255,255,255,0.78);
      --pill:rgba(0,0,0,0.55);
      --pillBorder:rgba(255,255,255,0.12);
      --btnBg:#fff;
      --btnText:#0b0b0b;
      --shadow:0 14px 40px rgba(0,0,0,0.45);
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial;color:var(--text);background:#0b0b0b}

    .hero{min-height:100vh;position:relative;overflow:hidden;display:flex;flex-direction:column}

    .hero::before{
      content:"";
      position:absolute;inset:0;
      background:
        linear-gradient(90deg, rgba(0,0,0,0.78) 0%, rgba(0,0,0,0.45) 45%, rgba(0,0,0,0.75) 100%),
        url("{{ site.baseurl }}/assets/lion-pride-dry-forest_23-2151661739.avif");
      background-size:cover;
      background-position:center;
      transform:scale(1.03);
    }

    .nav{position:relative;z-index:2;display:flex;align-items:center;justify-content:space-between;padding:22px 28px;gap:18px}
    .brand{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--text);font-weight:700;letter-spacing:.08em;text-transform:uppercase;font-size:15px;white-space:nowrap}
    .logoMark{width:26px;height:26px;border-radius:8px;background:rgba(255,255,255,0.18);border:1px solid rgba(255,255,255,0.22);display:grid;place-items:center;box-shadow:0 10px 24px rgba(0,0,0,0.25)}
    .logoMark img{width:16px;height:16px;display:block}

    .navCenter{flex:1;display:flex;justify-content:center;gap:26px;font-size:13px;letter-spacing:.06em;text-transform:uppercase}
    .navCenter a{color:var(--muted);text-decoration:none;padding:8px 6px;border-radius:10px;transition:160ms ease;display:inline-block}
    .navCenter a:hover{color:var(--text);background:rgba(255,255,255,0.08)}

    .navRight{display:flex;align-items:center;gap:14px;white-space:nowrap}
    .link{color:var(--muted);text-decoration:none;font-size:13px;letter-spacing:.06em;text-transform:uppercase;padding:10px 10px;border-radius:10px;transition:160ms ease}
    .link:hover{color:var(--text);background:rgba(255,255,255,0.08)}
    .btnTop{border:0;background:var(--btnBg);color:var(--btnText);font-weight:700;letter-spacing:.06em;text-transform:uppercase;font-size:12px;padding:12px 18px;border-radius:12px;cursor:pointer;box-shadow:var(--shadow)}

    .content{position:relative;z-index:2;flex:1;display:flex;align-items:center;justify-content:center;padding:40px 18px 110px;text-align:center}
    .contentInner{max-width:980px}
    .headline{font-family:ui-serif,Georgia,"Times New Roman",Times,serif;font-weight:500;line-height:.96;font-size:clamp(44px,7vw,88px);margin:0 0 26px;text-shadow:0 30px 70px rgba(0,0,0,0.65)}
    .cta{border:0;background:var(--btnBg);color:var(--btnText);font-weight:800;letter-spacing:.06em;text-transform:uppercase;font-size:12px;padding:16px 26px;border-radius:14px;cursor:pointer;box-shadow:var(--shadow)}

    .bottomPill{position:absolute;z-index:3;left:50%;bottom:28px;transform:translateX(-50%);display:flex;gap:6px;padding:8px;border-radius:999px;background:var(--pill);border:1px solid var(--pillBorder);backdrop-filter:blur(10px);box-shadow:var(--shadow)}
    .pillItem{
      border:0;
      background:transparent;
      color:var(--muted);
      font-weight:650;
      font-size:13px;
      padding:10px 16px;
      border-radius:999px;
      cursor:pointer;
      transition:160ms ease;
      display:inline-block;
      text-decoration:none;
    }
    .pillItem:hover{color:var(--text);background:rgba(255,255,255,0.10)}
    .pillItem.active{color:var(--text);background:rgba(255,255,255,0.16)}

    @media (max-width:860px){.navCenter{display:none}.headline{line-height:1.0}.bottomPill{bottom:18px}}
  </style>
</head>

<body>
  <section class="hero">
    <header class="nav">
      <a class="brand" href="#">
        <span class="logoMark" aria-hidden="true">
          <img src="{{ site.baseurl }}/assets/img/lion.svg" alt="">
        </span>
        <span>MAFOX</span>
      </a>

      <nav class="navCenter" aria-label="Primary">
        <a href="{{ site.baseurl }}/">Blog</a>
        <a href="{{ site.baseurl }}/Untitled.png">Pictures</a>
        <a href="#">Videos</a>
      </nav>

      <div class="navRight">
        <a class="link" href="#">Log In</a>
        <button class="btnTop" type="button">***</button>
      </div>
    </header>

    <main class="content">
      <div class="contentInner">
        <h1 class="headline">Welcome to my story<br/>when a father re-writes History</h1>
        <button class="cta" type="button">Begin the Journey</button>
      </div>
    </main>

    <div class="bottomPill" role="tablist" aria-label="Sections">
      <button class="pillItem active" type="button">Iran</button>
      <button class="pillItem" type="button">America</button>

      <a class="pillItem" href="{{ site.baseurl }}/about/">Divorce Court</a>
      <a class="pillItem" href="{{ site.baseurl }}/Untitled.png">Images</a>

      <button class="pillItem" type="button">Resume</button>
    </div>

  </section>

  <script>
    const tabs = document.querySelectorAll('.pillItem');
    tabs.forEach(btn => btn.addEventListener('click', () => {
      tabs.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
    }));
  </script>
</body>
</html>
