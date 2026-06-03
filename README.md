# 🤖 הבוטים הסוררים — AI Escape Room

משחק Escape Room תלת-ממדי אינטראקטיבי לחינוך בינה מלאכותית, מיועד לכיתות ז׳–ח׳.

---

## 🎮 על המשחק

השחקנים נכנסים לחדר שנשתלט בידי בוטים סוררים של מערכת AI בשם **נובה**.  
המשימה: לפתור שש תחנות, לאסוף קודים, ולברוח מהחדר תוך 60 דקות.

---

## 🗺️ תחנות המשחק

| תחנה | נושא AI | מנגנון |
|------|---------|--------|
| 📱 **טלפון** | אימון מודלים — Learning from Examples | חידת סמלים מתמטית, קוד: `32` |
| 📺 **טלויזיה** | Computer Vision | מציאת 16 כלבים בתמונה, קוד: `16` |
| 💻 **מחשב** | עץ החלטות — Decision Tree | קריאת קוד עברי, ALGO TRADE, קוד: `76` |
| 🤖 **רובוט** | — | עמדת ניהול מאובטחת |
| 🔑 **מפתח** | — | לוח מקשים עם קוד 8 ספרות |
| 🚪 **דלת** | — | פאזל מנעולים |

---

## ⚙️ טכנולוגיות

- **Three.js r170** — עולם תלת-ממד עם Gaussian Splat (`room.spz`)
- **PointerLockControls** — תנועה בגוף ראשון (WASD + עכבר)
- **HTML / CSS / Vanilla JS** — ממשק משתמש, פאזלים, אנימציות
- **Electron** — אפליקציה שולחנית, מסך מלא

---

## 🚀 הרצה מקומית

```bash
# דפדפן בלבד
פתח את index.html בדפדפן

# אפליקציה שולחנית (Electron)
npm install
npm start
```

## 📦 בניית EXE

```bash
npm run build
# הקובץ יופיע בתיקיית dist/
```

---

## 📋 Release Notes

### v1.0.0 — יוני 2025

**תחנות חדשות:**
- ✅ תחנת הטלפון — typewriter intro + חידת סמלים + `hesber.mp3`
- ✅ תחנת הטלויזיה — 3 מסכים, מציאת 16 כלבים, zoom/pan, `beep.mp3`
- ✅ תחנת המחשב — סרטון `graph.mp4`, מסך `badgraph.png` + typewriter, קוד ALGO TRADE בעברית מלאה, סרטון `goodgraph.mp4` בסיום
- ✅ תחנת המפתח — סרטון כניסה + keypad 8 ספרות (כולל `0`)

**UI / UX:**
- ✅ Badge קוד על עיגולי משימות בסיום כל תחנה
- ✅ מסך ניצחון עם קונפטי + זמן שנשאר + כפתור "התחילו מחדש"
- ✅ Syntax highlighting בסגנון VSCode לקוד בעברית

**Electron:**
- ✅ `main.js` — fullscreen, `webSecurity: false`, F11 לבקר
- ✅ `package.json` — `electron-builder`, NSIS installer, `asar: false`

---

## 📁 מבנה הפרויקט

```
aiEroom/
├── index.html          ← כל המשחק
├── main.js             ← Electron entry point
├── package.json        ← build config
├── images/             ← תמונות UI ותחנות
├── audio/              ← קבצי סאונד
├── video/              ← סרטוני תחנות
└── models/             ← room.spz, room.glb, key.glb
```
