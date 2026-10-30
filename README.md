# Nexzare Website

Static website (plain HTML) — koi build step nahi chahiye, seedha Vercel par chal jati hai.
Har page apne folder mein `index.html` hai, is liye har URL direct open aur refresh par bhi chalta hai.

## Files

```
nexzare-website/
├── index.html                 ← /            Home (products first)
├── products/index.html        ← /products
├── gemnix/
│   ├── index.html             ← /gemnix          (product page)
│   ├── privacy/index.html     ← /gemnix/privacy  (Chrome Web Store)
│   ├── terms/index.html       ← /gemnix/terms    (Gumroad + Chrome Web Store)
│   ├── support/index.html     ← /gemnix/support  (Chrome Web Store "Support URL")
│   ├── icon-128.png
│   └── screenshot-1.png … screenshot-5.png
├── foxi-flow/
│   ├── index.html             ← /foxi-flow
│   ├── privacy/index.html     ← /foxi-flow/privacy
│   ├── terms/index.html       ← /foxi-flow/terms
│   ├── support/index.html     ← /foxi-flow/support
│   ├── icon-128.png
│   └── screenshot-1.png … screenshot-5.png
├── services/index.html        ← /services     (purana service content)
├── 404.html                   ← galat link par
├── css/site.css               ← poori design (sab pages ek hi file use karte hain)
├── sitemap.xml
├── robots.txt
├── vercel.json                ← clean URLs + purane links ke redirects
├── README.md
└── assets/
    ├── logo-white.png, logo-icon.png, favicon.png
    └── step-discover.webp, step-design.webp, step-build.webp, step-launch.webp
```

## Placeholders (baad mein replace karein)

Poore folder mein search & replace karein (VS Code: Ctrl+Shift+H):

| Token | Kya dalna hai | Kahan hai |
|---|---|---|
| `[CHROME WEB STORE LINK]` | Gemnix ka Chrome Web Store URL | index.html, products/index.html, gemnix/index.html, gemnix/support/index.html |
| `[FOXI CHROME WEB STORE LINK]` | Foxi Flow ka Chrome Web Store URL | index.html, products/index.html, foxi-flow/index.html, foxi-flow/support/index.html |

Payments: Gumroad (Gemnix: https://nexzare.gumroad.com/l/Gemnix · Foxi Flow: https://nexzare.gumroad.com/l/FoxiFlow · library: https://app.gumroad.com/library).

## GitHub par upload

1. Apni `nexzare-website` repository kholein.
2. Purani files `gemnix.html`, `privacy-bulk-image-generator.html` aur `terms-bulk-image-generator.html` delete karein (unke purane links `vercel.json` khud naye pages par bhej deta hai).
3. **Add file → Upload files** → is folder ke **andar** ki saari cheezein drag & drop karein (folders samet). `index.html` repository ke root mein hi rahe.
4. **Commit changes** dabayein — Vercel khud dobara deploy kar dega.

## Vercel settings

Framework Preset: **Other**. Build Command aur Output Directory khali.

## Baad mein changes

Kisi bhi page ki `index.html` GitHub par edit karke commit karein. Design badalna ho to sirf `css/site.css`.
