# clip.com

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clipedia | Producción Audiovisual & Vídeo IA</title>
    <style>
        :root {
            --bg-color: #0b0f17;
            --card-bg: #131b2e;
            --accent: #38bdf8;
            --text-main: #ffffff;
            --text-muted: #94a3b8;
            --border: #1e293b;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body { background: var(--bg-color); color: var(--text-main); line-height: 1.6; }

        /* Barra Superior Ecosistema */
        .ecosystem-bar {
            background: #05070c;
            border-bottom: 1px solid var(--border);
            padding: 0.35rem 1.5rem;
            font-size: 0.8rem;
            color: var(--text-muted);
        }
        .ecosystem-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .ecosystem-links { display: flex; gap: 1.2rem; }
        .ecosystem-links a { color: var(--text-muted); text-decoration: none; font-weight: 500; transition: color 0.2s; }
        .ecosystem-links a:hover, .ecosystem-links a.active { color: var(--accent); font-weight: 700; }

        /* Header Principal */
        header { background: rgba(11, 15, 23, 0.95); border-bottom: 1px solid var(--border); position: sticky; top: 0; z-index: 100; backdrop-filter: blur(10px); }
        .nav-container { max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; padding: 0.8rem 1.5rem; }
        
        .logo { display: flex; align-items: center; gap: 10px; text-decoration: none; color: #fff; font-weight: 800; font-size: 1.5rem; }
        .logo svg { width: 32px; height: 32px; }

        .nav-menu { display: flex; gap: 1.5rem; list-style: none; align-items: center; }
        .nav-menu a { color: #fff; text-decoration: none; font-weight: 600; font-size: 0.95rem; }
        .nav-menu a:hover { color: var(--accent); }

        .menu-toggle { display: none; background: none; border: none; color: #fff; font-size: 1.8rem; cursor: pointer; }

        /* Adaptabilidad móvil completa */
        @media (max-width: 768px) {
            .ecosystem-container { flex-direction: column; gap: 0.3rem; text-align: center; }
            .menu-toggle { display: block; }
            .nav-menu { 
                display: none; 
                flex-direction: column; 
                position: absolute; 
                top: 100%; 
                left: 0; 
                right: 0; 
                background: var(--bg-color); 
                border-bottom: 1px solid var(--border); 
                padding: 1.5rem; 
                gap: 1rem; 
            }
            .nav-menu.active { display: flex; }
        }

        .hero { max-width: 900px; margin: 0 auto; text-align: center; padding: 4rem 1.5rem; }
        .hero h1 { font-size: clamp(2rem, 5vw, 3.5rem); font-weight: 800; margin-bottom: 1rem; }
        .hero h1 span { color: var(--accent); }
        .hero p { font-size: 1.15rem; color: var(--text-muted); margin-bottom: 2rem; }

        .cta-btn { display: inline-block; background: var(--accent); color: #000; font-weight: 700; padding: 0.8rem 2rem; border-radius: 8px; text-decoration: none; }

        .grid { max-width: 1200px; margin: 0 auto; padding: 2rem 1.5rem; display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; }
        .card { background: var(--card-bg); border: 1px solid var(--border); padding: 2rem; border-radius: 12px; }
        .card h3 { color: var(--accent); margin-bottom: 0.8rem; }
        .card p { color: var(--text-muted); font-size: 0.95rem; }

        /* Pie de página entrelazado */
        footer { border-top: 1px solid var(--border); padding: 3rem 1.5rem 2rem 1.5rem; background: #070a0f; }
        .footer-container { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 2rem; }
        .footer-col h4 { color: #fff; margin-bottom: 1rem; font-size: 1rem; }
        .footer-col ul { list-style: none; }
        .footer-col ul li { margin-bottom: 0.5rem; }
        .footer-col ul li a { color: var(--text-muted); text-decoration: none; font-size: 0.9rem; }
        .footer-col ul li a:hover { color: var(--accent); }
        .footer-bottom { text-align: center; margin-top: 2rem; padding-top: 1.5rem; border-top: 1px solid var(--border); color: var(--text-muted); font-size: 0.85rem; }
    </style>
</head>
<body>

    <!-- BARRA DE RED / ECOSISTEMA (ENTRELAZADO SUPERIOR) -->
    <div class="ecosystem-bar">
        <div class="ecosystem-container">
            <span>Servicios de la Red:</span>
            <div class="ecosystem-links">
                <a href="https://clipedia.com" class="active">● Clipedia (Vídeo & IA)</a>
                <a href="https://tudirecto.com">TuDirecto (Streaming)</a>
                <a href="https://tuagente.ai">TuAgente (Agentes IA)</a>
            </div>
        </div>
    </div>

    <!-- HEADER DE CLIPEDIA -->
    <header>
        <div class="nav-container">
            <a href="#" class="logo">
                <svg viewBox="0 0 100 100"><polygon points="50,10 20,40 32,52 62,22" fill="#034ea2"/><polygon points="62,22 32,52 44,64 74,34" fill="#0072ce"/><polygon points="74,34 44,64 56,76 86,46" fill="#38bdf8"/></svg>
                <span>Clipedia</span>
            </a>
            <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#clips">Clips & Reels</a></li>
                <li><a href="#ia">Vídeo IA Generativo</a></li>
                <li><a href="#edicion">Edición Pro</a></li>
                <li><a href="#contacto" class="cta-btn" style="color:#000;">Contacto</a></li>
            </ul>
        </div>
    </header>

    <section class="hero">
        <h1>Producción Audiovisual y <span>Vídeo IA</span> de Alto Impacto</h1>
        <p>Transformamos material bruto y conceptos en clips virales, piezas publicitarias y generación sintética de vídeo para marcas modernas.</p>
        <a href="#contacto" class="cta-btn">Crear Contenido</a>
    </section>

    <section class="grid">
        <div class="card" id="clips">
            <h3>Clips & Short-Form Content</h3>
            <p>Edición dinámica y optimizada para TikTok, Instagram Reels y YouTube Shorts orientada a retención y viralidad.</p>
        </div>
        <div class="card" id="ia">
            <h3>Generación de Vídeo e Imagen IA</h3>
            <p>Creación de avatares, hiperrealismo, guiones asistidos y mejora algorítmica de resolución hasta 4K.</p>
        </div>
        <div class="card" id="edicion">
            <h3>Edición & Motion Graphics</h3>
            <p>Postproducción cinematográfica, etalonaje de color, diseño de sonido y animaciones vectoriales para empresas.</p>
        </div>
    </section>

    <!-- FOOTER CON ENLACES CRUZADOS -->
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h4>Clipedia</h4>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Especialistas en edición de vídeo en formato corto, generación IA y piezas audiovisuales.</p>
            </div>
            <div class="footer-col">
                <h4>Ecosistema de Servicios</h4>
                <ul>
                    <li><a href="https://clipedia.com">Clipedia (Vídeo & Clips)</a></li>
                    <li><a href="https://tudirecto.com">TuDirecto (Streaming & eTickets)</a></li>
                    <li><a href="https://tuagente.ai">TuAgente.ai (Agentes Virtuales)</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Contacto</h4>
                <ul>
                    <li><a href="mailto:info@clipedia.com">info@clipedia.com</a></li>
                    <li><a href="tel:+34614218154">+34 614 218 154</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Red de Servicios Digitales. Todos los derechos reservados.</p>
        </div>
    </footer>

    <script>
        function toggleMenu() {
            document.getElementById('navMenu').classList.toggle('active');
        }
    </script>
</body>
</html>
