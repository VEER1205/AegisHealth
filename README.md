# 🏥 MediGuard — AI Triage Companion

A premium health triage web app featuring a **liquid glass UI** with an animated WebGL background. MediGuard helps users assess symptoms, measure vitals, scan skin conditions, and generate doctor-ready reports — all powered by AI.

![License](https://img.shields.io/badge/license-MIT-blue)
![React](https://img.shields.io/badge/React-19-61dafb)
![Three.js](https://img.shields.io/badge/Three.js-WebGL-black)
![Vite](https://img.shields.io/badge/Vite-⚡-646cff)

---

## ✨ Features

| Feature | Description |
|---|---|
| **💬 AI Symptom Chat** | Conversational triage with follow-up questions; outputs a tier-based recommendation (ER / Doctor / Home Care) |
| **📷 Skin & Wound Scanner** | Guided camera UI with real-time tips for capturing affected areas |
| **❤️ Vital Signs Monitor** | Camera-based heart rate and respiratory rate measurement (PPG simulation) |
| **🎤 Cough & Breath Analysis** | 10-second sound recording with pattern classification |
| **📄 Doctor Report** | One-tap shareable summary with patient profile, triage result, and vitals |
| **🔔 Follow-Up Reminders** | Scheduled 6h / 24h / 48h check-ins to track symptom progression |
| **🚨 Emergency Detection** | Red-flag keyword detection triggers an immediate 911/108 call prompt |

---

## 🎨 Design

- **Liquid Glass Theme** — Dark glassmorphism with frosted panels, translucent cards, and subtle backdrop blur
- **Animated WebGL Background** — Floating cyan wave lines rendered via Three.js fragment shaders with mouse interactivity and parallax
- **Responsive Layout** — Desktop sidebar + mobile bottom nav with adaptive grid layouts
- **Micro-Animations** — Fade-ups, heart pulse, scan lines, wave bars, and smooth hover transitions

---

## 🛠️ Tech Stack

- **React 19** — Component-based UI
- **Vite** — Lightning-fast dev server and bundler
- **Three.js** — WebGL floating lines background (custom GLSL shaders)
- **Vanilla CSS** — Glassmorphism, keyframe animations, utility classes
- **DM Sans + Playfair Display** — Premium typography via Google Fonts

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 18
- **npm** ≥ 9

### Installation

```bash
# Clone the repository
git clone https://github.com/VEER1205/AegisHealth.git
cd Health-cheker

# Install dependencies
npm install --legacy-peer-deps

# Start development server
npm run dev
```

The app will be available at **http://localhost:5173**

### Build for Production

```bash
npm run build
npm run preview
```

---

## 📁 Project Structure

```
Health-cheker/
├── index.html              # HTML entry point
├── package.json            # Dependencies & scripts
├── vite.config.js          # Vite configuration
├── src/
│   ├── main.jsx            # React root mount
│   ├── App.jsx             # Main app — all screens, components, and logic
│   ├── App.css             # Global styles, animations, glass utilities
│   ├── FloatingLines.jsx   # Three.js WebGL animated background component
│   ├── FloatingLines.css   # Background container styles
│   └── assets/             # Static assets
└── dist/                   # Production build output
```

---

## 🔧 Configuration

### Floating Lines Background

The `FloatingLines` component accepts these props:

| Prop | Type | Default | Description |
|---|---|---|---|
| `linesGradient` | `string[]` | — | Array of hex colors for the line gradient |
| `enabledWaves` | `string[]` | `['top','middle','bottom']` | Which wave groups to render |
| `lineCount` | `number[]` | `[6]` | Number of lines per wave group |
| `animationSpeed` | `number` | `1` | Speed multiplier for the animation |
| `interactive` | `boolean` | `true` | Enable mouse-bend interaction |
| `parallax` | `boolean` | `true` | Enable parallax on mouse move |
| `bendStrength` | `number` | `-0.5` | How much lines bend near the cursor |

---

## ⚠️ Disclaimer

MediGuard is a **prototype** and does **not** provide real medical diagnoses. It is intended for educational and demonstration purposes only. Always consult a qualified healthcare professional for medical advice.

---

## 📄 License

This project is licensed under the MIT License.
