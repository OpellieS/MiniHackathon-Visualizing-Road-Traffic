# Development-of-an-Interactive-Map-for-Visualizing-Road-Traffic-Accidents-at-Chiang-Mai-University
An Interactive Map of Road Traffic Accidents at Chiang Mai University (Up to 2024)
🚗 Interactive Traffic Incident Dashboard
An advanced geospatial visualization tool that transforms raw traffic and accident data (CSV) into an interactive HTML dashboard. This project leverages Folium and Pandas to create layered maps with clustering, heatmaps, and custom data filtering.

✨ Key Features
🗺️ Interactive Layered Map: Toggle between different data views (Points, Heatmaps, Categories) using a built-in layer control.

🔥 Heatmap Visualization: Analyze high-density accident zones with an integrated Heatmap layer.

📍 Smart Clustering: Uses MarkerCluster to group nearby points, preventing map clutter at low zoom levels.

🎨 Dynamic Coloring: Automatically assigns distinct colors to different accident categories or time periods.

📝 Rich Popups: Click on any marker to see detailed information (Location, Vehicle Type, Date/Time, Description).

🏷️ On-Screen Legend: Features a custom HTML-based floating legend that explains the color coding dynamically.

🛠️ Tech Stack
Python: Core logic and data processing.

Pandas: Data cleaning, timestamp parsing, and filtering.

Folium: Map rendering and HTML generation.

Folium Plugins: HeatMap, MarkerCluster.

📂 Project Structure
Plaintext
.
├── carfinalkub.csv          # Input Dataset (Raw Data)
├── layered_dashboard_map.py # Main Python Script
├── car_map_dashboard.html   # Output (Generated Dashboard)
└── README.md                # Project Documentation
🚀 Getting Started
1. Prerequisites

Make sure you have Python installed, then install the required libraries:

Bash
pip install pandas folium
2. Configuration

Open layered_dashboard_map.py and adjust the configuration block at the top to match your dataset:

Python
# --------- Config ----------
CSV_PATH = Path("your_data_file.csv")  # Path to your CSV file
OUT_HTML = Path("output_map.html")     # Desired output filename
MAX_POINTS = 1000                      # Limit points for performance
HEATMAP_DEFAULT_VISIBLE = False        # Toggle heatmap visibility by default
# ---------------------------
3. Running the Dashboard

Execute the script to generate the HTML map:

Bash
python layered_dashboard_map.py
4. Viewing the Result

Open the generated .html file in any modern web browser (Chrome, Edge, Firefox, Safari) to interact with the map.

📊 Data Format
Your input CSV should ideally contain the following columns for the best experience:

Latitude & Longitude (Required)

detail_category (For color coding)

created_date & created_time (For time-based analysis)

detail (For popup descriptions)
