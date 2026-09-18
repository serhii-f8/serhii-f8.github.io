# serhii-f8.github.io

Personal site of Serhii Fedorenko, published at <https://serhii-f8.github.io/>.

Plain HTML and CSS, no build step and no dependencies. Every push to `main` deploys the site
automatically through GitHub Actions and GitHub Pages.

## Layout

| Path | Purpose |
| --- | --- |
| `index.html` | The whole site. Content lives here; edit it directly. |
| `assets/site.css` | Styles and design tokens. Colours and type roles are defined at the top. |
| `assets/fonts/` | IBM Plex woff2 faces, vendored so the site needs no third-party requests. SIL OFL, see `LICENSE.txt`. |
| `assets/portrait.jpg` | Portrait used in the hero and for link previews. |
| `cv/serhii-fedorenko-cv.pdf` | The CV. A copy of the one built in `serhii-f8/.github`; replace it after rebuilding there. |
| `404.html` | Served by GitHub Pages for unknown URLs. |
| `.github/workflows/deploy.yml` | Checks local references, then publishes the repository root to GitHub Pages. |

## Editing

1. Edit `index.html` (or `assets/site.css`).
2. Open `index.html` in a browser to check it. Nothing needs to be built.
3. Commit and push to `main`. The **Deploy to GitHub Pages** workflow runs and the site updates
   within a minute or two. Progress is under the repository's *Actions* tab.

The workflow fails, and nothing is published, if the HTML or CSS references a local file that does
not exist. Run it by hand from the *Actions* tab (*Run workflow*) to redeploy without a new commit.

## Keeping content in sync

The content mirrors the profile README and CV in `serhii-f8/.github`. When a result, project or
stack entry changes there, change it here as well, and copy the rebuilt PDF into `cv/`.

Conventions carried over from those documents: British spelling, no employer or client names,
ochre is used only for measured figures, and IBM Plex Mono is used only for figures and dates.
