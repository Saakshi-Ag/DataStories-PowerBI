# Evaluating the Economic Impact of Climate Policy through Emissions, Energy, and Taxation

**Author**: **Saakshi Agarwal**

## Overview

This project analyzes the relationship between climate policy, greenhouse gas (GHG) emissions, renewable energy adoption, and environmental taxation across selected OECD countries (United States, United Kingdom, Belgium, Portugal, and Lithuania) from 2016 to 2021.

By connecting environmental outcomes with policy effort, the dashboard offers insights into:
-How emissions evolved in the aftermath of the Paris Agreement (2015).
-The growth of renewable energy share and its link to emissions reductions.
-The role of environmental taxation in driving sustainability.
-The impact of the COVID-19 pandemic (2020) on global emissions and energy demand.

Data from **OECD Health Statistics** was cleaned, modeled, and visualized through an interactive **Power BI dashboard**. Despite minor OCR-related limitations during PDF exports, the dashboard provides robust insights across countries.

---

## Table of Contents

- [Dataset Overview](#dataset-overview)  
- [Data Preparation, Wrangling & Modeling](#data-preparation-wrangling--modeling)  
- [Visualization and Page Interpretations](#visualization-and-page-interpretations)  
- [Results](#results)  
- [Conclusions](#conclusions)  
- [Requirements](#requirements)  
- [Data Sources](#data-sources)  
- [License](#license)  
- [Acknowledgments](#acknowledgments)

---

## Dataset Overview

This project draws from **3 datasets** accessed via the **OECD Data Explorer**, covering **nly the selected OECD countries featured in the dashboard**(United States, United Kingdom, Belgium, Portugal, and Lithuania), not all 38 members. Key variables include:

### Emission Metrics
-Total GHG emissions (Mt CO₂-equivalent)
-Country-wise emissions (2016–2021)
-Sectoral emissions breakdown (Agriculture, Energy industries, Energy sector, Transport, Waste)

### Renewable Energy Metrics
-Renewable energy share (%) in total energy consumption
-Country-level renewable adoption trends (2016–2021)
-Linkages between renewable share and emission outcomes

### Environmental Policy Metrics
-Environmental tax revenue as % of GDP
-Country-level tax effort over time
-Sustainability scoring (combined indicator of emissions, renewables, and taxation)

> OCR-related issues affected some fields during Power BI PDF export, but core metric trends and country-level comparisons remain valid and insightful.

---

## Data Preparation, Wrangling & Modeling

A **high-quality, intensive data preparation process** was conducted entirely within **Power BI**, involving both automated and manual techniques to transform, cleanse, and model the data.

### Integration & Cleaning
- Combined multiple datasets using **country ISO codes** and **five-year benchmark intervals**.
- Standardized definitions and formats across disparate sources for consistency.

### High-Quality Imputation
- Missing values were handled using **benchmark-year-based logic**:
  - If data for a given year (e.g., 2005) was unavailable, values were **imputed from the next or previous benchmark year** (e.g., 2000 or 2010) based on temporal proximity and trend integrity.
- Used **if-then logic**, **pivot/unpivot transformations**, and **merge/append queries** to maintain structural consistency.

### Data Transformation.
- Standardized data units.
- Categorized and cleaned data enable cross-country comparisons.

### Star Schema Modeling
- Constructed a **robust star schema** to support dynamic, drill-down capabilities in Power BI:
  - **Fact Table**: Heart disease-related health outcomes by year and country
  - **Dimension Tables**: Country metadata, lifestyle factors, healthcare metrics, policy spending

### Validation
- Final values were compared against official OECD reports for accuracy.
- Anomalous entries flagged during OCR exports were reviewed manually and corrected when necessary.

> This rigorous data modeling approach enabled smooth, scalable dashboard functionality and ensured the integrity of analytical outputs across years and dimensions.

---

## Visualization and Page Interpretations

The **Power BI dashboard** consists of four core pages, each designed for thematic storytelling and analytical depth:

### Page 1: Project Overview
- Introduces the project context: the role of climate policy in shaping emissions, renewable adoption, and taxation outcomes.
- Highlights key focus areas: GHG emissions, renewable energy transition, and environmental policy tools.
- State data sources (OECD datasets) and study period (2016–2021

### Page 2: Emission Patterns
- Shows country-wise GHG emissions across five selected nations.
- Tracks emission trends over time (2016–2021), noting the dip in 2020 (COVID-19) and rebound in 2021.
- Breaks down emissions by sector (Agriculture, Energy industries, Energy sector, Transport, Waste).

### Page 3: Renewable Energy
- Displays the overall renewable share (%) across all countries.
- Tracks renewable adoption trends by year (2016–2021).
- Compares renewable shares by country (e.g., Lithuania leading, U.S. lagging).
- Explores the relationship between rising renewable shares and declining emissions.

### Page 4:  Environmental Policy in Action
- Examines environmental tax (% of GDP) across countries.
- Tracks policy effort over time and its link to renewable adoption.
- Visualizes policy effort vs. emission outcomes using bubble charts.
- Ranks countries by a Sustainability Score (Belgium highest, U.S. lowest).

**Note**: From **Page 2 to Page 4**, each dashboard page contains a **Fun Facts panel** (to highlight key takeaways) and a **Filter panel** (to customize views by country and year).

---

## Key Insights
- United States dominates emissions (~66,000 Mt CO₂-eq), over 90% of the total among selected nations.
- Emissions dipped in 2020, largely due to COVID-19’s effect on transport/industry, not permanent reforms.
- Renewable share rose steadily (avg. ~33.6% in 2016 → 41.3% in 2021), but adoption varies widely.
- Energy sector remains the biggest emitter, dwarfing Waste and Agriculture.
- Belgium and Portugal show consistent declines in emissions and stronger renewable adoption.
- Environmental tax effort: Belgium leads (>0.4% of GDP), U.S. lags far behind (<0.1%).
- Sustainability rankings: 1-> Belgium (70.1), 2-> Portugal (63.3), 3-> UK (63.1), 4-> Lithuania (60.2), 5-> USA (10.9)
---

## Conclusions

### Policy Implications

**1. Expand Renewable Adoption**: Greater alignment of U.S. with European efforts could significantly cut global emissions.

**2. Strengthen Tax Policy**: Higher environmental taxation correlates with stronger renewable adoption.

**3. Sustain Momentum Post-COVID**: Lockdowns temporarily reduced emissions; long-term reforms are needed.

**4. Sectoral Focus**: Energy and transport remain the most impactful levers for climate change mitigation

**2030 Targets**:

↓ Emissions by **20%** from 2016 levels.

↑ Renewable energy share above **50%**.

↑ Global environmental tax effort to **0.3–0.4**% of GDP.

---

## Requirements

### Tools Used
- **Power BI Desktop** (latest version)
- **Web scraping connectors within Power BI** (OECD public data portals)

### Hardware
- Recommended: **16 GB RAM**, modern CPU
- Minimum: **8 GB RAM**, 4-core CPU

---

## Data Sources

- [OECD Greenhouse Gas Emissions Dataset]([[https://www.oecd.org/health/](https://dataexplorer.oecd.org/)](https://dataexplorer.oecd.org/vispg=0&bp=true&snb=33&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_AIR_GHG%40DF_AIR_GHG&df[ag]=OECD.ENV.EPI&df[vs]=1.0&dq=.A.GHG..KG_CO2E_PS&pd=2014%2C&to[TIME_PERIOD]=false&isAvailabilityDisabled=false&hc[Measure]=&tm=Air%20emissions))
- [OECD Renewable Energy Consumption Dataset]([https://data.oecd.org/gga/general-government-spending.htm](https://dataexplorer.oecd.org/vispg=0&bp=true&snb=32&vw=tb&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_SDG%40DF_SDG&df[ag]=OECD.WISE.RSB&df[vs]=1.0&dq=..7_2%2B1_2..._T._T._T._T._T.&to[TIME_PERIOD]=false&lom=LASTNPERIODS&lo=5&isAvailabilityDisabled=false&hc[SDG%20goal]=&tm=Sustainable%20Development%20Goals))
- [OECD Environmental Tax Revenue Dataset]([https://sdgs.un.org/goals/goal3](https://dataexplorer.oecd.org/vispg=0&bp=true&snb=23&vw=tb&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_ERTR%40DF_ERTR&df[ag]=OECD.ENV.EPI&df[vs]=1.0&dq=A..TAXREV.CAT_ENE._T..&pd=2017%2C&to[TIME_PERIOD]=false&isAvailabilityDisabled=false&hc[Unit%20of%20measure]=&hc[Category%20of%20environmentally%20related%20tax%20revenue]=&tm=Environmentally%20related%20tax%20))

---

## License

This project is licensed under the **MIT License**.

---

## Acknowledgments

- Thanks to the **OECD** for making comprehensive health datasets publicly accessible.
- Developed as part of an academic and analytical exploration in public health and policy at the [University of Auckland](https://www.auckland.ac.nz/en.html).
