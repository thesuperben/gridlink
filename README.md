# GridLink

**The Professional Endurance Strategy Suite for iRacing.**

GridLink is a distributed, AI-powered strategy platform that runs locally on your machine but connects your entire team. It replaces generic spreadsheets with live, actionable intelligence.

## 🏁 Key Features

*   **🎙️ AI Race Engineer**: Real-time voice coaching and strategy advice powered by Gemini Flash 2.5. Uses live telemetry to predict tire wear and fuel stints.
*   **🏎️ Live Telemetry**: Self-hosted dashboard with strict data privacy. Your setup data stays on your machine.
*   **🤝 Team Command Center**: Remote pit wall for team managers. Monitor multiple cars and drivers from a single "Owner" dashboard.
*   **📊 Smart Calculations**:
    *   Dynamic Lift & Coast targets.
    *   Automated Pit Window calculation and adjustments.
    *   Audio Alerts ("Box Box", "Fuel Low").
*   **💸 Subscription & Team Management**: Integrated Stripe billing for "Seat" management (Pro vs Free implementations).

---

## 🚀 Quick Start

**GridLink is designed to be "Zero-Config"**.

### 1. Download & Install
1.  Download the latest release from [Releases](https://github.com/thesuperben/GridLink/releases).
2.  Ensure you have **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** installed and running.

### 2. Start the Engine
Double-click **`run_gridlink.bat`** in the root folder.
*   This script will automatically pull the latest updates, build the containers, and launch the application.
*   Access the dashboard at: **`http://localhost:8000`**

### 3. Connect iRacing
1.  Open the Dashboard (`http://localhost:8000`).
2.  Go to **Settings** and download the **Windows Relay**.
3.  Run the Relay application while iRacing is open to start feeding data.

For detailed setup instructions, see [INSTALL.md](INSTALL.md).

---

## 🛠️ Architecture

*   **Frontend**: Vue 3 + TailwindCSS (Glassmorphism UI).
*   **Backend**: FastAPI (Python) + Supabase Edge Functions.
*   **Data**: Redis (Hot Telemetry) + Supabase (Relational Data).
*   **AI**: Gemini 2.5 Flash (via Secure Edge Function).

## 🔒 Security

*   **No Sensitive Keys Needed**: The application is built to run without you needing to manage API keys.
*   **Billing & AI**: Handled securely via serverless functions.
*   **Local-First**: Telemetry data flows from your Sim -> Your Local Docker Container. It is not sent to a central cloud unless you explicitly share it.

---

## 📄 License
GridLink is proprietary software.
