
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portafolio | Josue</title>
  <meta name="color-scheme" content="light dark" />
  <style>
    :root{
      --bg:#0b0c10;--text:#eaf6ff;--muted:#b8c7d9;--card:#11131a;
      --p:#60a5fa;--p2:#a78bfa;--acc:#34d399;--bd:#1f2430;--r:18px;
    }
    .light{--bg:#f8fafc;--text:#0b1220;--muted:#556276;--card:#ffffff;--bd:#e6e9f2;--p:#2563eb;--p2:#7c3aed;--acc:#059669;}
    *{box-sizing:border-box}
    body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;background:var(--bg);color:var(--text);line-height:1.6}
    a{color:inherit;text-decoration:none}
    .container{max-width:1060px;margin:auto;padding:0 18px}
    /* NAV */
    .nav{position:sticky;top:0;backdrop-filter:saturate(140%) blur(8px);border-bottom:1px solid var(--bd);z-index:10;background:color-mix(in oklab,var(--bg) 85%,transparent)}
    .nav .row{display:flex;align-items:center;justify-content:space-between;height:64px}
    .brand{display:flex;gap:.6rem;align-items:center;font-weight:800}
    .dot{width:12px;height:12px;border-radius:999px;background:linear-gradient(135deg,var(--p),var(--acc))}
    .links{display:flex;gap:.6rem;align-items:center}
    .link{padding:.5rem .75rem;border-radius:10px;color:var(--muted)}
    .link:hover{background:color-mix(in oklab,var(--text) 10%,transparent);color:var(--text)}
    .toggle{border:1px solid var(--bd);background:var(--card);color:var(--text);padding:.5rem .75rem;border-radius:10px;cursor:pointer}
    /* HERO */
    header{padding:90px 0 64px;border-bottom:1px solid var(--bd);
      background:
        radial-gradient(800px 400px at 80% -10%, color-mix(in oklab,var(--p) 30%,transparent), transparent),
        radial-gradient(800px 400px at 20% -10%, color-mix(in oklab,var(--p2) 30%,transparent), transparent);
    }
    .hero{display:grid;grid-template-columns:1.1fr .9fr;gap:28px;align-items:center}
    @media (max-width:880px){.hero{grid-template-columns:1fr}}
    .kicker{color:var(--acc);font-weight:800;text-transform:uppercase;letter-spacing:.12em;font-size:.8rem}
    .title{font-size:clamp(2rem,6vw,3.6rem);line-height:1.1;margin:.4rem 0 1rem;font-weight:900}
    .gradient{background:linear-gradient(135deg,var(--p),var(--p2));-webkit-background-clip:text;background-clip:text;color:transparent}
    .sub{color:var(--muted);max-width:60ch}
    .cta{display:flex;gap:.8rem;flex-wrap:wrap;margin-top:1.2rem}
    .btn{display:inline-flex;align-items:center;gap:.5rem;padding:.8rem 1rem;border-radius:999px;border:1px solid var(--bd);font-weight:700}
    .primary{background:linear-gradient(135deg,var(--p),var(--p2));color:#fff;border:none}
    .card{background:var(--card);border:1px solid var(--bd);padding:16px;border-radius:var(--r);box-shadow:0 12px 30px rgba(0,0,0,.25)}
    .badges{display:flex;flex-wrap:wrap;gap:.4rem}
    .badge{padding:.35rem .65rem;border-radius:999px;border:1px dashed var(--bd);color:var(--muted)}
    /* SECTIONS */
    section{padding:64px 0}
    h2{margin:0 0 8px;font-size:clamp(1.4rem,3.5vw,2rem)}
    .hint{color:var(--muted);margin-bottom:22px}
    .grid{display:grid;gap:14px}
    @media (min-width:720px){.grid{grid-template-columns:repeat(3,1fr)}}
    .proj{display:flex;flex-direction:column;background:var(--card);border:1px solid var(--bd);border-radius:var(--r);overflow:hidden}
    .thumb{aspect-ratio:16/9;display:grid;place-items:center;color:#fff;font-weight:900;letter-spacing:.08em;background:linear-gradient(135deg, color-mix(in oklab,var(--p) 60%,transparent), color-mix(in oklab,var(--acc) 50%,transparent))}
    .body{padding:14px;display:flex;flex-direction:column;gap:.6rem}
    .tags{display:flex;flex-wrap:wrap;gap:.4rem}
    .tag{font-size:.8rem;padding:.3rem .55rem;border:1px solid var(--bd);border-radius:999px;color:var(--muted)}
    .row-actions{margin-top:auto;display:flex;gap:.5rem}
    .about{background:linear-gradient(180deg,color-mix(in oklab,var(--p) 12%,transparent),transparent);border-block:1px solid var(--bd)}
    .contact-card{background:var(--card);border:1px solid var(--bd);border-radius:var(--r);padding:16px}
    footer{padding:26px 0;color:var(--muted);border-top:1px solid var(--bd)}
  </style>
</head>
<body>
  <nav class="nav">
    <div class="container row">
      <a class="brand" href="#inicio"><span class="dot"></span><span>Josue.dev</span></a>
      <div class="links">
        <a class="link" href="#proyectos">Proyectos</a>
        <a class="link" href="#habilidades">Habilidades</a>
        <a class="link" href="#sobre-mi">Sobre mí</a>
        <a class="link" href="#contacto">Contacto</a>
        <button class="toggle" id="toggle">🌓</button>
      </div>
    </div>
  </nav>

  <header id="inicio">
    <div class="container hero">
      <div>
        <span class="kicker">Portafolio</span>
        <h1 class="title">Hola, soy <span class="gradient">Josue</span></h1>
        <p class="sub">Construyo interfaces web limpias, rápidas y accesibles. Mira mis proyectos, habilidades y cómo contactarme.</p>
        <div class="cta">
          <a class="btn primary" href="#proyectos">🚀 Ver proyectos</a>
          <a class="btn" href="https://github.com/tu-usuario" target="_blank" rel="noopener">⭐ Mi GitHub</a>
        </div>
      </div>
      <div class="card" aria-label="Stack favorito">
        <strong>Stack favorito</strong>
        <div class="badges" style="margin-top:.5rem">
          <span class="badge">HTML</span><span class="badge">CSS</span><span class="badge">JavaScript</span>
          <span class="badge">Git & GitHub</span><span class="badge">Responsive</span>
        </div>
      </div>
    </div>
  </header>

  <section id="proyectos">
    <div class="container">
      <h2>Proyectos</h2>
      <p class="hint">Enlaces listos para demo y código.</p>
      <div class="grid">
        <article class="proj">
          <div class="thumb">Landing</div>
          <div class="body">
            <strong>Landing moderna</strong>
            <p class="sub">Layout fluido, tipografía clara y buen performance.</p>
            <div class="tags"><span class="tag">HTML</span><span class="tag">CSS Grid</span><span class="tag">A11y</span></div>
            <div class="row-actions">
              <a class="btn" href="#" target="_blank">🔗 Demo</a>
              <a class="btn" href="#" target="_blank">💻 Código</a>
            </div>
          </div>
        </article>
        <article class="proj">
          <div class="thumb">SPA</div>
          <div class="body">
            <strong>Mini SPA</strong>
            <p class="sub">Navegación sin recargas y componentes modulares.</p>
            <div class="tags"><span class="tag">JS</span><span class="tag">Router</span><span class="tag">LocalStorage</span></div>
            <div class="row-actions">
              <a class="btn" href="#" target="_blank">🔗 Demo</a>
              <a class="btn" href="#" target="_blank">💻 Código</a>
            </div>
          </div>
        </article>
        <article class="proj">
          <div class="thumb">API</div>
          <div class="body">
            <strong>Dashboard API</strong>
            <p class="sub">Consumo de API y visualización de datos.</p>
            <div class="tags"><span class="tag">Fetch</span><span class="tag">REST</span><span class="tag">Charts</span></div>
            <div class="row-actions">
              <a class="btn" href="#" target="_blank">🔗 Demo</a>
              <a class="btn" href="#" target="_blank">💻 Código</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section id="habilidades" class="about">
    <div class="container">
      <h2>Habilidades</h2>
      <p class="hint">Tecnologías que uso y estoy aprendiendo.</p>
      <div class="badges">
        <span class="badge">Semántica HTML</span><span class="badge">Flexbox & Grid</span>
        <span class="badge">Accesibilidad</span><span class="badge">JS DOM</span>
        <span class="badge">Git</span><span class="badge">GitHub Pages</span>
      </div>
    </div>
  </section>

  <section id="sobre-mi">
    <div class="container">
      <h2>Sobre mí</h2>
      <p class="sub">Me gusta resolver problemas y convertir ideas en interfaces útiles. Disfruto aprender y trabajar en equipo.</p>
    </div>
  </section>

  <section id="contacto">
    <div class="container">
      <h2>Contacto</h2>
      <div class="contact-card">
        <p>¿Tienes un proyecto o una vacante? Escríbeme:</p>
        <div class="cta">
          <a class="btn primary" href="mailto:tu-correo@ejemplo.com">✉️ Enviar correo</a>
          <a class="btn" href="https://github.com/tu-usuario" target="_blank" rel="noopener">🐙 GitHub</a>
          <a class="btn" href="https://www.linkedin.com/in/tu-usuario" target="_blank" rel="noopener">💼 LinkedIn</a>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <div class="container" style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap">
      <small>© <span id="year"></span> Josue.</small>
      <small>Hecho con ♥ y buen café.</small>
    </div>
  </footer>

  <script>
    // Cambia año automáticamente
    document.getElementById("year").textContent = new Date().getFullYear();

    // Toggle modo claro/oscuro
    const toggle = document.getElementById("toggle");
    toggle.addEventListener("click", () => {
      document.body.classList.toggle("light");
    });
  </script>
</body>
</html>
Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
