# BPL Registered Players - Web Viewer

An ultra-fast, immersive PDF viewer built with **Astro** for hosting on **Cloudflare Pages**.
Designed for a smooth, distraction-free viewing experience with **CrazyGames-style full screen HUD** and **expanding quick search**.

---

## 🌟 Key Features

1. **Distraction-Free PDF Viewer**:
   - Displays all 137 BPL Registered Player cards at full resolution.
   - High-DPI canvas rendering (crisp on Retina / mobile displays).
   - Centered sports-stadium dark UI theme.

2. **CrazyGames-Style Fullscreen**:
   - Native browser fullscreen toggle via button or keyboard shortcut (`F`).
   - Floating badge on fullscreen: *"Press ESC to exit fullscreen"*.
   - **Auto-hiding HUD**: Navigation controls and floating widgets automatically fade out after 2.6 seconds of inactivity and instantly reappear when you move the mouse or touch the screen.

3. **Expanding Corner Search ("search button boro hobe")**:
   - Floating circular search button at top-right corner.
   - When clicked, it smoothly expands into an interactive search bar.
   - Type any page number (1 to 137) or SL number (e.g. `25`, `025`, `SL 025`) and press Enter to jump immediately.
   - Quick jump chips for `SL 001`, `SL 010`, `SL 025`, `SL 050`, `SL 075`, `SL 100`, `SL 137`.
   - Click outside or press `ESC` to collapse back.

4. **Navigation & Controls**:
   - Left / Right subtle navigation chevrons on screen edges.
   - Bottom dock:
     - `[ < ]` Previous Player
     - Quick Page input: `Page [ X ] of 137`
     - `[ > ]` Next Player
     - Zoom In (`+`), Zoom Out (`-`), Fit Screen (`⊡`)
     - Download original PDF button
     - CrazyGames Fullscreen toggle button
   - Keyboard navigation:
     - `←` / `PageUp`: Previous page
     - `→` / `PageDown` / `Space`: Next page
     - `Home` / `End`: First / Last page
     - `F`: Toggle Fullscreen
     - `S` or `/`: Open Search
     - `Esc`: Close Search / Exit Fullscreen
   - Touch gestures on mobile:
     - Swipe left: Next page
     - Swipe right: Previous page

5. **Cloudflare Pages Ready**:
   - Assets are optimized under Cloudflare Pages' 25 MiB single file limit.
   - Static output configuration (`output: 'static'`) for zero-cold-start edge delivery.

---

## 🚀 How to Run Locally

```bash
cd /home/lordbandhan/jbsa-cricket/bpl-viewer

# Start development server
npm run dev

# Or build and preview production build
npm run build
npm run preview
```

---

## ☁️ How to Deploy to Cloudflare Pages

### Option 1: Direct Deploy with Wrangler
```bash
cd /home/lordbandhan/jbsa-cricket/bpl-viewer
npm run build
npx wrangler pages deploy dist --project-name=bpl-player-viewer
```

### Option 2: Connect via Cloudflare Dashboard (GitHub / GitLab)
1. Push this directory to your GitHub repository.
2. In Cloudflare Dashboard, go to **Workers & Pages** -> **Create application** -> **Pages**.
3. Select your repository.
4. Set **Build command**: `npm run build`
5. Set **Build output directory**: `dist`
6. Click **Save and Deploy**!
