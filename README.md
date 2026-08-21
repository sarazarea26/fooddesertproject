# fooddesertproject

## Dataset Folder
Contains both the cleaned and original CSV files used throughout the project. Data sources include the CDC PLACES dataset, the American Community Survey (ACS), the Equal Justice Initiative (EJI), U.S. Census tract data, OpenStreetMap (OSM), and the USDA.

## Extra Figures Folder
Contains graphs, maps, and statistical models that were created during the data exploration phase to better understand the relationships within the dataset. 

## Final Figures Folder
Contains all final figures and tables from the visualisation and tables list from the Box Folder (see below) 

### Visualization List for Manuscript
MAPS (Core Contribution)

#### Figure 2: 
Urban farm locations by metro, layered onto the food desert maps from Figure 2. Same 5-panel small multiples format for direct comparability. Stars or points indicating farm locations, with grow-and-give operations distinguished from in-scope farms.

#### Figure 3: 
Health outcomes choropleth maps showing the composite CDC PLACES health score at the census tract level, one panel per metro. This is the novel layer beyond Avila et al.

#### Figure 4: 
Integrated map combining food desert classification, urban farm locations, and health outcome quartiles for each metro. This is the hero figure of the paper, likely full-page.

STATISTICAL/ANALYTICAL FIGURES

#### Figure 5: 
Scatter plots showing bivariate relationships between distance to nearest urban farm and composite health score by census tract, faceted by metro. This gives readers an intuitive look at the correlational findings before the regression results.

TABLES

#### Table 1: 
Descriptive statistics for all variables by county (median household income, vehicle access, distance to grocery store, distance to urban farm, distance to farmers market, walkability, age, composite health score).

#### Table 2: 
Correlation matrix of key predictors and the composite health outcome.

#### Table 3: 
Regression results table showing the full model, with a column each for OLS baseline, spatial regression model, and multilevel model if all three are run. Lets reviewers compare model specifications directly

## Urban Farm Data Folder
Contains all datasets, scripts, and documentation related to the collection and processing of urban farm data

## Contributions

### Brandon Kung
- [Web-scraped](urbanFarmData/local_harvest_geocoded/scrapingLocalHarvest.ipynb) / gathered farm site data from LocalHarvest, Dallas urban farm maps, USDA/Texas Center for Local Food Directories, other county local org lists
- Assisted filtering of farm sites using county shapefile joins/manual web-based verification based on scope criteria (grows staple produce, generates revenue from sales)
- [Merged](extra_figures/modeling_data/assembling_df.ipynb) final urban farm site dataset, health outcomes and walkability index from CDC Environmental Justice Index, and American Community Survey (ACS) control variables
- [Generated](final_figures/Table_2/exploratory_visualization.ipynb) several pre-model figures, including summary statistics, correlation matrices, bivariate scatterplots, Local Indicators of Spatial Association [(LISA)](https://smu.box.com/s/k42bbdqho5serps2vbg5xjjrtbmz1ta1) maps
- [Ran spatial regression models](final_figures/Table_3/specifying_model.ipynb), testing different specifications and fitting final Spatial Durbin Models

### Charlotte Lin
- [Sourced and cleaned](datasets/cleaned/snap_data) grocery store location data from the USDA SNAP-Eligible Retailer Locator, manually verifying ambiguous retailers to ensure the final dataset accurately represented produce access.
- [Generated](datasets/cleaned/health_income_composite_score) census tract–level composite health risk and income/mobility indices by combining CDC diabetes and coronary heart disease prevalence with ACS median income and vehicle access data.
- [Collected, merged, and geocoded](urbanFarmData) urban farm location data from the [Google Places API](urbanFarmData/google_maps_api) and [OpenStreetMap](urbanFarmData/osm_data) using Python, producing a cleaned dataset for spatial analysis and mapping.
- [Created](final_figures) three core project figures in Python, including [grocery store and urban farm distribution maps](final_figures/Figure_2), [health risk choropleths](final_figures/Figure_3), and [bivariate maps](final_figures/Figure_5)
- [Ran](final_figures/Global_Moran) Global Moran's I analyses to assess spatial autocorrelation in diabetes prevalence and distance to urban farms.

### Sara Zarea
-  Created exploratory choropleth and bivariate maps to investigate relationships among urban farms, grocery access, health outcomes, and socioeconomic indicators across the five major metropolitan Texas counties: [Bexar](not_used/heat_maps/bexar_county/bexar_heat_maps.ipynb), [Dallas](not_used/heat_maps/dallas_county/dallas_heat_maps.ipynb), [Harris](not_used/heat_maps/harris_county/harris_county_heat_maps.ipynb), [Tarrant](not_used/heat_maps/tarrant_county/tarrant_heat_maps_updated.ipynb), and [Travis](not_used/heat_maps/travis_county/travis_heat_maps.ipynb).
- Created [binary maps](extra_figures/binary_maps) for each county to visualize geographic overlap between urban farm access and socioeconomic, health, and food-access indicators.
- Developed an [LLM-assisted workflow](urbanFarmData/webscraping/updated.ipynb) to identify, classify, and verify urban farms using publicly available data sources.
- Constructed [population density and urban farm maps for Harris County](final_figures/Figure_4/combined_mapping.ipynb) to examine potential geographic patterns in food access and resource distribution.
- Implemented spatial autocorrelation analyses using [manual Global Moran's I](extra_figures/modeling_data/global_moran_plots/manual_global_moran.ipynb), [Global Moran's I](extra_figures/modeling_data/global_moran_plots/global_moran.ipynb), [Global Moran's I and correlogram analyses](extra_figures/modeling_data/global_moran_plots/global_moran_correlograms.ipynb), and [spatial correlograms](extra_figures/modeling_data/global_moran_plots/correlograms_notebook_final.ipynb) to evaluate spatial dependence and inform model selection.
