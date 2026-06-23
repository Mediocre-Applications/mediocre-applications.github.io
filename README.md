# mediocre-applications.github.io

Public web pages for **Mediocre Applications** — the brand landing page and the
privacy policies / support pages for each app. Served by GitHub Pages at the
root of the org:

<https://mediocre-applications.github.io/>

## Structure

```
index.html              brand landing page (lists the apps)
404.html                not-found page
.nojekyll               serve files as-is (no Jekyll build)
hass-todo/
  privacy/index.html    Todo for Home Assistant — privacy policy
```

Each app gets its own top-level folder. Stable URLs to paste into Play Console:

| App | Privacy policy URL |
|---|---|
| Todo for Home Assistant | `https://mediocre-applications.github.io/hass-todo/privacy/` |

## Rules

- **Never rename an app folder or its `privacy/` path** once it's live — the
  store listing points at it and a 404 can get the app flagged.
- Keep this repo **public** (org Pages on the free plan only serve public repos).

## Enabling Pages

Repo → Settings → Pages → Build and deployment → Source: **Deploy from a branch**,
branch `main` / `/ (root)`. The site is live a minute or two after the first push.
