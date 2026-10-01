# 🌍 EcoPulse OS
**Autonomous Municipal Solid Waste Logistics & GIS Command Platform**

EcoPulse OS is an enterprise-grade, zero-dependency municipal operating system. It bridges the gap between citizen waste reporting and city sanitation dispatch through interactive GIS mapping, client-side neural vision simulation, and algorithmic fleet route optimization.

🔗 **[Click Here to Test the Live Web App](https://<your-username>.github.io/ecopulse-os/)**  
*(Note: Replace the link above with your actual GitHub Pages URL)*

---

## 🔐 Demo Login Credentials

To evaluate the platform, please use the following pre-provisioned credentials:

| Role | Email Address | Password | Access Level & Seeded State |
| :--- | :--- | :--- | :--- |
| **Admin Command** | `admin@ecopulse.org` | `Admin@123` | Root access to GIS Radar, AI TSP Route Optimizer, and CSV export. |
| **Citizen Profile** | `citizen@ecopulse.org` | `Citizen@123` | *Click "Load Demo Data" as admin first.* Pre-loaded with 24 tickets & 240 Eco-Credits. |

*(Judges may also use the **Register** portal to create a custom citizen profile to test the live Web Crypto password strength evaluator).*

---

## 🏗️ System Architecture

This platform was engineered with strict **zero-dependency** constraints, meaning it requires NO external libraries (no React, Node.js, Leaflet, or Bootstrap) and NO remote CDNs. It executes entirely in the browser.

*   **Presentation Layer:** Pure HTML5 and CSS3 utilizing a custom cyber-industrial glassmorphic design system (`backdrop-filter`).
*   **Logic & Routing Layer:** Modern Vanilla JavaScript (ES6+) with a custom hash-based Single Page Application (SPA) router.
*   **Storage & Resiliency Layer:** Multi-tier wrapper around browser `localStorage`. If quota is exceeded or storage is disabled, it seamlessly falls back to an in-memory runtime dictionary (`memoryCache`) to prevent crashes.
*   **Security Layer:** Client-side cryptographic hashing using the native **Web Crypto API** (`window.crypto.subtle`) for SHA-256 password salting, plus a universal `escapeHTML()` pipeline to prevent XSS injection.
*   **GIS & Graphics Engine:** Custom math-driven SVG rendering for the map and analytics charts, decoupled from heavy external libraries.

---

## ✨ High-Impact Features

### 1. Interactive Vector GIS Mapping Engine
*   **Zero-Dependency SVG Map:** A fully interactive map with mouse-drag panning and scroll-wheel zooming (0.6x to 2.8x).
*   **4 Operational Modes:** 
    *   *Picker:* Citizens click the map to dynamically tag coordinates (`{x}E, {y}N`) and municipal sectors.
    *   *Inspector:* Admins and citizens can launch modals to zoom directly into a specific incident's geographic waypoint.
    *   *Radar:* Live telemetry displaying all active incidents as color-coded pulse pins based on SLA urgency.
    *   *Optimizer:* Solves the **Traveling Salesperson Problem (TSP)** using a Nearest-Neighbor algorithm, animating the most fuel-efficient route for compactor trucks across all unresolved points.

### 2. Client-Side AI Computer Vision Simulator
*   Upload an evidence photo to trigger the HTML5 Canvas pixel analyzer.
*   The engine extracts the raw byte array (`getImageData`), analyzing RGB spectrum balance and luminance to predict the waste classification (e.g., Organic vs. Hazardous) with a live confidence score and animated HUD laser scanline.
*   **Auto-Downsampler:** Automatically compresses heavy smartphone photos to 400px or less JPEGs, ensuring browser storage quotas are never exceeded.

### 3. Concurrency-Protected Fleet Dispatcher
*   Citizens can book doorstep recovery for bulky or hazardous waste. 
*   The engine enforces a strict **concurrency lock of 3 bookings per time slot**. Real-time capacity meters update instantly, disabling booking buttons when a fleet window reaches saturation.

### 4. Multimedia & Gamification (Zero External Assets)
*   **Web Audio Synthesizer:** Procedural acoustic feedback (clicks, laser scans, error buzzers, success chords) generated purely via the browser's native `AudioContext`—no MP3 files required.
*   **Canvas Physics:** A mathematical 2D confetti particle simulator triggers upon successful incident resolution.
*   **Eco-Credits System:** Citizens earn verifiable points for reporting and completing the 10-round Waste Sorting Speed Challenge, upgrading their civic rank.

### 5. Multi-Language Engine (i18n)
*   A reactive, client-side dictionary supporting 26 distinct languages (English, Hindi, Spanish, Arabic, Mandarin, etc.).
*   Language switching instantly translates the UI without causing a page reload, preserving all map viewports and active form drafts.

---

## 💻 How to Run Locally

If you prefer to run the code locally instead of using the live web link:
1. Clone or download this repository.
2. Double-click the `index.html` file to open it in Google Chrome, Microsoft Edge, or Brave.
3. No build tools, `npm`, or local servers are required.
