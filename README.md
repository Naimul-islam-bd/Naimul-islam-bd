<div align="center">

# Naimul Islam

**Civil & Water Resources Engineer**

Hydrology · Water Quality · Coastal Salinity · Climate Risk · Machine Learning for Water Resources

Dhaka, Bangladesh

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-1B3A5C?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/naimul-islam-bd)
[![Email](https://img.shields.io/badge/Email-Contact-1B3A5C?style=flat-square&logo=gmail&logoColor=white)](mailto:naimul.islam.bangladesh@gmail.com)
[![ORCID](https://img.shields.io/badge/ORCID-Profile-1B3A5C?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0002-3442-8980)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd)

</div>

---

I work on water and environmental problems where field observations, geospatial data, and computational modelling can help answer a practical question.

My research centres on hydrologic extremes, water quality, coastal salinity, climate risk, remote sensing, and machine learning for water resources. What interests me is not prediction on its own. It is whether a model holds up across space and time, whether it carries over to events it was never trained on, and whether its output can support a decision that someone actually has to make.

I am preparing for PhD and research-assistant opportunities in hydrology, water resources, environmental engineering, climate risk, and environmental data science.

> **The question behind the work:** how can environmental observations and machine learning support better decisions under hydrologic and climate uncertainty?

---

## Contents

- [Research directions](#research-directions)
- [Research projects](#research-projects)
- [Research in progress](#research-in-progress)
- [Why water resources](#why-water-resources)
- [Methods & tools](#methods--tools)
- [What I am looking for](#what-i-am-looking-for)
- [Publication](#publication)
- [Contact](#contact)

---

## Research directions

| Direction | What it covers |
|---|---|
| **Hydrologic extremes** | rainfall thresholds, flash-flood forecasting, extreme-event prediction, early warning |
| **Water quality** | drinking-water source forecasting, PFAS occurrence modelling |
| **Coastal systems** | salinity dynamics, cyclone impacts, long-term change in the Ganges-Brahmaputra-Meghna delta |
| **Climate-resilient infrastructure** | spatial planning of water and energy infrastructure under hazard constraints |
| **Remote sensing** | Landsat, Sentinel-1 SAR, Google Earth Engine, spatial environmental analysis |
| **Hydrologic machine learning** | Random Forest, XGBoost, LSTM, and work toward physics-constrained Transformers |
| **Decision support** | turning predictions into thresholds, screening priorities, and infrastructure choices |

---

## Research projects

| # | Project | Focus | Repository |
|---|---------|-------|:----------:|
| 1 | Flash-Flood Anticipatory Action, Sylhet | Rainfall triggers for early action | [link](https://github.com/Naimul-islam-bd/sylhet_flash_flood_aa) |
| 2 | PFAS Occurrence in U.S. Drinking Water | Do local sources add predictive signal? | [link](https://github.com/Naimul-islam-bd/pfas-source-decoupling) |
| 3 | Salinity Dynamics in Southwest Bangladesh | Remote sensing + Random Forest projection | [link](https://github.com/Naimul-islam-bd/salinity-dynamics-bangladesh-2050) |
| 4 | Climate-Resilient Solar PV Siting | Geospatial multi-criteria decision analysis | [link](https://github.com/Naimul-islam-bd/solar-pv-mcda-bangladesh) |
| 5 | Drinking-Water Source Quality Forecasting | PyTorch LSTM on USGS NWIS data | [link](https://github.com/Naimul-islam-bd/drinking-water-quality-lstm) |

<br>

### 1. Flash-Flood Anticipatory Action in Sylhet, Bangladesh

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/sylhet_flash_flood_aa)

**Rainfall trigger thresholds for anticipatory action.** This is my most developed work on hydrologic extremes and decision support.

The question is whether rainfall accumulation can give useful triggers for anticipatory action before a flash flood hits Sylhet. The analysis pulls together long-term CHIRPS and ERA5-Land rainfall records, satellite flood mapping, exposure data, and event-based forecast verification.

The pipeline derives rainfall thresholds across different accumulation windows and seasons, then scores them with POD, FAR, CSI, HSS, ETS and ROC/AUC. Rainfall and flood events are not independent from one day to the next, so the uncertainty analysis uses block-bootstrap confidence intervals rather than treating every observation as a fresh draw.

The manuscript also carries exposure and benefit-cost analysis, so the chain runs the whole way through:

`rainfall → flood occurrence → forecast skill → exposed population → anticipatory action`

The repository holds a structured Python package, CLI pipeline stages, Google Earth Engine scripts, tests, manuscript materials, and reproducible outputs.

The main thing this project taught me is that a useful forecast is not just the model with the highest score. The threshold has to be interpretable, the uncertainty has to be understood, and the result has to make sense for the decision that comes after it.

`CHIRPS` · `ERA5-Land` · `Google Earth Engine` · `Python` · `block bootstrap` · `forecast verification`

<br>

### 2. PFAS Occurrence in U.S. Drinking Water

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/pfas-source-decoupling)

**National-scale modelling of PFAS detection using UCMR5.** This one asks something narrower than "can we predict PFAS":

> Does proximity to local PFAS-relevant point sources add real predictive information once broader water-system and regional structure is already accounted for?

The analysis uses the U.S. EPA UCMR5 dataset together with facility and public-water-system information. I built the pipeline end to end: data cleaning, geolocation, facility-grade coordinate matching, source-distance and source-density features, feature assembly, XGBoost modelling, SHAP interpretation, and robustness checks.

A large part of the work is validation. Ordinary random cross-validation can leak information between neighbouring water systems, so the analysis uses spatially blocked and public-water-system-grouped validation, with repeated 5-fold evaluation.

The finding is not "sources do not matter." It is narrower: nearest local point-source proximity adds relatively little predictive information beyond the broader covariates, inside the framework I tested. That distinction is the part I care about. I am drawn to environmental ML where the modelling question stays tied to the scientific one, and where the validation design can change the answer.

`UCMR5` · `XGBoost` · `SHAP` · `spatial cross-validation` · `Python`

<br>

### 3. Salinity Dynamics in Southwest Bangladesh

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/salinity-dynamics-bangladesh-2050)

**Remote sensing, cyclone impacts and Random Forest projection.** This project covers Khulna, Satkhira and Bagerhat, where salinity is tied directly to coastal livelihoods, agriculture and water security.

I built a long-term Landsat workflow in Google Earth Engine to reconstruct surface salinity through an NDSI-based approach, then combined the satellite time series with field electrical-conductivity measurements, cyclone-event analysis, seasonal anomaly detection, and Random Forest modelling.

The current analysis rests on **667 cloud-free Landsat observations** and a field-validation set of **162 measurements**. The Random Forest reaches roughly **R² = 0.496**, with a projected domain-mean increase through 2050 if the observed regime continues.

The result I find most interesting is seasonal. The analysis picks up a late-monsoon / August anomaly that does not fit the usual dry-season-only picture of coastal salinity.

Working on it pushed me toward a wider interest in how remote sensing, field data and statistical learning can be combined to read environmental change in data-limited delta regions.

`Landsat` · `Google Earth Engine` · `NDSI` · `Random Forest` · `field validation`

<br>

### 4. Climate-Resilient Solar PV Siting in Bangladesh

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/solar-pv-mcda-bangladesh)

**Geospatial multi-criteria decision analysis.** Here the problem is infrastructure planning seen through spatial risk.

I built a Python geospatial MCDA workflow that combines flood hazard, cyclone exposure, road-network accessibility and solar-resource information to flag candidate sites for utility-scale solar PV in Bangladesh, using GeoPandas, Shapely and Rasterio with projected-coordinate processing for distance and area.

Two accessibility scenarios are built in: a stricter 1 km road-buffer case and a looser 3 km case. The workflow returns **688 sites** under the strict scenario and **6,777** under the relaxed one.

The point is not the site count. It is the shape of the decision: you should not plan infrastructure from resource availability alone when flood and cyclone risk can undo the long-term suitability of a site.

`GeoPandas` · `Shapely` · `Rasterio` · `MCDA` · `Python`

<br>

### 5. Drinking-Water Source Quality Forecasting

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/drinking-water-quality-lstm)

**PyTorch LSTM on USGS NWIS data.** A smaller project, but it sharpened how I think about what makes an environmental ML result trustworthy.

Using public USGS NWIS data from the Cedar River, I built a multi-step LSTM forecasting pipeline for turbidity, dissolved oxygen and specific conductance. The workflow covers chronological train/validation/test splits, short-gap handling, training-only feature scaling, sliding-window sequence construction, PyTorch LSTM training with early stopping, comparison against persistence, climatology and seasonal-naive baselines, and RMSE, MAE, NSE and KGE evaluation.

For turbidity the LSTM reaches an **NSE of about 0.31**, against about **0.06 for persistence** on the reported test period.

It does not win everywhere. Dissolved oxygen ends up effectively tied with persistence, and specific conductance stays hard to forecast. I left those results in the repository on purpose. A model that fails on one variable is often more informative than a clean claim that it works on all of them.

`PyTorch` · `LSTM` · `USGS NWIS` · `NSE / KGE` · `baseline comparison`

---

## Research in progress

### Physics-Constrained Transformer for Extreme Flood Peaks

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/pc-former-flood-forecasting)

I started this around a limitation I keep running into in hydrologic ML: a model can look strong inside the range it was trained on and still fall apart on events beyond that range.

The planned framework brings together a Transformer architecture, a water-balance constraint, an extreme-event-focused loss, and uncertainty estimation. The repository is still early. Right now the work is establishing the baseline experiments before moving to the proposed architecture.

> Can physical constraints and a different sequence architecture improve extrapolation to extreme flood peaks, rather than just improve average prediction?

<br>

### Southwest Bangladesh Salinity to 2100

[![Repository](https://img.shields.io/badge/Repository-View%20on%20GitHub-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd/sw-bangladesh-salinity-2100)

The longer-term extension of my coastal salinity work.

The planned framework pairs remote sensing with LSTM temporal modelling and XGBoost spatial modelling, conditioned on CMIP6 climate scenarios, IPCC AR6 sea-level rise and storm-surge events. It is still in development, and I treat it as a research framework rather than presenting 2100 projections as finished results.

The aim is to move from describing past salinity change toward understanding how compound climate drivers may reshape where salinity sits across the southwest coastal zone.

---

## Why water resources

My background is in civil and water resources engineering, but the research questions only became concrete once I worked on real projects. I have worked around coastal water infrastructure, WASH systems, reverse-osmosis treatment, solar-powered water systems, field operations and infrastructure planning in climate-vulnerable parts of Bangladesh.

That work changed how I read a model output. A rainfall threshold stops being just a number the moment someone has to act on it. A salinity raster is not an abstraction to the households drinking that water. A water-quality forecast is only a benchmark until a treatment operator has to decide what to do with it.

That is the direction I want to carry into graduate research: keeping environmental modelling connected to the decisions it is supposed to support.

---

## Methods & tools

**Programming & data science**

![Python](https://img.shields.io/badge/Python-1B3A5C?style=flat-square&logo=python&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-1B3A5C?style=flat-square&logo=numpy&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-1B3A5C?style=flat-square&logo=pandas&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-1B3A5C?style=flat-square&logo=scipy&logoColor=white) ![xarray](https://img.shields.io/badge/xarray-1B3A5C?style=flat-square) ![Jupyter](https://img.shields.io/badge/Jupyter-1B3A5C?style=flat-square&logo=jupyter&logoColor=white)

**Machine learning**

![PyTorch](https://img.shields.io/badge/PyTorch-1B3A5C?style=flat-square&logo=pytorch&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-1B3A5C?style=flat-square&logo=scikitlearn&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-1B3A5C?style=flat-square) ![LSTM](https://img.shields.io/badge/LSTM-1B3A5C?style=flat-square) ![Random Forest](https://img.shields.io/badge/Random%20Forest-1B3A5C?style=flat-square) ![SHAP](https://img.shields.io/badge/SHAP-1B3A5C?style=flat-square)

**Geospatial & remote sensing**

![GeoPandas](https://img.shields.io/badge/GeoPandas-1B3A5C?style=flat-square) ![Shapely](https://img.shields.io/badge/Shapely-1B3A5C?style=flat-square) ![Rasterio](https://img.shields.io/badge/Rasterio-1B3A5C?style=flat-square) ![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-1B3A5C?style=flat-square&logo=googleearthengine&logoColor=white) ![ArcGIS](https://img.shields.io/badge/ArcGIS-1B3A5C?style=flat-square) ![QGIS](https://img.shields.io/badge/QGIS-1B3A5C?style=flat-square&logo=qgis&logoColor=white)

**Hydrology & environmental data**

![CAMELS-US](https://img.shields.io/badge/CAMELS--US-1B3A5C?style=flat-square) ![USGS NWIS](https://img.shields.io/badge/USGS%20NWIS-1B3A5C?style=flat-square) ![ERA5-Land](https://img.shields.io/badge/ERA5--Land-1B3A5C?style=flat-square) ![CHIRPS](https://img.shields.io/badge/CHIRPS-1B3A5C?style=flat-square) ![GloFAS](https://img.shields.io/badge/GloFAS-1B3A5C?style=flat-square) ![CMIP6](https://img.shields.io/badge/CMIP6-1B3A5C?style=flat-square) ![Sentinel-1](https://img.shields.io/badge/Sentinel--1-1B3A5C?style=flat-square) ![Landsat](https://img.shields.io/badge/Landsat-1B3A5C?style=flat-square)

**Hydrological / hydraulic modelling**

![MIKE 21 FM](https://img.shields.io/badge/MIKE%2021%20FM-1B3A5C?style=flat-square) ![TUFLOW](https://img.shields.io/badge/TUFLOW-1B3A5C?style=flat-square) ![HEC-HMS](https://img.shields.io/badge/HEC--HMS-1B3A5C?style=flat-square) ![Aquaveo SMS](https://img.shields.io/badge/Aquaveo%20SMS-1B3A5C?style=flat-square)

**Water engineering**

Reverse osmosis · desalination · solar-powered water systems · drinking-water treatment · WASH infrastructure

---

## What I am looking for

I am looking for PhD and research-assistant positions where I can contribute to ongoing work in hydrologic machine learning, flood forecasting and extreme-event prediction, climate risk and water resources, drinking-water quality, environmental data science, coastal hydrology and salinity, remote sensing for water systems, physics-informed machine learning, and early-warning and decision-support systems.

What I want most is a group where a graduate student is expected to do more than run models: to work with the data, the assumptions, the validation, the uncertainty, the code, and the physical meaning of the result. I would be glad to join an existing project as a research assistant and grow that work into a PhD direction.

The problems I want to work on are large enough to matter and specific enough to test properly. If your group works on hydrology, water quality, climate risk, environmental machine learning, or related water-resources problems, I would like to hear about the questions your lab is trying to answer.

---

## Publication

**Islam, N.** (2023). *Estimation of Changes in Ecosystem Service Values for a Mega Project of Nuclear Power Plant in Bangladesh.* 9th International Conference on Water and Flood Management (ICWFM), BUET.

---

## Contact

<div align="center">

**Naimul Islam** · Civil & Water Resources Engineer · Dhaka, Bangladesh

[![Email](https://img.shields.io/badge/Email-naimul.islam.bangladesh@gmail.com-1B3A5C?style=flat-square&logo=gmail&logoColor=white)](mailto:naimul.islam.bangladesh@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-1B3A5C?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/naimul-islam-bd)
[![ORCID](https://img.shields.io/badge/ORCID-Profile-1B3A5C?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0002-3442-8980)
[![GitHub](https://img.shields.io/badge/GitHub-Naimul--islam--bd-1B3A5C?style=flat-square&logo=github&logoColor=white)](https://github.com/Naimul-islam-bd)

<sub>Repositories are updated as the analyses, manuscripts and experiments progress.</sub>

</div>
