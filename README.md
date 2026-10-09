# Nexzare Website

Single-page static website — koi build step nahi chahiye, seedha Vercel par chal jati hai.

## Files

```
nexzare-website/
├── index.html        ← poori website
├── vercel.json       ← Vercel settings (images ki fast caching)
├── README.md
└── assets/
    ├── logo-white.png
    ├── logo-icon.png
    ├── favicon.png
    ├── step-discover.webp
    ├── step-design.webp
    ├── step-build.webp
    └── step-launch.webp
```

## GitHub par upload

1. github.com par login karein → **New repository** → naam `nexzare-website` → **Create repository**.
2. "uploading an existing file" link par click karein.
3. Is folder ke **andar** ki saari cheezein (index.html, vercel.json, README.md aur `assets` folder) drag & drop karein.
   Folder khud nahi, uske andar ki files — `index.html` repository ke root mein honi chahiye.
4. **Commit changes** dabayein.

## Vercel par deploy

1. vercel.com par GitHub se login karein.
2. **Add New → Project** → apni `nexzare-website` repository **Import** karein.
3. Framework Preset: **Other**. Build Command aur Output Directory khali chhor dein.
4. **Deploy** dabayein — 1 minute mein site live.

## Apna domain lagana

Vercel project → **Settings → Domains** → `nexzare.com` add karein, phir jo DNS records Vercel bataye wo apne domain provider mein laga dein.

## Baad mein changes

GitHub par `index.html` edit karke commit karein — Vercel khud dobara deploy kar dega.
