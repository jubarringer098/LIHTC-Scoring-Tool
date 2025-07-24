# LIHTC Scoring Tool

This repository contains the Streamlit-based scoring tool that computes and visualizes location-based scores for affordable housing developments in Georgia, based on the 2024 Qualified Allocation Plan (QAP) for Low-Income Housing Tax Credits (LIHTC).

Built on top of the core scoring engine in [aggregate_scoring](https://github.com/jubarringer098/LIHTC-Project), this interactive app allows users to enter a site location and view total and component scores across key QAP criteria, along with geospatial maps of opportunity across the Atlanta metro area.

---

## Features

- Site-based scoring for LIHTC developments using QAP logic
- Interactive maps with toggleable layers (Folium)
- Modular architecture powered by `aggregate_scoring`
- Built with Streamlit + streamlit-folium

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/jubarringer098/LIHTC-Scoring-Tool.git
cd LIHTC-Scoring-Tool
```
### 2. Create and Activate a Virtual Environment (optional but recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

Alternatively, you can install the requirements globally or use a tool like conda.

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## Run the App

```bash
streamlit run scoring_tool.py
```

This app will launch in your browser at `http://localhost:8501`.

## Project Structure
```
├── data/                              # All input data files (CSV, GeoJSON, shapefiles)
│   ├── community_transportation_options/   # Data used to compute community transportation scores
│   ├── desirable_undesirable_activities/   # Data used to compute desirable and undesirable activity scores
│   ├── maps/   # Data used to create the maps
│   ├── quality_education_areas/   # Data used to compute quality education scores#   
│   ├── shapefiles/                     # Shapefiles for geospatial data
│   └── stable_communities/ # Data used to compute stable communities scores
├── map_layers/                        # Map builder and styling scripts
│   ├── build_layers.py
│   ├── colours.py
│   └── maps/
│       └── location_score_map.html
├── scoring_tool.py                   # Main Streamlit app
├── requirements.txt                 # Python dependencies
└── README.md                        # Project documentation (you're here)
```

## Project Status

As of Summer 2025, this tool is being carried forward by Emory's student AI team for continued development and expanded impact.