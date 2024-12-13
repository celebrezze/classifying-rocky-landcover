# GitHub Repository: Classifying rocky land cover using random forest modeling

This repository hosts all necessary code (for R and GEE), data, and figures for the manuscript entitled 'Classifying rocky land cover using random forest modeling: lessons learned and potential applications in Washington, USA' authored by Joe V. Celebrezze, Okikiola Michael Alegbeleye, Doug A. Glavich, Lisa Shipley, and Arjan J.H. Meddens

------------------------

The repository is organized as follows:

**data**

This folder contains all of the data necessary to run analyses and make the figures associated with this manuscript.

It includes *GIS* data, which was visualized and used in QGIS for this project, as well as in GEE as the area of interest (aoi) and the points needed to run random forest models.
It also includes *point_bands* data, which - for each sub region and region - includes testing/training points (..._presence.csv) and the predictor values associated with those points (..._bands.csv).
Third, it includes *stability-analysis* data, derived from the stability_analysis GEE script (described below).
Lastly, it includes *varimp* data, which are compilations of variable importance for regional and subregional models (both *full* and *optimized*).

------------------------

**scripts**

This folder contains all *R* and *GEE* scripts that were used for analysis and visualization. Each script is described below:

*R*

1_variable_importance.Rmd: This visualizes and analyzes variable importance for the random forest models and includes code necessary for Figure 5 and Figure S2

2_points_bands.Rmd: This visualizes and analyzes predictor values for training/testing data, relying on *point_bands* data, and includes code necessary for Figure S1

3_breakpoint_optimization.Rmd: This uses segmented regressions to optimize the number of predictors included in random forest models using accuracy statistics. It includes code necessary for Figure 6 and Figure 7

4_stability_analysis.Rmd: The visualization for the stability analysis (Figure 11) went through many iterations. This script includes various ways of visualizing that data, saving them all in the *stability-plot* folder; therefore, it includes code necessary for Figure 11

*GEE*

main_random_forest: This was the script relied most heavily on, to prepare data and run random forest models in GEE

naip_random_forest: This was used for Case Study 1, where we sought to better define rocky land cover patch boundaries using high resolution NAIP data

stability_analysis: This was derived from a script from Stahl et al 2021, and it was used for Case Study 3

------------------------

**figures**

This folder contains all figures used in this manuscript, as well as a few extra figures or other iterations of figures

*from-R*: Various figures were made in R and are stored here

*from-pptx*: However, most figures were arranged in Microsoft Powerpoint and are stored here; these figures often required a combination of screenshots from QGIS and editing/text on Powerpoint. Consequently, for these figures to be replicable, one would need to pay careful attention about where to take screenshots and how to arrange figures. Note that many of these figures are either conceptual or are meant as an example; therefore, replicability is not as important as for the figures *from-R* or figures in a different manuscript.

------------------------

This repository was meant to store **all** necessary data, scripts, and figures for this manuscript, but we may have made mistakes! Feel free to reach out to celebrezze@ucsb.edu if you have any questions or concerns about the scripts, data, and/or figures or if you plan on using any of these things for a separate analysis or metanalysis.

This GitHub repository was written and is managed by *Joe Celebrezze* (celebrezze@ucsb.edu)