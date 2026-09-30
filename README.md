# svg sanitize probe

## A: filter primitives (feGaussianBlur chain)

<svg xmlns="http://www.w3.org/2000/svg" width="220" height="120" viewBox="0 0 220 120">
  <defs>
    <filter id="neu" x="-40%" y="-40%" width="180%" height="180%" color-interpolation-filters="sRGB">
      <feOffset in="SourceAlpha" dx="-6" dy="-6" result="off1"/>
      <feGaussianBlur in="off1" stdDeviation="7" result="b1"/>
      <feFlood flood-color="#ffffff" flood-opacity="1" result="c1"/>
      <feComposite in="c1" in2="b1" operator="in" result="s1"/>
      <feOffset in="SourceAlpha" dx="6" dy="6" result="off2"/>
      <feGaussianBlur in="off2" stdDeviation="7" result="b2"/>
      <feFlood flood-color="#9aa6bd" flood-opacity="1" result="c2"/>
      <feComposite in="c2" in2="b2" operator="in" result="s2"/>
      <feMerge>
        <feMergeNode in="s2"/>
        <feMergeNode in="s1"/>
      </feMerge>
    </filter>
  </defs>
  <rect x="30" y="25" width="160" height="70" rx="18" fill="#e7ecf3" filter="url(#neu)"/>
</svg>

## B: feDropShadow

<svg xmlns="http://www.w3.org/2000/svg" width="220" height="120" viewBox="0 0 220 120">
  <rect x="30" y="25" width="160" height="70" rx="18" fill="#e7ecf3" filter="url(#ds)"/>
  <filter id="ds"><feDropShadow dx="5" dy="5" stdDeviation="5" flood-color="#999"/></filter>
</svg>

## C: image href + clipPath

<svg xmlns="http://www.w3.org/2000/svg" width="120" height="120" viewBox="0 0 120 120">
  <defs><clipPath id="c"><circle cx="60" cy="60" r="50"/></clipPath></defs>
  <circle cx="60" cy="60" r="50" fill="#e7ecf3"/>
  <image href="https://github.com/ndyy2.png?size=160" x="10" y="10" width="100" height="100" clip-path="url(#c)" preserveAspectRatio="xMidYMid slice"/>
</svg>

## D: anchor wrapping svg

<a href="https://example.com" target="_blank">
  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 48 48"><circle cx="24" cy="24" r="20" fill="#3b5bdb"/></svg>
</a>

## E: style + quoted font-family + emoji + named entity

<svg xmlns="http://www.w3.org/2000/svg" width="400" height="60" viewBox="0 0 400 60">
  <style>.t{fill:#2b3444}</style>
  <text x="10" y="35" font-family="'Segoe UI',Helvetica,Arial,sans-serif" font-size="20" fill="#2b3444">Hi&nbsp;👋 &amp; ok</text>
  <text class="t" x="300" y="35" font-size="16">styled</text>
</svg>

## F: use/linearGradient/tspan

<svg xmlns="http://www.w3.org/2000/svg" width="300" height="60" viewBox="0 0 300 60">
  <defs>
    <linearGradient id="g"><stop offset="0" stop-color="#3b5bdb"/><stop offset="1" stop-color="#0d7a6f"/></linearGradient>
    <circle id="dot" cx="20" cy="30" r="12" fill="url(#g)"/>
  </defs>
  <use href="#dot"/>
  <text x="50" y="36" font-size="18" fill="#2b3444">A<tspan fill="#3b5bdb">B</tspan></text>
</svg>

## G: html img round

<img src="https://github.com/ndyy2.png?size=80" width="80" height="80" style="border-radius:50%" alt="a"/>
