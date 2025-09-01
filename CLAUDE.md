# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static landing page for "Whetstone Books" - a reading tracking iOS app. The site serves as a promotional splash page linking to the App Store download.

## Architecture & Structure

**Static Site Structure:**
- `index.html` - Main landing page with hero section, features, and CTA
- `style.css` - Complete styling with gradient hero, card-based features, and responsive design
- `assets/images/` - App icons and screenshots for promotional use

**Design System:**
- Gradient backgrounds (`#e66465` to `#9198e5` for hero, `#fdc830` to `#f37335` for icons)
- System fonts (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto`)
- Minimal, lowercase branding ("whetstone books")
- Card-based feature layout with hover effects
- Mobile-responsive flexbox design

## Development Commands

**Local Development:**
```bash
# Serve locally (any HTTP server)
python3 -m http.server 8000
# or
npx serve .
```

**Deployment:**
- Static files can be deployed to any web server
- Currently links to App Store: `https://apps.apple.com/us/app/whetstone-books/id1620581442`

## Content & Copy

The site uses casual, modern language ("vibe", "bruhs out", "cosmic") to appeal to younger readers. Key sections:
- Hero: "sharpen your reading prowess" 
- Features: reading tracking, notes/highlights, device sync
- CTA: emphasizes free download

## Related Projects

The footer links to the main Whetstone app repository: `https://github.com/phrazzld/whetstone`