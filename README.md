## Hi there 👋
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Josue | Portafolio</title>
  <meta name="description" content="Portafolio de Josue: proyectos, habilidades y contacto." />
  <meta name="color-scheme" content="light dark">
  <style>
    /* ====== Reset & Base ====== */
    *, *::before, *::after { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      line-height: 1.6; background: var(--bg); color: var(--text);
    }

    :root{
      --bg: #0b0c10; /* dark base */
      --text: #eaf6ff;
      --muted: #b8c7d9;
      --card: #11131a;
      --card-2: #0f172a;
      --primary: #60a5fa; /* azul */
      --primary-2:#a78bfa; /* violeta */
      --accent: #34d399; /* verde */
      --ring: rgba(96,165,250,.55);
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 1.25rem;
      --radius-sm: .875rem;
      --maxw: 1100px;
      --nav-h: 64px;
    }
    .light{
      --bg: #f8fafc;
      --text: #0b1220;
      --muted: #4b5563;
      --card: #ffffff;
      --card-2: #f1f5f9;
      --primary: #2563eb;
      --primary-2: #7c3aed;
      --accent: #059669;
      --ring: rgba(37,99,235,.35);
      --shadow: 0 12px 30px rgba(2,6,23,.08);
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }
    .container { width: min(100%, var(--maxw)); margin-inline: auto; padding-inline: 1.2rem; }

    /* ====== Navbar ====== */
    .nav {
      position: sticky; top: 0; z-index: 50; height: var(--nav-h);
      backdrop-filter: saturate(140%) blur(8px);
      background: color-mix(in oklab, var(--bg) 80%, transparent);
      border-bottom: 1px solid color-mix(in oklab, var(--text) 12%, transparent);
    }
    .nav .wrap{display:flex; align-items:center; justify-content:space-between; height:100%;}
    .brand{ display:flex; align-items:center; gap:.65rem; font-weight:800; letter-spacing:.4px; }
    .dot{ width: .9rem; height: .9rem; border-radius: 999px; background: linear-gradient(135deg, var(--primary), var(--accent)); box-shadow: 0 0 0 .25rem color-mix(in oklab, var(--ring), transparent 60%);} 
    .links{ display:flex; gap: .8rem; align-items:center; }
    .links a{ padding:.55rem .8rem; border-radius: .8rem; color: var(--muted); font-weight:600; }
    .links a:hover{ color: var(--text); background: color-mix(in oklab, var(--text) 8%, transparent); }
    .btn-theme{border:1px solid color-mix(in oklab, var(--text) 15%, transparent); background: var(--card); padding:.55rem .8rem; border-radius: .8rem; cursor:pointer; color:var(--text)}

    /* ====== Hero ====== */
    .hero{
      position: relative; overflow:hidden; padding-top: calc(1.2rem + var(--nav-h)); padding-bottom: 4rem;
      background: radial-gradient(1200px 600px at 80% -10%, color-mix(in oklab, var(--primary), transparent 65%), transparent),
                  radial-gradient(1200px 600px at 20% -10%, color-mix(in oklab, var(--primary-2), transparent 65%), transparent);
      border-bottom: 1px solid color-mix(in oklab, var(--text) 8%, transparent);
    }
    .hero .content{ display:grid; grid-template-columns: 1.1fr .9fr; gap: 2rem; align-items:center; }
    .kicker{ color: var(--accent); font-weight:700; letter-spacing:.12em; text-transform:uppercase; font-size:.8rem; }
    .title{ font-size: clamp(2rem, 5vw, 3.8rem); line-height:1.1; margin:.4rem 0 1rem; font-weight:900; }
    .subtitle{ font-size: clamp(1rem, 2.2vw, 1.25rem); color: var(--muted); max-width: 60ch; }
    .cta{ display:flex; gap: .8rem; flex-wrap:wrap; margin-top:1.4rem; }
    .btn{
      display:inline-flex; align-items:center; gap:.55rem; padding:.85rem 1rem; border-radius: 999px; border:1px solid color-mix(in oklab, var(--text) 15%, transparent); font-weight:700; transition: transform .15s ease; box-shadow: var(--shadow);
    }
    .btn:hover{ transform: translateY(-2px); }
    .btn-primary{ background: linear-gradient(135deg, var(--primary), var(--primary-2)); color: white; border-color: transparent; }
    .btn-ghost{ background: var(--card); color: var(--text); }

    .hero .card{
      background: linear-gradient(180deg, color-mix(in oklab, var(--card-2), transparent 0%), var(--card));
      border:1px solid color-mix(in oklab, var(--text) 10%, transparent); padding:1.2rem; border-radius: var(--radius);
      transform: rotate(-1deg); box-shadow: var(--shadow);
    }
    .badge{
      display:inline-block; padding:.35rem .7rem; border-radius:999px; background: color-mix(in oklab, var(--text) 8%, transparent); color: var(--muted); font-size:.85rem; margin:.25rem; border:1px dashed color-mix(in oklab, var(--text) 15%, transparent);
    }

    /* ====== Sections ====== */
    section { padding: 4rem 0; }
    .section-title{ font-size: clamp(1.4rem, 3.5vw, 2rem); margin: 0 0 1rem; }
    .section-sub{ color: var(--muted); margin-bottom: 2rem; }

    /* Projects Grid */
    .grid{ display:grid; gap:1.2rem; }
    @media(min-width: 720px){ .grid{ grid-template-columns: repeat(3, minmax(0,1fr)); } }
    .card-project{
      background: var(--card); border:1px solid color-mix(in oklab, var(--text) 12%, transparent);
      border-radius: var(--radius); overflow:hidden; display:flex; flex-direction:column; transition: transform .2s ease, box-shadow .2s ease; box-shadow: var(--shadow);
    }
    .card-project:hover{ transform: translateY(-4px); box-shadow: 0 18px 45px rgba(0,0,0,.35); }
    .thumb{ aspect-ratio: 16/9; background: linear-gradient(135deg, color-mix(in oklab, var(--primary), transparent 30%), color-mix(in oklab, var(--accent), transparent 40%)); display:grid; place-items:center; font-weight:900; letter-spacing:.1em; color: rgba(255,255,255,.9); }
    .card-body{ padding:1rem; display:flex; flex-direction:column; gap:.6rem; }
    .tags{ display:flex; flex-wrap:wrap; gap:.5rem; }
    .tag{ padding:.35rem .6rem; font-size:.8rem; background: color-mix(in oklab, var(--text) 8%, transparent); border:1px solid color-mix(in oklab, var(--text) 14%, transparent); border-radius: 999px; color: var(--muted); }
    .card-actions{ margin-top:auto; display:flex; gap:.6rem; }

    /* Skills */
    .skills{ display:flex; flex-wrap:wrap; gap:.6rem; }
    .chip{ background: var(--card); border:1px solid color-mix(in oklab, var(--text) 12%, transparent); padding:.6rem .8rem; border-radius:999px; }

    /* About */
    .about{
      background: linear-gradient(180deg, color-mix(in oklab, var(--primary) 12%, transparent), transparent);
      border-top:1px solid color-mix(in oklab, var(--text) 8%, transparent);
      border-bottom:1px solid color-mix(in oklab, var(--text) 8%, transparent);
    }

    /* Contact */
    .contact-card{
      background: var(--card); border:1px solid color-mix(in oklab, var(--text) 12%, transparent); border-radius: var(--radius); padding: 1.2rem; box-shadow: var(--shadow);
    }
    .contact-actions{ display:flex; flex-wrap:wrap; gap:.8rem; }

    /* Footer */
    footer{ padding: 2rem 0; color: var(--muted); border-top:1px solid color-mix(in oklab, var(--text) 8%, transparent); }

    /* Motion */
    @keyframes floaty {
      from { transform: translateY(0px) rotate(-1deg); }
      50% { transform: translateY(-6px) rotate(-1deg); }
      to { transform: translateY(0px) rotate(-1deg); }
    }
    .hero .card{ animation: floaty 7s ease-in-out infinite; }

    /* Small screens */
    @media(max-width: 860px){ .hero .content { grid-template-columns: 1fr; } }
  </style>
</head>
<body>
  <!-- ====== Navbar ====== -->
  <nav class="nav">
    <div class="container wrap">
      <a href="#inicio" class="brand" aria-label="Ir al inicio">
        <span class="dot" aria-hidden="true"></span>
        <span>Josue.dev</span>
      </a>
      <div class="links" role="navigation" aria-label="Secciones del sitio">
        <a href="#proyectos">Proyectos</a>
        <a href="#habilidades">Habilidades</a>
        <a href="#sobre-mi">Sobre mí</a>
        <a href="#contacto">Contacto</a>
        <button class="btn-theme" id="themeToggle" aria-label="Cambiar tema">🌓</button>
      </div>
    </div>
  </nav>

  <!-- ====== Hero ====== -->
  <header class="hero" id="inicio">
    <div class="container content">
      <div>
        <span class="kicker">Portafolio</span>
        <h1 class="title">¡Hola, soy <span style="background:linear-gradient(135deg,var(--primary),var(--primary-2));-webkit-background-clip:text;background-clip:text;color:transparent;">Josue</span>!</h1>
        <p class="subtitle">Desarrollador en construcción, curioso por la tecnología y fan de crear experiencias web limpias, rápidas y accesibles. Aquí encontrarás mis proyectos, habilidades y formas de contactarme.</p>
        <div class="cta">
          <a class="btn btn-primary" href="#proyectos">🚀 Ver proyectos</a>
          <a class="btn btn-ghost" href="https://github.com/tu-usuario" target="_blank" rel="noopener">⭐ Mi GitHub</a>
        </div>
      </div>
      <div class="card" aria-label="Resumen de tecnologías favoritas">
        <h3 style="margin:0 0 .5rem">Stack favorito</h3>
        <div>
          <span class="badge">HTML</span>
          <span class="badge">CSS</span>
          <span class="badge">JavaScript</span>
          <span class="badge">Git & GitHub</span>
          <span class="badge">Responsive Design</span>
        </div>
      </div>
    </div>
  </header>

  <!-- ====== Projects ====== -->
  <section id="proyectos">
    <div class="container">
      <h2 class="section-title">Proyectos destacados</h2>
      <p class="section-sub">Algunos trabajos y experimentos que demuestran mi estilo y lo que puedo aportar.</p>

      <div class="grid">
        <!-- Card 1 -->
        <article class="card-project">
          <div class="thumb" aria-hidden="true">Landing</div>
          <div class="card-body">
            <h3 style="margin:.2rem 0">Landing responsiva moderna</h3>
            <p style="margin:0;color:var(--muted)">Página de aterrizaje optimizada con layout fluido, tipografía clara y componentes reutilizables.</p>
            <div class="tags">
              <span class="tag">HTML</span><span class="tag">CSS Grid</span><span class="tag">Accesible</span>
            </div>
            <div class="card-actions">
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">🔗 Demo</a>
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">💻 Código</a>
            </div>
          </div>
        </article>
        <!-- Card 2 -->
        <article class="card-project">
          <div class="thumb" aria-hidden="true">SPA</div>
          <div class="card-body">
            <h3 style="margin:.2rem 0">Mini SPA con rutas</h3>
            <p style="margin:0;color:var(--muted)">Aplicación de una sola página con navegación sin recargas y componentes modulares.</p>
            <div class="tags">
              <span class="tag">JS</span><span class="tag">Router</span><span class="tag">LocalStorage</span>
            </div>
            <div class="card-actions">
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">🔗 Demo</a>
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">💻 Código</a>
            </div>
          </div>
        </article>
        <!-- Card 3 -->
        <article class="card-project">
          <div class="thumb" aria-hidden="true">API</div>
          <div class="card-body">
            <h3 style="margin:.2rem 0">Dashboard con API pública</h3>
            <p style="margin:0;color:var(--muted)">Consumo de API, manejo de estados y visualización de datos en tarjetas y tablas.</p>
            <div class="tags">
              <span class="tag">Fetch</span><span class="tag">Charts</span><span class="tag">REST</span>
            </div>
            <div class="card-actions">
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">🔗 Demo</a>
              <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">💻 Código</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <!-- ====== Skills ====== -->
  <section id="habilidades" class="about">
    <div class="container">
      <h2 class="section-title">Habilidades</h2>
      <p class="section-sub">Tecnologías y conceptos que uso y estoy aprendiendo.</p>
      <div class="skills">
        <span class="chip">Semántica HTML</span>
        <span class="chip">Flexbox & Grid</span>
        <span class="chip">Accesibilidad (a11y)</span>
        <span class="chip">JavaScript DOM</span>
        <span class="chip">Control de versiones (Git)</span>
        <span class="chip">GitHub Pages</span>
        <span class="chip">SEO básico</span>
        <span class="chip">Optimización web</span>
      </div>
    </div>
  </section>

  <!-- ====== About ====== -->
  <section id="sobre-mi">
    <div class="container">
      <h2 class="section-title">Sobre mí</h2>
      <p class="section-sub">Me gusta resolver problemas y convertir ideas en interfaces útiles. Disfruto aprender cada día y colaborar en equipo.</p>
      <p>Estoy abierto a oportunidades como desarrollador front‑end/junior. Si te interesa lo que hago, ¡hablemos!</p>
    </div>
  </section>

  <!-- ====== Contact ====== -->
  <section id="contacto">
    <div class="container">
      <h2 class="section-title">Contacto</h2>
      <div class="contact-card">
        <p style="margin-top:0">¿Tienes una idea, proyecto o vacante? Escríbeme:</p>
        <div class="contact-actions">
          <a class="btn btn-primary" href="mailto:tu-correo@ejemplo.com">✉️ Enviar correo</a>
          <a class="btn btn-ghost" href="https://github.com/tu-usuario" target="_blank" rel="noopener">🐙 GitHub</a>
          <a class="btn btn-ghost" href="https://www.linkedin.com/in/tu-usuario" target="_blank" rel="noopener">💼 LinkedIn</a>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <div class="container" style="display:flex;justify-content:space-between;gap:1rem;flex-wrap:wrap;align-items:center">
      <small>© <span id="year"></span> Josue. Hecho con ♥ y buen café.</small>
      <small>Diseño simple, rápido y accesible.</small>
    </div>
  </footer>

  <script>
    // Año automático
    document.getElementById('year').textContent = new Date().getFullYear();

    // Tema: guarda preferencia en localStorage y sincroniza con OS
    const root = document.documentElement;
    const prefersLight = window.matchMedia('(prefers-color-scheme: light)');
    const saved = localStorage.getItem('theme');

    function applyTheme(mode){
      if(mode === 'light'){ root.classList.add('light'); }
      else { root.classList.remove('light'); }
    }

    applyTheme(saved ?? (prefersLight.matches ? 'light' : 'dark'));

    prefersLight.addEventListener('change', e => {
      if(!localStorage.getItem('theme')) applyTheme(e.matches ? 'light' : 'dark');
    });

    document.getElementById('themeToggle').addEventListener('click', () => {
      const isLight = root.classList.toggle('light');
      localStorage.setItem('theme', isLight ? 'light' : 'dark');
    });
  </script>
</body>
</html>

<!--
**Josue1895/Josue1895** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

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
