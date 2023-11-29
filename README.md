# QTQtPlot
This Jupyter notebook is designed to take the raw time-temperature (t-T) output file from the QTQt thermal history modelling software of [Gallagher (2012)](https://doi.org/10.1029/2011JB008825) and replot the output as an image displaying t-T path density. So in these plots, relative probability is proportional to t–T path density, where darker colors (or higher saturation) denotes higher posterior probability. Any t-T constraint boxes that were utilized during modelling can be plotted along with individual 'representative' model solutions (i.e., the maximum likehood or expected models). The example QTQt output file used here is from Figure 3a in [McDannell and Issler (2021)](https://doi.org/10.5194/gchron-3-321-2021). Many thanks go to Brenhin Keller for code contributions.

**Please read the Jupyter plotting instructions**

Right now the code only handles single samples and cannot deal with vertical sample profiles. The way QTQt does this internally is to plot the normal model posterior paths output (i.e., for the highest elevation sample) and then adds the model offset value (the value between each t-T pair in the main QTQt output file) to each Temp. value. This gives you the "hotter" or lower elevation sample.

_NOTE: Deep-time QTQt models with multiple thermochronometers over 500 My to billion year+ time span(s)--TLDR--run them for a long, long time._ 

_Convergence on the stable posterior is difficult to assess, so a rule of thumb would be 500k to 1M burn in iterations and >500k to >1M post burn in iterations. If you see 'multi-modal' t-T behavior, ragged-looking inflections or bifurcation in the thermal history solutions within a specific region(s) of t-T space (i.e., at a turning point between heating and cooling)---then you likely need to run QTQt longer._

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kmcdannell/QTQtPlot.git/main?filepath=%2FQTQtPlot.ipynb)
