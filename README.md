# Principal-Component-Analysis-(PCA)
Essentially, in PCA we make a transition from one variable space to another, with the new space containing fewer variables (n_component), where the new variables are uncorrelated and are the weighted sum of the old variables.
As a result we get m variables: {PC1, PC2, PC3... PCm} , where PC1 will receive the most information(maximum sample variance), PC2 - less, and so on (A variable is considered informative if it has a high sample variance).
Note: PCA is a linear transformation, and linearity is sensitive to the scale of data. Therefore, PCA works best when all data values are on the same scale. This can be done by subtracting the column mean from its values and dividing the result by its standard deviation. That is called data standardization. Prior to using PCA, make sure the data is scaled!
After getting the covariance matrix, PCA tries to find a linear combination of features that best explains it - it fits linear models until it identifies the one that explains the maximum amount of variance.
One important detail to take into consideration here is that, due to its linear nature, PCA will concentrate most of the explained variance in the first principal components. So, when looking at the explained variance, usually our first two components will suffice. 
In a nutshell, this is what PCA is all about: Finding the directions of maximum variance in high-dimensional data and project it onto a smaller dimensional subspace while retaining most of the information. So main advantages of PCA are data compression (reduce memory, speed up learning) and visualization.
As humans, we can only visualize things in 2-dimensions or 3-dimensions. For data, this rule does not apply! Data can have an infinite amount of dimensions, but this is where the curse of dimensionality comes into play.
For example let’s say that we have two variables height and weight. To represent these 2 lines, PCA combines both height and weight to create two brand new variables. It could be 30% height and 70% weight, or 87.2% height and 13.8% weight, or any other combinations depending on the data that we have. PCA creates new variables with the original features trying to include the majority of the variance into the principal components. 
A rule of thumb here is that the cumulative variance explained by the components should be at least 70%.

PCA creates new features trying to collect the major variance as possible within the data given in order to not lose the main information of the data. 
Since PCA is a linear method, it has a main disadvantage in order to make it works properly. 
PCA needs features, variables to be highly correlated, before doing the reduction. 
•	However there is a solution to solve this disadvantage and are the algorithms called Non-linear methods (Manifold learning). 
Notice how the steps in principal component analysis such as computing the covariance matrix, performing eigendecomposition or singular value decomposition on the covariance matrix to get the principal components have all been abstracted away when we use scikit-learn’s implementation of PCA.
PCA takes advantage of existing correlations between the input variables in the dataset and combines those correlated variables into a new set of uncorrelated variables.
PCA is an unsupervised machine learning algorithm as it does not require labels in the data.
Important considerations: 
•	Each new variable is a linear combination of the original variables.
•	The first new variable is chosen to capture the maximum amount of variance in the data set.
•	The second will account for the maximum variance not captured by the first.
•	The pth new variable will account for the maximum variance in the data not captured by the p−1 new variables.
•	The new variables are not correlated.

