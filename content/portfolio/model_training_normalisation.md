---
title: Why Normalisation is important ?
date: 
thumbnail: images/portfolio/normalize_anim.gif
service: The main goal of this small snippet of the code is to show the effects of the unnormalized data points on the model training.
solution: Normalized data would boost up the overall training process and help the model to converge fast.
---
Deep learning neural network models learn a mapping from input variables to an output variable.

The scale and distribution of the data drawn from the domain may be different for each variable. Scaling techniques are really depends on the domain that we are working in.  

Overall, differences in the scales across input variables may increase the difficulty of the problem being modeled. An example of this is that large input values (e.g. a spread of hundreds or thousands of units) can result in a model that learns large weight values. A model with large weight values is often unstable, meaning that it may suffer from poor performance during learning and sensitivity to input values resulting in higher generalization error. Additionally, a target variable with a large spread of values, in turn, may result in large error gradient values causing weight values to change dramatically, making the learning process unstable.

To solve this unstable learning process, we should normalize the data. There are so many different types of normalization procedures we could apply such as, 

1. Min-max normalization
2. Standardization (Z-score normalization)
3. Median Absolute Deviation (MAD)
4. Tanh-estimators

After normalizing the values we could train our model as usual. 

To show the learning process difference between normalized and unnormalized data, I have created the following visualization in which, the upper two plots show the pattern of how accuracy and loss behave while training whereas the lower two plots show the same training process utilizing normalized data. 

We can clearly see that model with normalized data converges faster than unnormalized data. Model fed with normalized data showed fewer fluctuations and steady performance while training.




##### Please visit the GitHub repository 
### [GitHub Link ](https://github.com/ronakjpatel/Data_Science_Projects/blob/2a2002ea6f362e1d0edbaf79920e2678f417f8e9/Data_Normalization.ipynb)