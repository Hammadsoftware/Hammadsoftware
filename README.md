<svg viewBox="0 0 900 340" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0B1120"/>
      <stop offset="100%" stop-color="#0F2027"/>
    </linearGradient>
    <linearGradient id="lineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00C4FF" stop-opacity="0.2"/>
      <stop offset="50%" stop-color="#00C4FF" stop-opacity="1"/>
      <stop offset="100%" stop-color="#7CFFCB" stop-opacity="1"/>
    </linearGradient>
    <radialGradient id="glow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00C4FF" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#00C4FF" stop-opacity="0"/>
    </radialGradient>
    <filter id="softBlur" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="4"/>
    </filter>
  </defs>

  <rect x="0" y="0" width="900" height="340" rx="18" fill="url(#bgGrad)"/>

  <!-- Terminal window (left) -->
  <g transform="translate(30,30)">
    <rect x="0" y="0" width="330" height="280" rx="12" fill="#0D1117" stroke="#1F2937" stroke-width="1.5"/>
    <rect x="0" y="0" width="330" height="34" rx="12" fill="#161B22"/>
    <circle cx="20" cy="17" r="6" fill="#FF5F56"/>
    <circle cx="42" cy="17" r="6" fill="#FFBD2E"/>
    <circle cx="64" cy="17" r="6" fill="#27C93F"/>
    <text x="165" y="22" fill="#8B949E" font-family="Consolas, monospace" font-size="12" text-anchor="middle">server.js</text>

    <g font-family="Consolas, monospace" font-size="13">
      <text x="18" y="65"><tspan fill="#FF7B72">const</tspan><tspan fill="#C9D1D9"> app = </tspan><tspan fill="#79C0FF">require</tspan><tspan fill="#C9D1D9">(</tspan><tspan fill="#A5D6FF">'express'</tspan><tspan fill="#C9D1D9">)()</tspan></text>
      <text x="18" y="90"><tspan fill="#FF7B72">const</tspan><tspan fill="#C9D1D9"> db = </tspan><tspan fill="#79C0FF">connect</tspan><tspan fill="#C9D1D9">(URI)</tspan></text>
      <text x="18" y="115"><tspan fill="#8B949E">// power up the API</tspan></text>
      <text x="18" y="140"><tspan fill="#FF7B72">async function</tspan><tspan fill="#D2A8FF"> boot</tspan><tspan fill="#C9D1D9">() {</tspan></text>
      <text x="34" y="165"><tspan fill="#79C0FF">await</tspan><tspan fill="#C9D1D9"> db.</tspan><tspan fill="#D2A8FF">ready</tspan><tspan fill="#C9D1D9">()</tspan></text>
      <text x="34" y="190"><tspan fill="#C9D1D9">app.</tspan><tspan fill="#D2A8FF">listen</tspan><tspan fill="#C9D1D9">(</tspan><tspan fill="#79C0FF">PORT</tspan><tspan fill="#C9D1D9">)</tspan></text>
      <text x="18" y="215"><tspan fill="#C9D1D9">}</tspan></text>
      <text x="18" y="245"><tspan fill="#8B949E">status: </tspan><tspan fill="#7CFFCB">"online"</tspan></text>
    </g>

    <!-- blinking cursor -->
    <rect x="18" y="252" width="8" height="14" fill="#00C4FF">
      <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- Connection lines carrying "power" from code to server -->
  <g stroke="url(#lineGrad)" stroke-width="2.5" fill="none">
    <path id="wire1" d="M360,90 C 480,90 480,120 620,120"/>
    <path id="wire2" d="M360,170 C 480,170 480,170 620,170"/>
    <path id="wire3" d="M360,250 C 480,250 480,220 620,220"/>
  </g>

  <!-- animated energy pulses traveling along the wires -->
  <circle r="5" fill="#7CFFCB" filter="url(#softBlur)">
    <animateMotion dur="1.8s" repeatCount="indefinite" path="M360,90 C 480,90 480,120 620,120"/>
  </circle>
  <circle r="5" fill="#00C4FF" filter="url(#softBlur)">
    <animateMotion dur="1.6s" begin="0.4s" repeatCount="indefinite" path="M360,170 C 480,170 480,170 620,170"/>
  </circle>
  <circle r="5" fill="#7CFFCB" filter="url(#softBlur)">
    <animateMotion dur="2s" begin="0.8s" repeatCount="indefinite" path="M360,250 C 480,250 480,220 620,220"/>
  </circle>

  <!-- Power glow at the junction where lines meet the server -->
  <circle cx="620" cy="170" r="34" fill="url(#glow)">
    <animate attributeName="r" values="28;38;28" dur="2s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.5;0.9;0.5" dur="2s" repeatCount="indefinite"/>
  </circle>

  <!-- Server rack (right) -->
  <g transform="translate(620,45)">
    <rect x="0" y="0" width="250" height="250" rx="14" fill="#111827" stroke="#00C4FF" stroke-width="1.5"/>
    <!-- rack units -->
    <g>
      <rect x="18" y="20" width="214" height="42" rx="6" fill="#1B2433" stroke="#233045"/>
      <rect x="18" y="74" width="214" height="42" rx="6" fill="#1B2433" stroke="#233045"/>
      <rect x="18" y="128" width="214" height="42" rx="6" fill="#1B2433" stroke="#233045"/>
      <rect x="18" y="182" width="214" height="42" rx="6" fill="#1B2433" stroke="#233045"/>
    </g>

    <!-- blinking LEDs on each unit -->
    <circle cx="36" cy="41" r="4.5" fill="#7CFFCB">
      <animate attributeName="opacity" values="1;0.2;1" dur="1.1s" repeatCount="indefinite"/>
    </circle>
    <circle cx="36" cy="95" r="4.5" fill="#00C4FF">
      <animate attributeName="opacity" values="0.3;1;0.3" dur="1.4s" repeatCount="indefinite"/>
    </circle>
    <circle cx="36" cy="149" r="4.5" fill="#7CFFCB">
      <animate attributeName="opacity" values="1;0.3;1" dur="0.9s" repeatCount="indefinite"/>
    </circle>
    <circle cx="36" cy="203" r="4.5" fill="#00C4FF">
      <animate attributeName="opacity" values="0.4;1;0.4" dur="1.2s" repeatCount="indefinite"/>
    </circle>

    <!-- vent lines on each unit -->
    <g stroke="#3A4B63" stroke-width="2">
      <line x1="70" y1="30" x2="220" y2="30"/><line x1="70" y1="41" x2="220" y2="41"/><line x1="70" y1="52" x2="220" y2="52"/>
      <line x1="70" y1="84" x2="220" y2="84"/><line x1="70" y1="95" x2="220" y2="95"/><line x1="70" y1="106" x2="220" y2="106"/>
      <line x1="70" y1="138" x2="220" y2="138"/><line x1="70" y1="149" x2="220" y2="149"/><line x1="70" y1="160" x2="220" y2="160"/>
      <line x1="70" y1="192" x2="220" y2="192"/><line x1="70" y1="203" x2="220" y2="203"/><line x1="70" y1="214" x2="220" y2="214"/>
    </g>

    <text x="125" y="242" fill="#7CFFCB" font-family="Consolas, monospace" font-size="13" text-anchor="middle" font-weight="bold">SERVER: ONLINE</text>
  </g>

  <!-- power bolt icon at the junction -->
  <g transform="translate(608,152)">
    <path d="M14 0 L4 20 L12 20 L8 36 L26 14 L16 14 Z" fill="#FFD166" stroke="#FFB703" stroke-width="1">
      <animateTransform attributeName="transform" type="scale" values="1;1.15;1" dur="1s" repeatCount="indefinite" additive="sum"/>
    </path>
  </g>
</svg>
