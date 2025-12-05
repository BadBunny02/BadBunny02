<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 250" width="100%" height="250" role="img" aria-labelledby="title desc">
  <title id="title">Anupam — GitHub Banner</title>
  <desc id="desc">Animated banner: glowing gradient, floating particles and subtle text wave.</desc>

  <defs>
    <linearGradient id="bgGradient" x1="0" x2="1" y1="0" y2="1">
      <stop offset="0%" stop-color="#0f1724"/>
      <stop offset="50%" stop-color="#07102b">
        <animate attributeName="stop-color" dur="8s" values="#07102b;#10243a;#07102b" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#021026"/>
    </linearGradient>

    <linearGradient id="light" x1="0" x2="1">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0"/>
      <stop offset="50%" stop-color="#ffffff" stop-opacity="0.06"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    </linearGradient>

    <linearGradient id="textGradient" x1="0" x2="1">
      <stop offset="0%" stop-color="#7dd3fc"/>
      <stop offset="50%" stop-color="#60a5fa"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>

    <filter id="softShadow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="6" result="blur"/>
      <feOffset dx="0" dy="6" result="offset"/>
      <feMerge><feMergeNode in="offset"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>

    <g id="particle">
      <circle cx="0" cy="0" r="2.6" fill="#9fbff6" opacity="0.9"/>
    </g>

    <mask id="sweepMask">
      <rect x="0" y="0" width="100%" height="100%" fill="white"/>
      <rect x="-240" y="0" width="260" height="100%" fill="black">
        <animate attributeName="x" from="-240" to="1200" dur="5s" repeatCount="indefinite"/>
      </rect>
    </mask>
  </defs>

  <!-- background -->
  <rect x="0" y="0" width="100%" height="100%" fill="url(#bgGradient)"/>

  <!-- moving light -->
  <rect x="-200" y="-200" width="1400" height="650" fill="url(#light)" transform="rotate(-18 500 125)">
    <animate attributeName="x" from="-400" to="400" dur="12s" repeatCount="indefinite"/>
  </rect>

  <!-- particles -->
  <g aria-hidden="true">
    <use href="#particle" x="80" y="30" opacity="0.9">
      <animateTransform attributeName="transform" type="translate" from="0 0" to="0 110" dur="9s" repeatCount="indefinite"/>
    </use>
    <use href="#particle" x="200" y="-10" opacity="0.7">
      <animateTransform attributeName="transform" type="translate" from="0 0" to="0 150" dur="13s" repeatCount="indefinite"/>
    </use>
    <use href="#particle" x="320" y="10" opacity="0.85">
      <animateTransform attributeName="transform" type="translate" from="0 0" to="0 120" dur="10s" repeatCount="indefinite"/>
    </use>
    <use href="#particle" x="560" y="-5" opacity="0.6">
      <animateTransform attributeName="transform" type="translate" from="0 0" to="0 140" dur="11s" repeatCount="indefinite"/>
    </use>
  </g>

  <!-- avatar circle -->
  <g transform="translate(60,48)" filter="url(#softShadow)">
    <circle cx="60" cy="60" r="60" fill="#07182b" stroke="#18324b" stroke-width="2"/>
    <text x="60" y="76" text-anchor="middle" font-family="Inter, system-ui" font-weight="700" font-size="46" fill="white">A</text>
  </g>

  <!-- text block (hard-coded — no JS) -->
  <g transform="translate(160,72)">
    <text x="0" y="0" font-family="Inter, system-ui" font-weight="800" font-size="46" fill="url(#textGradient)" paint-order="stroke fill" stroke="#071428" stroke-width="0.6">Anupam</text>
    <text x="0" y="44" font-family="Inter, system-ui" font-weight="600" font-size="18" fill="#9fb0d9">C++ • Python • Linux • Machine Learning</text>
    <text x="0" y="82" font-family="Inter, system-ui" font-weight="500" font-size="14" fill="#9aa4c0">Building tools, systems & learning by breaking things.</text>
    <!-- subtle sweep using mask to add shine -->
    <rect x="-8" y="-36" width="420" height="70" fill="white" opacity="0.06" mask="url(#sweepMask)"/>
  </g>

  <!-- code block at right -->
  <g transform="translate(600,36)">
    <rect x="0" y="0" width="320" height="178" rx="12" ry="12" fill="#031226" stroke="#0b2540"/>
    <rect x="18" y="18" width="250" height="12" rx="6" fill="#071a2f"/>
    <rect x="18" y="40" width="220" height="10" rx="5" fill="#071a2f"/>
    <rect x="18" y="60" width="190" height="10" rx="5" fill="#071a2f"/>
    <rect x="18" y="82" width="240" height="10" rx="5" fill="#071a2f"/>
    <rect x="22" y="108" width="8" height="14" fill="url(#textGradient)">
      <animate attributeName="y" values="108;104;108" dur="1.2s" repeatCount="indefinite"/>
    </rect>
  </g>
</svg>
