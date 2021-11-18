# DTS-Complete-Streets
Repository for technical documentation and code related to DTS - Complete Streets Analysis

## How to use these files
Option 1 - Use GitHub Desktop

Option 2 - Manually download sources files (no notification of changes)



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
1. Load DTS Pedesrian Plan datset to the street centerline GIS Dataset to create "modal composite 01"
2. Load DTS Bike Plan datasets to the street centerline GIS dataset to create "modal composite 02"

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)


## 04b - Modal Composite - Episode 02

1. Load attributes from ROW Estimate, 1986 ROW Conversion, and 2020 TransCAD data to the street centerline GIS dataset to create "modal composite 03"
2. Load attributes from 2040 TransCAD (modal composite 04) to the street centerline GIS dataset to create "modal composite 04"
3. Load attributes from Bus Transit Priority Network (modal composite 05) to the street centerline GIS dataset to create "modal composite 05"

- ArcGIS Pro Python Toolbox
- [link](google.com)

## 05 - Modal Widths

Utilize 

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 06 - Street Typology Assignment

Load DTS Pedesrian Plan (modal composite 01) and Bike Plan (modal composite 02) datasets to the street centerline GIS dataset

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 07 - Street Typology Overrides

Load DTS Pedesrian Plan (modal composite 01) and Bike Plan (modal composite 02) datasets to the street centerline GIS dataset

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)

## 08 - Modal Priortization

Load DTS Pedesrian Plan (modal composite 01) and Bike Plan (modal composite 02) datasets to the street centerline GIS dataset

- ArcGIS Pro Standalone Python Script (jupyter notebook)
- [link](google.com)
