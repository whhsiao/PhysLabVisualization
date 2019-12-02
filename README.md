# PhysLabVisualization
Here I present a module that helps to visualize the linear regression performed in 1st year physics lab

## Background
I have TAed the physics lab for first year college students across different disciplines for a couple of times. Very often I had to ask students to perform linear regressions so as to interpret data. On most occasions students analyze data using excel spreadsheet. From time to time I would show them the data I took using python plots. (I attached them in the repo as well for comparison.) 
Nevertheless, I couldn't do really much beyond asking them to plot straight lines. They are required to judge the goodness of the analysis, yet they may not have enough tools in the wheelhouse. Therefore I create this module to help students, or maybe TAs to visualize not only the fit but also the bound of certain level of confidence, say, 1-alpha.

## Description of the Module
In the module I construct a module ___LinearFitCom___ that helps us to visualize the linear fit of data pairs (x,y) as well as the (1-alpha) confidence interval bound based on the t statistics. In addition to the best fit line from simple least square fit I also plot two dashed lines, which provide a area enclosing estimators at the confidence level (1-alpha). 

The function takes 5 arguments: ___arr: xdata___, ___arr: ydata___, ___float: alpha___, ___str: h___, ___str: v___. The first two arguments of the function take the independent variable and the dependent variable in the form of lists/arrays respectively. The third argument is the type I error threshold value alpha. The last two arguments take the label on the horizontal and vertical axes.

This module then generates the linear model, the estimations of parameters and the confidence interval subject to the given _alpha_. All a user needs to do is to document 2 lists of data and do some processing before fitting.

### Examples:
In the following I present some examples from freshmen physics (referencing the Phys 122 course at _the University of Chicago_).
#### Electron deflection:
The first example presented here is the study of the deflection of an electron in electric field. The electron is accelerated horizontally with the potential ___Va___ and then in enters a region between 2 horizontally placed parallel plate capacitor. It can be shown the vertical displacement ___D___ is linearly proportional to vertical voltage Subscript ___Vd___. Here I plot the result for ___Va___=300 volt and two-tailed ___alpha___ = 0.01 (99% level of confidence).

![Mathematica version of D-Vd plot](https://github.com/whhsiao/PhysLabVisualization/blob/master/newDVdPlot.png)

#### RLC circuits:
The other two examples I present here are the linear relationships of ___XL, XC___ and ___omega___, ___1/omega___ in the context of RLC circuit. 

![Mathematica version of XL plot](https://github.com/whhsiao/PhysLabVisualization/blob/master/newXLPlot.png)

![Mathematica version of XL plot](https://github.com/whhsiao/PhysLabVisualization/blob/master/newXCPlot.png)

## More Developments
I consider extending this for multilinear regression or maybe making it to return a LinearModelFit module. To make it more accessible perhaps I will do a python version in the future. It may not help students that substantially immediately but I hope it can help some TAs to generate pretty plots when TAing labs.
