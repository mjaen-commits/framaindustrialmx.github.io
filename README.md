<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>FRAMA INDUSTRIAL SUPPLY | Proveedor Industrial</title>
  <meta name="description" content="FRAMA Industrial Supply: proveedor industrial para maquiladoras y empresas. Catálogo amplio de MRO, empaques, adhesivos, PPE, herramientas y más.">
  <!-- PRODUCCIÓN: listo para GitHub Pages / Netlify -->
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{ --brand-blue:#0E4DA4; --brand-yellow:#FFC300; --brand-gray:#4B5563; --ink:#0f172a; --bg:#ffffff; --muted:#f3f4f6; --card:#ffffff; --ring:rgba(14,77,164,.2)}
    *{box-sizing:border-box}
    html,body{margin:0}
    body{font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,"Apple Color Emoji","Segoe UI Emoji"; color:var(--ink); background:var(--bg)}
    a{color:var(--brand-blue); text-decoration:none}
    img{max-width:100%; display:block}
    .container{width:min(1200px, 92vw); margin-inline:auto}
    .btn{display:inline-flex; gap:.6rem; align-items:center; padding:.9rem 1.15rem; border-radius:12px; font-weight:600; border:1px solid var(--ring); background:var(--brand-blue); color:#fff; box-shadow:0 8px 22px rgba(14,77,164,.25); transition:.2s}
    .btn:hover{transform:translateY(-2px)}
    .btn.alt{background:var(--brand-yellow); color:#111827; border-color:#eab30833; box-shadow:0 8px 22px rgba(234,179,8,.2)}
    .chip{display:inline-flex; align-items:center; padding:.35rem .6rem; border:1px solid #e5e7eb; border-radius:999px; font-size:.85rem; background:#fff}
    header.nav{position:sticky; top:0; z-index:50; backdrop-filter:saturate(180%) blur(8px); background:rgba(255,255,255,.85); border-bottom:1px solid #eef2f7}
    header .row{display:flex; align-items:center; justify-content:space-between; gap:1rem; padding:.9rem 0}
    .brand{display:flex; align-items:center; gap:.75rem}
    .brand-logo{width:42px; height:42px; border-radius:10px; background:linear-gradient(135deg,var(--brand-blue),#122b5c); display:grid; place-items:center; color:#fff; font-weight:800}
    nav a{margin:0 .65rem; font-weight:600; color:#111827}
    nav a:hover{color:var(--brand-blue)}
    .hero{position:relative; isolation:isolate; overflow:hidden; background:
      radial-gradient(1200px 500px at 10% -20%, #e6efff,transparent 60%),
      radial-gradient(1000px 500px at 110% 20%, #fff1c2, transparent 50%),
      #ffffff}
    .hero::after{content:""; position:absolute; inset:0; z-index:-1; opacity:.08; background-image:url('https://images.unsplash.com/photo-1581092921461-eab62e97a780?q=80&w=1600&auto=format&fit=crop'); background-size:cover; background-position:center}
    .hero-wrap{display:grid; grid-template-columns: 1.2fr .8fr; gap:2rem; align-items:center; padding:clamp(2rem, 4vw + 1rem, 5rem) 0}
    .kicker{display:inline-flex; align-items:center; gap:.5rem; padding:.3rem .6rem; background:#ffffff; border:1px solid #e5e7eb; border-radius:999px; font-weight:600; color:#374151}
    h1{font-size:clamp(2.1rem, 2.6vw + 1.2rem, 3.2rem); line-height:1.12; margin:.6rem 0 1rem; color:#0b1324}
    .lead{font-size:1.1rem; color:#374151}
    .hero-cards{display:grid; gap:1rem; grid-template-columns:repeat(2, minmax(0,1fr))}
    .card{background:var(--card); border:1px solid #e5e7eb; border-radius:18px; padding:1rem; box-shadow:0 6px 18px rgba(2,8,23,.06)}
    .card h4{margin:.4rem 0 .3rem}
    .section{padding:clamp(2.2rem, 3.8vw + 1rem, 4rem) 0}
    .section h2{font-size:clamp(1.6rem, 1.8vw + 1rem, 2.2rem); margin:0 0 1rem}
    .grid{display:grid; gap:1rem}
    .grid.cols-3{grid-template-columns: repeat(3, minmax(0,1fr))}
    .grid.cols-4{grid-template-columns: repeat(4, minmax(0,1fr))}
    @media (max-width: 980px){ .hero-wrap{grid-template-columns:1fr} .grid.cols-3{grid-template-columns: repeat(2, minmax(0,1fr))} .grid.cols-4{grid-template-columns: repeat(2, minmax(0,1fr))} }
    @media (max-width:680px){ nav{display:none} .grid.cols-3,.grid.cols-4{grid-template-columns:1fr} }
    .service{display:grid; grid-template-columns:60px auto; gap:.9rem; align-items:flex-start; padding:1rem; border:1px solid #eef2f7; border-radius:16px; background:#fff}
    .service b{display:block; font-size:1.05rem}
    .catalog-toolbar{display:flex; flex-wrap:wrap; gap:.6rem; align-items:center; justify-content:space-between; margin-bottom:1rem}
    .search{flex:1 1 260px; display:flex; align-items:center; gap:.5rem; background:#fff; border:1px solid #e5e7eb; border-radius:14px; padding:.6rem .8rem}
    .search input{border:0; outline:0; width:100%; font-size:1rem}
    .filters{display:flex; gap:.5rem; flex-wrap:wrap}
    .product{display:flex; flex-direction:column; border:1px solid #e5e7eb; background:#fff; border-radius:18px; overflow:hidden}
    .product .thumb{aspect-ratio:4/3; background:#f8fafc; overflow:hidden}
    .product .body{padding:.9rem}
    .product .title{font-weight:700}
    .price-row{display:flex; align-items:center; gap:.6rem; justify-content:space-between; margin-top:.6rem}
    .price{font-weight:800; color:#0b1324}
    .badge{padding:.2rem .5rem; border-radius:999px; border:1px dashed #cbd5e1; font-size:.8rem; color:#334155}
    .foot{background:#0b1324; color:#cbd5e1}
    .foot a{color:#fff}
    .foot .wrap{display:grid; grid-template-columns: 1.2fr 1fr 1fr; gap:1.2rem; padding:2rem 0}
    .foot small{display:block; margin-top:1rem; color:#94a3b8}
    @media (max-width: 900px){.foot .wrap{grid-template-columns:1fr}}
    .list-unstyled{list-style:none; padding:0; margin:0}
    .list-unstyled li{margin:.35rem 0}
    .tagbar{display:flex; flex-wrap:wrap; gap:.4rem; margin-top:.5rem}
    .pill{background:#0e4da4; color:white; padding:.22rem .55rem; border-radius:999px; font-size:.8rem}
    .whatsapp{position:fixed; right:18px; bottom:18px; z-index:40}
    .muted{color:#6b7280}
    .contact-card{border:1px solid #e5e7eb; border-radius:18px; padding:1rem; background:#fff}
    .map{border:0; width:100%; height:260px; border-radius:12px}
    .tests{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; font-size:.85rem; background:#0b1324; color:#cbd5e1; border-radius:12px; padding:.75rem 1rem; margin-top:.75rem}
  </style>
</head>
<body>
  <!-- =================== NAV =================== -->
  <header class="nav">
    <div class="container row">
      <div class="brand">
        <div class="brand-logo">F</div>
        <div>
          <strong>FRAMA INDUSTRIAL SUPPLY</strong><br>
          <small class="muted">Proveedor industrial para maquiladoras y empresas</small>
        </div>
      </div>
      <nav>
        <a href="#servicios">Servicios</a>
        <a href="#catalogo">Catálogo</a>
        <a href="#nosotros">Nosotros</a>
        <a href="#contacto" class="btn" style="padding:.55rem .9rem">Contactar</a>
      </nav>
    </div>
  </header>

  <!-- =================== HERO =================== -->
  <section class="hero">
    <div class="container hero-wrap">
      <div>
        <span class="kicker">Abastecimiento integral • Entregas confiables</span>
        <h1>Todo lo que tu planta necesita, con servicio ágil y catálogo robusto.</h1>
        <p class="lead">Suministros MRO, empaques, adhesivos, PPE, ferretería, oficina y más. Atendemos <b>maquiladoras</b> y empresas de todos los tamaños en Baja California y el resto de México.</p>
        <div style="display:flex; gap:.6rem; margin-top:1rem">
          <a href="#catalogo" class="btn">Ver catálogo</a>
          <a href="#contacto" class="btn alt">Solicitar cotización</a>
        </div>
        <div class="tagbar">
          <span class="pill">Entrega local</span>
          <span class="pill" style="background:#111827">Facturación 100%</span>
          <span class="pill" style="background:#374151">Crédito empresarial</span>
        </div>
      </div>
      <div class="hero-cards">
        <div class="card">
          <img alt="Almacén industrial" src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3"/>
          <h4>Abasto inteligente</h4>
          <p class="muted">Consolidamos compras y reducimos tiempos muertos con inventario bajo pedido.</p>
        </div>
        <div class="card">
          <img alt="Equipo de protección personal" src="https://images.unsplash.com/photo-1581091870622-7b1c1c2d05a8?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3"/>
          <h4>Calidad y cumplimiento</h4>
          <p class="muted">Productos con especificaciones para seguridad, empaque y procesos productivos.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- =================== SERVICIOS =================== -->
  <section id="servicios" class="section">
    <div class="container">
      <h2>Servicios para tu operación</h2>
      <div class="grid cols-3">
        <div class="service">
          <img width="60" height="60" alt="Consolidación" src="https://images.unsplash.com/photo-1566576912321-d58ddd7a6088?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Consolidación de compras MRO</b>
            <small class="muted">Un solo proveedor para consumibles, refacciones y ferretería. Simplifica requisiciones y pagos.</small>
          </div>
        </div>
        <div class="service">
          <img width="60" height="60" alt="Urgentes" src="https://images.unsplash.com/photo-1544620347-c4fd4a3d5957?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Atención a urgencias y paros</b>
            <small class="muted">Respuesta ágil para evitar tiempos muertos. Alternativas equivalentes certificadas.</small>
          </div>
        </div>
        <div class="service">
          <img width="60" height="60" alt="Entrega" src="https://images.unsplash.com/photo-1529078155058-5d716f45d604?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Entregas locales y nacionales</b>
            <small class="muted">Cobertura en Baja California y envíos a todo México con paqueterías confiables.</small>
          </div>
        </div>
        <div class="service">
          <img width="60" height="60" alt="Sourcing" src="https://images.unsplash.com/photo-1581093588401-16ec5a09f95d?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Sourcing y equivalencias</b>
            <small class="muted">Te ayudamos a encontrar equivalentes en adhesivos, tapes, químicos y PPE.</small>
          </div>
        </div>
        <div class="service">
          <img width="60" height="60" alt="Contrato" src="https://images.unsplash.com/photo-1554224155-6726b3ff858f?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Precios y contratos</b>
            <small class="muted">Acuerdos de precio, listas y catálogos por planta para control y auditoría.</small>
          </div>
        </div>
        <div class="service">
          <img width="60" height="60" alt="Facturación" src="https://images.unsplash.com/photo-1554224155-3a589877a98d?q=80&w=300&h=300&auto=format&fit=crop" />
          <div>
            <b>Facturación 100% y crédito</b>
            <small class="muted">Facturamos a tiempo y ofrecemos crédito empresarial para clientes recurrentes.</small>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- =================== CATALOGO =================== -->
  <section id="catalogo" class="section" style="background:var(--muted)">
    <div class="container">
      <h2>Catálogo de productos</h2>
      <div class="catalog-toolbar">
        <div class="search">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M21 21l-3.5-3.5M10.5 18a7.5 7.5 0 1 1 0-15 7.5 7.5 0 0 1 0 15Z" stroke="#64748b" stroke-width="2" stroke-linecap="round"/></svg>
          <input id="q" placeholder="Buscar por nombre, SKU, categoría…"/>
        </div>
        <div class="filters" id="filters"></div>
        <button class="btn alt" id="downloadCsv" title="Exportar tabla">Descargar CSV</button>
      </div>
      <div class="grid cols-4" id="grid"></div>
      <div id="testPanel" class="tests"></div>
    </div>
  </section>

  <!-- =================== NOSOTROS =================== -->
  <section id="nosotros" class="section">
    <div class="container">
      <div class="grid cols-3" style="align-items:center">
        <div style="grid-column: span 2">
          <h2>¿Por qué FRAMA?</h2>
          <p class="lead">Somos tu aliado de abastecimiento industrial. Integramos múltiples líneas de producto para <b>reducir proveedores</b>, estandarizar compras y asegurar <b>entregas confiables</b> con excelente relación costo‑beneficio.</p>
          <ul class="list-unstyled" style="columns:2; gap:1rem">
            <li>• Más de 10 categorías MRO</li>
            <li>• Catálogos por planta/área</li>
            <li>• Alternativas y equivalencias</li>
            <li>• Atención a urgencias</li>
            <li>• Facturación y soporte</li>
            <li>• Crédito empresarial</li>
          </ul>
        </div>
        <div class="contact-card">
          <b>Datos de empresa</b>
          <p class="muted">FRAMA INDUSTRIAL SUPPLY<br>Puebla 91‑2, Emiliano Zapata, 21460 Tecate, B.C.</p>
          <p>Tel: <a href="tel:+526656545282">(665) 654 5282</a> · WhatsApp: <a href="https://wa.me/526658515273" target="_blank" rel="noopener">(665) 851 5273</a><br>
          Correo: <a href="mailto:ventas@frama.com">ventas@frama.com</a></p>
          <iframe class="map" loading="lazy" allowfullscreen referrerpolicy="no-referrer-when-downgrade" src="https://www.google.com/maps?q=Puebla%2091-2%2C%20Emiliano%20Zapata%2C%2021460%20Tecate&t=&z=15&ie=UTF8&iwloc=&output=embed"></iframe>
        </div>
      </div>
    </div>
  </section>

  <!-- =================== CONTACTO =================== -->
  <section id="contacto" class="section" style="background:var(--muted)">
    <div class="container">
      <h2>Solicitar cotización</h2>
      <div class="grid cols-3">
        <form id="quoteForm" class="contact-card" style="grid-column: span 2">
          <label>Nombre<br>
            <input name="nombre" required placeholder="Tu nombre" style="width:100%; padding:.7rem .8rem; border:1px solid #e5e7eb; border-radius:12px">
          </label><br><br>
          <label>Empresa<br>
            <input name="empresa" required placeholder="Nombre de tu empresa" style="width:100%; padding:.7rem .8rem; border:1px solid #e5e7eb; border-radius:12px">
          </label><br><br>
          <label>Correo<br>
            <input type="email" name="correo" required placeholder="correo@empresa.com" style="width:100%; padding:.7rem .8rem; border:1px solid #e5e7eb; border-radius:12px">
          </label><br><br>
          <label>Mensaje<br>
            <textarea name="mensaje" rows="5" required placeholder="Cuéntanos qué necesitas (SKU, cantidad, entrega, etc.)" style="width:100%; padding:.7rem .8rem; border:1px solid #e5e7eb; border-radius:12px"></textarea>
          </label>
          <div style="display:flex; gap:.6rem; margin-top:1rem">
            <button type="submit" class="btn">Enviar por correo</button>
            <a id="waLink" class="btn alt" target="_blank" rel="noopener" href="#">Enviar por WhatsApp</a>
          </div>
          <small class="muted">*Este formulario abre tu app de correo o WhatsApp con el mensaje prellenado.</small>
        </form>
        <div class="contact-card">
          <b>Atención a clientes</b>
          <p>Lun–Vie: 8:00–17:00<br> Sáb–Dom: Cerrado</p>
          <p><a class="btn" style="width:100%; justify-content:center" href="tel:+526656545282">Llamar ahora</a></p>
          <p><a class="btn alt" style="width:100%; justify-content:center" target="_blank" rel="noopener" href="https://wa.me/526658515273">WhatsApp ventas</a></p>
        </div>
      </div>
    </div>
  </section>

  <!-- =================== FOOTER =================== -->
  <footer class="foot">
    <div class="container wrap">
      <div>
        <div class="brand" style="color:#fff">
          <div class="brand-logo">F</div>
          <div>
            <strong>FRAMA INDUSTRIAL SUPPLY</strong><br>
            <small>Proveedor industrial integral</small>
          </div>
        </div>
        <small>© <span id="year"></span> FRAMA Industrial Supply. Todos los derechos reservados.</small>
      </div>
      <div>
        <b style="color:#fff">Categorías</b>
        <ul class="list-unstyled">
          <li><a href="#catalogo">PPE / Seguridad</a></li>
          <li><a href="#catalogo">Empaques y Tapes</a></li>
          <li><a href="#catalogo">Herramientas</a></li>
          <li><a href="#catalogo">Químicos y Limpieza</a></li>
        </ul>
      </div>
      <div>
        <b style="color:#fff">Soporte</b>
        <ul class="list-unstyled">
          <li><a href="#contacto">Solicitar cotización</a></li>
          <li><a href="mailto:ventas@frama.com">ventas@frama.com</a></li>
          <li><a href="https://wa.me/526658515273" target="_blank" rel="noopener">WhatsApp</a></li>
        </ul>
      </div>
    </div>
  </footer>

  <a class="whatsapp btn" href="https://wa.me/526658515273" target="_blank" rel="noopener" aria-label="WhatsApp"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M7.4 10.5c.2 0 .4 0 .5.3l.8 1.7c.1.2.1.4 0 .6l-.5 1c.7.4 1.6.7 2.4.8 1 .1 2-.1 2.9-.5.9-.4 1.6-1 2.1-1.8.5-.7.8-1.6.8-2.6 0-.9-.3-1.7-.8-2.5-.5-.7-1.2-1.3-2.1-1.7-.8-.4-1.7-.5-2.6-.4-.9.1-1.7.4-2.4.9-.7.5-1.2 1.1-1.6 1.8-.3.6-.5 1.3-.5 2 0 .2 0 .4 0 .6H6.1c-.3 0-.5-.2-.5-.5C5.5 8 6.2 6.7 7.4 5.7 8.7 4.6 10.4 4 12.2 4c1.7 0 3.3.5 4.5 1.4 1.2.9 2.1 2 2.7 3.2.6 1.2.8 2.5.7 3.7-.2 1.3-.7 2.5-1.6 3.5-.9 1-2 1.8-3.3 2.4-1.3.6-2.8 1.2-4.4 1.2-1.3 0-2.6-.3-3.8-.8" stroke="#fff" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round"/></svg></a>

  <script>
    // =================== DATA (mock para catálogo) ===================
    const CATEGORIES = [
      "PPE / Seguridad","Empaques y Tapes","Herramientas","MRO / Refacciones",
      "Químicos y Limpieza","Adhesivos y Selladores","Eléctrico","Oficina"
    ];
    const PRODUCTS = [
      {sku:"PPE-001", title:"Guantes de Nitrilo (Caja 100 pzas)", price:189, cat:"PPE / Seguridad", img:"https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?q=80&w=900&auto=format&fit=crop"},
      {sku:"PPE-002", title:"Lentes de Seguridad Antiempañantes", price:129, cat:"PPE / Seguridad", img:"https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?q=80&w=900&auto=format&fit=crop"},
      {sku:"PPE-003", title:"Casco Industrial ABS Clase E", price:349, cat:"PPE / Seguridad", img:"https://images.unsplash.com/photo-1558929996-da64ba858215?q=80&w=900&auto=format&fit=crop"},
      {sku:"PPE-004", title:"Respirador Media Cara + Filtros", price:799, cat:"PPE / Seguridad", img:"https://images.unsplash.com/photo-1584367369853-8b966cf2235d?q=80&w=900&auto=format&fit=crop"},
      {sku:"PPE-005", title:"Protector Auditivo Tipo Copa", price:229, cat:"PPE / Seguridad", img:"https://images.unsplash.com/photo-1543269865-0a740d43b90c?q=80&w=900&auto=format&fit=crop"},

      {sku:"PKG-101", title:"Cinta Canela 48mm x 150m (Pack 6)", price:239, cat:"Empaques y Tapes", img:"https://images.unsplash.com/photo-1584917865442-de89df76afd3?q=80&w=900&auto=format&fit=crop"},
      {sku:"PKG-102", title:"Stretch Film 18\" x 1500' 80G", price:649, cat:"Empaques y Tapes", img:"https://images.unsplash.com/photo-1599920044706-5e1aaf8d7388?q=80&w=900&auto=format&fit=crop"},
      {sku:"PKG-103", title:"Etiquetas Térmicas 4x6\" (Rollo 1000)", price:299, cat:"Empaques y Tapes", img:"https://images.unsplash.com/photo-1585386959984-a41552231653?q=80&w=900&auto=format&fit=crop"},
      {sku:"PKG-104", title:"Cinta Doble Cara Industrial", price:199, cat:"Empaques y Tapes", img:"https://images.unsplash.com/photo-1615485737651-6ea37d16b912?q=80&w=900&auto=format&fit=crop"},
      {sku:"PKG-105", title:"Bolsas Plásticas Grado Industrial (Kg)", price:179, cat:"Empaques y Tapes", img:"https://images.unsplash.com/photo-1516637090014-cb1ab0d08fc7?q=80&w=900&auto=format&fit=crop"},

      {sku:"TL-201", title:"Juego Llaves Combinadas 14pzas", price:999, cat:"Herramientas", img:"https://images.unsplash.com/photo-1517059224940-d4af9eec41e5?q=80&w=900&auto=format&fit=crop"},
      {sku:"TL-202", title:"Taladro Percutor 1/2\" 750W", price:1499, cat:"Herramientas", img:"https://images.unsplash.com/photo-1504148455329-4ff0802cfb7e?q=80&w=900&auto=format&fit=crop"},
      {sku:"TL-203", title:"Multímetro Digital True RMS", price:899, cat:"Herramientas", img:"https://images.unsplash.com/photo-1604228741406-3faa38f33201?q=80&w=900&auto=format&fit=crop"},
      {sku:"TL-204", title:"Juego Destornilladores Aislados", price:649, cat:"Herramientas", img:"https://images.unsplash.com/photo-1520671452279-9b53dbdbeaf3?q=80&w=900&auto=format&fit=crop"},
      {sku:"TL-205", title:"Rotomartillo SDS-Plus", price:2399, cat:"Herramientas", img:"https://images.unsplash.com/photo-1621891330380-3f0fd1677877?q=80&w=900&auto=format&fit=crop"},

      {sku:"MRO-301", title:"Rodamiento 6203 2RS", price:69, cat:"MRO / Refacciones", img:"https://images.unsplash.com/photo-1605540436563-1def02d31153?q=80&w=900&auto=format&fit=crop"},
      {sku:"MRO-302", title:"Banda V A45", price:139, cat:"MRO / Refacciones", img:"https://images.unsplash.com/photo-1599282962456-0d2db569f4b0?q=80&w=900&auto=format&fit=crop"},
      {sku:"MRO-303", title:"Grasa Litio EP-2 (Cartucho)", price:119, cat:"MRO / Refacciones", img:"https://images.unsplash.com/photo-1615485737651-6ea37d16b912?q=80&w=900&auto=format&fit=crop"},
      {sku:"MRO-304", title:"Engrane Recto Módulo 2", price:319, cat:"MRO / Refacciones", img:"https://images.unsplash.com/photo-1454179083322-198bb4daae73?q=80&w=900&auto=format&fit=crop"},
      {sku:"MRO-305", title:"Manguera Neumática PU 3/8\"", price:249, cat:"MRO / Refacciones", img:"https://images.unsplash.com/photo-1566385101042-74eaa0f0b795?q=80&w=900&auto=format&fit=crop"},

      {sku:"CLN-401", title:"Desengrasante Industrial 20L", price:799, cat:"Químicos y Limpieza", img:"https://images.unsplash.com/photo-1622228051698-7ef31b5b9d0c?q=80&w=900&auto=format&fit=crop"},
      {sku:"CLN-402", title:"Alcohol Isopropílico 99% 1L", price:169, cat:"Químicos y Limpieza", img:"https://images.unsplash.com/photo-1583947581924-860bda6a26c6?q=80&w=900&auto=format&fit=crop"},
      {sku:"CLN-403", title:"Toallas Industriales Plegadas", price:229, cat:"Químicos y Limpieza", img:"https://images.unsplash.com/photo-1581578731548-c64695cc6952?q=80&w=900&auto=format&fit=crop"},
      {sku:"CLN-404", title:"Sanitizante Superficies 4L", price:269, cat:"Químicos y Limpieza", img:"https://images.unsplash.com/photo-1581578017426-c2c5a4b5c609?q=80&w=900&auto=format&fit=crop"},
      {sku:"CLN-405", title:"Detergente Alcalino 20L", price:949, cat:"Químicos y Limpieza", img:"https://images.unsplash.com/photo-1581579188871-45ea61f2a0d3?q=80&w=900&auto=format&fit=crop"},

      {sku:"ADH-501", title:"Silicón RTV Alta Temperatura", price:149, cat:"Adhesivos y Selladores", img:"https://images.unsplash.com/photo-1581091012993-2d460104fe1c?q=80&w=900&auto=format&fit=crop"},
      {sku:"ADH-502", title:"Epóxico 5 Minutos (2 Partes)", price:119, cat:"Adhesivos y Selladores", img:"https://images.unsplash.com/photo-1608571425182-9e3c988bd5e6?q=80&w=900&auto=format&fit=crop"},
      {sku:"ADH-503", title:"Cianoacrilato 20g Industrial", price:79, cat:"Adhesivos y Selladores", img:"https://images.unsplash.com/photo-1615485737651-6ea37d16b912?q=80&w=900&auto=format&fit=crop"},
      {sku:"ADH-504", title:"Sellador PU Construcción", price:189, cat:"Adhesivos y Selladores", img:"https://images.unsplash.com/photo-1581093588401-16ec5a09f95d?q=80&w=900&auto=format&fit=crop"},
      {sku:"ADH-505", title:"Cinta de Aluminio 2\"", price:129, cat:"Adhesivos y Selladores", img:"https://images.unsplash.com/photo-1615484499515-4de9dfc3f6c7?q=80&w=900&auto=format&fit=crop"},

      {sku:"ELC-601", title:"Cable THHN Calibre 12 (100m)", price:1499, cat:"Eléctrico", img:"https://images.unsplash.com/photo-1593287073863-1bb100a2cde3?q=80&w=900&auto=format&fit=crop"},
      {sku:"ELC-602", title:"Terminales de Ojo SurtiPack", price:159, cat:"Eléctrico", img:"https://images.unsplash.com/photo-1581094377146-e3aee5269ba9?q=80&w=900&auto=format&fit=crop"},
      {sku:"ELC-603", title:"Canaleta Plástica 40x60mm 2m", price:219, cat:"Eléctrico", img:"https://images.unsplash.com/photo-1618897996318-5e9f9d54b9cd?q=80&w=900&auto=format&fit=crop"},
      {sku:"ELC-604", title:"Breaker Termomagnético 2P 20A", price:329, cat:"Eléctrico", img:"https://images.unsplash.com/photo-1573739025193-d7c5a6b1b059?q=80&w=900&auto=format&fit=crop"},
      {sku:"ELC-605", title:"Conectores Rápidos Wago (Pack)", price:129, cat:"Eléctrico", img:"https://images.unsplash.com/photo-1558346648-9757f2fa4475?q=80&w=900&auto=format&fit=crop"},

      {sku:"OFF-701", title:"Papel Bond Carta 75g (500)", price:139, cat:"Oficina", img:"https://images.unsplash.com/photo-1517048676732-d65bc937f952?q=80&w=900&auto=format&fit=crop"},
      {sku:"OFF-702", title:"Plumas Gel 0.7mm (12)", price:89, cat:"Oficina", img:"https://images.unsplash.com/photo-1587614382346-4ec70e388b28?q=80&w=900&auto=format&fit=crop"},
      {sku:"OFF-703", title:"Cinta Masking 24mm x 50m", price:59, cat:"Oficina", img:"https://images.unsplash.com/photo-1484480974693-6ca0a78fb36b?q=80&w=900&auto=format&fit=crop"},
      {sku:"OFF-704", title:"Folder Colgante Letter (25)", price:169, cat:"Oficina", img:"https://images.unsplash.com/photo-1553729784-e91953dec042?q=80&w=900&auto=format&fit=crop"},
      {sku:"OFF-705", title:"Tóner Compatible (Modelo común)", price:579, cat:"Oficina", img:"https://images.unsplash.com/photo-1587825140400-5cfa2f5f3b63?q=80&w=900&auto=format&fit=crop"}
    ];

    // =================== RENDER ===================
    const grid = document.getElementById('grid');
    const filterWrap = document.getElementById('filters');
    const q = document.getElementById('q');

    function renderFilters(){
      filterWrap.innerHTML = '<span class="chip" data-cat="Todos">Todas</span>' +
        CATEGORIES.map(c=>`<span class="chip" data-cat="${c}">${c}</span>`).join('');
      [...filterWrap.querySelectorAll('.chip')].forEach(chip=>{
        chip.addEventListener('click',()=>{
          const cat = chip.dataset.cat;
          document.querySelectorAll('.chip').forEach(c=>c.style.outline='none');
          chip.style.outline='2px solid var(--ring)';
          applyFilters(cat, q.value.trim().toLowerCase());
        })
      })
    }

    function productCard(p){
      return `<article class="product" data-cat="${p.cat}" data-title="${p.title.toLowerCase()}" data-sku="${p.sku.toLowerCase()}">
        <div class="thumb"><img alt="${p.title}" src="${p.img}"></div>
        <div class="body">
          <div class="badge">${p.sku}</div>
          <div class="title">${p.title}</div>
          <div class="price-row"><span class="price">$${p.price}</span>
          <button class="btn" style="padding:.45rem .7rem" onclick="requestQuote('${p.sku}','${p.title.replace(/'/g, "&#39;")}')">Cotizar</button></div>
          <div class="muted" style="margin-top:.45rem">Cat: ${p.cat}</div>
        </div>
      </article>`
    }

    function renderGrid(list){ grid.innerHTML = list.map(productCard).join('') }

    function applyFilters(cat='Todos', text=''){
      const items = PRODUCTS.filter(p=> (cat==='Todos' || p.cat===cat) &&
        (p.title.toLowerCase().includes(text) || p.sku.toLowerCase().includes(text)) );
      renderGrid(items)
    }

    renderFilters();
    renderGrid(PRODUCTS);

    q.addEventListener('input', e=> applyFilters('Todos', e.target.value.trim().toLowerCase()))

    // =================== Actions ===================
    function requestQuote(sku,title){
      const subject = encodeURIComponent(`[Cotización] ${sku} – ${title}`);
      const body = encodeURIComponent(`Hola FRAMA,\n\nMe gustaría cotizar:\nSKU: ${sku}\nProducto: ${title}\nCantidad: ___\nEntrega: ___\n\nEmpresa: ___\nContacto: ___\nTeléfono: ___\n`);
      window.location.href = `mailto:ventas@frama.com?subject=${subject}&body=${body}`;
    }

    document.getElementById('downloadCsv').addEventListener('click', ()=>{
      const headers = ['SKU','Título','Precio','Categoría'];
      const rows = PRODUCTS.map(p=>[p.sku, p.title, p.price, p.cat]);
      const csv = [headers, ...rows]
        .map(r=>r.map(v=>`"${String(v).replaceAll('"','""')}"`).join(','))
        .join('\n');
      const blob = new Blob([csv], {type:'text/csv;charset=utf-8;'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href=url; a.download='FRAMA_catalogo.csv'; a.click(); URL.revokeObjectURL(url);
    })

    // Contact form handlers
    const form = document.getElementById('quoteForm');
    const wa = document.getElementById('waLink');
    form.addEventListener('submit', (e)=>{
      e.preventDefault();
      const data = new FormData(form);
      const msg = `Solicitud de cotización\nNombre: ${data.get('nombre')}\nEmpresa: ${data.get('empresa')}\nCorreo: ${data.get('correo')}\nMensaje: ${data.get('mensaje')}`;
      const subject = encodeURIComponent('[Cotización] Sitio Web FRAMA');
      const body = encodeURIComponent(msg);
      window.location.href = `mailto:ventas@frama.com?subject=${subject}&body=${body}`;
    });
    wa.addEventListener('click', (e)=>{
      const data = new FormData(form);
      const nombre = (data.get('nombre')||'').trim();
      const empresa = (data.get('empresa')||'').trim();
      const mensaje = (data.get('mensaje')||'').trim();
      const text = encodeURIComponent(`Hola FRAMA,\n${nombre && empresa ? nombre+" de "+empresa : 'Cliente FRAMA'} solicita cotización.\n${mensaje || 'Por favor contacten para detalles.'}`);
      const url = `https://wa.me/526658515273?text=${text}`;
      e.preventDefault();
      window.open(url, '_blank', 'noopener');
    });

    document.getElementById('year').textContent = new Date().getFullYear();

    // =================== TESTS (se muestran en consola + panel) ===================
    function runTests(){
      const results = [];
      try {
        const hasBroken = PRODUCTS.some(p => /18\"|4x6\"|1\/2\"|3\/8\"|2\"/.test(p.title) === false && /\"/.test(p.title));
        results.push({name:'Títulos con pulgadas escapadas', pass: !hasBroken});
      } catch(err){ results.push({name:'Títulos con pulgadas escapadas', pass:false, err}); }
      const sample = encodeURIComponent('Hola FRAMA,\nMiguel de FRAMA solicita cotización.\nLentes 4x6"');
      const waUrl = `https://wa.me/526658515273?text=${sample}`;
      results.push({name:'WhatsApp URL codificada', pass: !/\s/.test(waUrl)});
      const field = 'Cinta 2" x 50m';
      const csvField = `"${field.replaceAll('"','""')}"`;
      results.push({name:'CSV escapa comillas correctamente', pass: csvField === '"Cinta 2"" x 50m"'});
      applyFilters('Todos','ppe');
      const countAfter = grid.children.length;
      results.push({name:'Filtro por texto (ppe) devuelve resultados', pass: countAfter > 0});
      renderGrid(PRODUCTS);
      const panel = document.getElementById('testPanel');
      panel.style.display = 'block';
      panel.innerHTML = '<b>Resultados de pruebas</b><ul style="margin:.5rem 0 0; padding-left:1rem">' +
        results.map(r=>`<li>${r.pass ? '✅' : '❌'} ${r.name}${r.err? ' — ' + r.err : ''}</li>`).join('') + '</ul>';
      console.log('[TEST RESULTS]', results);
    }
    runTests();
  </script>
</body>
</html>
