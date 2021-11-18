# DTS-Complete-Streets
Repository for technical documentation and code related to DTS - Complete Streets Analysis

---

## Analysis Milestones

### 01 - 1986 ROW Table Conversion ###

Convert the original 1986 ROW table scan to a digital table and load it's attribute fields onto the current Honolulu street centerline GIS dataset.

*manual conversion*

link



### 02 - ROW Width Estimation ###

Estimate ROW width for all street segments in Honolulu county by calculating average parcel to parcel distances tangent to the street centerline.

*ArcGIS Pro Python Toolbox*

link

### 03 - Parking Estimation ###

Develop a high-level estimate of total on-street parking spaces for Honolulu County

*ArcGIS Pro Python Toolbox*

### 04a - Modal Composite ###

Load DTS Pedesrian Plan (modal composite 01) and Bike Plan (modal composite 02) datasets to the street centerline GIS dataset

*ArcGIS Pro Standalone Python Script - Jupyter Notebook*

### 04b - Modal Composite ##

1. Load attributes from ROW Estimate, 1986 ROW Conversion, and 2020 TransCAD data (modal composite 03) to the street centerline GIS dataset
2. Load attributes from 2040 TransCAD (modal composite 04) to the street centerline GIS dataset
3. Load attributes from Bus Transit Priority Network (modal composite 05) to the street centerline GIS dataset

*ArcGIS Pro Python Toolbox*

### 05 - Modal Width ### - *description*

### 06 - Street Typology Assignment ### - *description*

### 07 - Street Typology Overrides ### - *description*

### 08 - Modal Priortization ### - *description*
