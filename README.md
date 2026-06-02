# ⚡ EV Charging Station Finder

A web-based EV routing system that helps users find the nearest electric vehicle (EV) charging station and displays the shortest route using real road networks.

## 🚀 Features

* 🗺 Interactive map using Leaflet.js
* 📍 Click anywhere to set your location
* ⚡ Finds nearest EV charging station
* 🛣 Calculates shortest route using real road network (OSMNX + NetworkX)
* 📏 Displays distance to nearest station
* 🔄 Multiple EV charging locations (Islamabad demo dataset)
* 🌐 Flask backend API
* 🎯 Real-time route rendering on map

---

## 🛠 Tech Stack

**Frontend:**

* HTML
* CSS
* JavaScript

**Backend:**

* Python
* Flask


**Routing Engine:**
* OSMnx
* NetworkX


## 📂 Project Structure

```text
EV-Station-Routing-WebApp/
│
├── app.py                  # Flask backend
├── templates/
│   └── index.html         # Frontend map UI

``````

## ⚙️ How It Works

1. User clicks on the map
2. Frontend sends coordinates to Flask API
3. Backend:

   * Finds nearest EV station
   * Calculates shortest path using road network
4. Route is returned to frontend
5. Map displays route + distance

---

## ▶️ Run Locally

### Install dependencies

```bash
pip install flask osmnx networkx flask-cors
```

### Run backend

```bash
python app.py
```

###  Open in browser

```
http://127.0.0.1:8080
```

---

## 📡 API Endpoint

### Find nearest EV station

```http
GET /find_ev?lat={latitude}&lon={longitude}
```

### Response

```json
{
  "distance_meters": 1234.56,
  "route": [[lat, lon], ...],
  "nearest_ev": [lat, lon]
}
```

---

## ScreenShots
<img width="300" height="362" alt="image" src="https://github.com/user-attachments/assets/dc7ce0fb-56d6-43fc-98f5-8541292a9284" />
<img width="300" height="131" alt="image" src="https://github.com/user-attachments/assets/5d76e157-696e-4e51-86ce-85274c8c737a" />
<img width="300" height="368" alt="image" src="https://github.com/user-attachments/assets/493a7a71-e032-4b5a-b9ef-faea99348a94" />
<img width="710" height="486" alt="image" src="https://github.com/user-attachments/assets/f9ac780c-eb24-4d2e-ab7f-9ee887f30ff5" />

## 📍 Dataset

EV charging locations (Islamabad demo):

* F-8 Markaz
* Blue Area
* I-8 Markaz
* G-9 Markaz
* H-9 Sector
* F-10 Markaz
* G-6 Markaz
* I-9 Industrial Area
* G-11 Markaz
* H-8 Markaz
* E-11 Sector

---

## 🎯 Future Improvements

* Real-time EV availability
* Google Maps integration
* User authentication
* Mobile app version
* Live traffic-based routing

---

## 👨‍💻 Author

Muhammad Hamza Shahzad

---

## 📜 License

This project is for educational and learning purposes.
