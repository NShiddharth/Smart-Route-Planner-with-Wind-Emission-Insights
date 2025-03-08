# FEDEXhackathon

This Flask web application calculates the optimal route between two locations using the TomTom Routing API, estimates CO₂ emissions based on vehicle type, and fetches wind speed data using the Open-Meteo API.

Features

Fetch GPS coordinates of locations using the TomTom Geocoding API

Calculate optimal routes with distance, travel time, and route polyline

Estimate CO₂ emissions based on vehicle type

Fetch wind speed at the destination

User-friendly web interface


Tech Stack

Flask (Backend)

TomTom API (Geocoding & Routing)

Open-Meteo API (Weather data)

HTML, CSS, JavaScript (Frontend)


Setup Instructions

1. Clone the Repository

2. Install Dependencies

pip install flask requests

3. Set Up API Keys

Update the TOMTOM_API_KEY in app.py with your TomTom API key.

4. Run the Flask App

python app.py

The app will run on http://127.0.0.1:5000/

API Endpoints

1. Homepage

GET / → Loads the main webpage


2. Route Calculation

POST /route
Request Parameters:

origin: Starting location

destination: Ending location

vehicleType: Type of vehicle (car, truck, bus, motorcycle, bike)


Response:

{
  "success": true,
  "routes": [
    {
      "distance": 10.5,
      "travel_time": 15.2,
      "polyline": [[lat1, lon1], [lat2, lon2], ...],
      "emissions": 1260.0,
      "wind_speed": 5.2
    }
  ]
}


Future Enhancements

Add real-time traffic updates

Display map visualization of the route




