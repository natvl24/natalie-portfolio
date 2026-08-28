# natalie-portfolio — GitHub Pages

Live: https://natvl24.github.io/natalie-portfolio/

## Structure

    index.html              /
    work/index.html         /work/
    rhode/index.html        /rhode/
    abercrombie/index.html  /abercrombie/
    bumble/index.html       /bumble/
    for-the-plot/index.html /for-the-plot/
    nyc-map.html            venue map, iframed by index.html
    support.js
    image-slot.js
    _ds/                    Industry design system
    assets/                 images, videos, resume PDF (add separately)
    .nojekyll               stops Jekyll skipping files

All paths are RELATIVE, so the site works both at the /natalie-portfolio/
subpath and later at a domain root — no rebuild needed if you move it.

## Assets

`assets/` is not in the repo yet. Merge the three `assets-part*` downloads into
one folder named `assets/` next to `index.html`:

    assets/
      opt/  logos/  reel/
      anniversary.mp4
      Natalie_Lui_Resume.pdf   <- what every "Résumé" button opens
      designlab.png  ftp-logo-x.png  rowan-owl.png  tiktok.png

## Video files and GitHub's size limit

`assets/anniversary.mp4` and `assets/reel/reel-1..4.mp4` are the only large
files. GitHub warns over 50 MB and rejects any single file over 100 MB. If a
push is refused, either use Git LFS or host those five elsewhere and point the
`<video src>` at the hosted URLs.

## Publishing

Settings -> Pages -> Source: "Deploy from a branch", branch `main`, folder
`/ (root)`. Pushes to `main` republish automatically.
