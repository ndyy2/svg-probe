# probe3

## R1 relative svg

<img src="./assets/card-light.svg" width="440" alt="rel" />

## R2 absolute raw svg

<img src="https://raw.githubusercontent.com/ndyy2/svg-probe/master/assets/card-light.svg" width="440" alt="raw" />

## R3 picture dark

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/card-dark.svg">
  <img src="./assets/card-light.svg" width="440" alt="pic" />
</picture>

## R4 data uri

<img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAiIGhlaWdodD0iNDAiPjxyZWN0IHdpZHRoPSIxMDAiIGhlaWdodD0iNDAiIGZpbGw9IiNmZjAiLz48dGV4dCB4PSI2IiB5PSIyNiIgZmlsbD0iIzAwMCI+ZGF0YTwvdGV4dD48L3N2Zz4=" width="100" alt="datauri" />

## R5 social link with svg img

<a href="https://example.com"><img src="./assets/card-light.svg" width="40" height="40" alt="social" /></a>
