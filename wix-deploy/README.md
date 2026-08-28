# natalie-lui.com — deploy to Wix Managed Headless

Site: Natalie Lui — Portfolio
Site ID: def11777-060a-4e80-a28a-2eefa78d5732
Domain: https://www.natalie-lui.com

## What's in this folder

The finished site as flat static files. Paths are root-absolute, so every page,
asset and the resume PDF resolve from the domain root.

    index.html            ->  /
    work/index.html       ->  /work
    rhode/index.html      ->  /rhode
    abercrombie/index.html->  /abercrombie
    bumble/index.html     ->  /bumble
    for-the-plot/index.html -> /for-the-plot
    nyc-map.html          ->  /nyc-map.html   (iframe on the home page)
    support.js
    image-slot.js
    _ds/                  Industry design system
    assets/               <-- SEPARATE DOWNLOAD, see below

## Assets are a separate download

`assets/` is not in this zip — the photos and anniversary video made the
archive too large to build. Download the `assets` folder from the second
download card and put it in this folder as `assets/`, alongside `index.html`.
It contains `opt/`, `logos/`, `reel/`, `anniversary.mp4` and
`Natalie_Lui_Resume.pdf` (the file every "Résumé" button opens).

## Steps

1. Node 20.11 or newer:  `node -v`

2. Download and unzip your Wix Headless project:
   https://manage.wix.com/download-headless-business/def11777-060a-4e80-a28a-2eefa78d5732/download.zip

3. Copy everything from this folder (except README.md) into that project's
   `public/` directory.

4. Delete `src/pages/index.astro` in the project — otherwise it serves at `/`
   instead of your `index.html`.

5. Log in and release:

       npx skills add wix/skills
       CI=1 npx wix login
       CI=1 npx wix build
       CI=1 npx wix preview
       CI=1 npx wix release

## Features to switch on

None beyond what's already there — hosting plus the custom domain (connected)
and the Promote SEO app (installed). No Stores, Bookings, Events or CMS; the
site is static. Leave every other Business Solution off.
