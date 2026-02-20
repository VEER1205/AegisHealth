<div align="center">

# MediGuard

### AI-Powered Medical Triage Companion

A premium health triage web application featuring a **liquid glass UI** with an animated WebGL background.
MediGuard helps users assess symptoms, measure vitals, scan skin conditions, and generate doctor-ready reports — all powered by artificial intelligence.

![License](https://img.shields.io/badge/license-MIT-blue)
![React](https://img.shields.io/badge/React-19-61dafb)
![Three.js](https://img.shields.io/badge/Three.js-WebGL-black)
![Vite](https://img.shields.io/badge/Vite-Fast-646cff)

</div>

---

## Table of Contents

- [Features](#features)
- [Design Philosophy](#design-philosophy)
- [Tech Stack](#tech-stack)
- [Team Members](#team-members)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Disclaimer](#disclaimer)
- [License](#license)

---

## Features

### AI Symptom Chat

An intelligent conversational interface that guides users through a structured medical interview. The AI asks focused follow-up questions about symptom onset, severity (1-10 scale), duration, and associated factors. After gathering sufficient information through 3-4 exchanges, it produces a **three-tier triage recommendation**:

- **Tier 1 — GO TO ER NOW**: Immediate emergency care required
- **Tier 2 — SEE DOCTOR (24-48 hrs)**: Non-emergency but needs professional evaluation
- **Tier 3 — MANAGE AT HOME**: Self-care with monitoring guidance

Each recommendation includes confidence level, top contributing symptoms, a plain-language explanation, and caveats about what the system cannot assess.

### Skin and Wound Scanner

A guided camera interface designed for dermatological assessment. The scanner provides:

- **Real-time capture tips** that cycle through positioning, lighting, stability, and framing guidance
- **Visual alignment overlay** with corner brackets and center-frame indicators
- **Scanning animation** with a moving laser-line effect during analysis
- **AI-generated results** with confidence level (Low / Moderate / High), condition identification, and recommended next steps

Supports assessment of skin rashes, open wounds, swelling, and mole changes.

### Vital Signs Monitor

A camera-based vital signs measurement system that uses photoplethysmography (PPG) principles. Users place their fingertip over the camera lens, and the system detects pulse patterns through subtle light changes. It measures:

- **Heart Rate (HR)** — Displayed in BPM with normal/low/elevated classification
- **Respiratory Rate (RR)** — Displayed in breaths per minute with status indicators

Results are shown with animated progress rings during measurement and visual waveform displays after completion.

### Cough and Breath Sound Analysis

A 10-second microphone recording feature that classifies respiratory sounds. The system analyzes audio patterns and identifies:

- **Dry Cough** — Non-productive, likely upper respiratory irritation
- **Wet Cough** — Productive pattern, may need medical attention if persistent
- **Wheezing** — Airway narrowing detected, medical evaluation recommended

Each classification includes severity rating and actionable advice.

### Doctor Report Generator

A one-tap shareable medical summary compiled from all collected data. The report includes:

- Patient demographics (age, sex, conditions, medications)
- Triage assessment with tier, confidence, and explanation
- Vital signs readings with normal range comparison
- Skin scan results (if performed)
- Sound analysis findings (if recorded)
- Timestamp and disclaimer

Designed for easy sharing with healthcare providers during consultations.

### Follow-Up Reminders

An automated check-in system with three scheduled touchpoints:

- **6 hours** — Early check: "How are you feeling compared to earlier?"
- **24 hours** — Next day check: "Did your symptoms improve overnight?"
- **48 hours** — Follow-up: "Has your condition resolved or are you still experiencing symptoms?"

Users can respond to each reminder and add notes, creating a symptom progression timeline.

### Emergency Red-Flag Detection

A real-time safety layer that monitors all user input for life-threatening keywords. When detected, it immediately triggers a full-screen emergency modal with:

- Clear identification of the emergency type
- Direct one-tap call button for emergency services (911/108)
- Keywords monitored include: chest pain, difficulty breathing, stroke symptoms, unconsciousness, seizures, and severe bleeding

---

## Design Philosophy

### Liquid Glass Theme

The interface uses a dark glassmorphism aesthetic where every panel, card, and button is a frosted glass surface. Semi-transparent backgrounds with `backdrop-filter: blur()` create depth and layering, while subtle white border highlights and inset shadows simulate light refraction on glass edges.

### Animated WebGL Background

Behind the glass UI sits a full-screen Three.js canvas rendering animated floating wave lines through custom GLSL fragment shaders. The lines respond to mouse movement with bend and parallax effects, creating a living, breathing backdrop that reinforces the health-tech aesthetic.

### Responsive Layout

- **Desktop (1024px+)**: Fixed sidebar navigation with scrollable content area
- **Mobile**: Bottom tab navigation with compact card layouts

### Typography and Motion

- **DM Sans** for UI text — clean, geometric, highly readable
- **Playfair Display** for headings — elegant serif for premium feel
- Micro-animations throughout: fade-ups, heart pulse, scan lines, wave bars, and smooth hover state transitions

---

## Tech Stack

| Technology | Purpose |
|---|---|
| **React 19** | Component-based UI architecture |
| **Vite** | Lightning-fast dev server and production bundler |
| **Three.js** | WebGL-powered animated background with custom GLSL shaders |
| **Vanilla CSS** | Glassmorphism effects, keyframe animations, utility classes |
| **Google Fonts** | DM Sans and Playfair Display typography |

---

## Team Members

<table>
  <tr>
    <th>Name</th>
    <th>Role</th>
    <th>Contributions</th>
  </tr>
  <tr>
    <td><strong>Hrishikesh Ganji</strong></td>
    <td>Team Lead / ML Engineer</td>
    <td>Project leadership and coordination, machine learning model architecture and development, AI triage logic design, overall system integration and technical decision-making</td>
  </tr>
  <tr>
    <td><strong>Veer Dodiya</strong></td>
    <td>Full Stack Developer</td>
    <td>End-to-end application development, React component architecture, Three.js WebGL background implementation, liquid glass UI theming, backend API integration, deployment pipeline</td>
  </tr>
  <tr>
    <td><strong>Nirjal Jagtap</strong></td>
    <td>Frontend Developer</td>
    <td>UI component development, responsive layout implementation, animation and interaction design, cross-browser testing and optimization</td>
  </tr>
  <tr>
    <td><strong>Keval Shah</strong></td>
    <td>Frontend Developer</td>
    <td>Feature screen development, form handling and validation, mobile-first design implementation, accessibility improvements</td>
  </tr>
  <tr>
    <td><strong>Dev Shah</strong></td>
    <td>ML Engineer</td>
    <td>Symptom classification model development, cough and breath sound analysis algorithms, vital signs detection logic, AI response pipeline</td>
  </tr>
  <tr>
    <td><strong>Chinmay Chopade</strong></td>
    <td>PPT / Docs / Presentation / UI-UX</td>
    <td>Presentation deck creation and delivery, project documentation, user experience research and wireframing, visual design direction and branding</td>
  </tr>
</table>

---

## Getting Started

### Prerequisites

- **Node.js** >= 18
- **npm** >= 9

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

## Project Structure

```
Health-cheker/
│
├── index.html                 # HTML entry point
├── package.json               # Dependencies and scripts
├── vite.config.js             # Vite bundler configuration
│
├── src/
│   ├── main.jsx               # React root mount
│   ├── App.jsx                # Main application — screens, components, state, logic
│   ├── App.css                # Global styles, keyframe animations, glass utilities
│   ├── FloatingLines.jsx      # Three.js WebGL animated background (GLSL shaders)
│   ├── FloatingLines.css      # Background container positioning
│   └── assets/                # Static assets (images, icons)
│
└── dist/                      # Production build output (generated)
```

---

## Configuration

### Floating Lines Background

The `FloatingLines` component accepts the following props for customization:

| Prop | Type | Default | Description |
|---|---|---|---|
| `linesGradient` | `string[]` | — | Array of hex color codes for the line gradient |
| `enabledWaves` | `string[]` | `['top', 'middle', 'bottom']` | Which wave layer groups to render |
| `lineCount` | `number \| number[]` | `[6]` | Number of lines per wave group |
| `lineDistance` | `number \| number[]` | `[5]` | Spacing between lines in each group |
| `animationSpeed` | `number` | `1` | Global speed multiplier for wave animation |
| `interactive` | `boolean` | `true` | Enable cursor-based line bending |
| `bendRadius` | `number` | `5.0` | Radius of the mouse influence area |
| `bendStrength` | `number` | `-0.5` | Intensity of the line bend near cursor |
| `parallax` | `boolean` | `true` | Enable parallax offset on mouse move |
| `parallaxStrength` | `number` | `0.2` | Intensity of the parallax effect |
| `mouseDamping` | `number` | `0.05` | Smoothing factor for mouse tracking (lower = smoother) |

---

## Disclaimer

MediGuard is a **prototype application** built for educational and demonstration purposes. It does **not** provide real medical diagnoses, and its recommendations should **never** replace professional medical advice. Always consult a qualified healthcare provider for any health concerns.

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
