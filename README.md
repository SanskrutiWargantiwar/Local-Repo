💧 Water Quality Monitor Dashboard - Frontend Structure This repository contains the complete, responsive React frontend structure for the Water Quality Monitoring Dashboard, styled using Tailwind CSS. This work is 100% complete and ready for API integration by the backend team. Getting Started (Installation): 1. Pull the Latest Changes: git pull origin team-b 2. Navigate to the frontend directory: cd frontend 3. Install dependencies: npm install OR yarn install 4. Start the application: npm start OR yarn start (opens at http://localhost:3000)

API Integration Endpoints (Required Data Structure): The backend must return data in these exact JSON formats.

1. Real-Time Stats (Home Overview) Integration Point: src/pages/Dashboard.js Purpose: Populates the four main statistic cards.
[
  {"label": "pH", "value": "7.2", "status": "Normal"},
  {"label": "Turbidity", "value": "3 NTU", "status": "Safe"},
  {"label": "TDS", "value": "450 ppm", "status": "Normal"},
  {"label": "Temperature", "value": "24°C", "status": "Normal"}
]

2. Sensor Locations (Base Map & Table) Integration Point: src/components/MapComponent.js Purpose: Provides data for map markers (lat/lng) and the site table.
[
  {
    "id": 1,
    "name": "Intake Site A",
    "lat": 34.05,
    "lng": -118.25,
    "status": "Warning",
    "lastReading": "7.2 pH"
  }
]

3. Alert Thresholds (Settings Page) Endpoint: /api/v1/config/thresholds Method: POST / PUT Purpose: Required structure for saving threshold values.
{
  "phWarning": 7.8,
  "phCritical": 6.5,
  "turbidityWarning": 5,
  "turbidityCritical": 10,
  "tempCritical": 30
}

4. Historical Chart Data (pH Trend) Integration Point: src/components/PhLineChart.js Purpose: Provides time-series pH levels for chart visualization.
[
  {"time": "00:00", "pH": 7.2},
  {"time": "04:00", "pH": 7.0}
]

5. Alerts Data Integration Point: src/pages/Alerts.js Purpose: Provides data for the alerts feed.
[
  {
    "id": 1,
    "title": "High Turbidity Spike",
    "location": "Intake Site A",
    "time": "10:12 AM",
    "severity": "CRITICAL",
    "details": "Turbidity exceeded 15 NTU.",
    "acknowledged": false
  }
]
