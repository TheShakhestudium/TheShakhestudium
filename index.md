---
layout: default
permalink: /
---

<script>
  // Spinner visible mientras se decide la redirección
  document.body.insertAdjacentHTML('afterbegin', `
    <div id="spinner"></div>
    <style>
      #spinner {
        border: 4px solid #f3f3f3;
        border-top: 4px solid #333;
        border-radius: 50%;
        width: 24px;
        height: 24px;
        animation: spin 1s linear infinite;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 9999;
      }
      @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    </style>
  `);

  // Redirección basada en el idioma del navegador
  const userLang = navigator.language || navigator.userLanguage;

  switch (true) {
    case userLang.startsWith('es'): // Español
      window.location.href = "/es/";
      break;
    case userLang.startsWith('fr'): // Francés
      window.location.href = "/fr/";
      break;
    case userLang.startsWith('de'): // Alemán
      window.location.href = "/de/";
      break;
    default: // Idioma por defecto: inglés
      window.location.href = "/en/";
  }
</script>

<p>Redirigiendo según el idioma de tu navegador…</p>

<noscript>
  <!-- Meta-refresh para navegadores sin JS -->
  <meta http-equiv="refresh" content="0; URL=/en/" />

  <!-- Opciones manuales para seleccionar el idioma -->
  <p>JavaScript está deshabilitado. Selecciona tu idioma:</p>
  <ul>
    <li><a href="/es/">Español</a></li>
    <li><a href="/en/">English</a></li>
    <li><a href="/fr/">Français</a></li>
    <li><a href="/de/">Deutsch</a></li>
  </ul>
</noscript>
