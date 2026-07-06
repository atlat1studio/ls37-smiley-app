# ls37-smiley-app

Static data + asset CDN for the Smiley Face Live Wallpaper app, served for free via jsDelivr.

## Layout

```
ls37-smiley-wallpaper/
  ls37_updated4.json         - catalog the app fetches (data_url)
  content/                   - 353 wallpapers (gif / webp / jpeg)
  trending/                  - 20 trending wallpapers
zip-lock-screen/
  wallpaper/                 - 230 wallpapers
```

## URLs (jsDelivr)

- Catalog JSON:
  `https://cdn.jsdelivr.net/gh/atlat1studio/ls37-smiley-app@v3/ls37-smiley-wallpaper/ls37_updated4.json`
- Any asset:
  `https://cdn.jsdelivr.net/gh/atlat1studio/ls37-smiley-app@v3/<path>`

## Adding new wallpapers later

1. Drop the new file into the right folder, for example `ls37-smiley-wallpaper/content/my-new.gif`.
2. Add an entry pointing to its jsDelivr URL inside `ls37_updated4.json`.
3. Commit and push the change.
4. For updates, create a new tag such as `v2` and update the app/JSON URLs to that tag.

Keep files under 50 MB each for jsDelivr.
