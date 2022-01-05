# DTS-Right-of-Way Widths for Planned Street Improvements
Repository for technical documentation and code related to DTS - Right-of-Way Widths for Planned Street Improvements project.

Note:
Input and output datasets are not included in this repository.

## Table of Contents
1. About the Project
2. How to use these files
3. Key Assumptions & Notes
5. Analysis Overview & Individual Milestones

## About The Project
The aim of this project is to develop a single, comprehensive, GIS dataset for Honolulu that include attributes and metrics from numerous other projects. 

Individual goals:

1) Estimate Existing ROW area
2) Compile multiple different GIS datasets, previously developed, into a single "modal composite" dataset
3) Assign Complete Street types to all street segments
4) Determine what streets may have ROW limitations if multiple improvements are being proposed
5) Develop a method to prioritize proposed facilities in areas where ROW limitations occur

## How to use these files
**Option 1** - Use GitHub Desktop to clone this repository to your local machine
1. Install GitHub Desktop client & create an account
2. Click the green "code" button on the top right of the repository main page
3. Select "Open with GitHub Desktop" from the dropdown menu
4. Using GitHub Desktop, clone this repository to the directory of your choice on your local machine.

**Option 2** - Fork this repository (create a copy of it) to your own GitHub account

**Option 3** - Manually download sources files (no notification of changes)
1. Click the green "code" button on the top right of the repository main page
2. Select "download ZIP" from the dropdown menu

## Key Assumptions & Notes
1. This analysis builds upon and utilizes multiple datasets created by a wide range of sources. As such, this analysis inherits all assumptions from it's individual component inputs
2. The 2020 ROW width was estimated using the Honolulu TMK parcel dataset as it's main input, and the **key assumption that distances between parcels on opposite sides of the street are suitably accurate** for this analysis.
3. All GIS analysis was performed with **ArcGIS Pro 2.6** and **Python 3.6**
4. Numerous geoprocessing routines in this project utilize arcpy functions which require an Advanced license level.
5. The final modal composite dataset for this project is a **static dataset**, and will need to be updated over time as the Honolulu Street Centerline geometry changes, tax parcels change, and new modal plans and datasets are developed.

## Analysis Overview

>*Convert 1986 ROW Table --> Estimate 2020 ROW --> Estimate Parking --> Create Composite Modal Dataset --> Calculate Current & Unconstrained Modal Widths --> Assign Complete Street Typologies --> Implement Modal Prioritization Logic & Constrained Modal Widths --> Calculate Economic Justice & Sea Level Rise Metrics --> Summarize Results*

### Please see Wiki--> Methodology for full technical documentation

### 01 - 1986 ROW Table Conversion
Convert the original 1986 ROW table scan to a digital table and load it's attribute fields onto the current Honolulu street centerline GIS dataset.
- manual conversion


### 02 - ROW Width Estimation
Estimate ROW width for all street segments in Honolulu county by calculating average parcel to parcel distances tangent to the street centerline.

- ArcGIS Pro Python Toolbox
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/ROW%20Tools.tbx)


### 03 - Parking Estimation
Develop a high-level estimate of total on-street parking spaces for Honolulu County

- ArcGIS Pro Python Toolbox
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/ROW%20Tools.tbx)

### 04a - Modal Composite Development - Step 1
1. Load DTS Pedestrian Plan dataset to the street centerline GIS Dataset to create *modal composite 01*
2. Load DTS Bike Plan datasets to the street centerline GIS dataset to create *modal composite 02*

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2004%20-%20Modal%20Composite.ipynb)


### 04b - Modal Composite Development Step 2

1. Load attributes from 2020 ROW Estimate, 1986 ROW Conversion, and TransCAD 2020 data to the street centerline GIS dataset to create *modal composite 03*
2. Load attributes from TransCAD 2040 to the street centerline GIS dataset to create *modal composite 04*
3. Load attributes from Bus Transit Priority Network to the street centerline GIS dataset to create *modal composite 05*

- ArcGIS Pro Python Toolbox
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/ROW%20Tools.tbx)

### 05 - Modal Widths

Utilize all previously compiled attributes in *modal composite 05* in conjunction with standardized width parameters for elements in the street cross section to calcualte Unconstrained Modal Width, Area, and other metrics.

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2005%20-%20Modal%20Widths.ipynb)

### 06 - Street Typology Assignment

Utilzie all previously compiled attributes in *modal composite 05* to auto-assign Complete Street Types to street segments. To be used as a starting point for manual review by project team.

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2006%20-%20Street%20Typologies.ipynb)

### 07 - Street Typology Overrides
Load manual over-rides for complete street types (assigned by project team) back to the main modal composite dataset

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2007%20-%20Street%20Typology%20Overrides.ipynb)

### 08 - Modal Prioritization
Implement modal prioritization logic for street segments where Unconstrained Modal Width exceeds the currently available ROW width. Calculate Constrained Modal Width, Area, and other metrics

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2008%20-%20Modal%20Prioritization.ipynb)

### 09 - Environmental Analysis
Calculate metrics related to Economic Justice and Sea Level Rise Exposure Area

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2009%20-%20Environmental%20Analysis.ipynb)

### 10 - Results Summary
Calculate final summary metrics

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2010%20-%20Results%20Summary.ipynb)

