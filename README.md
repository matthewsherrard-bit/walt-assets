# WALT Labs public assets

Publicly hosted images for event pages, email, and social. Served via raw.githubusercontent.com.

- `events/` — event banner / hero images
- `headshots/` — team and guest headshots, square JPEG (800x800 standard)

## Headshots

Square JPEG, EXIF stripped, sRGB. Filenames are `firstname-lastname.jpg`. The standard
is 800x800; anything smaller is noted below because its source had no more real detail
and upscaling would only have added bytes.

### WALT Labs team

| Name | File | URL |
|---|---|---|
| Gordon Kedslie | `headshots/gordon-kedslie.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/gordon-kedslie.jpg |
| Morgan Atkins | `headshots/morgan-atkins.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/morgan-atkins.jpg |
| Sean Sherrard | `headshots/sean-sherrard.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/sean-sherrard.jpg |
| Stewart Smith | `headshots/stewart-smith.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/stewart-smith.jpg |
| Ted Everett | `headshots/ted-everett.jpg` | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/ted-everett.jpg |

### External speakers and partners

Not WALT Labs staff — do not present these as team members.

| Name | Role | File | URL |
|---|---|---|---|
| Poornima Balaraju | Customer Engineer, Google | `headshots/poornima-balaraju.jpg` (200x200) | https://raw.githubusercontent.com/matthewsherrard-bit/walt-assets/main/headshots/poornima-balaraju.jpg |

### Faster CDN alternative

Any file here is also served by jsDelivr, which is cached at the edge and a better
choice for high-traffic pages. Swap the host and use `@main` in place of `/main`:

```
https://cdn.jsdelivr.net/gh/matthewsherrard-bit/walt-assets@main/headshots/sean-sherrard.jpg
```

jsDelivr caches aggressively, so replacing an image in place can keep serving the old
one. You do not need a new filename to fix that — purge the path instead, which
evicts it from both CDN providers within seconds:

```
curl https://purge.jsdelivr.net/gh/matthewsherrard-bit/walt-assets@main/headshots/<file>.jpg
```

Afterwards, confirm the swap took by comparing checksums rather than trusting a 200:

```
curl -s <raw-url> | shasum -a 256
```

## Adding an image

Commit it to the relevant folder on `main` and it is live at the `raw.githubusercontent.com`
URL immediately. Keep filenames lowercase and hyphenated — spaces require percent-encoding
and break in several email clients.
