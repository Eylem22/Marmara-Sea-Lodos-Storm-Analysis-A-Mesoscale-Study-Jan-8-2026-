#  Marmara Sea Lodos Storm Analysis: A Mesoscale Study (Jan 8, 2026)
Conducted a multi-scale meteorological analysis of the January 8, 2026 Lodos storm over the Marmara region using nested WRF simulations (9 km and 3 km) and ERA5 reanalysis data. Investigated wind dynamics across synoptic and mesoscale processes, including ageostrophic flow, surface friction effects, and topographic wind channeling through the Bosphorus and Dardanelles. Quantified vertical structure via Ekman spiral analysis and examined the relationship between boundary layer height and surface wind intensity. Integrated thermodynamic diagnostics such as warm air advection and applied numerical filtering techniques for robust visualization. The study highlights the role of coastal geometry and terrain in amplifying extreme wind events.
<img width="656" height="652" alt="image" src="https://github.com/user-attachments/assets/42c64c53-75da-434f-9edd-183317fcd995" />








```
Lodos_Storm_Analysis/
├── data/                      # Raw datasets (NetCDF format)
│   ├── era5_lodos_vaka.nc     # Synoptic verification data
│   ├── wrfout_d01...          # Parent domain (9km resolution)
│   └── wrfout_d02...          # Nested domain (3km resolution)
├── notebooks/                 # Analysis scripts
│   └── analysis.ipynb         # Full step-by-step meteorological study
├── visuals/                   # Exported plots and maps for documentation
└── README.md                  # Project overview and documentation
```

# Key Research Features

# 1. Horizontal Wind Dynamics & Friction
- Geostrophic vs. Real Wind: Analysis of ageostrophic components and the impact of surface friction on wind speed and direction.
- Topographic Channeling: High-resolution (3km) visualization of wind acceleration through the Dardanelles (Çanakkale) and Bosphorus straits.

# 2. Vertical Structure & Boundary Layer
- Ekman Spiral: Calculation of the vertical wind profile and deviation angles within the Planetary Boundary Layer (PBL).
- PBLH Correlation: Investigating the relationship between Boundary Layer Height and surface wind intensity.

# 3. Thermodynamic Analysis
- Temperature Advection (WAA): Quantification of Warm Air Advection (WAA) using MetPy's gradient calculations.
- Gaussian Smoothing: Implementation of numerical noise reduction techniques for cleaner synoptic-scale visualization.

# 4. Coastal Impact
- Wind Fetch: Analysis of the effective fetch length over the Aegean Sea and its contribution to storm surge potential in the Marmara Sea.

# Tech Stack & Libraries
- **Language:** Python 3.10+
- **Data Handling:** `xarray`, `netCDF4`
- **Meteorology:** `MetPy` (Calculations & Units)
- **Visualization:** `Cartopy` (Map projections), `Matplotlib`
- **Numerical Analysis:** `Scipy` (Gaussian Filtering)

# Dataset Information
The analysis is based on two primary datasets included in the `/data` directory:
- **WRF-ARW (d01 & d02):** 3km nested grid simulation outputs.
- **ERA5 Reanalysis:** Global climate data for synoptic-scale verification.

##  How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/Eylem22/Marmara-Sea-Lodos-Storm-Analysis-A-Mesoscale-Study-Jan-8-2026-
   cd Marmara-Sea-Lodos-Storm-Analysis-A-Mesoscale-Study-Jan-8-2026-
   cd Lodos_Storm_Analysis
   pip install xarray metpy cartopy scipy netcdf4 matplotlib
