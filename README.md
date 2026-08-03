# WALT Labs public assets

Publicly hosted images for event pages, email, and social. Served via raw.githubusercontent.com.

- `events/` — event banner / hero images
- `headshots/` — team headshots, square 800x800 JPEG

## Headshots

All headshots are 800x800 JPEG, EXIF stripped, sRGB. Filenames are `firstname-lastname.jpg`.

| Name | File | URL |
|---|---|---|
| Gordon Kedslie | `headshots/gordon-kedslie.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/gordon-kedslie.jpg |
| Sean Sherrard | `headshots/sean-sherrard.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/sean-sherrard.jpg |
| Stewart Smith | `headshots/stewart-smith.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/stewart-smith.jpg |
| Ted Everett | `headshots/ted-everett.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/ted-everett.jpg |

### Faster CDN alternative

Any file here is also served by jsDelivr, which is cached at the edge and a better
choice for high-traffic pages. Swap the host and use `@main` in place of `/main`:

```
https://cdn.jsdelivr.net/gh/matthewsherrard-bit/walt-assets@main/headshots/sean-sherrard.jpg
```

Note that jsDelivr caches aggressively — if you replace an image in place, the old
version can persist for up to 7 days. To force a fresh image, commit it under a new
filename rather than overwriting.

## Adding an image

Commit it to the relevant folder on `main` and it is live at the `raw.githubusercontent.com`
URL immediately. Keep filenames lowercase and hyphenated — spaces require percent-encoding
and break in several email clients.
