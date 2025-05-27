# Ship Routing Optimizer  

## Overview  
A web app that optimizes ship routes in the Indian Ocean, focusing on fuel efficiency, travel time, and safety. It integrates environmental data to generate secure and efficient routes for various ship types.  

---

## Key Features  
- **Interactive Map**: Centered on the Indian Ocean with animated route visualization.  
- **Route Optimization**: Considers wave height, wind speed, currents, and other factors.  
- **Environmental Data**: Processes netCDF files for dynamic overlays.  
- **Ship Types**: Supports Passenger, Cargo, and Tanker ships.  
- **Additional Tools**: Weather overlays, location search, and 3D visualization.  

---

## Technologies  
### **Frontend**  
- **Frameworks**: Next.js, React, TypeScript  
- **Mapping**: Leaflet, React-Leaflet  
- **3D & Animation**: Three.js, Framer Motion  
- **Styling**: Tailwind CSS  
- **Utilities**: Lucide React, date-fns  

### **Backend**  
- **Framework**: Flask  
- **Libraries**: NumPy, SciPy, netCDF4, Numba  

---

## Setup  

1. Clone the repository

2. Install dependencies:  
   - **Frontend**:  
     ```bash  
     npm install  
     ```  
   - **Backend**:  
     ```bash  
     pip install flask flask-cors netCDF4 numpy scipy numba  
     ```  

3. Run the application:  
   - **Frontend**:  
     ```bash  
     npm run dev  
     ```  
   - **Backend**:  
     ```bash  
     python backend/app.py  
     ```  

4. Open [http://localhost:3000](http://localhost:3000) in your browser.  

---

## Usage  
1. Open the sidebar and select a ship type.  
2. Choose start and end ports via the map or search bar.  
3. Set the departure date and click **Calculate Optimal Route**.  
4. Visualize the route and toggle weather overlays as needed.  

---

## Route Optimization  
The backend uses the **Dijkstra algorithm** to optimize routes, considering:  
- Ship type and speed  
- Wave height, wind speed, currents, temperature, and salinity  

Environmental data is processed from netCDF files and interpolated onto a grid for precision.  

---

