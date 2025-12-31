# Climatic Analysis of Ecoregions of the United States

## Data sources used in this project:
The following data sources were extracted and merged for data exploration and machine learning work. <br>
[AWS Open Data Terrain Tiles](https://registry.opendata.aws/terrain-tiles) Elevation data <br>
[EPA Ecoregions Level I, II, and III](https://www.epa.gov/eco-research/ecoregions-north-america) <br>
[EPA Ecoregions Level IV](https://www.epa.gov/eco-research/level-iii-and-iv-ecoregions-continental-united-states) <br>
[Köppen-Geiger climate classification](https://www.cec.org/north-american-environmental-atlas/climate-zones-of-north-america/) <br>
[Open Plant Hardiness Zones](https://github.com/kgjenkins/ophz) <br>
[PRISM 30 year climate norms](https://prism.oregonstate.edu/normals/) All monthly 4km resolution climate norms<br>
[WWF Global 200 Ecoregions](https://globil-panda.opendata.arcgis.com/maps/panda::wwf-global-200-ecoregions/about) <br>

## Unsupervised Learning
Climatic features extracted from the above data sources and feature engineering resulted in approximately 160 total features and 460,000 locations within the Continental United States.  These features were placed into groups to prevent data redundancy and data was standardized.  PCA was used to reduce data dimensionality retaining 99% of the variance.  Data was subsampled per ecoregion to aid computation of UMAP and to balance highly unbalanced ecoregion categories.  Two-dimensional UMAP was then carried out on PCA reduced and subsampled data sets.  Features that retained the most defined groupings with UMAP were retained.  It was determined that raw climatic and elevation features were the most important in grouping ecoregions.  

## Select Unsupervised Learning Plots
<div align="center">
   <img src="docs/umap_ecoregions.png" width="600"><br>
   <em>UMAP of climatic features for EPA Level 1 Ecoregions.</em>
</div>
<br>

<div align="center">
   <img src="docs/umap_wwf_10common.png" width="600"><br>
   <em>UMAP of climatic features for WWF Ecoregions.</em>
</div>
<br>

<div align="center">
  <img src="docs/umap_arizona_ecoregions.png" width="600"><br>
  <em>UMAP of climatic features for Arizona WWF Ecoregions.</em>
</div>
<br>

<div align="center">
  <img src="docs/umap_arizona_level3_ecoregions.png" width="600"><br>
  <em>UMAP of climatic features for Arizona EPA Level 3 ecoregions.</em>
</div>
<br>

<div align="center">
  <img src="docs/umap_desert_level3_ecoregions.png" width="600"><br>
  <em>UMAP of climatic features for EPA Level 3 desert ecoregions.</em>
</div>
<br>
