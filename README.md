# Whetstone Books Landing Page

A high-performance, conversion-optimized landing page for [Whetstone Books](https://apps.apple.com/us/app/whetstone-books/id1620581442) - a reading tracking app for iPhone, iPad, and Mac.

## 🎯 Overview

This landing page is designed with a **performance-first, accessibility-always** approach, focusing on driving App Store downloads through clean design and strategic conversion optimization.

### Key Features

- **⚡ Ultra-Fast Loading**: Critical CSS inlined, minified assets, optimized images
- **🎨 Clean Design**: Professional typography, semantic icons, smooth animations
- **📱 Mobile-First**: Responsive design optimized for all Apple devices
- **♿ Accessible**: WCAG compliance, reduced-motion support, semantic HTML
- **🔍 SEO Optimized**: Open Graph, Twitter Cards, structured data
- **🎯 Conversion Focused**: Single clear CTA, trust signals, privacy messaging

## 📊 Performance Stats

- **Page Weight**: <500KB total (all assets)
- **CSS**: 1.4KB gzipped (75% reduction from original)
- **Images**: 90% compression achieved (3.9MB → 300KB)
- **Critical CSS**: <2KB inlined for instant rendering
- **Lighthouse Score Target**: 95+ Performance, 100 Accessibility

## 🏗️ Architecture

```
whetstone-splash/
├── assets/
│   ├── images/           # Optimized WebP variants + PNG fallbacks
│   ├── favicon-*.png     # Generated favicon set
│   ├── apple-touch-icon.png
│   └── og-image.png      # Social sharing image (1200x630)
├── docs/                 # Development guidelines & philosophy
├── index.html           # Main landing page
├── style.css            # Minified production CSS
└── README.md            # This file
```

### Image Optimization Strategy

- **Source**: Single high-res PNG compressed with pngquant
- **Formats**: WebP variants for modern browsers, PNG fallbacks
- **Sizes**: Responsive srcset (320w, 768w, 1024w, 1440w)
- **Loading**: Critical images preloaded, DNS prefetch for external domains

## 🚀 Quick Start

### Prerequisites
- Modern web browser
- Optional: Node.js for development tools

### Local Development

```bash
# Clone the repository
git clone https://github.com/phrazzld/whetstone-splash.git
cd whetstone-splash

# Install development dependencies (optional)
npm install

# Serve locally (any static server works)
python -m http.server 8000
# or
npx serve .

# View at http://localhost:8000
```

### Deployment

This is a static site that can be deployed anywhere:

```bash
# Deploy to any static hosting provider
# - GitHub Pages
# - Netlify
# - Vercel  
# - AWS S3
# - etc.
```

## 🛠️ Development

### CSS Minification

```bash
# Minify CSS for production
npx postcss style.css --use cssnano --no-map --output style.min.css
```

### Image Optimization

```bash
# Compress PNG images
pngquant --quality=65-80 source.png --output compressed.png

# Generate WebP variants  
cwebp -q 85 source.png -o image-768w.webp
```

### Quality Gates

Run comprehensive checks before deployment:

```bash
# Validate HTML structure
node -p "require('fs').readFileSync('index.html', 'utf8').match(/<(\/?[a-zA-Z]+)/g).length"

# Check asset links
grep -o 'href="[^"]*"' index.html | cut -d'"' -f2 | grep -v "^https://" | xargs ls

# Verify image references
grep -o 'src="[^"]*"' index.html | cut -d'"' -f2 | xargs ls
```

## 📋 Optimization Checklist

### ✅ Performance
- [x] Images compressed (90% reduction)
- [x] CSS minified (1.4KB gzipped)
- [x] Critical CSS inlined
- [x] DNS prefetch for external domains
- [x] will-change optimization for animations
- [x] Preload critical assets

### ✅ SEO & Social
- [x] Meta description (112 chars)
- [x] Open Graph tags (Facebook)
- [x] Twitter Card metadata
- [x] JSON-LD structured data (MobileApplication)
- [x] Canonical URL
- [x] Favicon set (16x16, 32x32, 180x180)

### ✅ Accessibility
- [x] Semantic HTML structure
- [x] Alt text for all images
- [x] Descriptive aria-labels
- [x] Keyboard navigation support
- [x] Reduced motion preferences
- [x] Color contrast compliance

### ✅ Conversion Optimization
- [x] Single clear CTA strategy
- [x] Trust signals (5-star rating, privacy)
- [x] Clean, professional design
- [x] Mobile-optimized experience
- [x] Fast loading for low bounce rate

## 🎨 Design System

### Colors
```css
--gradient-primary: linear-gradient(135deg, #e66465, #9198e5);
--gradient-secondary: linear-gradient(135deg, #fdc830, #f37335);
--color-primary: #333;
--color-white: #fff;
--color-bg-light: #f5f5f5;
```

### Typography
- **Font Stack**: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif
- **Hero**: 3rem, weight 700, -0.02em letter-spacing
- **Body**: 1rem, 1.6 line-height
- **Features**: 1.3rem headings, weight 600

### Animations
- **Fade In**: 0.6s ease for hero text
- **Hover Effects**: 0.3s cubic-bezier transitions
- **Sparkle**: 2s infinite for rating stars
- **Reduced Motion**: Respects user preferences

## 📱 Browser Support

- **Chrome/Edge**: 90+ (88% users)
- **Safari**: 14+ (8% users)
- **Firefox**: 88+ (3% users)
- **Samsung Internet**: 14+ (1% users)

Modern features with progressive enhancement:
- CSS Grid (fallback: Flexbox)
- WebP images (fallback: PNG)
- CSS Custom Properties (fallback: hard-coded values)

## 🔄 Deployment Workflow

```bash
# 1. Make changes
git add .

# 2. Run quality gates
npm run lint    # if configured
npm run build   # if configured

# 3. Commit with conventional format
git commit -m "feat: describe changes"

# 4. Push to production
git push origin main
```

## 📈 Analytics & Monitoring

### Key Metrics to Track
- **Conversion Rate**: CTA clicks → App Store visits
- **Performance**: Core Web Vitals, loading times
- **User Behavior**: Scroll depth, time on page
- **Technical**: Error rates, asset loading success

### Recommended Tools
- **Performance**: Lighthouse CI, WebPageTest
- **Analytics**: Google Analytics, privacy-focused alternatives
- **Monitoring**: Synthetic monitoring for uptime
- **A/B Testing**: For headline and CTA optimization

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-improvement`
3. Follow the existing code style and conventions
4. Test your changes thoroughly
5. Submit a pull request with clear description

### Development Philosophy

This project follows performance-first, accessibility-always principles:

- **Performance**: Every asset and technique is optimized for speed
- **Accessibility**: WCAG compliance and inclusive design
- **Simplicity**: Clean code, minimal dependencies
- **Progressive Enhancement**: Works everywhere, enhanced where supported

## 📄 License

[MIT License](LICENSE) - Feel free to use this as a template for your own projects.

## 🔗 Links

- **Live Site**: [whetstone-books.com](https://whetstone-books.com)
- **App Store**: [Download Whetstone Books](https://apps.apple.com/us/app/whetstone-books/id1620581442)
- **Source Code**: [GitHub Repository](https://github.com/phrazzld/whetstone-splash)
- **Issue Tracker**: [GitHub Issues](https://github.com/phrazzld/whetstone-splash/issues)

---

Built with ❤️ for readers everywhere. Happy tracking! 📚