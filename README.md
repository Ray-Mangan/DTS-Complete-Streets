# DTS-Right-of-Way Widths for Planned Street Improvements
Repository for technical documentation and code related to DTS - Right-of-Way Widths for Planned Street Improvements project.

Note:
Input and output datasets are not included in this repository.

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

## Main Assumptions & Notes
1. This analysis builds upon and utilizes multiple datasets created by a wide range of sources. As such, this analysis inherits all assumptions from it's individual component inputs
2. The 2020 ROW width was estimated using the Honolulu TMK parcel dataset as it's main input, and the key assumption that distances between parcels on opposite sides of the street are suitably accurate for this analysis.
3. All GIS analysis was performed with ArcGIS Pro 2.6 and Python 3.6.

# Analysis Milestones

## 01 - 1986 ROW Table Conversion
Convert the original 1986 ROW table scan to a digital table and load it's attribute fields onto the current Honolulu street centerline GIS dataset.
- manual conversion
- [link](google.com)


## 02 - ROW Width Estimation
Estimate ROW width for all street segments in Honolulu county by calculating average parcel to parcel distances tangent to the street centerline.

- ArcGIS Pro Python Toolbox
- [link](www.google.com)


## 03 - Parking Estimation
Develop a high-level estimate of total on-street parking spaces for Honolulu County

- ArcGIS Pro Python Toolbox
- [link](google.com)

## 04a - Modal Composite - Episode 01
1. Load DTS Pedesrian Plan datset to the street centerline GIS Dataset to create *modal composite 01*
2. Load DTS Bike Plan datasets to the street centerline GIS dataset to create *modal composite 02*

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2004%20-%20Modal%20Composite.ipynb)


## 04b - Modal Composite - Episode 02

1. Load attributes from 2020 ROW Estimate, 1986 ROW Conversion, and TransCAD 2020 data to the street centerline GIS dataset to create *modal composite 03*
2. Load attributes from TransCAD 2040 to the street centerline GIS dataset to create *modal composite 04*
3. Load attributes from Bus Transit Priority Network to the street centerline GIS dataset to create *modal composite 05*

- ArcGIS Pro Python Toolbox
- [link](google.com)

## 05 - Modal Widths

Utilize all previously compiled attributes in *modal composite 05* in conjunction with standardized width parameters for elements in the street cross section to calcualte Unconstrained Modal Width, Area, and other metrics.

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](https://github.com/Ray-Mangan/DTS-Complete-Streets/blob/main/DTS%20-%2005%20-%20Modal%20Widths.ipynb)

## 06 - Street Typology Assignment

Utilzie all previously compiled attributes in *modal composite 05* to auto-assign Complete Street Types to street segments. To be used as a starting point for manual review by project team.

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 07 - Street Typology Overrides
Load manual over-rides for complete street types (assigned by project team) back to the main modal composite dataset

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 08 - Modal Priortization
Implement modal prioritization logic for street segments where Unconstrained Modal Width exceeds the currently available ROW width. Calculate Constrained Modal Width, Area, and other metrics

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 09 - Economic Justice & Sea Level Rise Exposure Area Analysis
Calculate metrics related to Economic Justice and Sea Level Rise Exposure Area

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 10 - Results Summary
Calculate final summary metrics

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)
