# get.stillkeep.app

The official download page for **Stillkeep: Journal & Diary** (iPhone), built to rank in Google
and to send visitors to the App Store.

## Go live

1. Create a new GitHub repo (e.g. `stillkeep-get`) and upload everything in this folder.
2. Repo → Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. DNS at your registrar: type **CNAME**, name **get**, value **jhr1986.github.io**.
4. Settings → Pages: confirm the custom domain `get.stillkeep.app`, then tick **Enforce HTTPS**.
5. Google Search Console: add `get.stillkeep.app` (or a Domain property for `stillkeep.app`, which covers every subdomain),
   then use URL Inspection on `https://get.stillkeep.app/` and click Request indexing.

## Link it up (this is what gets it indexed)

- On stillkeep.app, point your main "Get the app" / download buttons to `https://get.stillkeep.app/`.
- Redirect `stillkeep.app/photo-journal-app-iphone.html` to `https://get.stillkeep.app/`. It targets the same
  "download" searches, so keeping both would split them. On GitHub Pages: replace that page with a stub
  containing `<meta http-equiv="refresh" content="0; url=https://get.stillkeep.app/">` and
  `<link rel="canonical" href="https://get.stillkeep.app/">`, and remove it from stillkeep.app's sitemap.xml.
- Add `get.stillkeep.app` to llms.txt and the README on the main site.
- Use `get.stillkeep.app` everywhere you share a download link: social bios, Reddit, email signature, QR codes.

## Keep it accurate

- **App Store campaign link:** in `index.html`, search for `APP_STORE_URL` near the bottom and paste your
  App Store Connect campaign link (App Analytics → Campaigns). Every download button uses it.
- **Ratings:** when your rating or rating count changes, update both the visible text and `aggregateRating`
  in the JSON-LD block in `<head>`. They must match what the App Store shows.
- **Price:** the Premium price ($3.99/month, US) appears in the pricing section and the JSON-LD.
- **New versions:** update the "Version 4, updated October 2026" line, `softwareVersion` and `dateModified`
  only when something on the page actually changes.
- **Reviews:** add new App Store reviews to the "What early users say" section as they come in.

## Privacy

The page sets no cookies, runs no analytics and loads nothing from third-party servers. The only outbound
links are to the App Store, stillkeep.app and the Stillkeep legal pages. Downloads are measured through the
App Store campaign link.
