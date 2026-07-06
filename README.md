# ls37-smiley-app

Static data + asset CDN for the Smiley Face Live Wallpaper app, served for free via **jsDelivr**
(migrated off the expiring `cdn.leansoft-ai.com`).

## Layout

```
ls37-smiley-wallpaper/
  ls37_updated4.json         â† catalog the app fetches (data_url)
  content/                   â† 353 wallpapers (gif / webp / jpeg)
  trending/                  â† 20 trending wallpapers
zip-lock-screen/
  wallpaper/                 â† 230 wallpapers
```

## URLs (jsDelivr)

- Catalog JSON:
  `https://cdn.jsdelivr.net/gh/atlat1studio/ls37-smiley-app@main/ls37-smiley-wallpaper/ls37_updated4.json`
- Any asset:
  `https://cdn.jsdelivr.net/gh/atlat1studio/ls37-smiley-app@main/<path>`

## Adding new wallpapers later

1. Drop the new file into the right folder (e.g. `ls37-smiley-wallpaper/content/my-new.gif`).
2. Add an entry pointing to its jsDelivr URL inside `ls37_updated4.json`.
3. `git add -A && git commit -m "add wallpaper" && git push`
4. New files show up on jsDelivr immediately. To refresh the **edited JSON** instantly
   (instead of waiting up to ~12h for the branch cache), hit the purge URL once:
   ```
   https://purge.jsdelivr.net/gh/atlat1studio/ls37-smiley-app@main/ls37-smiley-wallpaper/ls37_updated4.json
   ```

Keep files < 50 MB each (jsDelivr limit) and the repo < ~1 GB.
