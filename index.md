---
layout: default
permalink: /
title: Inicio
description: Creación de experiencias audiovisuales con una lente contracultural…
keywords: contracultural, audiovisual, análisis crítico
---

<header class="site-header" role="banner">
  <nav class="nav--top" aria-label="Selector de idioma">
    <a href="{{ '/es/' | relative_url }}" class="lang-toggle" aria-current="{% if page.lang == 'es' %}page{% endif %}">ES</a>
    <a href="{{ '/en/' | relative_url }}" class="lang-toggle" aria-current="{% if page.lang == 'en' %}page{% endif %}">EN</a>
  </nav>
  <div class="hero" role="region" aria-labelledby="hero-title">
    <div class="hero__overlay" aria-hidden="true"></div>
    <div class="hero__content">
      <h1 id="hero-title" class="hero__title">
        En silencio y contracorriente.<br>
        <span class="hero__subtitle">No para vencer, sino para descifrar.</span>
      </h1>
      <p class="hero__text">
        Creación de experiencias audiovisuales con una lente contracultural…
      </p>
      <a href="#podcast" class="btn btn--primary" aria-label="Ir a la sección de podcast">Escuchar ahora</a>
    </div>
  </div>
</header>

<main role="main">
  <section id="about" class="section section--split" aria-labelledby="about-title">
    <div>
      <h2 id="about-title">Misión</h2>
      <p>Aquí la descripción de tu misión…</p>
    </div>
    <div>
      <h2>Visión</h2>
      <p>Aquí la descripción de tu visión…</p>
    </div>
  </section>

  <!-- Sección Podcast -->
  <section id="podcast" class="section" aria-labelledby="podcast-title">
    <h2 id="podcast-title">Podcast</h2>
    <!-- Aquí iría tu reproductor embebido, listado de episodios, etc. -->
  </section>
</main>

<footer class="site-footer" role="contentinfo">
  <p>© 2025 TheShakhestudium. Todos los derechos reservados.</p>
  <ul>
    <li><a href="{{ '/terminos/' | relative_url }}">Términos y condiciones</a></li>
    <li><a href="{{ '/privacidad/' | relative_url }}">Política de privacidad</a></li>
    <li><a href="{{ '/contacto/' | relative_url }}">Contacto</a></li>
  </ul>
</footer>
