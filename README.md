Table of Contents
=================

* [Cirium's HackAI Challenge - 2022#](#ciriums-hackai-challenge---2022)
   * [Aims](#aims)
   * [Solution](#solution)
      * [Team](#team)

# Cirium's HackAI Challenge - 2022

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) &emsp;
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) &emsp;
![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green)
<br />

## Aims

The aim of this hackathon was to process data about organized events and online flight query volumes to determine the events that lead to a spike in flight requirements. This would be used to inform airlines about when flights could be scheduled optimally.

An overview of our teams solution to the problem is given in the [presentation](./HackAI.pptx), with a slightly more detailed overview given below.

***We have been asked to not publish the data and we respect Cirium's request. All references to the dataset have been expunged.***

## Solution

Our process uses an AutoEncoder NN to locate flight query volume anomalies that occur due to particular events. An autoencoder takes an input and performs an “encoding” (essentially a generalised PCA) on the input, resulting in a bottleneck of the most important features. A "decoding" is then performed on the bottleneck to reconstruct the input using only the features with largest variance. This reconstructed input can be compared with the original image by taking a mean absolute error between the input and the reconstructed input. 

<p align="center"><img src="./img/autoencoder.png"></p>

This gives us an array of losses for each individual event. The sum of the mean and standard deviation losses represents the value for the threshold used for anomaly detection.

<p align="center"><img src="./img/HistogramDist.png"></p>


For a more detailed overview, you can download our presentation in the files or have a look here:
https://docs.google.com/presentation/d/1I-U3-zCT2FVroj4rzkMSEnIKHSEPsJTvHFEt0GWElgE/edit?usp=sharing

### Team

Team: Benjamin Sanati, Emil Stoev, Miroslav Milanov

Our team presented our solution to a panel of judges at the hackathon, the majority of which where representatives from Cirium. 

<p align="center"><img src="./img/Team.png"></p>

From left to right: Benjamin Sanati, Miroslav Milanov and Emil Stoev
