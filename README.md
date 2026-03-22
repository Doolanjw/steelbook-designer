# SteelBook Cover Designer

A browser-based tool for designing custom SteelBook covers for home movies and personal media collections.

![SteelBook Designer](https://img.shields.io/badge/version-v8-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## Features

### Core Design Tools
- **G2 Standard Dimensions** — Accurate sizing for 4K UHD and Blu-ray cases (136mm × 171.4mm covers, 8.7mm × 154.2mm spine)
- **Multi-panel Layout** — Front cover, back cover, spine, and interior panels
- **Image Cropping** — Built-in Cropper.js integration with correct aspect ratios per panel
- **Spine Designer** — Create spines with custom background color, text, fonts, and logo slots (top/bottom)
- **Text Overlays** — Add title, spine text, and credits with customizable positioning
- **Image Adjustments** — Brightness, contrast, saturation, hue rotation, and filter presets

### AI Integration
- **AI Image Generation** — Support for OpenAI DALL-E 3, Stability AI, and Together AI / FLUX
- **AI Remix** — Transform existing images with style changes using Stability AI img2img
- **Prompt Templates** — Pre-built prompts for Action, Horror, Sci-Fi, Drama, Comedy, Thriller, Romance, and Fantasy genres
- **Generation History** — Track last 5 generations per panel with one-click restore

### Production Assets
- **Format Logos** — 4K UHD, Blu-ray, DVD badges
- **Rating Badges** — G, PG, PG-13, R, NR
- **Audio Logos** — Dolby Atmos, Dolby Vision, DTS-HD
- **UPC Barcode** — Customizable 12-digit barcode
- **Copyright Text** — Legal text block

### Export Options
- **PNG Export** — Full 300 DPI print-ready exterior and interior images
- **PDF Export** — Print-ready PDF with crop marks and 3mm bleed
- **Project Save/Load** — Save entire project as `.steelbook` file for later editing

### Quality of Life
- **Auto-save** — Automatic localStorage persistence (run via local server)
- **DPI Warnings** — Alerts when uploaded images are below print resolution
- **Collapsible UI** — Accordion sections keep the workspace clean
- **Keyboard Accessible** — Full keyboard navigation support
- **Quick Links** — Direct links to ThePosterDB, MoviePosterDB, Fanart.tv, TMDB, and more

## Usage

### Quick Start (Local)

1. Download `index.html`
2. Start a local server:
   ```bash
   python -m http.server 8000
   ```
3. Open `http://localhost:8000/index.html` in your browser

### Why a Local Server?

Running via `file://` protocol blocks localStorage in some browsers. A local server ensures auto-save works correctly.

## G2 Dimensions Reference

| Panel | Width | Height | Notes |
|-------|-------|--------|-------|
| Front Cover | 136mm | 171.4mm | Main cover image |
| Back Cover | 136mm | 171.4mm | Credits, scene art |
| Spine | 8.7mm | 154.2mm | Shorter than covers (fits between hinges) |
| Full Wrap | 280.7mm | 171.4mm | Single continuous print |
| Bleed | 3mm | — | Add to all edges for print |

**Resolution:** 300 DPI for print quality

## Tech Stack

- Vanilla HTML/CSS/JavaScript (single file, no build step)
- [Cropper.js](https://fengyuanchen.github.io/cropperjs/) — Image cropping
- [jsPDF](https://github.com/parallax/jsPDF) — PDF generation
- [Google Fonts](https://fonts.google.com/) — Typography (Bebas Neue, Oswald, Montserrat, etc.)

## API Keys

The designer supports these AI providers (bring your own API key):

- **OpenAI** — [Get API key](https://platform.openai.com/api-keys)
- **Stability AI** — [Get API key](https://platform.stability.ai/account/keys)
- **Together AI** — [Get API key](https://api.together.xyz/)

API keys are **not** stored in localStorage for security. You'll need to re-enter them each session.

## Artwork Resources

- [ThePosterDB](https://theposterdb.com/) — Curated movie posters
- [MoviePosterDB](https://www.movieposterdb.com/) — Large poster archive
- [Fanart.tv](https://fanart.tv/movie-fanart/) — Movie posters & disc art
- [TMDB](https://www.themoviedb.org/) — High-res movie posters
- [DeviantArt](https://www.deviantart.com/tag/steelbook) — Custom SteelBook art
- [r/SteelBooks](https://www.reddit.com/r/SteelBooks/) — Community & inspiration
- [The Steelverse (Etsy)](https://www.etsy.com/search?q=steelbook%20stickers) — Pre-made stickers & magnets

## License

MIT License — Use freely for personal projects.

## Acknowledgments

- Inspired by the DIY SteelBook community
- Tutorial reference: "DIY SteelBooks for $15" by Mike at the Marvel Man Cave
