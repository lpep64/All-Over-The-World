# Personnel Accountability MVP

# Personnel Accountability MVP

## System Architecture

This project is a simulated personnel accountability system for demonstration and development purposes. It allows a manager to define a geographic area and time, then query simulated personnel nodes to report whether they were present in that area at that time.

- **Backend (Python/FastAPI):**

  - Simulates 10 employee nodes, each with a randomly generated silly name (including Impractical Jokers name game names).## Structure

  - Each node has a single current location (randomly generated).- **backend/**: Python FastAPI service simulating nodes and handling queries/responses

  - Provides API endpoints to query which nodes are inside a user-defined geographic area.- **frontend/**: React app with Leaflet map, area/time selection, and roster visualization

  - Returns only "Yes" or "No" for each node—never shares exact location.

  - No historical location or time-based logic; only current location is checked.## How it works

  - CORS enabled for frontend communication.1. Manager draws an area and selects a time on the map (frontend)

2. Frontend sends area/time to backend

- **Frontend (React/Leaflet):**3. Backend simulates message publishing to all nodes

  - Interactive map of the US for area selection (center + radius in km).4. Each node checks its historical location data and responds

  - Roster of 9 employees shown in a compact list with silly names and contact info.5. Frontend displays roster and node responses

  - User can select area and radius, then send a query to backend.

  - Responses update in real time, with a "Last updated" timestamp.## Quick Start Instructions

  - "Clear Responses" button resets the roster status.

### 1. Backend Setup

## Getting StartedOpen a terminal and run:



### 1. Backend Setup```powershell

```powershellcd backend

cd backendpip install -r requirements.txt

pip install -r requirements.txtpython -m uvicorn main:app --reload

python -m uvicorn main:app --reload```

```

Backend runs at: http://localhost:8000This will start the FastAPI backend server at `http://localhost:8000`.



### 2. Frontend Setup### 2. Frontend Setup

```powershellOpen a new terminal and run:

cd frontend

npm install```powershell

npm startcd frontend

```npm install

Frontend runs at: http://localhost:3000npm start

```

### 3. Usage

- Open http://localhost:3000 in your browser.This will start the React development server at `http://localhost:3000`.

- Draw/select an area on the map and set the radius (km).

- Click "Send Query" to see which employees are inside the area.### 3. Using the MVP

- View responses in the roster list below the map.- Open `http://localhost:3000` in your browser.

- Use "Clear Responses" to reset the roster status.- Draw an area on the map, select a time range, and click "Send Query".

- View live responses from simulated nodes in the roster below the map.

## Notes

- All data is simulated; no real employee/location data is used.## Note

- No employee location is ever revealed—only "Yes" or "No" for area presence.All data is simulated. No real employee/location data is used.

- Names are randomly generated and intentionally silly for demo purposes.

---