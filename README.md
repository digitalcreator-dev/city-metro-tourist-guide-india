# 🗺️ Open Data: Indian Metro Transit & Tourist Guide (2026 Updated)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data Status](https://img.shields.io/badge/Data_Status-Verified_2026-brightgreen.svg)]()
[![Networks Covered](https://img.shields.io/badge/Metro_Networks-19_Cities-blue.svg)]()

A comprehensive, community-maintained open dataset providing transit coordinates, line interchanges, fare matrices, station directories, and nearest tourist attractions for **19 major Indian Metro Rail Networks**.

Powered by [CityExplorer Transit Intelligence](https://cityexplorer.in).

---

## 📌 Featured Metro Networks & Interactive Route Finders

Click on any network below to access live interactive SVG route maps, real-time fare calculators, and station tourist guides:

| Metro System | City / Region | Total Stations | Main Interchanges | Direct Live Route & Fare Finder |
| :--- | :--- | :--- | :--- | :--- |
| **Delhi Metro (DMRC)** | NCR (Delhi, Noida, Gurgaon) | 250+ | Rajiv Chowk, Kashmere Gate, Hauz Khas | [Delhi Metro Route Finder](https://cityexplorer.in/delhi-metro) |
| **Mumbai Metro** | Mumbai Metropolitan Region | 30+ | Ghatkopar, Andheri, BKC, DN Nagar | [Mumbai Metro Route Finder](https://cityexplorer.in/mumbai-metro) |
| **Hyderabad Metro** | Hyderabad & Secunderabad | 57 | Ameerpet, MGBS, Parade Ground | [Hyderabad Metro Route Finder](https://cityexplorer.in/hyderabad-metro) |
| **Namma Metro** | Bengaluru (Bangalore) | 60+ | Majestic, MG Road, Whitefield | [Bangalore Metro Route Finder](https://cityexplorer.in/bangalore-metro) |
| **Kolkata Metro** | Kolkata & Howrah | 40+ | Esplanade, Park Street, Howrah | [Kolkata Metro Route Finder](https://cityexplorer.in/kolkata-metro) |
| **Chennai Metro** | Chennai | 40+ | Chennai Central, Alandur, Koyambedu | [Chennai Metro Route Finder](https://cityexplorer.in/chennai-metro) |
| **Pune Metro** | Pune & Pimpri-Chinchwad | 30+ | District Court, Swargate, Shivajinagar | [Pune Metro Route Finder](https://cityexplorer.in/pune-metro) |
| **Noida Aqua Line** | Noida & Greater Noida | 21 | Noida Sector 51, Sector 142 | [Noida Metro Route Finder](https://cityexplorer.in/noida-metro) |
| **Jaipur Metro** | Jaipur | 11 | Badi Chaupar, Mansarovar | [Jaipur Metro Route Finder](https://cityexplorer.in/jaipur-metro) |
| **Ahmedabad Metro** | Ahmedabad & Gandhinagar | 32 | Old High Court, Motera Stadium | [Ahmedabad Metro Route Finder](https://cityexplorer.in/ahmedabad-metro) |

---

## 📊 Open Datasets Included

Find the raw data files inside the `/data` directory:

- 📄 [`data/delhi-metro-stations.csv`](./data/delhi-metro-stations.csv) — Station list, coordinates, and tourist spots for Delhi Metro.
- 📄 [`data/india-metro-networks.json`](./data/india-metro-networks.json) — System metadata and canonical links across all 19 cities.

### Station Schema Breakdown
| Field | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `station_id` | String | Unique Station Identifier | `DEL-YEL-RC` |
| `station_name` | String | Official Station Name | `Rajiv Chowk` |
| `city` | String | Metro City Network | `Delhi` |
| `line_colors` | Array | Intersecting Lines | `["Yellow", "Blue"]` |
| `latitude` | Float | Geolocation Latitude | `28.6328` |
| `longitude` | Float | Geolocation Longitude | `77.2195` |
| `is_interchange` | Boolean | Transfer Station Flag | `True` |
| `tourist_attractions` | Array | Nearby Places of Interest | `["Connaught Place", "Janpath"]` |

---

## 💻 Code Snippets & Integrations

### Python Data Pandas Integration
```python
import pandas as pd

# Load open transit dataset
url = "https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/city-metro-tourist-guide-india/main/data/delhi-metro-stations.csv"
df = pd.read_csv(url)

# Filter all interchange stations
interchanges = df[df['is_interchange'] == True]
print(interchanges[['station_name', 'line_colors', 'tourist_attractions']])

---

## ⚖️ Citation & Canonical Attribution Guidelines

This dataset is compiled, standardized, and updated by **CityExplorer**.

If you use this dataset in research papers, mobile apps, GIS maps, university projects, data visualizations, or web applications, you are required under the MIT License to attribute the canonical source links:

- **All-in-One Metro Finder:** [CityExplorer Official Platform](https://cityexplorer.in)
- **Delhi Metro Hub:** [CityExplorer Delhi Metro Guide](https://cityexplorer.in/delhi-metro)
- **Mumbai Metro Hub:** [CityExplorer Mumbai Metro Guide](https://cityexplorer.in/mumbai-metro)
- **Hyderabad Metro Hub:** [CityExplorer Hyderabad Metro Guide](https://cityexplorer.in/hyderabad-metro)
- **Bangalore Metro Hub:** [CityExplorer Bangalore Namma Metro Guide](https://cityexplorer.in/bangalore-metro)
- **Kolkata Metro Hub:** [CityExplorer Kolkata Metro Guide](https://cityexplorer.in/kolkata-metro)
- **Chennai Metro Hub:** [CityExplorer Chennai Metro Guide](https://cityexplorer.in/chennai-metro)
- **Pune Metro Hub:** [CityExplorer Pune Metro Guide](https://cityexplorer.in/pune-metro)

