# The Data Behind Our Food

A data journalism project exploring the intersection of nutrition, sustainability, and the environmental cost of modern diets.

## 1. Project Objectives
### Primary Goal
To analyse how the foods we rely on for essential nutrition contribute to environmental impact (CO₂e, water use, land use, import distances), with a specific focus on the UK & EU context.

#### What You'll Show
- Which nutrients are the most carbon-intensive to obtain
- The hidden carbon footprint of a typical UK meal or diet
- How the UK’s reliance on imported foods affects environmental impact
- Trade-offs between nutritional density and environmental burden
- Actionable insights for consumers, policymakers, and businesses



## 2. Repository Structure

/the-data-behind-our-food
│
├── data/
│   ├── raw/
│   │   ├── cofid_uk.xlsx
│   │   ├── agribalyse_lca.csv
│   │   ├── uk_food_imports.csv
│   │   ├── faostat_data.csv
│   │   └── …
│   ├── processed/
│   │   ├── nutrition_clean.csv
│   │   ├── environment_clean.csv
│   │   └── combined_dataset.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploration.ipynb
│   ├── 03_analysis_env_vs_nutrition.ipynb
│   ├── 04_import_dependence.ipynb
│   ├── 05_visualisations.ipynb
│
├── src/  
│   ├── data_processing.py
│   ├── helpers.py
│   └── visualisation_tools.py
│
├── outputs/
│   ├── charts/
│   ├── tables/
│   └── final_story/
│       ├── story_assets/
│       ├── story_text.md
│       └── full_project_article.pdf
│
├── README.md
└── PROJECT_PLAN.md

## 3. 📥 Datasets & Data Sources

### UK/EU-focused dataset stack:
#### Nutrition Data
- CoFID (UK) — main dataset
- EFSA EU nutrient dataset (optional)
- myfood24 (optional branded food extension)

#### Environmental Impact
- Agribalyse (France/EU) — high-quality LCA food dataset
- eplca — European platform for LCA
- openLCA Nexus processes
- FAOSTAT emissions for specific food categories
- UK Gov GHG agricultural reports

Trade & Imports
- UK trade statistics (HMRC)
- Eurostat food import volumes
- FAOSTAT imports / exports

## 4. Step-by-Step Analysis Workflow
#### STEP 1 — Build the Combined Dataset

Create a single table containing:

| Food | Category | Calories | Protein | Carbs | Fat | Key minerals | CO₂e per kg | Water use | Land use | UK import % | Main import countries |

You will:
✔ clean CoFID
✔ clean Agribalyse
✔ map foods by name or create a lookup table
✔ join them
✔ add import % for context

Deliverable: combined_dataset.csv

STEP 2 — Exploratory Data Analysis

Questions to explore:

Nutritional perspective

Which foods give the most nutrients per kcal?

Which foods offer the highest nutrient-density index?

Environmental perspective

Which foods have the highest CO₂e per kg?

Which categories (meat, dairy, veg, grain) drive most emissions?

What is the relationship between protein source and emissions?

Nutrition vs CO₂ trade-offs

CO₂ per gram of protein

CO₂ per gram of fibre

CO₂ per mg of iron / B12 / Omega-3 (this will tell a story!)

Foods that are nutritionally poor but carbon expensive

Deliverables:

summary tables

scatter plots

correlation matrices

category comparisons

STEP 3 — Import Dependence Analysis

Show:

Which foods the UK imports most

Embodied carbon in imported foods

High-nutrition foods that rely heavily on imports

Seasonal variation opportunity

Deliverables:

bar charts of import reliance

a Sankey diagram (country → UK food supply)

map visual (import origins)

5. 🖼️ Visuals to Produce (Story-Ready)
Core Charts

CO₂ per gram of protein — food by food

Nutrient density vs environmental footprint (bubble chart)

“Breakfast CO₂”: The footprint of a typical UK breakfast

Foods imported the most by the UK

Sankey: How UK fruit/veg travel to your plate

Scatter: Land use vs CO₂ for common foods

Stacked chart: Emissions by food category

Visual Explanations / Journalism-style

These boost storytelling impact:

“How far your avocado travels” mini-diagram

Timeline of UK food import dependence over 20 years

“Which nutrients are hardest to get sustainably?” list/chart

Infographic: What 1 kg CO₂ buys you in nutrient terms