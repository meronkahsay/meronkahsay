# Hi, I’m Meron Kahsay :wave:
Welcome to my GitHub. Below are two animated intro styles. Use the one you like. Both show my highlighted repos and tech stack in a neat, animated scene.
---
> **Repos highlighted**
- `tesfa-frontend`
- `ankole`
- `movie recommendation agent`
> **Tech stack**
Python · Kotlin · React · Next.js · TailwindCSS · SQL
---
# How to use
- The file contains two sections: "Colorful Cartoon" and "Minimal Line-Art".
- Comment out the section you do not want to show by wrapping it in HTML comments:
  `<!--` `...` `-->`
- GitHub will render the inline SVG animations automatically.
---
# Colorful Cartoon Style
<!--
  To hide this whole section, wrap this block in <!-- ... --> in your README.
-->
<div align="center">
<!-- Animated scene: waving, jump to reveal repos and techs, fly to top -->
<svg xmlns="http://www.w3.org/2000/svg" width="880" height="320" viewBox="0 0 880 320" role="img" aria-label="Colorful cartoon animation greeting Meron">
  <style>
    .bg { fill: #f7fbff }
    .girl-body { fill: #ffd8d8 }
    .girl-hair { fill: #6b4f9a }
    .dress { fill: #ff8ba7 }
    .tech { fill: #222; font: 600 13px/1.1 sans-serif }
    .repo { fill: #fff; stroke: #ddd; stroke-width: 1; font: 600 12px/1 sans-serif; }
    .card { rx:10; ry:10 }
    .sparkle { fill: #fff }
  </style>
  <!-- Background -->
  <rect class="bg" x="0" y="0" width="880" height="320"/>
  <!-- Girl group with waving hand -->
  <g id="girl" transform="translate(120,180)">
    <!-- drop shadow -->
    <ellipse cx="0" cy="65" rx="40" ry="10" fill="#000" opacity="0.08"/>
    <!-- body -->
    <g id="body">
      <ellipse class="girl-body" cx="0" cy="20" rx="24" ry="28"/>
      <rect x="-22" y="40" width="44" height="36" rx="8" class="dress"/>
      <!-- head -->
      <circle class="girl-body" cx="0" cy="-8" r="18"/>
      <!-- hair -->
      <path class="girl-hair" d="M-18 -16 C -16 -30, 16 -30, 18 -16 C 8 -10, -8 -10, -18 -16 Z"/>
      <!-- eye -->
      <circle cx="-5" cy="-12" r="2" fill="#222"/>
      <circle cx="4" cy="-12" r="2" fill="#222"/>
      <!-- smile -->
      <path d="M-6 -4 Q 0 0 6 -4" stroke="#222" stroke-width="1.2" fill="none" stroke-linecap="round"/>
    </g>
    <!-- waving arm: right arm that animates -->
    <g id="arm" transform="translate(22,8)">
      <rect x="0" y="-6" width="28" height="10" rx="6" ry="6" fill="#ffd8d8" transform-origin="0 0">
        <animateTransform attributeName="transform" type="rotate" from="0 0 0" to="-25 0 0" dur="0.5s" begin="0s;wave.end+2.5s" id="wave" repeatCount="3"/>
      </rect>
      <!-- hand -->
      <circle cx="30" cy="-1" r="6" fill="#ffd8d8">
        <animateTransform attributeName="transform" type="translate" values="0 0; -6 -6; 0 0" dur="0.5s" begin="wave.begin" repeatCount="3"/>
      </circle>
    </g>
    <!-- name text appears after wave -->
    <text id="name" x="60" y="-24" font-family="sans-serif" font-weight="700" font-size="20" fill="#222" opacity="0">Hi, I'm Meron Kahsay</text>
    <animate xlink:href="#name" attributeName="opacity" from="0" to="1" begin="wave.end" dur="0.6s" fill="freeze"/>
    <!-- small jump animation for whole girl -->
    <animateTransform xlink:href="#girl" attributeName="transform" type="translate" values="120,180; 120,150; 120,180" begin="name.end+0.6s" dur="0.9s" fill="freeze"/>
  </g>
  <!-- Repo cards that pop up while girl jumps -->
  <g id="repos" transform="translate(320,180)" opacity="0">
    <!-- card 1 -->
    <g transform="translate(0,-30)">
      <rect class="repo card" x="0" y="0" width="200" height="36" rx="8" />
      <text x="14" y="23" class="tech">tesfa-frontend</text>
    </g>
    <!-- card 2 -->
    <g transform="translate(0,10)">
      <rect class="repo card" x="0" y="0" width="200" height="36" rx="8" />
      <text x="14" y="23" class="tech">ankole</text>
    </g>
    <!-- card 3 -->
    <g transform="translate(0,50)">
      <rect class="repo card" x="0" y="0" width="200" height="36" rx="8" />
      <text x="14" y="23" class="tech">movie recommendation agent</text>
    </g>
  </g>
  <!-- show repos when jump happens -->
  <animate xlink:href="#repos" attributeName="opacity" from="0" to="1" begin="girl.begin+1.5s" dur="0.4s" fill="freeze"/>
  <!-- Tech stack monochrome badges on the right -->
  <g id="techs" transform="translate(580,160)" opacity="0">
    <!-- helper function: each badge a rounded rect with initials -->
    <g transform="translate(0,-36)">
      <rect x="0" y="0" rx="8" ry="8" width="160" height="28" class="repo"/>
      <text x="12" y="19" class="tech">Py · Kotlin · React</text>
    </g>
    <g transform="translate(0,4)">
      <rect x="0" y="0" rx="8" ry="8" width="160" height="28" class="repo"/>
      <text x="12" y="19" class="tech">Next.js · TailwindCSS · SQL</text>
    </g>
  </g>
  <animate xlink:href="#techs" attributeName="opacity" from="0" to="1" begin="repos.end" dur="0.4s" fill="freeze"/>
  <!-- Girl flies up to top right at the end -->
  <animateTransform xlink:href="#girl" attributeName="transform" type="translate"
    values="120,180; 520,60" begin="repos.end+0.6s" dur="0.9s" fill="freeze"/>
  <animateTransform xlink:href="#girl" attributeName="transform" type="scale"
    values="1;0.95" begin="repos.end+0.6s" dur="0.9s" additive="sum" fill="freeze"/>
  <!-- final sparkle -->
  <g transform="translate(560,28)">
    <polygon class="sparkle" points="0,-6 2,-1 8,0 2,1 0,6 -2,1 -8,0 -2,-1" opacity="0">
      <animate attributeName="opacity" from="0" to="1" begin="repos.end+1.4s" dur="0.3s" fill="freeze"/>
      <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="1.2s" begin="repos.end+1.4s" repeatCount="indefinite"/>
    </polygon>
  </g>
  <!-- accessibility: label -->
  <desc>Animated cartoon girl waves, shows Meron Kahsay name, reveals repos and tech stack, then flies up and sparkles.</desc>
</svg>
</div>
---
# Minimal Line-Art Style
<!--
  To hide this whole section, wrap this block in <!-- ... --> in your README.
-->
<div align="center">
<!-- Simple line-art SVG with the same sequence in minimalist style -->
<svg xmlns="http://www.w3.org/2000/svg" width="880" height="240" viewBox="0 0 880 240" role="img" aria-label="Minimal line art animation greeting Meron">
  <style>
    .bg { fill: #ffffff }
    .line { stroke: #222; stroke-width: 1.6; fill: none; stroke-linecap: round; stroke-linejoin: round }
    .fill { fill: #fff }
    .label { font: 600 13px/1 sans-serif; fill: #222 }
    .card { fill: #fff; stroke: #e6e6e6; rx:8; ry:8 }
  </style>
  <rect class="bg" x="0" y="0" width="880" height="240"/>
  <!-- girl composed with simple lines -->
  <g id="girl2" transform="translate(140,140)">
    <ellipse cx="0" cy="46" rx="36" ry="10" fill="#000" opacity="0.06"/>
    <g transform="translate(0,-36)">
      <circle r="12" class="fill"/>
      <path class="line" d="M-8,-2 Q0 6 8 -2" />
      <path class="line" d="M-12,-10 Q0 -18 12 -10" />
    </g>
    <!-- body line -->
    <path class="line" d="M0,-24 v24 a12 12 0 0 0 12 12 h-24 a12 12 0 0 0 12 -12 z"/>
    <!-- arm waving -->
    <g id="arm2" transform="translate(18,-6)">
      <path class="line" d="M0 0 q18 -6 32 0" stroke-linecap="round"/>
      <circle cx="34" cy="-2" r="4" fill="#fff" stroke="#222" stroke-width="1.2">
        <animateTransform attributeName="transform" type="translate" values="0 0; -6 -6; 0 0" dur="0.5s" begin="0s;armwave.end+2.5s" id="armwave" repeatCount="3"/>
      </circle>
    </g>
    <!-- name appears -->
    <text id="name2" x="60" y="-24" class="label" opacity="0">Hi, I am Meron Kahsay</text>
    <animate xlink:href="#name2" attributeName="opacity" from="0" to="1" begin="armwave.end" dur="0.5s" fill="freeze"/>
    <!-- little jump -->
    <animateTransform attributeName="transform" type="translate" values="140,140; 140,120; 140,140" begin="name2.end+0.4s" dur="0.7s" fill="freeze"/>
  </g>
  <!-- repos as simple outline cards -->
  <g id="repos2" transform="translate(360,120)" opacity="0">
    <rect class="card" x="0" y="-34" width="220" height="32"></rect>
    <text class="label" x="12" y="-12">tesfa-frontend</text>
    <rect class="card" x="0" y="6" width="220" height="32"></rect>
    <text class="label" x="12" y="28">ankole</text>
    <rect class="card" x="0" y="46" width="220" height="32"></rect>
    <text class="label" x="12" y="68">movie recommendation agent</text>
  </g>
  <animate xlink:href="#repos2" attributeName="opacity" from="0" to="1" begin="girl2.begin+1.4s" dur="0.4s" fill="freeze"/>
  <!-- tech badges minimal monochrome -->
  <g transform="translate(620,100)" opacity="0" id="techs2">
    <rect x="0" y="-30" width="200" height="28" rx="8" class="card"/>
    <text x="12" y="-12" class="label">Python · Kotlin · React</text>
    <rect x="0" y="6" width="200" height="28" rx="8" class="card"/>
    <text x="12" y="24" class="label">Next.js · TailwindCSS · SQL</text>
  </g>
  <animate xlink:href="#techs2" attributeName="opacity" from="0" to="1" begin="repos2.end" dur="0.4s" fill="freeze"/>
  <!-- final lift -->
  <animateTransform xlink:href="#girl2" attributeName="transform" type="translate" values="140,140; 520,40" begin="repos2.end+0.6s" dur="0.9s" fill="freeze"/>
  <desc>Minimal line art animation: girl waves then jumps, repos and tech stack appear, finishes with a lift.</desc>
</svg>
</div>
