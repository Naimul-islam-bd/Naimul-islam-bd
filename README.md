# Naimul Islam

**Civil and Water Resources Engineer · Coastal WASH Delivery · Hydrological ML and Geospatial Research**

Dhaka, Bangladesh

[LinkedIn](https://www.linkedin.com/in/naimul-islam-bd) · [Email](mailto:naimul.islam.bangladesh@gmail.com) · Open to graduate research positions, consultancy engagements and research collaborations

---

## About

I am a Civil and Water Resources Engineer at Tetra Private Limited, delivering coastal water infrastructure and WASH services across six climate-vulnerable districts of southern Bangladesh (Khulna, Satkhira, Bagerhat) under IAP, Welthungerhilfe / German Humanitarian Assistance, BRAC, Aqua for All and IRC WASH programming. In 2025 I delivered the solar-powered community reverse-osmosis plant at Kulia, Debhata, Satkhira (BDT 36,94,372) single-handed from tender award through RCC civil works, a 7,020 W on-grid solar array, and a 1,500 GPD RO train on a 150 m deep tubewell, to two-year-warranty handover, and now prepare government and international-organisation tenders representing a bid portfolio above BDT 300 crore.

The other half of my week is research code. My portfolio spans spatiotemporal salinity dynamics for the Bay of Bengal delta, PFAS detection modelling on the U.S. EPA UCMR5 dataset (24,636 public water systems, 29 analytes, XGBoost under spatial-block cross-validation), physics-constrained transformer architectures for extreme flood peaks, compound flood-risk analysis under CMIP6 scenarios, geospatial multi-criteria analysis for climate-resilient solar siting, and community-based anticipatory action for last-mile early warning. I am available for graduate research positions (PhD, MASc), consultancy engagements, and research collaborations where hydrological machine learning, drinking-water source-quality forecasting, and climate-resilient water infrastructure can be drawn together, translating climate-model uncertainty into actionable infrastructure decisions for utility operators and resilience planners.

## Research Interests

- Climate-resilient water infrastructure in deltaic and coastal-vulnerable contexts
- Hydrological machine learning: transformer architectures, physics-informed neural networks, extreme-event prediction
- Drinking-water source-quality forecasting and PFAS occurrence modelling (U.S. EPA UCMR5)
- Compound flood risk and multi-driver hazard analysis under CMIP6 SSP2-4.5 / SSP5-8.5 scenarios
- Satellite remote sensing: Landsat, Sentinel-1 SAR, NDSI, LULC change detection
- Community-based anticipatory action and last-mile early-warning for humanitarian WASH
- Geospatial multi-criteria analysis for renewable energy siting and adaptation planning

## Featured Repositories

| Repository | Description | Stack |
|------------|-------------|-------|
| [**solar-pv-mcda-bangladesh**](https://github.com/Naimul-islam-bd/solar-pv-mcda-bangladesh) | Open-source Multi-Criteria Decision Analysis framework for climate-resilient utility-scale solar-PV siting. Two-scenario (1 km / 3 km buffer) identification of flood-free, cyclone-safe, grid-accessible sites: 688 premium and 6,777 candidate sites. | `geopandas` `shapely` `rasterio` |
| [**salinity-dynamics-bangladesh-2050**](https://github.com/Naimul-islam-bd/salinity-dynamics-bangladesh-2050) | 26-year Landsat NDSI reconstruction (667 scenes) with cyclone-event attribution and Random Forest projection of soil salinity through 2050 across Khulna, Satkhira and Bagerhat (R² = 0.496, +20.8% by 2050). Manuscript in preparation for ICSD 2026. | `gee` `scikit-learn` `geopandas` |
| [**pc-former-flood-forecasting**](https://github.com/Naimul-islam-bd/pc-former-flood-forecasting) | Physics-Constrained Transformer for extreme flood peak forecasting across CONUS. Benchmarked against CAMELS-US (671 basins) and CAMELSH (3,166 basins hourly). Target: Water Resources Research / Nature Water. | `PyTorch` `CAMELS` `NSE/KGE` |
| [**drinking-water-quality-lstm**](https://github.com/Naimul-islam-bd/drinking-water-quality-lstm) | LSTM forecast of Cedar River source-water turbidity (USGS NWIS), benchmarked honestly against persistence, climatology and seasonal-naive baselines. LSTM wins on turbidity (NSE 0.31 vs 0.06). | `PyTorch` `USGS NWIS` `NSE/KGE` |
| [**token-efficiency**](https://github.com/Naimul-islam-bd/token-efficiency) | A Claude skill that cuts token waste: lean replies, smart file reading, zero redundant work. | `Claude` `Anthropic` |

Additional repositories from the publication pipeline (PFAS-UCMR5 detection modelling, compound flood risk, community-based anticipatory action) are being prepared for release.

## Publications and Manuscripts

### Peer-reviewed conference publications

| # | Title | Venue | Year | Status |
|---|-------|-------|------|--------|
| 1 | Estimation of Changes in Ecosystem Service Values for a Mega Project of Nuclear Power Plant in Bangladesh | 9th International Conference on Water and Flood Management (ICWFM), BUET | 2023 | Published |

### Manuscripts in preparation

| # | Title | Target | Status |
|---|-------|--------|--------|
| 2 | Spatiotemporal Salinity Dynamics in Southwest Bangladesh (2000 to 2026): Cyclone Impacts, Seasonal Anomalies, and Random Forest Projections for Delta Governance | 8th International Conference on Sustainable Development (ICSD 2026), Dhaka | Finalising manuscript |
| 3 | Closing the Last-Mile Gap: Strengthening Community-Based Anticipatory Action for Flash Floods in Climate-Vulnerable Districts of Bangladesh | BMD and Save the Children National Conference on Weather, Climate Services and Anticipatory Action 2026 | Drafting |
| 4 | Geospatial Optimization of Climate-Resilient Solar Power Siting in Bangladesh: A Multi-Criteria Decision Analysis using Python | Journal submission pending | Preparing for submission |
| 5 | PFAS Detection in U.S. Drinking Water: A National Analysis of 24,636 Public Water Systems Using XGBoost with Spatial-Block Cross-Validation | Journal submission pending | Internal review draft |
| 6 | Future Compound Flood Risk Under Climate Change: A Global-Scale Assessment Integrating Triple Drivers Using Machine Learning | Natural Hazards and Earth System Sciences (NHESS) | Data collection |
| 7 | Physics-Constrained Transformer Architecture for Extreme Flood Peak Prediction: Breaking the Extrapolation Barrier in Data-Driven Hydrology | Water Resources Research / Nature Water | Data preparation |

## Technical Stack

**Programming and Data Science:** Python, NumPy, pandas, SciPy, xarray, Jupyter, R

**Hydrological Machine Learning:** PyTorch, scikit-learn, XGBoost, LSTM, Transformer, Physics-Informed Neural Networks, CAMELS-US, CAMELSH

**Geospatial and Remote Sensing:** GeoPandas, Rasterio, Shapely, Google Earth Engine, QGIS, ArcGIS

**Hydrological and Hydrodynamic Modelling:** MIKE 21 FM (DHI-certified), TUFLOW, HEC-HMS, Aquaveo SMS

**Climate Data:** CMIP6, ERA5, CHIRPS, GloFAS, GTSR

**Water Engineering:** Reverse Osmosis (brackish and sea-water), ETP, STP, iron and arsenic removal, solar-powered water systems, IoT water ATMs

## Consultancy Scope

Available for time-boxed consultancy engagements across Bangladesh and South Asia in:

- Water-infrastructure feasibility studies, design and commissioning support (reverse-osmosis, sea-water desalination, solar-powered community water systems, iron and arsenic removal)
- Tender preparation, technical specifications, Bills of Quantities and cost estimates for government and international-organisation contracts
- WASH programme design, inception-stage fieldwork, geo-tagged asset inventory, demand and willingness-to-pay surveys, water-quality testing to WHO limits
- Geospatial multi-criteria decision analysis for infrastructure siting under climate and flood risk (Python, GeoPandas, Google Earth Engine)
- Salinity and drinking-water-quality forecasting using Random Forest, LSTM and gradient-boosted models
- Ecosystem-service valuation and environmental impact assessment for large-infrastructure projects
- Donor-compliance and MEAL support under IAP, Welthungerhilfe, BRAC and UNICEF frameworks

## Currently

- Delivering the BRAC × Tetra three-year coastal water programme across Khulna, Satkhira, Bagerhat, alongside a competitive tender portfolio above BDT 300 crore with government (DPHE, LGED) and international-organisation (UNICEF, WHH, BRAC) clients
- Modelling PFAS detection across 24,636 U.S. public water-system locations with XGBoost under spatial-block and PWS-grouped cross-validation (UCMR5 working draft under internal review)
- Finalising the 2050 salinity-projection manuscript for ICSD 2026 (26-year Landsat time-series, Random Forest, late-monsoon anomaly detection)
- Drafting the last-mile anticipatory-action manuscript for the BMD and Save the Children 2026 conference (CHIRPS 1981 to 2024 pre-monsoon rainfall trend analysis)
- Preparing the global compound-flood-risk dataset (12.2 GB ERA5 1981 to 2019 plus GloFAS and GTSR ingestion pipeline, headed for NHESS)
- Drafting the Physics-Constrained Transformer benchmark against CAMELS-US (671 basins) and CAMELSH (3,166 basins hourly)
- Building the 3ZERO Club / 3Z Global Centre youth platform under Nobel Laureate Prof. Muhammad Yunus's global movement for zero carbon, zero poverty and zero unemployment, aligned with the UN SDGs

## Selected Certifications

MIKE 21 FM 2D Hydrodynamic Modelling (DHI Academy) · Responsible Business Conduct School (ILO and University of Dhaka) · Humanitarian WASH Coordination (UNICEF Agora) · Project DPro Essentials (PM4NGOs) · Managing Successful Field Research (World Bank IED) · Key Concepts of Project Management, PMBOK and PRINCE2 (IEB) · Practical Application of Generative AI for Project Managers (PMI)

## Memberships and Awards

American Society of Civil Engineers (ASCE) Student Member · American Concrete Institute (ACI) Student Member · Honorable Mention, ASCE Daniel W. Mead Prize 2022 (engineering ethics essay) · Runner-Up, Intra-CUET Eco Concrete Competition (fly-ash and silica-fume mix, 2.8x service life, 15.6% lower LCA impact)

## Get in Touch

I am open to:

- **Graduate research positions** (PhD, MASc) in climate-resilient water infrastructure, hydrological machine learning, drinking-water source-quality forecasting, PFAS occurrence modelling, and satellite environmental monitoring
- **Consultancy engagements** on water-infrastructure feasibility and delivery, tender preparation, WASH programme design, geospatial siting analysis, and salinity or water-quality forecasting across Bangladesh and South Asia
- **Research collaborations** on humanitarian WASH, decentralised water treatment, community-based anticipatory action, and last-mile early-warning programmes
- **Peer review, co-authorship and guest lectures** on hydrological ML, remote sensing and coastal water infrastructure

Contact:

- Email: naimul.islam.bangladesh@gmail.com
- LinkedIn: [linkedin.com/in/naimul-islam-bd](https://www.linkedin.com/in/naimul-islam-bd)
- Phone: +880 1771 707038

---

*This README is a living document, updated as repositories from the publication pipeline come online.*
