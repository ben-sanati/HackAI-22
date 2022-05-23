# Cirium's HackAI Challenge #
## Southampton 2022 ##

Team: Benjamin Sanati, Emil Stoev, Miroslav Milanov

The aim of this hackaton was to develop a machine learning model, which processes data about organized events, airports and online flight query volumes and predict anomalies in the data to find which events lead to a spike in searches of particular flights.

***We have been asked to not publish the data and we respect Cirium's request. All references to the dataset have been expunged.***

We use an AutoEncoder neural network. An autoencoder takes an input and performs an “encoding” (essentially a generalised PCA) on the input, resulting in a bottleneck of the most important features. A "decoding" is then performed on the bottleneck to reconstruct the input using only the features with largest variance. This reconstructed input can be compared with the original image by taking a mean absolute error between the input and the reconstructed input. 

<p align="center"><img src="./img/autoencoder.png"></p>

This gives us an array of losses for each individual event. The sum of the mean and standard deviation losses represents the value for the threshold used for anomaly detection.

<p align="center"><img src="./img/HistogramDist.png"></p>


For a more detailed overview, you can download our presentation in the files or have a look here:
https://docs.google.com/presentation/d/1I-U3-zCT2FVroj4rzkMSEnIKHSEPsJTvHFEt0GWElgE/edit?usp=sharing

Finally, here is our team at the hackaton:

<p align="center"><img src="./img/Team.png"></p>

From left to right: Benjamin Sanati, Miroslav Milanov and Emil Stoev
