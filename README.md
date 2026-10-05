# Traveller 2E Mega-Campaign Dashboard

A self-contained, browser-based gamemaster utility designed specifically for running multi-book Traveller 2E campaigns (such as the *Ancients* series). This tool automates the logistical, financial, tactical, and narrative minutia required to run the game smoothly without flipping through reference books.

## Features

### 1. Jump & Fuel Logistics Calculator
Automates the liquid hydrogen fuel consumption calculations based on standard Mongoose Traveller 2E core rules:
*   **Jump Fuel Formula:** `0.1 × Hull Size × Jump Distance` (Tons).
*   **Power Plant Fuel Formula:** Per-week calculation derived from standard 4-week operation requirements (`[0.05 × Hull Size × Power Plant Rating] / 4`).
*   **Total Core Reserve:** Sums jump requirements and operational plant demands for clean pre-flight planning.

### 2. Ship Ledger & Bank Balance
Tracks the party's ongoing operational overhead to keep ship economics threatening but manageable:
*   Maintains a persistent record of current bank funds.
*   Deducts fixed monthly liabilities (Mortgage payments, crew salaries, life support costs, and maintenance fund allocations).
*   Provides real-time validation of remaining liquidity post-autopay.

### 3. Tactics & Combat Tracker
A lightweight initiative manager optimized for both space and ground skirmishes:
*   Sorts all active combatants dynamically by initiative score.
*   Tracks crucial vital statistics (Hull Points/Stamina and Armor ratings) per unit.
*   Includes quick-removal triggers ("KIA") to clean up the battlefield instantly.

### 4. Speculative Cargo Generator & Exporter
Generates random market lots for commercial activities between narrative hubs:
*   Scales available lots based on the local system's **Starport Classification (A–E)**.
*   Rolls random lot sizes utilizing multi-dice variances tailored to specific trade goods.
*   **CSV Exporter:** Features a spreadsheet-ready exporter that packages current market manifests into a `.csv` file for external tracking.

### 5. System & Starship Encounter Generator
A procedural engine to instantly spawn random planetary contexts and deep space vectors:
*   **UWP Generator:** Generates a randomized 7-character Universal World Profile (Hex format) detailing local system parameters.
*   **Vessel Architect:** Constructs starship signatures pulling from standard Traveller hull types (Scouts, Free Traders, Yachts, Subsidized Merchants) complete with accurate base Hull Points, Armor, and hardpoint weaponry.
*   **Personnel & Quirk Matrix:** Generates the commanding officer's identity along with operational crew anomalies, tracking issues, or behavioral quirks.
*   **System Integration:** Features a **"Deploy to Combat Tracker"** utility that bridges modules, auto-populating structural statistics and rolling a baseline 2d6 initiative profile directly into the tactical manager.

### 6. Discovery & Clue Matrix
A persistent log designed to track long-term plot points, alien artifact data, or hyper-spatial observations. Entries are time-stamped down to the minute and saved automatically.

---

## Technical Architecture & Design

*   **Zero-Dependency Stack:** Built purely in vanilla **HTML5, CSS3, and JavaScript**. Requires no build tools, npm packages, or active internet connection to execute.
*   **Persistent Storage Model:** Utilizes the browser's native `localStorage` API. Configuration values, tactical combat states, and logged narrative data automatically persist across page refreshes and browser restarts.
*   **Fully Responsive Layout:** Utilizes a CSS Grid architecture that automatically snaps from desktop configurations to a single column for effortless table use on smartphones or tablets.

## Installation & Deployment

### Local Execution
1. Copy the full HTML source code block provided in your session.
2. Paste the contents into a plain text file.
3. Save the file exactly as `dashboard.html`.
4. Double-click the file to open it inside any modern web browser.

### Free Web Hosting (GitHub Pages)
1. Log into your GitHub account and create a new repository (e.g., `traveller-campaign`).
2. Add a new file named `index.html` and paste the code inside.
3. Commit the changes to the `main` branch.
4. Navigate to **Settings > Pages**, set the build source to the `main` branch, and click **Save**.
5. Your dashboard will be live at a public, secure `https://[your-username].github.io/traveller-campaign/` link accessible from any table device.
