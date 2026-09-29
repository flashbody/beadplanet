# Bead Planet — Marketing & Legal Site

Static site for the Bead Planet (豆趣星球) iOS app: landing page, support, privacy policy, and terms of service. English (primary market: US / Europe).

## Files

| File | Purpose | Public URL (once deployed) |
|---|---|---|
| `index.html` | Landing / marketing page | `https://flashbody.github.io/beadplanet/` |
| `support.html` | Support & FAQ (App Store **Support URL**) | `https://flashbody.github.io/beadplanet/support.html` |
| `privacy.html` | Privacy Policy (App Store **Privacy Policy URL**) | `https://flashbody.github.io/beadplanet/privacy.html` |
| `terms.html` | Terms of Service (EULA) | `https://flashbody.github.io/beadplanet/terms.html` |
| `style.css` | Shared styles | — |
| `.nojekyll` | Disable Jekyll so files publish as-is | — |

The legal text mirrors the in-app English documents at `docs/legal/PRIVACY_POLICY_en.md` and `docs/legal/TERMS_OF_SERVICE_en.md`. Keep them in sync when either changes.

## Deploy to GitHub Pages

Publishing under `flashbody.github.io/beadplanet/` requires a repo named **`beadplanet`**.

### Option A — new dedicated repo (recommended)

```bash
cd /Users/a39/Documents/AIProject/DIYPinduo/site

# Create the repo on GitHub first (name: beadplanet), then:
git init
git add .
git commit -m "Add Bead Planet marketing & legal site"
git branch -M main
git remote add origin https://github.com/flashbody/beadplanet.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save.**

After a minute the site is live at `https://flashbody.github.io/beadplanet/`.

### Verify (avoid the Guideline 1.5 404 pitfall)

```bash
curl -I https://flashbody.github.io/beadplanet/
curl -I https://flashbody.github.io/beadplanet/support.html
curl -I https://flashbody.github.io/beadplanet/privacy.html
curl -I https://flashbody.github.io/beadplanet/terms.html
```

All four must return `HTTP/2 200` before you paste the URLs into App Store Connect.

## App Store Connect field mapping

| ASC field | Value |
|---|---|
| Support URL | `https://flashbody.github.io/beadplanet/support.html` |
| Marketing URL (optional) | `https://flashbody.github.io/beadplanet/` |
| Privacy Policy URL | `https://flashbody.github.io/beadplanet/privacy.html` |

Also replace the placeholder URLs in the app's Settings screen (TC-07) with the Privacy Policy and Terms of Service links above.
