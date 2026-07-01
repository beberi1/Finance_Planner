# Finance Planner Pro

A lightweight, privacy-first, zero-dependency personal finance tracking ecosystem built entirely inside a single HTML file. 

Unlike traditional budgeting apps that lock your financial data behind subscriptions or cloud databases, **Finance Planner Pro** operates entirely within your browser cache (`localStorage`), giving you absolute ownership over your data.

---

## 🚀 Why This Exists

Most financial planners force you into strict calendar months (1st to 30th/31st). In reality, personal financial cycles revolve around **Salary Dates**. If you get paid on the 10th of every month, your "June cycle" doesn't start until June 10th. 

Furthermore, syncing local-first web applications across multiple devices (like a home PC and a work laptop) usually results in data overwrites. This project solves both issues by introducing:
1. **Dynamic Financial Months:** Configurable salary-to-salary billing periods.
2. **2-Way Git-Like Merge Engine:** A local conflict-resolution client to safely sync data between multiple PCs using JSON files without data loss.

---

## 🛠️ Key Features

### 📅 Smart Budgeting & UI
* **Financial Month Overrides:** Configure the exact day you receive your salary. The app shifts your tracking timeline automatically (e.g., if set to the 10th, June 5th still treats your budget under the May cycle).
* **Flexible Layouts:** Switch dynamically between a structural **Grid Layout** and an expansive **Horizontal Kanban-style Board**.
* **Personal Piggy Banks (Vaults):** Drag-and-drop prioritized savings goals with rapid manual increment/decrement adjustments.
* **Dual-Currency Layer:** Built-in dynamic conversion between **USD ($)** and **GEL (₾)** using a customizable global exchange rate.

### 📊 Advanced Analytics Engine
* **Custom Range Queries:** Select precise month-to-month and year-to-year boundaries to isolate long-term trends.
* **Predictive Filtering:** Toggle *"Limit to Current Month"* to instantly remove future planned or automated expenses from current financial reality statistics.
* **Granular Visualization:** Render data across **Bar, Pie, or Pyramid Charts** sorted dynamically by Value (Highest/Lowest) or Alphabetical Category.

### 🔄 Distributed Synced Data (The Merge Engine)
* **Conflict Isolation:** Importing a `.json` backup doesn't blindly overwrite data. The built-in sync engine parses every item, flagging discrepancies side-by-side.
* **Granular Control:** Interactively **Accept** incoming external updates, **Keep** local records, or accept automated item deletions patch-by-patch via a visual diff modal.

---

## 🛠️ Technical Architecture

* **Language Stack:** HTML5, CSS3 (CSS Variables for dynamic theme layers), Vanilla ECMAScript 6.
* **Dependencies:** `0` (No external frameworks, trackers, or charting engines).
* **Data Storage:** Primary state persistence inside browser client-side cache (`localStorage`).
* **Portability:** Native browser File System access constraints bypassed safely using structured JSON serialization for quick import/export snapshots.

---

## 🏃‍♂️ Getting Started

Because the app is entirely self-contained, there is no installation setup, environment configuration, or `npm install` required.

1. Download the `planner.html` file.
2. Double-click the file to launch it instantly in any modern web browser (Firefox, Chrome, Brave, Safari, Edge).
3. Start entering your records locally. 

### 💻 Cross-Device Syncing Workflow
To pass updates seamlessly between two computers:
1. Click **Export Copy** on your active device to download a structured JSON file.
2. Transfer the file to your secondary machine (via USB, local network, or secure messaging).
3. Click **Import (Sync)** on the second machine, select the file, and use the interactive **Merge Modal** to safely unify your timeline.
