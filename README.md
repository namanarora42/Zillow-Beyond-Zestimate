# Zillow-Beyond-Zestimate

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://githubtocolab.com/namanarora97/Zillow-Beyond-Zestimate/blob/main/Zillow_Zestimate_Prediction.ipynb)

Zillow's zestimate has been under a lot of scrutiny lately due to an increase in inaccurate estimation leading to losses for the company. 

This analysis takes a different approach, where we try to predict the log error in the zestimate prediction. Thus, instead of revisiting the actual model for Zestimate calculation (which is a black box to us), we try to analyze what parameters actually cause the Zestimate to be off. 

The data is provisioned by Zillow through a [Kaggle competition](https://www.kaggle.com/c/zillow-prize-1/overview). 

## Findings

Upon analyzing the feature importance for the best chosen model, the following features seem to be the most impactful in contributing to the error in Zestimates:

* Property/County Land Use Code
* Presence in Zip Code 964XXX (Properties in this area are generally incorrectly priced)
* Bedroom count (Properties with lower bedroom counts tend to have a higher error in the Zestimate)
* Garage Count
* Buildings that are rated at a Quality level of 5