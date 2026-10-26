# Spoor Sky Simulator

A sales-engineering sandbox for Spoor's two monitoring products:

- **AAM** (Aerial Activity Monitoring): what is flying here.
- **TIM** (Turbine Interaction Monitoring): what happened at this rotor.

The whole tool is one self-contained HTML file. Three.js, both fonts and every
asset are inlined, so it needs no network, no build step and no server. Open
`index.html` in a browser and it runs.

## Publishing it on GitHub Pages

1. Create a repository and upload the contents of this folder to the root of
   the default branch (`index.html`, `.nojekyll` and this README).
2. In the repository, go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, pick your default branch
   and the `/ (root)` folder, and save.
4. Wait for the Pages build to finish. The site appears at
   `https://<your-account>.github.io/<repository-name>/`.

`.nojekyll` is there on purpose: it stops GitHub running the page through
Jekyll, which would otherwise be free to mangle the inlined content.

## A note on who can see it

A GitHub Pages site published from a public repository is public to anyone with
the link, whether or not the link is advertised. A private repository can
publish Pages only on GitHub Enterprise Cloud, and that is the only
configuration in which Pages itself restricts access to members of your
organisation. If the content needs to stay inside Spoor and you are not on
Enterprise Cloud, host it somewhere with real access control rather than
relying on an unguessable URL.

## Keeping it current

The file is generated from the sources in the project, not edited by hand.
Rebuild with `python3 build.py` and copy the new `dist/spoor-sky-simulator.html`
over `index.html`.
