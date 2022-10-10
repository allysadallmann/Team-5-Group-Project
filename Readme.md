README
================
Group 5
October 10, 2022

## Readme

This is the Readme for Group 5’s SDS 322e project, a probabilistic
classification task that tries to predict whether a machine failure
occurs or not.

**Group Members**: Allysa Dallman, Michael Montez, Shreya Nallaparaju,
Jonathan Saldeen,Sebastian Utama, Kayla White, Emily Zhou

## **Project Description**

Our project seeks to analyze information from a realistic, yet
synthetic, predictive maintenance dataset to develop machine learning
models with high predictive capability that translate into explainable
dialogues for the end user. The comprised data classifies relevant
variables that correlate to five independent failure modes: tool wear
failure, heat dissipation failure, power failure, overstrain failure,
and random failures.

## **Goals**

Our task is to determine the probability a machine part will fail due to
any of the failure modes, and classify it as a failure or not.

## **Data**

**Raw Data**:
<https://archive.ics.uci.edu/ml/machine-learning-databases/00601/>  
**Data Description**:
<https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset>

**Data Description**: This is a realistic, synthetic maintenance
dataset. If at least one of the failure modes, described in the data
description, is true, the process fails and the ‘machine failure’ label
is set to 1. It is therefore not transparent to the machine learning
method, which of the failure modes has caused the process to fail. Our
goal is to predict whether a failure occurs or not.

## Further Details

Our raw data contains 10,000 observations of 14 features. The following
is a short description of these features…  
- UID: unique identifier ranging from 1 to 10000  
- product ID: consisting of a letter L, M, or H for low (50% of all
products), medium (30%) and high (20%) as product quality variants and a
variant-specific serial number  
- air temperature \[K\]  
- process temperature \[K\]  
- rotational speed \[rpm\]  
- torque \[Nm\]  
- tool wear \[min\]  
- ‘machine failure’ label that indicates, whether the machine has failed
in this particular datapoint for any of the following failure modes are
true.

**Criterias for which a machine fails:**  
- Tool wear failure (TWF): if the tool wear is between 200- 240 mins  
- Heat dissipation failure (HDF): if the difference between air- and
process temperature is below 8.6 K and the tool’s rotational speed is
below 1380 rpm  
- Power failure (PWF): if the product of tool wear and torque speed
(rad/s) equals power required. If this power is below 3500 W or above
9000 W, the process fails  
- Overstrain failure (OSF): If the product of tool wear and torque
exceeds 11,000 minNm for the L product variant (12,000 M, 13,000 H)  
- Random failures (RNF): each process 0.1% chance of failure regardless
of its process parameters.

## **References**

Stephan Matzka, ‘Explainable Artificial Intelligence for Predictive
Maintenance Applications’, Third International Conference on Artificial
Intelligence for Industries (AI4I 2020), 2020 (in press)
