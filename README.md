# 日本語 Conversation Learner PWA

A fully offline-capable Progressive Web App for learning Japanese through real conversations.

## Features

✅ **Real Conversations** - Add both your Japanese and friend's responses  
✅ **Spaced Repetition** - Track progress (new → reviewing → mastered)  
✅ **Offline First** - Works completely without internet  
✅ **Installable** - Add to home screen like a native app  
✅ **Text-to-Speech** - Hear Japanese pronunciation  
✅ **Search & Filter** - Find conversations by category or content  
✅ **Local Storage** - All data stays on your device  
✅ **Backup/Restore** - Export as JSON, import anytime  

## Files

- `index.html` - Main application (complete HTML + CSS + JavaScript)
- `sw.js` - Service Worker (enables offline functionality)
- `manifest.json` - PWA manifest (for installation)
- `README.md` - This file

## How to Deploy

### Option 1: Vercel (Recommended - Free & Easy)

1. Push files to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your GitHub repo
5. Deploy (takes ~1 minute)

Your app is live! Share the URL and anyone can add it to their home screen.

### Option 2: Netlify (Also Free)

1. Push files to GitHub
2. Go to [netlify.com](https://netlify.com)
3. Click "New site from Git"
4. Select your GitHub repo
5. Deploy

### Option 3: GitHub Pages (Simplest)

1. Create a GitHub repo named `username.github.io`
2. Upload the 3 files
3. Your app is live at `https://username.github.io`

### Option 4: Simple Server (Local Testing)

```bash
# Python 3
python -m http.server 8000

# Or Node.js
npx http-server

# Then visit: http://localhost:8000
```

## How to Use

### On Desktop/Laptop

1. Open the app URL in Chrome or Edge
2. You'll see an "Install" button in the header
3. Click to add to home screen or desktop
4. App opens in standalone window (no browser UI)

### On Mobile

1. Open the app URL in Chrome or Safari
2. Tap the menu (⋮) or share button
3. Select "Add to home screen"
4. Tap the icon to launch the app

## Workflow

### 1. Add Conversations

- Copy/paste Line chat exchanges or type in-person conversations
- Include both your Japanese and friend's response
- Add category (Daily Life, Food, Hobbies, etc.)
- Mark difficulty (easy/medium/hard)
- Add optional notes (grammar patterns, pronunciation tips)

### 2. Review

- Browse all conversations
- Search by category or content
- Mark as "reviewing" when practicing
- Mark as "mastered" when confident

### 3. Practice

- Random practice mode loads a conversation
- Click speaker button (🔊) to hear Japanese pronunciation
- Read aloud and practice
- Mark as mastered when confident

### 4. Track Progress

- See total conversations added
- Count mastered vs. reviewing
- Stats by category

### 5. Backup

- Download all conversations as JSON
- Email the file to yourself
- Restore anytime by uploading

## Offline Behavior

✅ **Works offline**: Everything syncs locally to your device  
✅ **No internet needed**: Service Worker caches the app  
✅ **Automatic sync**: Changes save to your device's storage  
✅ **Manual backup**: Export JSON whenever you want  

## Browser Support

- Chrome/Chromium: ✅ Full support
- Firefox: ✅ Full support (no home screen install on desktop)
- Safari: ✅ Mostly supported (iOS install works well)
- Edge: ✅ Full support
- IE11: ❌ Not supported

## Technical Details

- **Storage**: IndexedDB (no cloud sync)
- **Offline**: Service Worker + Cache API
- **Installation**: PWA manifest + beforeinstallprompt
- **Audio**: Web Speech API (native browser)
- **Zero dependencies**: Pure vanilla JavaScript

## Troubleshooting

**App won't install:**
- Make sure you're using HTTPS (required for PWA)
- Chrome/Edge on desktop or mobile Chrome
- Refresh the page and try again

**Data not saving:**
- Check browser's storage permissions
- Clear browser cache if you changed the app code
- Try importing your backup JSON

**Pronunciation not working:**
- Make sure browser has microphone permission
- Web Speech API requires Japanese language pack
- Try a different browser

**Offline issues:**
- Service Worker takes ~5 seconds to activate
- Visit the app once while online for caching
- Hard refresh (Ctrl+F5) if needed

## Customization

### Change Colors

Edit the `:root` section in `<style>`:

```css
:root {
  --primary: #0F6E56;        /* Main color */
  --accent: #D85A30;         /* Highlight color */
  --text-primary: #1a1a1a;   /* Text color */
}
```

### Change App Name

Edit in both `index.html` and `manifest.json`:

```json
{
  "name": "Your App Name",
  "short_name": "Short Name"
}
```

### Add Your Own Icon

Replace the SVG in `manifest.json` with a PNG URL.

## Privacy & Security

🔒 **All data stays on your device** - No cloud, no tracking, no servers  
🔒 **No login required** - Just use it  
🔒 **Offline first** - Works without internet  
🔒 **No permissions needed** - Only microphone for TTS  

## License

Free to use and modify. Share however you like!

## Support

If something doesn't work:

1. Check browser console (F12 → Console tab)
2. Clear browser cache and refresh
3. Try a different browser
4. Test offline mode (DevTools → Network → Offline)

---

**Happy learning! 頑張ってください！** 🎌
