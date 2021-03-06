# DABEST-Matlab

## About

DABEST is a data analysis tool that is intended to make estimation statistics more accessible to scientific communities. Estimation statistics is a superior alternative to null hypothesis significance testing (NHST), in which effect size and confidence intervals are used to interpret results as opposed to dichotomous significance testing.
 
This code allows the user to visualize the data as scatterplots; calculates the effect size and confidence intervals of the difference between multiple groups; and plots the results on the same figure. This figure design allows for a visual inspection of the observed values distribution, and displays the differences between multiple groups of data.

## Installation

DABEST-Matlab can be installed via MATLAB Central (https://www.mathworks.com/matlabcentral/fileexchange/65260-dabest-matlab) or GitHub (how to clone a repo: https://help.github.com/articles/cloning-a-repository/).

## Tutorial

### Data format

Data should be in *the csv file format* and contain two columns with the headers: *Identifiers* and *Values*.

*Identifiers* are the labels of each data point, and *Values* are the data points (see the example below).

![](https://github.com/ttumkaya/ContrastPlot_MATLAB/blob/master/SampleData/DataFormat.png)

*Note: All the sample data used in this tutorial are taken from S. Champely's  [anscombe2](https://www.rdocumentation.org/packages/PairedData/versions/0.9.9/topics/anscombe2) dataset, and can be found in DABEST-Matlab/SampleData/*.

Depending on the number of groups the data contain, the main function *dabest* produces various plots:

### 1. Two groups

If the data have two different groups, `dabest('TwoGroups_sample.csv')` generates a *two groups* plot.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/IndividualGroups/TwoGroups_sample.png)

### 2. Paired

Running `dabest('TwoGroups_sample.csv','Paired')` generates a *paired* plot with the two groups data.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/IndividualGroups/TwoGroupsPaired_sample.png)

### 3. Multiple groups

If the number of groups is an **even number**, a *multiple groups* plot will be automatically generated by `dabest('MultipleGroups_sample.csv')` command.  

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/IndividualGroups/MultipleGroups.png)

### 4. Shared control

If there are more than two groups in the data, `dabest('MultipleGroups_sample.csv')` generates a *shared control* plot.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/IndividualGroups/SharedControls.png)

### 5. Merged groups

To combine two groups of data and compare to a third group, run `dabest('MultipleGroups_sample.csv','mergeGroups')`.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/MergedGroups/MergedGroups.png)

### 6. Multiple merged groups

For the data that contain more than three groups -and a number that is divisible by 3, `dabest('MultipleGroups_sample.csv','mergeGroups')` generates a *multiple merged groups* plot.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/MergedGroups/MultipleMergedGroups.png)

### 7. Merged shared control

If the data contain more than three groups, `dabest('MultipleGroups_sample.csv','mergeGroups')` automatically generates a second plot in which all the groups are compared to the *merged shared control*.

![](https://github.com/ttumkaya/DABEST-Matlab/blob/master/SampleData/MergedGroups/MergedSharedControl.png)
