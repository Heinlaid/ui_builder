# UI Builder – Mockup Tool for Webpages

✨ What the extension does
UI Builder adds a lightweight, sketch-style prototyping layer on top of any site you visit.
Click the toolbar button → a floating palette appears in the top-right corner; from there you can drag ready-made “Balsamiq” widgets onto the current page (or onto a dedicated blank canvas that opens in a new tab).

Everything happens locally in your browser – no data ever leaves your machine.

🧰 Widget toolkit
(all rendered with Indie Flower font & a tiny –1 ° “hand-drawn” tilt)


Basic controls	Layout / decoration	Typography	Form bits
Button (auto width)	Frame (2 px outline, sits behind other items)	Header (bold, 2 rem)	Checkbox
Text input	Box (filled rectangle, eyedropper recolour)	Text (regular, 1.75 rem)	Radio button
Drop-down (readonly placeholder, triangle glyph)	Divider – double-click to swap horizontal / vertical		
All widgets:

can be dragged (interact.js)

have 4 resize handles; dividers resize only along their axis

remember their own initial width and font-size and scale text smoothly while you resize

support in-place editing – double-click most elements to change their label / placeholder

📋 Canvas-level features

Feature	How
Auto-save	Stored in chrome.storage.local, keyed per origin; blank-canvas tabs each get an isolated session ID
Copy / paste inside the mock-up	Ctrl / ⌘ + C then Ctrl / ⌘ + V (element-wise, duplicates appear offset by 20 px)
Delete	Del or Backspace
Selection outline & handles	Click a widget – dashed light-blue outline with 4 handles
Box eyedropper	While a Box is selected, click the pipette icon and pick any background-colour on the page
Panel drag	Grab the panel header to move; it always stays fixed to the viewport
Clear	Trash-can icon removes everything and resets storage
📸 Export & screenshots
Save Mock-up – enter Selection-mode → draw / resize a marquee → hit ✓ → saved as mockup.png (cropped client-side, no server round-trip).

Copy screenshot – one-click capture of the visible viewport directly to the clipboard (PNG).

Blank canvas – opens blank.html (white page, no DOM clutter) for presentation-ready exports.

The selection HUD shows live width/height, lets you enter exact numbers, and is draggable/resizable itself.

⌨️ Keyboard shortcuts

Keys	Action
Ctrl / ⌘ + C	Copy selected widget
Ctrl / ⌘ + V	Paste copy
Del / Backspace	Delete selection
Esc	Cancel current screenshot selection
Arrows inside selection HUD	Nudge marquee while selecting
🛠️ Permissions & privacy

Permission	Why it’s needed
activeTab / scripting	Inject the mock-up layer & capture screenshots
storage	Persist your canvas per site
downloads	Save PNG files locally
clipboardWrite	Copy screenshots to clipboard
No network requests, no analytics, no user data collection – everything is processed purely in-browser.

🌍 Localisation
UI Builder is ready for 24 languages (English, 中文, हिन्दी, Español, Français, …); all user-visible strings – tooltips, prompts, alerts – are pulled from Chrome i18n message files. The name “UI Builder” stays in English so it’s recognisable in every locale.

🚧 Known limitations
Some heavy sandboxed sites (e.g. Yahoo Mail) block prompt() dialogs – in those places the in-place text editor silently switches to a fallback method.

Screenshot capture requires the standard “Capture content of your screen” prompt on first use in Manifest V3; blank-canvas tabs show a reminder if permission is missing.

🏁 Getting started
Install, pin the toolbar icon.

Click the icon – the panel pops in.

Drag anything onto the page, resize / edit / recolour until it looks right.

Hit the disk icon, draw a rectangle, ✓ → PNG.

Or open a Blank Canvas, design at pixel-ratio-1 :1.

Share your mock-up – save to file or copy straight to Slack / Figma / Jira…

Happy sketching!

---

## 🚀 Installation (dev build)

1. Clone / download the repo.  
2. Open **`chrome://extensions`** in Chrome.  
3. Enable **Developer mode** (top-right).  
4. Hit **Load unpacked** and choose the project folder.  
5. Pin the *UI Builder* icon for quick access.

---

## 🖱️ Usage Guide

| Action | How |
|--------|-----|
| Toggle builder | Click the extension icon |
| Place element  | Drag from the panel, drop on the page |
| Move / Resize  | Drag element / drag handles |
| Edit text      | Double-click header/text/button |
| Pick box color | Select Box → click pipette icon → click any page area |
| Copy / Paste   | Select element → **Ctrl/Cmd +C**, then **Ctrl/Cmd + V** |
| Delete         | **Delete** or **Backspace** |
| Screenshot     | Click camera icon → draw area → ✓ |
| Clear canvas   | Trash-can icon |
| Blank canvas   | New-page icon |
| Quit builder   | Close (×) on the panel or click toolbar icon again |

---

## 🧩 Tech Stack

- **Manifest V3** Chrome Extension  
- **Vanilla JavaScript** (ES 2022)  
- **Interact.js** – drag, drop & resize  
- **Tailwind CSS** – zero-config styling  
- Inline Shadow DOM for panel isolation

---

## 🚧 Roadmap / TODO

- Switch, Checkbox, Radio, Slider components  
- Share / collaboration flow  
- JSON export & code generation  
- Multi-language UI (EN/RU) polishing  
- Accessibility improvements

---

## 📄 License

MIT
