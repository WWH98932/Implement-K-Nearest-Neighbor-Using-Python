# Implement-K-Nearest-Neighbor-Using-Python
UCLA Master of Applied Economics Econ 423 Assignment
In this assignment, you will develop a K-Nearest Neighbor implementation using Python and NumPy only. 
Your input will be the Iris training data set (consisting of four features). The data set is provided in two files:
3.M.1: iristest.csv 
3.M.2: iristrain.csv. 

This is a subset of the Iris Data Set that can be found on UCI Machine Learning Repository:
https://archive.ics.uci.edu/ml/datasets/Iris
Remember you will use the data provided in the files listed above and not the data from the repository. The training and test files are arranged similarly, that is, the first four column are input features while the fifth column is the species as shown below:
lsepal    wsepal    lpetal    wpetal    species.

You will develop a function that will take four parameters: 
- a text string consisting of the training data file name
- a text string consisting of the test data file name 
- a text string consisting of the file name for the output file
- the parameter k to be used in the k-nearest neighbors algorithm. 
Your job is to write a function that implements the k-nearest algorithm.
The function should have the exact function definition as below. Failure to follow this definition will result in a deduction of points.

      def knearestneighbor(trainfile, testfile, outputfile, k):
        #your code here
      return confusionmatrix
    
Your function will create an output file as per the file name provided . The output file should print the classification of the corresponding data record , each on its own line. For example, the first line in the output file should be the integer corresponding to the class the first data record in the testfile was classified as.

The function will assume that the input files exist in the same directory/folder where the file is being run from. The output will be created in the same folder. In addition to printing your classification results to a file, your function must return a confusion matrix . The returned value should be of type list and contain the 4 values of your confusion matrix. For example, [45, 32, 65, 3] is something your function can return given a certain dataset.

Below, we have some steps that you can take in implementing the algorithm. You should use numpy arrays/matrices to store your data as it will help make your algorithm efficient and easier to work with.

Your function will read the trainfile and populate a numpy array X (4 x 80) and a numpy array Y(1 x 80) following the convention give on slide 23 of Linear Regression. You function will read the testfile and populate a numpy array Xtest (4x20) and a numpy array Ytest(1 x 20). The function will also create a numpy array Yhat(1x20) consisting of all zeros. Next for each example in Xtest, your function will apply the K-Nearest Neighbor method to determine the class for that example and put in Yhat. Once all 20 test examples are processed, the output file will be written out and the confusion matrix will be returned. 
