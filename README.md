# Sahib Gill — Portfolio (Hugo + PaperMod)

A cybersecurity portfolio built with [Hugo](https://gohugo.io) and the
[PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, deployed
free via GitHub Pages.

## Run locally
Requires **Hugo Extended ≥ 0.146** (the bundled theme needs it).

```bash
hugo server        # → http://localhost:1313
```

## Edit content
- **Homepage / bio / buttons** → `hugo.toml` (`[params.profileMode]`)
- **About page** → `content/about.md`
- **Projects** → `content/projects/*.md` (one file per project)
- **Add a project** → `hugo new projects/my-new-project.md`, set `draft: false`
- **Résumé** → drop your PDF at `static/resume.pdf` (the homepage button links to it)
- **Social links / menu** → `hugo.toml`

## Deploy (GitHub Pages)
1. Create a **public** repo named exactly `SahibGill386.github.io`.
2. Push this folder to it (`main` branch).
3. Repo → **Settings → Pages → Source → GitHub Actions**.
4. The included workflow (`.github/workflows/hugo.yaml`) builds and publishes
   automatically on every push. Live at `https://sahibgill386.github.io`.

The PaperMod theme is vendored under `themes/PaperMod` (no submodule needed) —
it just works when you push.
