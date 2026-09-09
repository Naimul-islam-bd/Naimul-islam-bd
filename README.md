# Naimul Islam

**Civil & Water Resources Engineer | Hydrology, Water Quality & Climate Risk**

Dhaka, Bangladesh

[LinkedIn](https://www.linkedin.com/in/naimul-islam-bd) · [Email](mailto:naimul.islam.bangladesh@gmail.com) · [ORCID](https://orcid.org/0009-0002-3442-8980)

I work on water and environmental problems where field observations, geospatial data, and computational modelling can help answer practical questions.

My research interests sit around **hydrologic extremes, water quality, coastal salinity, climate risk, remote sensing, and machine learning for water resources**. I am particularly interested in research that does not stop at prediction, but asks whether a model is reliable in space and time, whether it generalises to unseen events, and whether its output can support a real decision.

I am currently preparing for **PhD and research-assistant opportunities** in hydrology, water resources, environmental engineering, climate risk, and environmental data science.

---

## What I am trying to understand

My work has gradually moved toward one broad question:

> **How can we use environmental observations and machine learning to make better decisions under hydrologic and climate uncertainty?**

I approach this from several connected directions:

- **Hydrologic extremes:** rainfall thresholds, flash-flood forecasting, extreme-event prediction, and early warning
- **Water quality:** drinking-water source forecasting and PFAS occurrence modelling
- **Coastal systems:** salinity dynamics, cyclone impacts, and long-term environmental change in the Ganges-Brahmaputra-Meghna delta
- **Climate-resilient infrastructure:** spatial planning of water and energy infrastructure under hazard constraints
- **Remote sensing:** Landsat, Sentinel-1 SAR, Google Earth Engine, and spatial environmental analysis
- **Hydrologic machine learning:** Random Forest, XGBoost, LSTM, and ongoing work toward physics-constrained Transformer models
- **Decision support:** translating environmental predictions into thresholds, screening priorities, and infrastructure decisions

I am especially interested in joining a research group where I can contribute as a **research assistant while developing toward PhD-level research**.

---

# Research Projects

## 1. Flash-Flood Anticipatory Action in Sylhet, Bangladesh

**Rainfall trigger thresholds for flash-flood anticipatory action**

[Repository](https://github.com/Naimul-islam-bd/sylhet_flash_flood_aa)

This is my most developed work on hydrologic extremes and decision support.

I am studying whether rainfall accumulation can provide useful triggers for anticipatory action before flash floods in Sylhet. The analysis brings together long-term **CHIRPS and ERA5-Land rainfall records**, satellite flood mapping, exposure data, and event-based forecast verification.

The pipeline derives rainfall thresholds across different accumulation windows and seasons, then evaluates them using **POD, FAR, CSI, HSS, ETS and ROC/AUC**. Because rainfall and flood events are temporally dependent, the uncertainty analysis uses **block bootstrap confidence intervals** rather than treating every observation as independent.

The current manuscript also includes exposure and benefit-cost analysis, so the research moves from:

**rainfall → flood occurrence → forecast skill → exposed population → anticipatory action**

The repository contains a structured Python package, CLI pipeline stages, Google Earth Engine scripts, tests, manuscript materials, and reproducible outputs.

**What I learned from this project:** a useful forecast is not simply the model with the highest score. The threshold has to be interpretable, uncertainty has to be understood, and the result has to make sense for the decision that follows.

---

## 2. PFAS Occurrence in U.S. Drinking Water

**National-scale modelling of PFAS detection using UCMR5**

[Repository](https://github.com/Naimul-islam-bd/pfas-source-decoupling)

This project asks a more specific question than simply predicting PFAS:

> **Does proximity to local PFAS-relevant point sources add meaningful predictive information once broader water-system and regional structure is taken into account?**

The analysis uses the U.S. EPA **UCMR5** dataset together with facility and public-water-system information.

I built a modelling pipeline covering data cleaning, geolocation, facility-grade coordinate matching, source-distance and source-density features, feature assembly, XGBoost modelling, SHAP interpretation, and robustness analysis.

A major part of the work is validation. Ordinary random cross-validation can leak information between neighbouring water systems, so the analysis uses **spatially blocked and public-water-system-grouped validation**, including repeated 5-fold evaluation.

The result is not framed as “sources do not matter.” The narrower finding is that **nearest local point-source proximity adds relatively little predictive information beyond broader covariates in the tested framework**.

That distinction matters to me. I am interested in environmental ML where the modelling question is tied closely to the scientific question, and where the validation design can change the conclusion.

---

## 3. Salinity Dynamics in Southwest Bangladesh

**Remote sensing, cyclone impacts and Random Forest projection**

[Repository](https://github.com/Naimul-islam-bd/salinity-dynamics-bangladesh-2050)

This project focuses on **Khulna, Satkhira and Bagerhat**, where salinity is closely connected to coastal livelihoods, agriculture and water security.

I built a long-term Landsat-based workflow using **Google Earth Engine** to reconstruct surface salinity dynamics through an NDSI-based approach. The project combines the satellite time series with field electrical-conductivity measurements, cyclone-event analysis, seasonal anomaly detection, and Random Forest modelling.

The current analysis includes **667 cloud-free Landsat observations** and a field-validation dataset of **162 measurements**. The repository reports a Random Forest performance of approximately **R² = 0.496** and a projected domain-mean increase through 2050 under continuation of the observed regime.

One result that particularly interests me is the seasonal behaviour: the analysis identifies a **late-monsoon/August anomaly** that does not fit neatly into the common dry-season-only picture of salinity.

The project has pushed me toward a broader research interest in how **remote sensing, field measurements and statistical learning can be combined to understand environmental change in data-limited delta regions**.

---

## 4. Climate-Resilient Solar PV Siting in Bangladesh

**Geospatial Multi-Criteria Decision Analysis**

[Repository](https://github.com/Naimul-islam-bd/solar-pv-mcda-bangladesh)

This project looks at infrastructure planning from a spatial-risk perspective.

I developed a Python-based geospatial MCDA workflow combining **flood hazard, cyclone exposure, road-network accessibility and solar-resource information** to identify candidate locations for utility-scale solar PV deployment in Bangladesh.

The workflow uses **GeoPandas, Shapely and Rasterio**, with projected-coordinate processing for distance and area calculations.

Two accessibility scenarios are implemented: a stricter 1 km road-buffer scenario and a broader 3 km scenario. The repository reports 688 sites under the strict scenario and 6,777 under the relaxed scenario.

The important idea for me is not the site count itself. It is the structure of the decision problem: infrastructure should not be planned from resource availability alone when **flood and cyclone risk can change the long-term suitability of a site**.

---

## 5. Drinking-Water Source Quality Forecasting

**PyTorch LSTM using USGS NWIS data**

[Repository](https://github.com/Naimul-islam-bd/drinking-water-quality-lstm)

This is a smaller project, but it helped me think more carefully about what makes an environmental ML result trustworthy.

I used public **USGS NWIS** data from the Cedar River and built a multi-step LSTM forecasting pipeline for turbidity, dissolved oxygen and specific conductance.

The workflow includes chronological train/validation/test splitting, short-gap handling, training-only feature scaling, sliding-window sequence construction, PyTorch LSTM training, early stopping, comparison with persistence, climatology and seasonal-naive baselines, and RMSE, MAE, NSE and KGE evaluation.

For turbidity, the LSTM achieves an NSE of about **0.31**, compared with about **0.06 for persistence** on the reported test period.

But the model does not win everywhere. Dissolved oxygen is effectively tied with persistence, and specific conductance remains difficult to forecast.

I kept those results in the repository because I think that is an important part of research: **a model failing on one variable can be more informative than a polished claim that it works for everything.**

---

# Research in Progress

## Physics-Constrained Transformer for Extreme Flood Peaks

[Repository](https://github.com/Naimul-islam-bd/pc-former-flood-forecasting)

I am developing this project around a limitation I find important in hydrologic ML: models can perform well within the range represented in the training data while struggling with events beyond that range.

The planned framework combines a **Transformer architecture**, a water-balance constraint, an extreme-event-focused loss, and uncertainty estimation.

The current repository is still in the early development stage. The immediate work is establishing the baseline experiments before moving to the proposed architecture.

The longer-term question is:

> **Can physical constraints and a different sequence architecture improve extrapolation to extreme flood peaks rather than simply improve average prediction?**

---

## Southwest Bangladesh Salinity to 2100

[Repository](https://github.com/Naimul-islam-bd/sw-bangladesh-salinity-2100)

This is the longer-term extension of my coastal salinity work.

The planned framework combines remote sensing with **LSTM temporal modelling and XGBoost spatial modelling**, conditioned on **CMIP6 climate scenarios, IPCC AR6 sea-level rise and storm-surge events**.

The project is currently in development. I am treating it as a research framework rather than presenting the final 2100 projections as completed results.

The aim is to move from describing historical salinity change toward understanding how **compound climate drivers may reshape the spatial distribution of salinity across the southwest coastal zone**.

---

# Why Water Resources?

My engineering background is in civil and water resources engineering, but working on real water projects has made the research questions more concrete.

In practice, I have worked around coastal water infrastructure, WASH systems, reverse-osmosis treatment, solar-powered water systems, field operations and infrastructure planning in climate-vulnerable areas of Bangladesh.

That experience changed how I look at modelling.

A rainfall threshold is not only a statistical threshold if someone has to act on it.

A salinity map is not only a raster if communities depend on the water represented by that raster.

A water-quality forecast is not only an ML benchmark if a treatment operator has to decide what to do with the forecast.

This is the direction I want to take further through graduate research: **connecting environmental modelling with the decisions that the modelling is supposed to support.**

---

# Methods & Tools

### Programming & Data Science
`Python` · `NumPy` · `pandas` · `SciPy` · `xarray` · `Jupyter`

### Machine Learning
`PyTorch` · `scikit-learn` · `XGBoost` · `LSTM` · `Random Forest` · `SHAP`

### Geospatial & Remote Sensing
`GeoPandas` · `Shapely` · `Rasterio` · `Google Earth Engine` · `ArcGIS` · `QGIS`

### Hydrology & Environmental Data
`CAMELS-US` · `USGS NWIS` · `ERA5-Land` · `CHIRPS` · `GloFAS` · `CMIP6` · `Sentinel-1` · `Landsat`

### Hydrological / Hydraulic Modelling
`MIKE 21 FM` · `TUFLOW` · `HEC-HMS` · `Aquaveo SMS`

### Water Engineering
Reverse osmosis · desalination · solar-powered water systems · drinking-water treatment · WASH infrastructure

---

# What I Am Looking For

I am preparing for **PhD and research-assistant opportunities** where I can contribute to ongoing work in:

- hydrologic machine learning
- flood forecasting and extreme-event prediction
- climate risk and water resources
- drinking-water quality
- environmental data science
- coastal hydrology and salinity
- remote sensing for water and environmental systems
- physics-informed / physics-constrained machine learning
- early warning and decision-support systems

I am particularly interested in research groups where a graduate student is expected to do more than run models — to work with **data, assumptions, validation, uncertainty, code, and the physical meaning of the result**.

I would be glad to contribute to an existing project as a research assistant and grow that work into a PhD research direction.

---

# Selected Publication

**Islam, N.** (2023). *Estimation of Changes in Ecosystem Service Values for a Mega Project of Nuclear Power Plant in Bangladesh.* 9th International Conference on Water and Flood Management (ICWFM), BUET.

---

# Current Focus

Right now, I am working toward a research profile that connects three things:

**Water systems**  
**Computational methods**  
**Real-world climate risk**

The problems I want to work on are large enough to matter, but specific enough to test properly.

If your group works on hydrology, water quality, climate risk, environmental machine learning, or related water-resources problems, I would be interested in learning about the questions your lab is currently trying to solve.

---

# Contact

**Naimul Islam**  
Civil & Water Resources Engineer  
Dhaka, Bangladesh

Email: naimul.islam.bangladesh@gmail.com

[LinkedIn](https://www.linkedin.com/in/naimul-islam-bd) · [ORCID](https://orcid.org/0009-0002-3442-8980) · [GitHub](https://github.com/Naimul-islam-bd)

---

*This profile is a living research portfolio. Repositories are updated as analyses, manuscripts and experiments progress.*
