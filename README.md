# k-NN with Dynamic Time Warping

The objective of this assignment is to implement and test a k-Nearest 
Neighbour (k-NN) classifier for time-series data.

The tasks are outlined below, and reiterated in `Assignment 1.ipynb` at 
each step:

### Task 1.1: Implement a 1-NN Classifier for Time-Series Data
Here I create a 1-NN Classifier for the time-series data, with fit, 
predict and scoring methods that behave similarly to sklearn 
implementations. I use the dtw function provided to calculate distances 
between time series arrays.

### Task 1.2: Test Classifier Performance Using The UMD Data
Here I read in the UMD data and isolate the target and feature values. 
Then I divide the dataset into a training and testing split. I use the 
training sets to train the classifier, and then work out the accuracy of 
the classifier using the unseen test data.
 
### Task 1.3: Using Euclidian Distance
Here I will implement the sklearn kNN model using Euclidian distance 
metrics with 1 nearest neighbour, and compare the performance with my own 
1NN DTW  classifier. I will then use cross validation with varying number 
of folds to see the effects on accuracy.

### Task 1.4: Best Value for Window Parameter
Here I experiment with changing window size of the dtw function to see the 
effect on the accuracy of the classifier.

### Task 2.1: Adapting DTW as a Metric Function
Here I have altered the dtw function to create `dtw_metric`, a function which can be used in the sklearn  
implementation of the KNeighborsClassifier, as a metric to calculate distance. The window size has been adjusted 
to be a kwarg now, with a default value of 3, that can be altered by the metric_params argument of the 
KNeighborsClassifier.

### Task 2.2, 2.3: Comparing Performance of Custom Classifier with Custom Metric Function and Euclidian Distances
Below I measure the performance of the Sklearn implementation of the KNeighborsClassifier with my new metric  
function. I test initially with 1NN and compare with the custom classifier, as expected, the results are the  
same. Then I experiment with 2 and 3 nearest neighbours of the sklearn implementation, in order to see the  
effect on the results. Finally, I check the performance of the model using euclidian distance with 2 and 3  
nearest neighbours
