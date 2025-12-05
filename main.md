<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Мой сайт</title>
  <style>
    :root{--bg:#0f1724;--card:#111827;--accent:#9b5cf6;--muted:#94a3b8}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,"Helvetica Neue";background:linear-gradient(180deg,#071028 0%,var(--bg) 100%);color:#e6eef8}
    .wrap{max-width:900px;margin:3rem auto;padding:1.5rem}
    header{display:flex;justify-content:space-between;align-items:center;gap:1rem}
    h1{margin:0;font-size:1.6rem}
    nav a{color:var(--muted);text-decoration:none;margin-left:1rem;font-size:.95rem}
    .hero{background:linear-gradient(135deg,rgba(155,92,246,.12),transparent);padding:1.25rem;border-radius:14px;margin-top:1rem}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1rem;margin-top:1rem}
    .card{background:rgba(255,255,255,.03);padding:1rem;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,.6)}
    footer{opacity:.7;margin-top:2rem;font-size:.85rem}
    button.cta{background:linear-gradient(90deg,var(--accent),#6ee7b7);border:0;padding:.5rem .9rem;border-radius:10px;font-weight:600;cursor:pointer}
    @media (max-width:520px){header{flex-direction:column;align-items:flex-start}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div>
        <h1>Привет — это мой сайт</h1>
        <div style="color:var(--muted);font-size:.9rem">Страница-визитка / портфолио</div>
      </div>
      <nav>
        <a href="#about">Обо мне</a>
        <a href="#work">Работы</a>
        <a href="#contact">Контакты</a>
      </nav>
    </header>

    <section class="hero" id="about">
      <div style="display:flex;justify-content:space-between;align-items:center;gap:1rem;flex-wrap:wrap">
        <p style="margin:0;max-width:62%">Я люблю рисовать простыми карандашами и украшать работы — здесь будут мои наброски и заметки.</p>
        <button class="cta" onclick="document.getElementById('work').scrollIntoView({behavior:'smooth'})">Посмотреть работы</button>
      </div>
    </section>

    <section class="grid" id="work">
      <div class="card">
        <h3 style="margin-top:0">Набросок 1</h3>
        <p style="margin:0;color:var(--muted)">Краткое описание. Можно вставить изображение через &lt;img src="..." alt="" /&gt;</p>
      </div>
      <div class="card">
        <h3 style="margin-top:0">Набросок 2</h3>
        <p style="margin:0;color:var(--muted)">Ещё немного текста о технике и идее.</p>
      </div>
      <div class="card">
        <h3 style="margin-top:0">Блок заметок</h3>
        <p style="margin:0;color:var(--muted)">Короткие мысли, ссылки на соцсети или загрузки.</p>
      </div>
    </section>

    <footer id="contact">
      <div class="card" style="margin-top:1rem">
        <strong>Контакты</strong>
        <p style="margin:.25rem 0 0;color:var(--muted)">email: <a href="mailto:you@example.com" style="color:inherit">you@example.com</a></p>
      </div>
      <div style="margin-top:.6rem;color:var(--muted)">© <span id="year"></span></div>
    </footer>
  </div>

  <script>
    // простая мелочь — текущий год
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>