# Bossaert Insights — Hugo + Decap CMS (Netlify)

Free starter blog for insights.tydbyt.com using Hugo and Decap CMS.

## Deploy

1. Create a new GitHub repo and push this folder.
2. On Netlify, **New site from Git**, pick the repo.
3. Build command: `hugo` · Publish directory: `public`.
   Set environment var `HUGO_VERSION=0.128.0` if not prefilled.
4. Assign your domain in **Site → Domain management** (add `insights.tydbyt.com`). Point DNS to Netlify per docs.

## Enable the `/admin` editor (Decap CMS)

**Option A — Netlify Identity + Git Gateway**  
- In Netlify **Identity**, click **Enable Identity**. In **Identity → Settings → Registration**, pick **Invite only**.  
- In **Site settings → Identity → Services**, enable **Git Gateway**.  
- Invite yourself (your email). Accept the invite and log in at `https://<yoursite>/admin/`.

**Option B — GitHub backend**  
- Change `backend` in `static/admin/config.yml` to use `github` and follow Decap docs.

## Content model

- Posts live in `content/posts/` (Markdown). Pages live in `content/<page>/_index.md`.
- Add images to `static/uploads/` and reference as `/uploads/filename.png`.

## Local dev

- Install Hugo 0.128+  
- Run `hugo server` and open http://localhost:1313
