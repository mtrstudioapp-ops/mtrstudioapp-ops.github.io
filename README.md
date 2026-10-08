# MTR Studio developer site

Generic MTR Studio site — hosts the developer website Google Play and AdMob need,
and lists every game on the account.

| File | Why it exists |
|---|---|
| `app-ads.txt` | AdMob crawls this to verify the app. **Must stay at the site root.** |
| `index.html` | Studio page listing all 7 games (copy a `.game` block + add a `game-*.png` to add one) |
| `privacy-policy.html` | Privacy policy URL for the Play listing |

## Publishing it (GitHub Pages, free)

1. On GitHub, create a **public** repo named exactly:
   `mtrstudioapp-ops.github.io`
   (owner must be `mtrstudioapp-ops` — the name has to match the account.)
2. Upload everything in this folder to the repo root.
3. Repo → **Settings → Pages** → Source: *Deploy from a branch*,
   Branch: `main`, folder `/ (root)` → Save.
4. Wait ~2 minutes, then confirm these open:
   - `https://mtrstudioapp-ops.github.io/app-ads.txt`
   - `https://mtrstudioapp-ops.github.io/`

## Then, in the two consoles

- **Play Console** → *each game* → *Store listing* → Contact details → **Website**:
  `https://mtrstudioapp-ops.github.io`
  (Must be the exact domain that serves app-ads.txt — AdMob matches them.)
- **AdMob** → Apps → *each app* → app-ads.txt → **Crawl**.
  One app-ads.txt covers every app on this AdMob publisher id.
  Google usually takes up to 24 hours, sometimes longer.

app-ads.txt is optional — ads keep serving without it — but some premium
buyers only bid on verified inventory, so it is worth having.
