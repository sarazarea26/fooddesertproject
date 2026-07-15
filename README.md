# fooddesertproject

## Dataset Folder
Contains both the cleaned and original CSV files used throughout the project. Data sources include the CDC PLACES dataset, the American Community Survey (ACS), the Equal Justice Initiative (EJI), U.S. Census tract data, OpenStreetMap (OSM), and the USDA.

## Extra Figures Folder
Contains graphs, maps, and statistical models that were created during the data exploration phase to better understand the relationships within the dataset. 

## Final Figures Folder
Contains all final figures and tables from the visualisation and tables list from the Box Folder (see below) 

### Visualization List for Manuscript
MAPS (Core Contribution)
Figure 2: Urban farm locations by metro, layered onto the food desert maps from Figure 2. Same
5-panel small multiples format for direct comparability. Stars or points indicating farm locations,
with grow-and-give operations distinguished from in-scope farms.
Figure 3: Health outcomes choropleth maps showing the composite CDC PLACES health score
at the census tract level, one panel per metro. This is the novel layer beyond Avila et al.
Figure 4: Integrated map combining food desert classification, urban farm locations, and health
outcome quartiles for each metro. This is the hero figure of the paper, likely full-page.
STATISTICAL/ANALYTICAL FIGURES
Figure 5: Scatter plots showing bivariate relationships between distance to nearest urban farm
and composite health score by census tract, faceted by metro. This gives readers an intuitive look
at the correlational findings before the regression results.
Figure 6: Regression coefficient plot (dot-and-whisker) showing predictor coefficients and
confidence intervals from the primary model, whether OLS, spatial lag, or multilevel. Clean and
readable for a mixed methods/public health audience.
TABLES
Table 1: Descriptive statistics for all variables by county (median household income, vehicle
access, distance to grocery store, distance to urban farm, distance to farmers market, walkability,
age, composite health score).
Table 2: Correlation matrix of key predictors and the composite health outcome.
Table 3: Regression results table showing the full model, with a column each for OLS baseline,
spatial regression model, and multilevel model if all three are run. Lets reviewers compare model
specifications directly

## Urban Farm Data Folder
Includes all the code and datasets collected when collecting urban farm data. Because this process was complicated and included many components we put all of it in its own folder.
