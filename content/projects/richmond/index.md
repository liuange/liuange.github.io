---
title: "Identifying Rental Properties in Richmond, CA"
date: 2023-03-01
draft: false
project_tags: ["python", "pandas", "geospatial", "arcGIS"]
weight: 2
---

Community Land Trusts (CLTs) like Richmond LAND aim to address the affordable housing crisis through community-controlled land acquisition and housing development. CLTs have limited resources for parcel acquisition; therefore, it is important to understand the landscape of rental properties to inform Richmond LAND policy making decisions. We wanted to identify characteristics correlated with existing rentals

### Research Question

What characteristics -- community, demographic, and physical housing characteristics -- best predict whether a property is a rental in Richmond, CA?

### Data Sources

- Richmond LAND-provided parcel dataset, a combination of Richmond City Parcel Data, Rent Board Data, and organization data
- Census Tract demographic data
- Zillow API Parcel Data

### Methods

1. Limit dataset to Residential Parcels in Richmond using ArcGIS
2. Created geospatial variables/features such as zone, neighborhood identifiers, distance to Parks, Schools, and Toxic Waste Sites.
3. Created definition of "Rental Property" based on available characteristics:

- Landlord ID exists
- Site Address that does not match Owner Address, or
- Rent Board Status indicates Owner Occupied or Outside City Boundaries
- Number of Units Owned by Landlord less than a certain threshold

4. Linked parcels to ancillary variables: housing characteristics from Zillow, community infrastructure, and Census Tract demographics/income
5. Identified variables that differ between rental and owner-occupied
6. Calculate correlations and odds ratios between these variables using logistic regression

### Conclusions

Several characteristics stood out as statistical differentiators of rental vs. owner-occupied housing. Among the strongest were **[municipal zones](https://www.ci.richmond.ca.us/3379/Zoning-Ordinance)**: parcels located in commercial or medium-to-high density zones were more likely to contain rentals. Additionally, we identified five specific neighborhoods that were more likely to contain rental housing.

Demographic characteristics also were predictive of owner-occupied housing: typically these were in Census tracts with a higher white population and increased income.

---

This was a class project for CYPLAN 204c -
Analytic and Research Methods for Planners: Introduction to GIS and City Planning at UC Berkeley.
