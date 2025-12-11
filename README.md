# 💧 Water Quality Monitor Dashboard - Frontend Structure

This repository contains the complete, responsive React frontend structure for the Water Quality Monitoring Dashboard, styled using Tailwind CSS. This work is 100% complete and ready for API integration by the backend team.

---

## 💻 Getting Started (Installation)

1.  **Pull the Latest Changes:**
    *(Before starting development, ensure you have your teammate's latest code.)*
    ```bash
    git pull origin team-b
    ```

2.  **Navigate to the Frontend Directory:**
    ```bash
    cd frontend
    ```

3.  **Install dependencies:**
    This command installs all necessary packages (React Icons, Recharts, etc.).
    ```bash
    npm install 
    # OR
    yarn install
    ```

4.  **Start the application:**
    ```bash
    npm start
    # OR
    yarn start
    ```
    The application will open in your browser, usually at `http://localhost:3000`.

---

## 🔗 API Integration Endpoints (Required Data Structure)

The backend team must ensure their API endpoints return data in these precise JSON formats to integrate with the existing frontend components.

### 1. Real-Time Stats (Home Overview)

**Integration Point:** `src/pages/Dashboard.js`
**Purpose:** Populates the four main statistic cards.

```json
[
  {"label": "pH", "value": "7.2", "status": "Normal"},
  {"label": "Turbidity", "value": "3 NTU", "status": "Safe"},
  {"label": "TDS", "value": "450 ppm", "status": "Normal"},
  {"label": "Temperature", "value": "24°C", "status": "Normal"}
]

2. Sensor Locations (Base Map & Table)
Integration Point: src/components/MapComponent.js Purpose: Provides data for map markers (lat/lng) and the site table.
