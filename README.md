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
minimal-launcher/
  index.html            Mediocre Minimal Launcher — app page (screenshots, features)
  icon.png              app icon, used by the app page and the landing card
  screenshots/*.png     phone screenshots shown on the app page
  privacy/index.html    Mediocre Minimal Launcher — privacy policy
neon-halo/
  index.html            NEON HALO — app page (description, support)
  icon.png              app icon, used by the app page and the landing card
  privacy/index.html            NEON HALO — privacy policy (Google Play)
  privacy/app-store/index.html  NEON HALO — privacy policy (App Store)
  delete-data/index.html        NEON HALO — how to delete your data
```

Each app gets its own top-level folder. Stable URLs to paste into Play Console:

| App | Privacy policy URL |
|---|---|
| Todo for Home Assistant | `https://mediocre-applications.github.io/hass-todo/privacy/` |
| Mediocre Minimal Launcher | `https://mediocre-applications.github.io/minimal-launcher/privacy/` |
| NEON HALO (Google Play) | `https://mediocre-applications.github.io/neon-halo/privacy/` |
| NEON HALO (App Store) | `https://mediocre-applications.github.io/neon-halo/privacy/app-store/` |

Play Console also asks for a **Delete data URL** in the Data safety form,
separately from the privacy policy. It has its own rules: it must name the app
or developer as the listing shows them, put the deletion *steps* up front, and
say what is deleted, what is kept, and for how long. A privacy policy that
merely mentions deletion doesn't qualify.

| App | Delete data URL |
|---|---|
| NEON HALO | `https://mediocre-applications.github.io/neon-halo/delete-data/` |

An app that ships on both stores gets **one page per store**, not one shared
page: the two stores name different things for the same feature (Play Games
Services vs. Game Center, Google Play Billing vs. the App Store), so a shared
page would either read wrong on one store or fill up with "Android only"
qualifiers. The pair is edited in step — a feature that changes one changes
both.

## Rules

- **Never rename an app folder or its `privacy/` path** once it's live — the
  store listing points at it and a 404 can get the app flagged.
- Keep this repo **public** (org Pages on the free plan only serve public repos).

## Enabling Pages

Repo → Settings → Pages → Build and deployment → Source: **Deploy from a branch**,
branch `main` / `/ (root)`. The site is live a minute or two after the first push.
