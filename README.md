# Landslide-Susceptibility-Analysis

### Author: Maria Pinto

### Study Area: Near the border of Uganda and the Democratic Republic of the Congo, encompassing parts of the Albertine Rift and Rwenzori Mountains.
 
## Introduction
This report presents a landslide susceptibility analysis for a mountainous region known for its complex terrain and geological activity. The goal is to identify areas at risk of landslides to inform mitigation strategies and enhance public safety.

## Data and Methods

* Digital Elevation Model (DEM): A high-resolution DEM (N01E023.hgt) was used to represent the terrain's elevation.
* Slope Calculation:
  	* Rationale: Slope steepness directly affects the gravitational forces acting on a slope. Steeper slopes are generally more susceptible to landslides.
   * Method: Calculated using the gradient of the DEM and converting to degrees.
*	Aspect Calculation:
 	* Rationale: The orientation of slopes can influence moisture levels, vegetation, and weathering processes.
 	* Method: Determined using the arctangent of the gradient components, adjusted to compass directions.
* Curvature Calculation:
  * Rationale: Curvature indicates the shape of the slope (convex or concave). Convex slopes (positive curvature) are more prone to failures due to the outward bending of materials.
  * Method: Computed using second-order derivatives of the smoothed DEM.
•	Gaussian Smoothing:
o	Purpose: Applied to the DEM to reduce noise from minor terrain variations, enhancing the accuracy of curvature calculation.
o	Sigma Value: A sigma of 1 was chosen as a balance between smoothing out minor irregularities and retaining significant terrain features.

## Threshold Selection

* Slope Thresholds:
   * Values Tested: 5°, 10°, 15°, and 20°.
   * Justification: These values represent varying degrees of steepness, with higher values indicating steeper slopes. The selection allows for assessing how different slope angles influence susceptibility.
*	Curvature Thresholds:
    * Values Tested: -0.5, 0, 0.5, and 1.
    * Justification: Thresholds range from slightly concave to convex slopes. Positive curvature values indicate convexity, which is associated with higher landslide risk.
* Local Geology Consideration:
   * The region's geology consists of weathered rocks and soils susceptible to erosion and mass movement, especially on steeper, convex slopes.

## Results
*	Sensitivity Analysis:
    * Findings: As slope and curvature thresholds increase, the areas classified as susceptible decrease. This indicates that higher thresholds are more selective, identifying only the most at-risk areas.
    * Implications: Lower thresholds may over-predict susceptibility, while higher thresholds might under-predict, potentially missing some risk areas.
*	Visualization:
 Susceptibility maps generated for each threshold combination illustrate the spatial distribution of risk areas.

## Discussion
* Impact of Threshold Choices:
 The choice of thresholds significantly affects the analysis outcome. Therefore, selecting appropriate values is crucial and should be informed by local terrain characteristics and historical landslide data if available.

## Conclusion
The landslide susceptibility analysis provides a valuable tool for identifying potential risk areas in the mountainous regions near the Uganda-DRC border. By adjusting slope and curvature thresholds, the analysis can be tailored to different terrains, enhancing its applicability. Proper documentation and understanding of the methodology ensure that stakeholders can make informed decisions based on the results.
 


