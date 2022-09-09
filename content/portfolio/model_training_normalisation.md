---
title: Why normalisation is important ?
date: 
thumbnail: images/portfolio/normalize_anim.gif
service: The main goal of this small snippet of the code is to show the adverse effects of the unnormalized data points on the model training.
solution: Normalized data would boost up the overall training process and helps the model to converge faster.
---
Deep neural networks learn mapping from input variables to an output variable in the training phase.
 
Overall, differences in the scales across input variables may increase the difficulty of the problem being modeled. As an example, large input values (e.g. a spread of hundreds or thousands of units) can result in a model that learns large weight values. A model with large weight values is often unstable, meaning that it may suffer from poor performance of the model in practice. 
 
To solve this unstable learning process, we should normalize the data. There are so many different types of normalization procedures we could apply such as,
 
1. Min-max normalization
2. Standardization (Z-score normalization)
3. Median Absolute Deviation (MAD)
4. Tanh-estimators
 
After normalizing the values we could train our model as usual.
 
To show the learning process difference between normalized and unnormalized data, I have created the following visualization in which, the upper two plots show the pattern of how accuracy and loss metrics behave while training on the unnormalized data whereas the lower two plots show the same matrices but for the normalized data.
 
It is evident that models with normalized data converge faster than unnormalized data. Models fed with normalized data showed fewer fluctuations and steady performance while training.





##### Please visit the GitHub repository 
### [GitHub Link ](https://github.com/ronakjpatel/Data_Science_Projects/blob/2a2002ea6f362e1d0edbaf79920e2678f417f8e9/Data_Normalization.ipynb)