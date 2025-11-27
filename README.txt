Position Sizing Calculator — APK-ready package

This package contains a PWA (Progressive Web App) ready to be hosted and converted into an Android APK/TWA.

Files included:
- index.html
- manifest.json
- service-worker.js
- icon-192.png
- icon-512.png
- icon-maskable.png
- bubblewrap-config.json

Quick steps to produce an APK:

1) Host the contents on GitHub Pages / Netlify / Vercel.
   - For GitHub Pages: create a repository, push these files to the `gh-pages` or `main` branch and enable GitHub Pages.
   - For Netlify / Vercel: drag-and-drop the folder or connect the repo.

2) Ensure your site is served over HTTPS (GitHub Pages / Netlify / Vercel provide HTTPS).

3) Go to https://www.pwabuilder.com or use Bubblewrap:
   - PWABuilder: enter your live site URL, follow prompts to build an Android package (APK or App Bundle).
   - Bubblewrap (command-line): use the included bubblewrap-config.json as reference.
     Example (after installing bubblewrap):
       bubblewrap init --manifest=https://yourdomain/manifest.json
       bubblewrap build

4) Signing & publishing:
   - PWABuilder can produce unsigned or signed packages. To publish on Google Play you will need to sign and prepare store listing.

Notes:
- In bubblewrap-config.json replace "host" with your hosted domain (example: myusername.github.io or yoursite.com).
- I included simple service-worker caching; adjust caching strategies for production as needed.