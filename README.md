# ThousandEyes - Splunk Integrations

Splunk.conf 2026 (OBS1217)

Workshop docs: https://ajimenez1503.github.io/splunk.conf-2026-OBS1217/

# TODO
- Add ThousandEyes alerts into Splunk (using Splunk App)

# Publish to GitHub Pages

One-time setup in the repository settings:

1. Open [Settings → Pages](https://github.com/ajimenez1503/splunk.conf-2026-OBS1217/settings/pages)
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**
3. Select branch **gh-pages** and folder **/ (root)**
4. Save — the site will be available at https://ajimenez1503.github.io/splunk.conf-2026-OBS1217/

Pushes to `main` automatically rebuild and deploy the site via GitHub Actions.

# Run it locally
```
python3 -m venv .venv 
source .venv/bin/activate
python3 -m pip install -r requirements.txt
python3 -m mkdocs serve
```
