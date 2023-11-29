# QTQtPlot
This Jupyter notebook is designed to take the raw time-temperature (t-T) output file from the QTQt thermal history modelling software of [Gallagher (2012)](https://doi.org/10.1029/2011JB008825) and replot the output as an image displaying t-T path density. So in these plots, relative probability is proportional to t–T path density, where darker colors (or higher saturation) denotes higher posterior probability. Any t-T constraint boxes that were utilized during modelling can be plotted along with individual 'representative' model solutions (i.e., the maximum likehood or expected models). The example QTQt output file used here is from Figure 3a in [McDannell and Issler (2021)](https://doi.org/10.5194/gchron-3-321-2021). Please read the Jupyter plotting intructions.

Many thanks go to C. Brenhin Keller for code contributions.

## NOTE: Deep-time QTQt models with multiple thermochronometers over billion year+ time span(s): TLDR--run them for a long, long time. Convergence on the stable posterior is difficult to assess, so a rule of thumb would be 500k to 1M burn in iterations and >500k to >1M post burn in iterations. If you see 'multi-modal' behavior or bifurcation in thermal history solutions then you likely need to run QTQt longer.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kmcdannell/QTQtPlot.git/main?filepath=%2FQTQtPlot.ipynb)
