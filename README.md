# Portfolio-1

Static personal website for **Viet Anh** — liquid glass UI, snow animation, music player, and PWA install support.

**Stack:** HTML · CSS · vanilla JS · Service Worker · Web App Manifest

## Features

- Glass-morphism layout (purple / pink anime aesthetic)
- Themes: default, Sakura, Cyber
- Snow particles with performance toggle
- Multi-track background music (play / pause / next / volume)
- Settings panel (effects, theme, reduced motion)
- Social links (Instagram, Facebook, Discord, X, Spotify, SoundCloud, GitHub)
- **PWA**: `manifest.json` + `service-worker.js` + `offline.html`
- Optional Nginx sample config and `.htaccess`

## Structure

```
Portfolio-1/
├── index.html
├── offline.html
├── manifest.json
├── service-worker.js
├── nginx.conf
├── package.json          # serve / minify helpers
└── assets/
    ├── css/              # style.css, snow.css
    ├── js/               # main.js, snow.js, music.js
    ├── images/
    └── music/
```

## Run locally

```bash
git clone https://github.com/duckzangryy/Portfolio-1.git
cd Portfolio-1

# zero-deps
python3 -m http.server 3000

# or
npm install -g serve
npm start
```

Open `http://localhost:3000`.

## Scripts (optional)

| Command | Purpose |
|---------|---------|
| `npm start` / `npm run dev` | Serve root with `serve` |
| `npm run build` | Minify CSS/JS/HTML into `dist/` |
| `npm run preview` | Serve `dist/` |
| `npm run test:performance` | Lighthouse against local server |

## Customize

1. **Identity & links** — edit copy and socials in `index.html`
2. **Colors / themes** — CSS variables in `assets/css/style.css`
3. **Music list** — `assets/js/music.js`
4. **Snow density** — `maxFlakes` in `assets/js/snow.js`
5. **PWA icons / name** — `manifest.json`

## Deploy

Upload the folder (or `dist/` after build) to any static host:

- Nginx / Apache (see `nginx.conf`, `.htaccess`)
- GitHub Pages / Cloudflare Pages / Netlify
- Use **HTTPS** so the service worker can register

## Browser support

Chrome 80+ · Firefox 75+ · Safari 13+ · Edge 80+ · modern mobile browsers

## Author

Viet Anh · [duckzangryy](https://github.com/duckzangryy)

## License

MIT
