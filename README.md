<svg width="900" height="220" viewBox="0 0 900 220" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#050b0a"/>
      <stop offset="100%" stop-color="#0a1512"/>
    </linearGradient>

    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <clipPath id="frame">
      <rect x="0" y="0" width="900" height="220" rx="14"/>
    </clipPath>
  </defs>

  <g clip-path="url(#frame)">
    <rect width="900" height="220" fill="url(#bgGrad)"/>

    <!-- scanlines -->
    <g opacity="0.12">
      <rect x="0" y="0" width="900" height="220" fill="url(#bgGrad)"/>
      <g stroke="#00ff9c" stroke-width="1">
        <line x1="0" y1="0" x2="900" y2="0"/>
        <line x1="0" y1="6" x2="900" y2="6"/>
        <line x1="0" y1="12" x2="900" y2="12"/>
        <line x1="0" y1="18" x2="900" y2="18"/>
        <line x1="0" y1="24" x2="900" y2="24"/>
        <line x1="0" y1="30" x2="900" y2="30"/>
        <line x1="0" y1="36" x2="900" y2="36"/>
        <line x1="0" y1="42" x2="900" y2="42"/>
        <line x1="0" y1="48" x2="900" y2="48"/>
        <line x1="0" y1="54" x2="900" y2="54"/>
        <line x1="0" y1="60" x2="900" y2="60"/>
        <line x1="0" y1="66" x2="900" y2="66"/>
        <line x1="0" y1="72" x2="900" y2="72"/>
        <line x1="0" y1="78" x2="900" y2="78"/>
        <line x1="0" y1="84" x2="900" y2="84"/>
        <line x1="0" y1="90" x2="900" y2="90"/>
        <line x1="0" y1="96" x2="900" y2="96"/>
        <line x1="0" y1="102" x2="900" y2="102"/>
        <line x1="0" y1="108" x2="900" y2="108"/>
        <line x1="0" y1="114" x2="900" y2="114"/>
        <line x1="0" y1="120" x2="900" y2="120"/>
        <line x1="0" y1="126" x2="900" y2="126"/>
        <line x1="0" y1="132" x2="900" y2="132"/>
        <line x1="0" y1="138" x2="900" y2="138"/>
        <line x1="0" y1="144" x2="900" y2="144"/>
        <line x1="0" y1="150" x2="900" y2="150"/>
        <line x1="0" y1="156" x2="900" y2="156"/>
        <line x1="0" y1="162" x2="900" y2="162"/>
        <line x1="0" y1="168" x2="900" y2="168"/>
        <line x1="0" y1="174" x2="900" y2="174"/>
        <line x1="0" y1="180" x2="900" y2="180"/>
        <line x1="0" y1="186" x2="900" y2="186"/>
        <line x1="0" y1="192" x2="900" y2="192"/>
        <line x1="0" y1="198" x2="900" y2="198"/>
        <line x1="0" y1="204" x2="900" y2="204"/>
        <line x1="0" y1="210" x2="900" y2="210"/>
        <line x1="0" y1="216" x2="900" y2="216"/>
      </g>
    </g>

    <!-- moving scan beam -->
    <rect x="0" y="-40" width="900" height="40" fill="#00ff9c" opacity="0.08">
      <animate attributeName="y" values="-40;220;-40" dur="4s" repeatCount="indefinite"/>
    </rect>

    <!-- border -->
    <rect x="3" y="3" width="894" height="214" rx="12" fill="none" stroke="#00ff9c" stroke-width="2" opacity="0.55"/>

    <!-- prompt tag -->
    <text x="40" y="50" font-family="Fira Code, Consolas, monospace" font-size="18" fill="#00ff9c" opacity="0.8">root@wolfmod:~$</text>

    <!-- Glitch layers of main text -->
    <g font-family="Fira Code, Consolas, monospace" font-weight="700" font-size="72" text-anchor="middle">

      <!-- red/cyan ghost offsets for chromatic aberration -->
      <text x="452" y="140" fill="#ff003c" opacity="0.55" filter="url(#glow)">
        WOLF MOD
        <animate attributeName="x" values="452;446;456;450;452" dur="2.6s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.55;0.15;0.6;0.2;0.55" dur="1.3s" repeatCount="indefinite"/>
      </text>

      <text x="448" y="140" fill="#00e5ff" opacity="0.55" filter="url(#glow)">
        WOLF MOD
        <animate attributeName="x" values="448;454;444;450;448" dur="2.2s" repeatCount="indefinite"/>
        <animate attributeName="opacity" values="0.5;0.6;0.15;0.55;0.5" dur="1.1s" repeatCount="indefinite"/>
      </text>

      <!-- main crisp text -->
      <text x="450" y="140" fill="#00ff9c" filter="url(#glow)">
        WOLF MOD
        <animate attributeName="opacity" values="1;1;1;0.35;1;1;1;1;0.55;1" dur="2.4s" repeatCount="indefinite"/>
      </text>
    </g>

    <!-- subtitle -->
    <text x="450" y="180" font-family="Fira Code, Consolas, monospace" font-size="16" fill="#7dffce" text-anchor="middle" opacity="0.8">
      &gt; key verification // vip tiers // memory patching_
      <animate attributeName="opacity" values="0.8;0.3;0.8" dur="1.6s" repeatCount="indefinite"/>
    </text>

    <!-- blinking cursor -->
    <rect x="632" y="167" width="10" height="18" fill="#00ff9c">
      <animate attributeName="opacity" values="1;1;0;0" dur="1s" repeatCount="indefinite"/>
    </rect>
  </g>
</svg>
