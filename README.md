<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Frank Junior Benítez Mosquera</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=UnifrakturCook:wght@700&family=Oswald:wght@500;600&family=Inter:wght@400;500&display=swap" rel="stylesheet">
<style>
  body { margin: 0; background: #060605; }

  /* ===== HEADER ===== */
  .hero {
    --gothic: 'UnifrakturCook', 'Old English Text MT', 'Blackadder ITC', Georgia, serif;
    --cond: 'Oswald', 'Arial Narrow', 'Segoe UI', sans-serif;
    --sans: 'Inter', 'Segoe UI', Arial, sans-serif;
    position: relative;
    overflow: hidden;
    min-height: 460px;
    padding: 70px 20px 50px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    background:
      radial-gradient(ellipse 50% 55% at 50% 48%, rgba(255,255,255,.10), transparent 70%),
      linear-gradient(rgba(255,255,255,.045) 1px, transparent 1px) 0 0 / 40px 40px,
      linear-gradient(90deg, rgba(255,255,255,.045) 1px, transparent 1px) 0 0 / 40px 40px,
      #060605;
    color: #8a8a8f;
  }

  /* Cuadrados flotantes */
  .hero .sq {
    position: absolute;
    left: var(--x); top: var(--y);
    width: var(--s); height: var(--s);
    background: rgba(255,255,255,.16);
    transform: rotate(var(--r));
    animation: float var(--d) ease-in-out infinite, blink var(--d) ease-in-out infinite;
    animation-delay: var(--delay, 0s);
    pointer-events: none;
  }
  @keyframes float {
    0%, 100% { translate: 0 0; }
    50%      { translate: 0 -22px; }
  }
  @keyframes blink {
    0%, 100% { opacity: .25; }
    50%      { opacity: 1; }
  }

  /* Línea superior */
  .hero .tag {
    position: relative;
    z-index: 1;
    display: flex;
    align-items: center;
    gap: 16px;
    font: 500 12px var(--sans);
    letter-spacing: .28em;
    text-transform: uppercase;
    animation: rise .9s ease both;
  }
  .hero .tag::before, .hero .tag::after {
    content: "";
    width: 60px; height: 1px;
    background: linear-gradient(90deg, transparent, #8a8a8f);
  }
  .hero .tag::after { transform: scaleX(-1); }

  /* Medallón */
  .hero .badge {
    position: relative;
    z-index: 1;
    width: 100px; height: 100px;
    margin: 34px 0 0;
    border-radius: 50%;
    display: grid; place-items: center;
    background: rgba(255,255,255,.04);
    border: 1.5px solid rgba(255,255,255,.18);
    font: 700 56px/1 var(--gothic);
    color: #e4e4e6;
    animation: rise .9s .1s ease both, pulse 4s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { border-color: rgba(255,255,255,.12); box-shadow: 0 0 0 0 rgba(255,255,255,0); }
    50%      { border-color: rgba(255,255,255,.32); box-shadow: 0 0 40px 4px rgba(255,255,255,.07); }
  }

  /* Nombre */
  .hero h1 {
    position: relative;
    z-index: 1;
    margin: 10px 0 0;
    font: 700 clamp(84px, 15vw, 150px)/1.05 var(--gothic);
    background: linear-gradient(180deg, #fff 0%, #c9c9cc 55%, #6f6f74 100%);
    -webkit-background-clip: text; background-clip: text;
    -webkit-text-fill-color: transparent; color: transparent;
    animation: rise .9s .2s ease both;
  }

  .hero h2 {
    position: relative;
    z-index: 1;
    margin: 0;
    font: 600 clamp(18px, 3.2vw, 32px) var(--cond);
    letter-spacing: .32em;
    text-transform: uppercase;
    background: linear-gradient(180deg, #d8d8da, #8a8a8f);
    -webkit-background-clip: text; background-clip: text;
    -webkit-text-fill-color: transparent; color: transparent;
    animation: rise .9s .3s ease both;
  }

  .hero .role {
    position: relative;
    z-index: 1;
    margin: 28px 0 0;
    font: 400 clamp(11px, 1.6vw, 15px) var(--sans);
    letter-spacing: .24em;
    text-transform: uppercase;
    color: #77777c;
    animation: rise .9s .4s ease both;
  }
  .hero .role i { font-style: normal; margin: 0 .8em; }

  @keyframes rise {
    from { opacity: 0; transform: translateY(14px); }
    to   { opacity: 1; transform: none; }
  }

  @media (prefers-reduced-motion: reduce) {
    .hero *, .hero *::before, .hero *::after { animation: none !important; }
  }
</style>
</head>
<body>

<header class="hero">
  <span class="sq" style="--x:9%;  --y:14%; --s:18px; --r:20deg; --d:9s"></span>
  <span class="sq" style="--x:38%; --y:7%;  --s:14px; --r:35deg; --d:8s;  --delay:-2s"></span>
  <span class="sq" style="--x:76%; --y:16%; --s:22px; --r:15deg; --d:10s; --delay:-4s"></span>
  <span class="sq" style="--x:88%; --y:50%; --s:16px; --r:40deg; --d:9s;  --delay:-1s"></span>
  <span class="sq" style="--x:25%; --y:50%; --s:24px; --r:25deg; --d:11s; --delay:-5s"></span>
  <span class="sq" style="--x:13%; --y:80%; --s:20px; --r:10deg; --d:10s; --delay:-3s"></span>
  <span class="sq" style="--x:92%; --y:80%; --s:16px; --r:30deg; --d:8s;  --delay:-6s"></span>
  <span class="sq" style="--x:58%; --y:90%; --s:26px; --r:45deg; --d:12s; --delay:-2s"></span>
  <span class="sq" style="--x:5%;  --y:48%; --s:12px; --r:28deg; --d:7s;  --delay:-4s"></span>

  <div class="tag">Medellín, Colombia &nbsp;·&nbsp; Disponible ahora</div>
  <div class="badge">F</div>
  <h1>Frank</h1>
  <h2>Junior Benítez Mosquera</h2>
  <p class="role">Análisis &amp; Desarrollo de Software<i>·</i>Creative Technologist</p>
</header>

</body>
</html>
<br>

<div align="center">

![](assets/divider.svg)

</div>

<br>

## `〔 01 〕` &nbsp; Sobre mí

```
✦  Profesional proactivo en análisis y desarrollo de software con enfoque
   en soluciones innovadoras. Especializado en prevención de violencia y
   protección de menores, con experiencia en liderazgo de equipos,
   comunicación efectiva y gestión de proyectos.

   Comprometido con la excelencia organizacional y el aprendizaje continuo.
   Si tienes un proyecto ambicioso, hablemos.
```

<br>

<table>
<tr>
<td width="50%" valign="top">

**`Nombre`** &nbsp;&nbsp; Frank Junior Benítez Mosquera  
**`Ubicación`** &nbsp;&nbsp; Medellín, Antioquia 🌆  
**`Teléfono`** &nbsp;&nbsp; 305 308 8049  
**`Email`** &nbsp;&nbsp; frankjunior5400@gmail.com  
**`GitHub`** &nbsp;&nbsp; [github.com/JUNI00R89](https://github.com/JUNI00R89)  
**`Disponibilidad`** &nbsp;&nbsp; `🟢 Inmediata`

</td>
<td width="50%" valign="top">

```
  Formación en curso    →  Tecnólogo SENA
  Proyectos clave       →  4
  Herramientas          →  10+
  Áreas                 →  Dev · Diseño · Gestión
```

</td>
</tr>
</table>

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 02 〕` &nbsp; Stack & Herramientas

<div align="center">
<br>

<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><g clip-path="url(#a)"><path d="M196 0H60C26.863 0 0 26.863 0 60v136c0 33.137 26.863 60 60 60h136c33.137 0 60-26.863 60-60V60C256 26.863 229.137 0 196 0z" fill="#242938"/><path d="M40 65.663 110.968 55.998 111 124.453l-70.934.404L40 65.663zm70.935 66.677.055 68.515-70.934-9.753-.004-59.221 70.883.459zm8.602-77.607L213.636 41v82.582l-94.099.748V54.733zm94.121 78.251-.022 82.211-94.099-13.281-.131-69.083 94.252.153z" fill="#00ADEF"/></g><defs><clipPath id="a"><rect width="256" height="256" fill="#fff"/></clipPath></defs></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="256" height="256" rx="60" fill="#242938"/><path d="M227.088 57.602 133.256 225.389c-1.938 3.465-6.915 3.485-8.881.038L28.682 57.618c-2.142-3.757.07-8.308 4.328-7.547l93.932 16.79c.599.107 1.213.106 1.812-.003l91.968-16.763c4.243-.773 7.47 3.742 5.366 7.507z" fill="url(#b)"/><path d="m172.687 28.049-69.438 13.606a2.667 2.667 0 0 0-2.055 2.352l-4.272 72.141c-.1 1.699 1.46 3.018 3.118 2.635l19.333-4.461c1.809-.417 3.443 1.176 3.072 2.995l-5.744 28.126c-.387 1.893 1.391 3.511 3.239 2.95l11.941-3.628c1.851-.562 3.63.861 3.238 2.956l-9.128 44.179c-.571 2.764 3.105 4.271 4.638 1.901l1.024-1.582 56.582-112.92c.948-1.89-.686-4.046-2.763-3.645l-19.899 3.841c-1.87.36-3.461-1.381-2.934-3.21l12.989-45.026c.528-1.832-1.069-3.575-2.941-3.21z" fill="url(#c)"/><defs><linearGradient id="b" x1="26.346" y1="44.075" x2="143.127" y2="202.673" gradientUnits="userSpaceOnUse"><stop stop-color="#41D1FF"/><stop offset="1" stop-color="#BD34FE"/></linearGradient><linearGradient id="c" x1="122.551" y1="31.743" x2="143.676" y2="176.66" gradientUnits="userSpaceOnUse"><stop stop-color="#FFEA83"/><stop offset=".083" stop-color="#FFDD35"/><stop offset="1" stop-color="#FFA800"/></linearGradient></defs></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="256" height="256" fill="#242938" rx="60"/><path fill="#00D8FF" d="M128.001 146.951a18.656 18.656 0 1 0 0-37.312 18.656 18.656 0 0 0 0 37.312z"/><path fill-rule="evenodd" stroke="#00D8FF" stroke-width="8.911" d="M128.002 90.363c25.048 0 48.317 3.594 65.862 9.634C215.003 107.275 228 118.306 228 128.295c0 10.409-13.774 22.128-36.475 29.649-17.162 5.686-39.746 8.654-63.523 8.654-24.378 0-47.463-2.786-64.818-8.717C41.225 150.376 28 138.506 28 128.295c0-9.908 12.41-20.854 33.252-28.12 17.61-6.14 41.453-9.812 66.746-9.812h.004z" clip-rule="evenodd"/><path fill-rule="evenodd" stroke="#00D8FF" stroke-width="8.911" d="M94.981 109.438c12.514-21.698 27.251-40.06 41.249-52.241 16.864-14.676 32.914-20.424 41.566-15.434 9.017 5.2 12.288 23.987 7.463 47.408-3.645 17.708-12.359 38.754-24.238 59.352-12.179 21.118-26.124 39.724-39.931 51.792-17.471 15.272-34.362 20.799-43.207 15.698-8.583-4.946-11.865-21.167-7.748-42.852 3.479-18.323 12.21-40.812 24.842-62.723h.004z" clip-rule="evenodd"/><path fill-rule="evenodd" stroke="#00D8FF" stroke-width="8.911" d="M95.012 147.578c-12.549-21.674-21.093-43.616-24.659-61.826-4.293-21.941-1.258-38.716 7.387-43.72 9.008-5.215 26.052.834 43.934 16.712 13.52 12.004 27.403 30.061 39.316 50.639 12.214 21.098 21.368 42.473 24.929 60.461 4.506 22.764.859 40.157-7.978 45.272-8.574 4.964-24.265-.291-40.996-14.689C108.809 188.263 107.685 169.468 95.012 147.578z" clip-rule="evenodd"/></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="256" height="256" fill="#00005B" rx="60"/><path fill="#99F" d="M54 182.68V72.813c0-.747.32-1.173 1.067-1.173 1.813 0 3.52 0 5.973-.107 2.56-.106 5.227-.106 8.107-.213 2.88-.107 5.973-.107 9.28-.213C81.733 71 84.933 71 88.133 71c8.747 0 16 1.067 21.974 3.307 5.333 1.813 10.24 4.8 14.293 8.746 3.413 3.414 6.08 7.574 7.787 12.16 1.6 4.48 2.453 9.067 2.453 13.867 0 9.173-2.133 16.747-6.4 22.72-4.267 5.973-10.24 10.453-17.173 13.013-7.254 2.667-15.254 3.627-24 3.627-2.56 0-4.267 0-5.333-.107-1.067-.106-2.56-.106-4.587-.106V182.467c.107.746-.427 1.386-1.173 1.493h-.427H55.28c-.853 0-1.28-.427-1.28-1.387V182.68zm23.253-90.347V128.173c1.494.107 2.88.214 4.16.214H87.067c4.16 0 8.32-.64 12.266-1.92 3.414-.96 6.4-2.987 8.747-5.654 2.24-2.666 3.307-6.293 3.307-10.986.106-3.307-.747-6.614-2.454-9.494-1.813-2.773-4.373-4.906-7.466-6.08-3.947-1.6-8.214-2.24-12.587-2.133-2.773 0-5.226 0-7.253.107-2.133-.107-3.627 0-4.373.106v.107zM150 98.627h18.667c1.067 0 1.92.746 2.24 1.706.32.854.533 1.707.64 2.667.213 1.067.427 2.24.533 3.307.107 1.173.214 2.453.214 3.84 3.2-3.734 7.04-6.827 11.413-9.174 4.907-2.773 10.56-4.16 16.213-4.16.747-.106 1.387.427 1.494 1.174v.426V119.213c0 .854-.534 1.174-1.707 1.174-3.84-.107-7.787.213-11.52 1.066-3.093.64-6.08 1.6-8.96 2.88-2.027.96-3.947 2.24-5.44 3.947V182.68c0 1.067-.427 1.493-1.387 1.493H151.387c-.853.107-1.6-.426-1.707-1.28v-.426V123.373c0-2.56 0-5.226-.106-8-.107-2.773-.107-5.546-.214-8.32 0-2.453-.213-4.8-.426-7.253-.107-.533.213-1.066.746-1.173.107 0 .32 0 .32.107v-.107z"/></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="256" height="256" fill="#001E36" rx="60"/><path fill="#31A8FF" d="M57.6 178.04V68.28c0-.747.32-1.173 1.067-1.173 1.813 0 3.52 0 5.973-.107 2.56-.107 5.227-.107 8.107-.213 2.88-.107 5.973-.107 9.28-.214C85.333 66.467 88.533 66.467 91.733 66.467c8.747 0 16 1.066 21.974 3.306 5.333 1.814 10.24 4.8 14.293 8.747 3.413 3.413 6.08 7.573 7.787 12.16 1.6 4.48 2.453 9.066 2.453 13.866 0 9.174-2.133 16.747-6.4 22.72-4.267 5.974-10.24 10.454-17.173 13.014-7.254 2.666-15.254 3.626-24 3.626-2.56 0-4.267 0-5.333-.106-1.067-.107-2.56-.107-4.587-.107V177.933c.107.747-.426 1.387-1.173 1.494h-.427H58.88c-.853 0-1.28-.427-1.28-1.387V178.04zm23.253-90.347V123.533c1.493.107 2.88.214 4.16.214H90.667c4.16 0 8.32-.64 12.266-1.92 3.414-.96 6.4-2.987 8.747-5.654 2.24-2.666 3.307-6.293 3.307-10.986.106-3.307-.747-6.614-2.454-9.494-1.813-2.773-4.373-4.906-7.466-6.08-3.947-1.6-8.214-2.24-12.587-2.133-2.773 0-5.226 0-7.253.107-2.133-.107-3.627 0-4.373.106zM204.8 117.027c-3.2-1.707-6.613-2.88-10.24-3.627-3.947-.853-7.893-1.387-11.947-1.387-2.133-.106-4.373.214-6.4.747-1.386.32-2.56 1.067-3.306 2.133-.534.854-.854 1.92-.854 2.88 0 .96.427 1.92 1.067 2.774.96 1.173 2.24 2.133 3.627 2.88 2.453 1.28 5.013 2.453 7.573 3.52 5.76 1.92 11.307 4.586 16.427 7.786 3.52 2.24 6.4 5.227 8.426 8.854 1.707 3.413 2.56 7.146 2.454 10.986.106 5.014-1.387 10.027-4.16 14.187-2.987 4.267-7.147 7.573-11.947 9.493-5.227 2.24-11.627 3.414-19.307 3.414-4.906 0-9.706-.427-14.506-1.387-3.734-.64-7.467-1.813-10.88-3.413-.747-.427-1.28-1.174-1.174-2.027V156.28c0-.32.107-.747.427-.96.32-.213.64-.107.96.107 4.16 2.453 8.533 4.16 13.227 5.226 4.053 1.067 8.32 1.6 12.586 1.6 4.054 0 6.934-.533 8.854-1.493 1.706-.747 2.88-2.56 2.88-4.48 0-1.493-.854-2.88-2.56-4.267-1.707-1.386-5.227-2.986-10.454-5.013-5.44-1.92-10.453-4.48-15.146-7.68-3.307-2.347-6.08-5.44-8.107-9.067-1.707-3.413-2.56-7.146-2.453-10.88 0-4.586 1.28-8.96 3.626-12.906 2.667-4.267 6.614-7.68 11.2-9.814 5.014-2.56 11.307-3.733 18.88-3.733 4.374 0 8.854.32 13.227.96 3.2.427 6.293 1.28 9.173 2.453.427.107.854.534 1.067.96.107.427.213.854.213 1.28V115.96c0 .427-.213.853-.533 1.067-.96.213-1.493.213-1.92 0z"/></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><g clip-path="url(#d)"><path d="M196 0H60C26.863 0 0 26.863 0 60v136c0 33.137 26.863 60 60 60h136c33.137 0 60-26.863 60-60V60C256 26.863 229.137 0 196 0z" fill="#242938"/><path d="M23 88h210v68.571H128V168H81.333v-11.429H23V88zm11.667 57.143H58v-34.286h11.667v34.286H81.333V99.429H34.667v45.714zM93 99.429V156.571h23.333V145.143H139.667V99.429H93zm23.333 34.285H128v-22.857h-11.667v22.857zM151.333 99.429v45.714H174.667v-34.286H186.333v34.286H198v-34.286h11.667v34.286H221.333V99.429H151.333z" fill="#CB3837"/><path d="M34.667 145.143H58v-34.286h11.667v34.286H81.333V99.429H34.667v45.714z" fill="#fff"/><path d="M93 99.429V156.571h23.333V145.143H139.667V99.429H93zm35 34.285h-11.667v-22.857H128v22.857z" fill="#fff"/><path d="M151.333 99.429v45.714H174.667v-34.286H186.333v34.286H198v-34.286h11.667v34.286H221.333V99.429H151.333z" fill="#fff"/></g><defs><clipPath id="d"><rect width="256" height="256" fill="#fff"/></clipPath></defs></svg>
&nbsp;&nbsp;
<svg width="48" height="48" viewBox="0 0 256 256" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="256" height="256" rx="60" fill="#F0DB4F"/><path d="M67.312 213.932 86.903 202.076c3.779 6.701 7.217 12.371 15.464 12.371 7.905 0 12.889-3.092 12.889-15.12V117.529h24.058v82.138c0 24.917-14.606 36.259-35.916 36.259-19.245 0-30.416-9.967-36.087-21.994M152.381 211.354l19.588-11.341c5.157 8.421 11.859 14.607 23.715 14.607 9.969 0 16.325-4.984 16.325-11.858 0-8.248-6.53-11.17-17.528-15.98l-6.013-2.579c-17.357-7.388-28.871-16.668-28.871-36.258 0-18.044 13.748-31.792 35.229-31.792 15.294 0 26.292 5.328 34.196 19.247l-18.731 12.029c-4.125-7.389-8.591-10.31-15.465-10.31-7.046 0-11.514 4.468-11.514 10.31 0 7.217 4.468 10.139 14.778 14.608l6.014 2.577c20.449 8.765 31.963 17.699 31.963 37.804 0 21.654-17.012 33.51-39.867 33.51-22.339 0-36.774-10.654-43.819-24.574" fill="#323330"/></svg>

<br>
<br>

</div>

<table>
<tr>
<td width="33%" valign="top">

**Desarrollo & Análisis**
```
· Análisis de Sistemas      ██████ Avanzado
· Desarrollo de Software    ██████ Avanzado
· Metodologías Ágiles       ████░░ Intermedio
· JavaScript / React        ████░░ En curso
```

</td>
<td width="33%" valign="top">

**Diseño Digital**
```
· Adobe Illustrator         ██████ Avanzado
· Adobe Photoshop           ██████ Avanzado
· After Effects             ████░░ Intermedio
```

</td>
<td width="33%" valign="top">

**Gestión & Ofimática**
```
· Microsoft Excel           ██████ Avanzado
· Microsoft Word            ██████ Avanzado
· Gestión de Proyectos      ██████ Avanzado
```

</td>
</tr>
</table>

<br>

> **Habilidades blandas** &nbsp;·&nbsp; `Comunicación` `Empatía` `Liderazgo` `Proactividad` `Trabajo en Equipo` `Resolución de Problemas`

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 03 〕` &nbsp; Experiencia

<br>

**`Proyecto Institucional`** &nbsp; — &nbsp; **Coordinador de Proyecto** &nbsp;·&nbsp; *Prevención de Violencia contra Menores, Medellín*

> Participé en un proyecto institucional enfocado en la **prevención de violencia contra menores de edad**.
> Implementé un enfoque innovador con valor compartido, realicé compras eficientes de materiales educativos
> y coordiné la entrega de recursos. Desarrollé y proporcioné capacitaciones sobre alternativas educativas al castigo físico.

`Gestión de Proyectos` &nbsp; `Liderazgo` &nbsp; `Capacitaciones` &nbsp; `Valor Compartido`

---

**`Experiencia Variada`** &nbsp; — &nbsp; **Coordinador Operativo** &nbsp;·&nbsp; *Diversas Organizaciones, Medellín*

> Experiencia en coordinación de productos, descarga de mercancía, organización de inventario y compra eficiente.
> Coordinación de entregas y gestión de equipo de trabajo en entornos dinámicos y de alta demanda operativa.

`Inventario` &nbsp; `Logística` &nbsp; `Gestión de Equipo` &nbsp; `Coordinación`

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 04 〕` &nbsp; Proyectos

<br>

**`I`** &nbsp; **Cero** &nbsp;·&nbsp; *Aplicación de gestión de gastos personales*

> Permite registrar movimientos, visualizar el balance en tiempo real y llevar un control claro de las finanzas del día a día.

`Finanzas Personales` &nbsp; `App`

---

**`II`** &nbsp; **GmailCleaner** &nbsp;·&nbsp; *Herramienta para limpieza masiva de correos*

> Automatiza la limpieza de bandejas de entrada saturadas en Gmail, ahorrando tiempo y espacio de almacenamiento.

`Automatización` &nbsp; `Gmail API`

---

**`III`** &nbsp; **Prevención de Violencia** &nbsp;·&nbsp; *Proyecto institucional*

> Proyecto para la protección de menores con enfoque de valor compartido. Coordinación de recursos, capacitaciones y materiales educativos.

`Impacto Social` &nbsp; `Gestión`

---

**`IV`** &nbsp; **Integración de Contenidos Digitales** &nbsp;·&nbsp; *Producción creativa*

> Formación técnica en integración de contenidos digitales, aplicando herramientas Adobe para producción creativa y comunicación visual.

`Diseño` &nbsp; `Adobe`

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 05 〕` &nbsp; Formación

<br>

| # | Período | Título | Institución |
|---|---|---|---|
| `I` | `En curso — Dic 2025` | Tecnólogo en Análisis y Desarrollo de Software | SENA · Medellín |
| `II` | `Diciembre 2024` | Bachiller Técnico en Integración de Contenidos Digitales | Inst. Educativa Alcaldía de Medellín |

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 06 〕` &nbsp; GitHub Stats

<div align="center">
<br>

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=JUNI00R89&show_icons=true&theme=github_dark&hide_border=true&bg_color=060605&title_color=c8c5be&text_color=555550&icon_color=888880)
&nbsp;&nbsp;
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=JUNI00R89&layout=compact&theme=github_dark&hide_border=true&bg_color=060605&title_color=c8c5be&text_color=555550)

<br>
</div>

<br>
<div align="center">

![](assets/divider.svg)

</div>
<br>

## `〔 07 〕` &nbsp; Contacto

<div align="center">
<br>

¿Tienes un proyecto? Hablemos.

<br>

[![Email](https://img.shields.io/badge/Email-frankjunior5400%40gmail.com-c8c5be?style=flat-square&logo=gmail&logoColor=white&labelColor=111110)](mailto:frankjunior5400@gmail.com)
&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-JUNI00R89-c8c5be?style=flat-square&logo=github&logoColor=white&labelColor=111110)](https://github.com/JUNI00R89)
&nbsp;
[![Portfolio](https://img.shields.io/badge/Portfolio-ver%20CV-c8c5be?style=flat-square&logo=vercel&logoColor=white&labelColor=111110)](https://juni00r89.github.io/CV-FRANK/CV.html)
&nbsp;
[![Teléfono](https://img.shields.io/badge/Tel-305%20308%208049-c8c5be?style=flat-square&logo=whatsapp&logoColor=white&labelColor=111110)](https://wa.me/573053088049)

<br><br>

![](assets/divider.svg)

<br>

```
✦  Frank Junior Benítez Mosquera  ·  Medellín, Antioquia  ·  2025  ✦
```

</div>
