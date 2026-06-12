# AgriVision

AgriVision is a precision agriculture prototype designed to deliver smart farm monitoring, real-time pest and nutrient analytics, and autonomous edge hardware onboarding. The application combines an interactive frontend dashboard with a backend architecture that supports zero-configuration edge device ingestion and dynamic PostgreSQL schema generation.

## Project Overview

AgriVision is built for modern agricultural operations that require:

- Real-time field mapping and boundary drawing
- Pest and weed detection through computer vision heatmaps
- Nutrient deficiency analysis and prescription suggestions
- Historical analytics for crop yield, irrigation, and fertilizer usage
- Responsive glassmorphic UI suitable for desktop and mobile
- Low-touch edge hardware onboarding with automatic backend schema creation

## Key Features

1. **Interactive Farm Dashboard**
   - Glassmorphic UI with responsive mobile layout
   - Bottom navigation for quick module access
   - Personalized login greeting with farmer name capture

2. **Automated Field Mapping**
   - Leaflet-powered map with draw/save field boundaries
   - GPS coordinate display with multiple area unit conversions
   - Multi-layer visibility toggles for coverage, pest, weed, and nutrient maps

3. **Pest & Nutrient Intelligence**
   - Spatial pest analytics and severity legends
   - Nutrient heatmap overlay and NPK index insights
   - Prescription matrix for targeted agronomic action

4. **Analytics & History**
   - Chart-driven yield and fertilizer trend visualization
   - Historical logging archive for seasonal performance review
   - Resource savings and efficiency gain indicators

5. **Edge Hardware Hookup**
   - Backend accepts machine node metadata from drones, irrigation units, and LoRaWAN nodes
   - New device types and metrics are inspected automatically
   - PostgreSQL tables are created or altered dynamically based on incoming metadata
   - No manual database schema changes are required for most hardware additions

## Technical Stack

- **Frontend:** HTML, CSS, JavaScript, Leaflet, Chart.js
- **Backend (Prototype Goal):** FastAPI, SQLAlchemy, PostgreSQL
- **Data Flow:** REST / MQTT / WebSocket edge ingestion with secure token validation
- **Design:** Native Vanilla JS, hardware-accelerated transforms, responsive CSS3

## Hardware Integration

When hardware is connected to the AgriVision ecosystem, the backend is designed to automatically form and configure itself by linking the hardware payload to the dynamic ingestion pipeline.

- Inspect the incoming JSON metadata payload from the node
- Validate secure token authentication
- Determine whether the device type already exists
- Create or alter the PostgreSQL schema dynamically for the new device metrics
- Persist device metadata without requiring additional configuration
- Automatically generate backend tables and schema definitions as soon as hardware registers

**Example payload:**

```json
{
  "device_id": "UAV_99",
  "device_type": "sprayer",
  "metrics": {
    "liquid_level_pct": "float",
    "lidar_altitude_m": "float"
  }
}
```

This makes AgriVision hardware-ready and flexible for future IoT expansions.

## Installation & Usage

1. Clone or download the repository.
2. Open `agrivision.html` in a browser to preview the frontend prototype.
3. For backend integration, implement the FastAPI schema listener and connect PostgreSQL.
4. Secure edge payload ingestion with bearer token authentication.
5. Link edge hardware to the system and verify automatic schema creation.

## Team Members

1. **Aditya Raj Chourasiya**
   - Role: Backend & Cloud Systems
   - Responsibility: Data ingestion, database pipeline, server-side reliability

2. **Kaushlendra Singh**
   - Role: AI & IoT Architecture Lead
   - Responsibility: Edge device architecture, backend design, system integration

3. **Shruti Chauhan**
   - Role: Frontend Engine Design
   - Responsibility: UI/UX, interactive dashboard design, responsive experience

   

## Contact

- Email: updated soon
- Location: Updated soon


