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
