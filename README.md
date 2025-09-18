
# Personnel Accountability MVP

## System Architecture

**Backend (Python/FastAPI):**
- Simulates 10 employee nodes, each with a randomly generated silly name (including Impractical Jokers name game names).
- Each node has a single current location (randomly generated).
- Provides API endpoints to query which nodes are inside a user-defined geographic area.
- Returns only "Yes" or "No" for each node—never shares exact location.
- No historical location or time-based logic; only current location is checked.
- CORS enabled for frontend communication.

**Frontend (React/Leaflet):**
- Interactive map of the US for area selection (center + radius in km).
- Roster of 9 employees shown in a compact list with silly names and contact info.
- User can select area and radius, then send a query to backend.
- Responses update in real time, with a "Last updated" timestamp.
- "Clear Responses" button resets the roster status.

## Getting Started

### 1. Backend Setup
Open a terminal and run:
```powershell
cd backend
pip install -r requirements.txt
python -m uvicorn main:app --reload
```
Backend runs at: http://localhost:8000

### 2. Frontend Setup
Open a new terminal and run:
```powershell
cd frontend
npm install
npm start
```
Frontend runs at: http://localhost:3000

### 3. Usage
- Open http://localhost:3000 in your browser.
- Draw/select an area on the map and set the radius (km).
- Click "Send Query" to see which employees are inside the area.
- View responses in the roster list below the map.
- Use "Clear Responses" to reset the roster status.

## Notes
- All data is simulated; no real employee/location data is used.
- No employee location is ever revealed—only "Yes" or "No" for area presence.
- Names are randomly generated and intentionally silly for demo purposes.

## Notes

- All data is simulated; no real employee/location data is used.## Note

- No employee location is ever revealed—only "Yes" or "No" for area presence.All data is simulated. No real employee/location data is used.

- Names are randomly generated and intentionally silly for demo purposes.

---