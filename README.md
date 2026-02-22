# Chat PWA - Claude AI Interface

A beautiful, iOS-optimized Progressive Web App for chatting with Claude AI.

## 🚀 Quick Start

### 1. Generate Icons & Splash Screens

Open `generate-assets.html` in your browser:
- Click "Generate All Assets"
- Click "Download All as ZIP"
- Extract the ZIP file
- Copy the `icons/` and `splash/` folders into your project root

### 2. Deploy to GitHub Pages

```bash
# Create a new repository or use existing one
git init
git add .
git commit -m "Initial PWA setup"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Then in GitHub:
1. Go to **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**

Your PWA will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO/`

## 📁 Project Structure

```
├── index.html           # Main app (all-in-one HTML/CSS/JS)
├── manifest.json        # PWA manifest for installation
├── sw.js               # Service worker for offline support
├── generate-assets.html # Icon & splash screen generator
├── README.md           # This file
├── icons/              # App icons (generate these first!)
│   ├── icon-16.png
│   ├── icon-32.png
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-167.png
│   ├── icon-180.png
│   ├── icon-192.png
│   ├── icon-384.png
│   ├── icon-512.png
│   ├── icon-maskable-192.png
│   ├── icon-maskable-512.png
│   ├── apple-touch-icon.png
│   └── shortcut-new.png
├── splash/             # iOS splash screens (generate these first!)
│   ├── splash-750x1334.png
│   ├── splash-828x1792.png
│   ├── splash-1125x2436.png
│   ├── splash-1170x2532.png
│   ├── splash-1179x2556.png
│   ├── splash-1242x2208.png
│   ├── splash-1242x2688.png
│   ├── splash-1284x2778.png
│   ├── splash-1290x2796.png
│   ├── splash-1536x2048.png
│   ├── splash-1668x2388.png
│   └── splash-2048x2732.png
└── screenshots/        # Optional: for app store listings
    ├── desktop.png
    └── mobile.png
```

## 📱 iOS Installation

### Adding to Home Screen
1. Open the PWA URL in Safari
2. Tap the **Share** button (square with arrow)
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **"Add"**

### Features Optimized for iOS
- ✅ Full-screen standalone mode (no browser UI)
- ✅ Splash screens for all iPhone/iPad sizes
- ✅ Safe area support (notch, Dynamic Island, home bar)
- ✅ Prevents overscroll bounce
- ✅ Momentum scrolling in chat
- ✅ Prevents zoom on input focus
- ✅ Haptic-style touch feedback
- ✅ System theme detection
- ✅ Keyboard handling
- ✅ Landscape mode support
- ✅ Reduced motion accessibility

## 🔧 Configuration

### API Key
Enter your Anthropic API key in the settings bar and click "Save". The key is stored locally in your browser.

### Theme
Click the sun/moon icon to toggle between dark and light themes. The app also respects your system preference.

### Model
The app uses `claude-opus-4-20250514` by default. To change this, edit line ~587 in `index.html`:
```javascript
model: 'claude-opus-4-20250514',  // Change to your preferred model
```

## 🛠 Customization

### Colors
Edit the CSS variables at the top of `index.html`:
```css
:root {
    --bg-body: #1a1a2e;
    --accent-color: #e94560;
    /* ... etc */
}
```

### Icon Design
Edit the `drawIcon()` and `drawSplash()` functions in `generate-assets.html` to customize the app icon and splash screens.

## 🔒 Security Notes

- API keys are stored in `localStorage` (stays on your device)
- Uses `anthropic-dangerous-direct-browser-access` header for CORS
- All data stays local - no server-side storage

## 📋 Browser Support

- **iOS Safari**: Full PWA support (14.0+)
- **Chrome**: Full support
- **Firefox**: Limited PWA support
- **Edge**: Full support

## 🐛 Troubleshooting

### PWA not installing on iOS
- Make sure you're using **Safari** (not Chrome or Firefox)
- The site must be served over **HTTPS**
- Clear Safari cache and try again

### Icons not showing
- Make sure you generated and copied all icons
- Check file paths match those in `manifest.json`
- Clear browser cache

### Service Worker issues
- Open DevTools → Application → Service Workers
- Click "Unregister" and reload the page
- Check Console for errors

### API errors
- Verify your API key is correct
- Check you have API credits
- Ensure CORS headers are properly set

## 📄 License

MIT License - feel free to modify and use as you wish!
