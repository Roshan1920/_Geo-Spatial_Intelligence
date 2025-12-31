# Clean Food Accessibility & Price Intelligence  
### Geospatial Analytics Project (Whitefield, Bengaluru)

## Overview
This project is a **geospatial data analytics system** designed to evaluate **clean food accessibility and affordability** across urban zones using spatial joins, distance modeling, and location-based aggregation.

The Phase-1 implementation focuses on **Whitefield, Bengaluru**, while the system architecture is intentionally designed to be **scalable across cities, zones, and domains** with minimal code changes.

---

## Objectives
- Quantify **physical accessibility** to clean food outlets
- Analyze **price distribution and affordability** by zone
- Identify **underserved areas** using spatial metrics
- Build a **config-driven foundation** that can scale to new geographies

---

## Key Metrics (KPIs)
- Nearest clean food store distance (km)
- Store density per 10,000 population
- Average normalized price index
- Composite accessibility score
- Underserved zone classification

Accessibility Score =
0.4 × normalized_distance +
0.4 × normalized_price +
0.2 × store_density

## Interactive Dashboard
🔗 Tableau Public:
https://public.tableau.com/shared/ZPW2R89Z8?:display_count=n&:origin=viz_share_link

---

## Data Sources
- **Administrative Boundaries:** BBMP Ward Boundaries
- **Store Locations:** OpenStreetMap (Overpass API)
- **Pricing Data:** Existing datasets + limited sampled data
- **Population Data:** Census / publicly available datasets

All datasets are **non-proprietary** and used for **directional analysis**, not transactional accuracy.

---

## Technology Stack

### Analytics & Geospatial
- Python
- pandas, geopandas, shapely, numpy
- folium (for sanity maps)

### Database
- Supabase (PostgreSQL)

### Visualization
- Tableau Public

### Development
- Google Colab (execution)
- GitHub (version control)



## Project Structure
```text
clean-food-geo-intelligence/
│
├── data/
│ ├── raw/
│ └── processed/
│
├── analytics/
│ ├── ingestion/
│ ├── spatial/
│ └── metrics/
│
├── config/
│ ├── project_config.yaml
│ └── weights.yaml
│
├── dashboard/
│
├── docs/
│ ├── assumptions.md
│ └── scalability_notes.md
│
├── notebooks/
│
└── README.md
```

## Design Principles
- **Configuration-driven logic** (no hardcoded geography)
- **Separation of concerns** (data, analytics, visualization)
- **Scalable spatial modeling**
- **Interview known limitations documented clearly**

---

## Assumptions & Limitations
- Pricing data is sampled and normalized
- Analysis is **comparative and directional**
- Not intended for real-time or transactional use
- Focus is strategic decision support

---

## Scalability & Future Scope
- Extend analysis to multiple Bengaluru zones
- Introduce scenario-based weighting (price-sensitive vs distance-sensitive)
- Integrate real transactional pricing data
- Expose results via API for downstream applications

---

## Author
Built as a technical geospatial analytics foundation project with a focus on **location intelligence, data modeling, and scalable analytics architecture**.
