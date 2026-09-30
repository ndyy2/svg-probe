# probe2

## V1 no xmlns single line

<svg width="40" height="40" viewBox="0 0 40 40"><circle cx="20" cy="20" r="18" fill="#3b5bdb"/></svg>

## V2 with xmlns single line

<svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40"><circle cx="20" cy="20" r="18" fill="#3b5bdb"/></svg>

## V3 multiline inside div

<div align="center">
<svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40">
  <circle cx="20" cy="20" r="18" fill="#3b5bdb"/>
</svg>
</div>

## V4 text element

<svg xmlns="http://www.w3.org/2000/svg" width="200" height="40" viewBox="0 0 200 40"><text x="4" y="26" font-size="20" font-family="Helvetica" fill="#2b3444">Andyy</text></svg>

## V5 link wrapping svg single line

<a href="https://example.com"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36"><circle cx="18" cy="18" r="16" fill="#0d7a6f"/></svg></a>

## V6 external svg img

<img src="https://img.shields.io/badge/hello-world-blue?style=flat" alt="b"/>

## V7 rounded img style

<img src="https://github.com/ndyy2.png?size=80" width="80" height="80" style="border-radius:50%" alt="a"/>

## V8 filter single line

<svg xmlns="http://www.w3.org/2000/svg" width="120" height="60" viewBox="0 0 120 60"><defs><filter id="f"><feGaussianBlur stdDeviation="4"/></filter></defs><rect x="20" y="10" width="80" height="40" rx="12" fill="#e7ecf3" filter="url(#f)"/></svg>

## V9 multiline filter indented children

<svg xmlns="http://www.w3.org/2000/svg" width="120" height="60" viewBox="0 0 120 60">
  <defs>
    <filter id="g">
      <feOffset in="SourceAlpha" dx="-4" dy="-4" result="o"/>
      <feGaussianBlur in="o" stdDeviation="5" result="b"/>
      <feFlood flood-color="#ffffff" result="c"/>
      <feComposite in="c" in2="b" operator="in"/>
    </filter>
  </defs>
  <rect x="20" y="10" width="80" height="40" rx="12" fill="#e7ecf3" filter="url(#g)"/>
</svg>

## V10 image href

<svg xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80"><image href="https://github.com/ndyy2.png?size=100" x="0" y="0" width="80" height="80"/></svg>

## V11 entity and emoji

<svg xmlns="http://www.w3.org/2000/svg" width="200" height="40" viewBox="0 0 200 40"><text x="4" y="26" font-size="18" fill="#2b3444">A &amp; B &#169; ok</text></svg>

## V12 clipPath + preserveAspectRatio

<svg xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80"><defs><clipPath id="c"><circle cx="40" cy="40" r="36"/></clipPath></defs><image href="https://github.com/ndyy2.png?size=100" width="80" height="80" clip-path="url(#c)" preserveAspectRatio="xMidYMid slice"/></svg>
