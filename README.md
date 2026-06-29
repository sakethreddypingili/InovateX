# InnovateX Developer Documentation

InnovateX is a premium development agency portfolio web application. Crafted with modern visual assets, dynamic theme selectors (dark/light), interactive project showcase carousels, testimonials, and a fully validation-backed contact form submission utility.

---

## Directory Structure

This repository contains the following structural layout:
* index.html - Houses primary section containers, navigation headers, testimonial grids, and contact form containers.
* CSS/styles.css - Defines layout parameters, visual variables, utility spacing, responsive overrides, and theme configurations.
* JS/app.js - Configures system entry points, binds user interaction events, and initializes system state objects.
* JS/state.js - Tracks global theme values, filters active categories, and runs persistent theme configuration saves.
* JS/ui.js - Updates class lists to handle dark/light transitions, filters project lists, and validates contact form inputs.

---

## Architectural Flow & Communication Diagram

```
[ User Interaction ] ──► [ JS/app.js ] ──► [ JS/state.js ] ──(Save Theme)──► [ LocalStorage ]
                             │                  │
                             ▼                  ▼
                         [ JS/ui.js ] ◄───── (Preference Load)
                         (Update HTML Class Lists, Filter Cards)
```

---

## Module Specifications

### 1. Application Orchestrator (JS/app.js)
Coordinates visual and interactive states. Binds event listeners to portfolio filters, testimonial carousels, menu triggers, and coordinates transitions between modes.

### 2. Preference & State Engine (JS/state.js)
Maintains system preferences in memory. Details include:
* Theme config: Tracks light/dark states, loading preferences from browser LocalStorage.
* Portfolio filter: Coordinates active categories to display matching project cards.

### 3. Rendering Engine (JS/ui.js)
Modifies class structures in the DOM:
* Toggles light and dark mode classes on root layouts.
* Controls project overlays, showing or hiding cards based on filtering.
* Intercepts contact form actions, verifying fields before triggering submit events.

---

## Technical Features & Implementation Details

* Theme Management: Seamless theme updates are supported by toggling helper utility classes on root container elements.
* Responsive Typography: Leverages viewport units and flex containers to scale headings dynamically.
* Form Validation: Runs client-side validation scripts, evaluating input syntax patterns before proceeding.

---

## Local Development & Setup

### Prerequisites
A modern browser and a command-line interface.

### Running Locally
1. Navigate to the project root directory:
   ```bash
   cd "Portfolio"
   ```
2. Start a simple web server:
   ```bash
   python -m http.server 8000
   ```
3. Open a browser and navigate to `http://localhost:8000`.
