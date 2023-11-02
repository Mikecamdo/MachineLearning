# Lab Assignment Four: Multi-Layer Perceptron 
In this lab, you will compare the performance of multi-layer perceptrons programmed  via your own various implementations. 

This report is worth 10% of the final grade. Please upload a report (**one per team**) with all code used, visualizations, and text in a rendered Jupyter notebook. Any visualizations that cannot be embedded in the notebook, please provide screenshots of the output. The results should be reproducible using your report. This lab project is slightly different from other reports in that you will be asked to complete more specific items.

**Dataset Selection**

For this assignment, you will be using a specific dataset chosen by the instructor.  This is US Census data available on Kaggle, and also downloadable from the following link: <https://www.dropbox.com/s/bf7i7qjftk7cmzq/acs2017_census_tract_data.csv?dl=0>

The Kaggle description appears here: <https://www.kaggle.com/muonneutrino/us-census-demographic-data/data>

The classification task you will be performing is to predict, for each tract, what the child poverty rate will be. You will need to convert this from regression to **four levels of classification** by quantizing the variable of interest. 

**Grading Rubric**

- Load, Split, and Balance (**1.5 points total**)
  - [**.5 points**] (1) Load the data into memory and save it to a pandas data frame. **Do not** normalize or one-hot encode any of the features until asked to do so later in the rubric. (2) Remove any observations that having missing data. (3) Encode any string data as integers for now. (4) You have the option of keeping the "county" variable or removing it. Be sure to discuss why you decided to keep/remove this variable. 
  - The next two requirements will need to be completed together as they might depend on one another:
    - [**.5 points**] Balance the dataset so that about the same number of instances are within each class. Choose a method for balancing the dataset and explain your reasoning for selecting this method. One option is to choose quantization thresholds for the "ChildPoverty" variable that equally divide the data into four classes. *Should balancing of the dataset be done for both the training and testing set? Explain.*
    - [**.5 points**] Assume you are equally interested in the classification performance for each class in the dataset. Split the dataset into 80% for training and 20% for testing. There is **no need** to split the data multiple times for this lab.
  - **Note:** You will need to one hot encode the target, but do not one hot encode the categorical data until instructed to do so in the lab. 
- Pre-processing and Initial Modeling (**2.5 points total**)
  - You will be using a two layer perceptron from class for the next few parts of the rubric. There are several versions of the two layer perceptron covered in class, with example code. When selecting an example two layer network from class be sure that you use: (1) vectorized gradient computation, (2) mini-batching, (3) cross entropy loss, and (4) proper Glorot initialization, at a minimum. There is no need to use momentum or learning rate reduction (assuming you choose a sufficiently small learning rate). It is recommended to use sigmoids throughout the network, but not required.
  - [**.5 points**] Use the example two-layer perceptron network from the class example and quantify performance using accuracy. **Do not** normalize or one-hot encode the data (not yet). Be sure that training converges by graphing the loss function versus the number of epochs. 
  - [**.5 points**] Now (1) normalize the continuous numeric feature data. Use the example two-layer perceptron network from the class example and quantify performance using accuracy. Be sure that training converges by graphing the loss function versus the number of epochs.  
  - [**.5 points**] Now (1) normalize the continuous numeric feature data AND (2) one hot encode the categorical data. Use the example two-layer perceptron network from the class example and quantify performance using accuracy. Be sure that training converges by graphing the loss function versus the number of epochs. 
  - [**1 points**] Compare the performance of the three models you just trained. Are there any meaningful differences in performance? Explain, in your own words, why these models have (or do not have) different performances.  
    - *Use one-hot encoding and normalization on the dataset for the remainder of this lab assignment.*
- Modeling (**5 points total**)
  - [**1 points**] Add support for a third layer in the multi-layer perceptron. Add support for saving (and plotting after training is completed) the average magnitude of the gradient for each layer, for each epoch (like we did in the flipped module for back propagation). For magnitude calculation, you are free to use either the average absolute values or the L1/L2 norm.
    - Quantify the performance of the model and graph the magnitudes for each layer versus the number of epochs.
  - [**1 points**] Repeat the previous step, adding support for a fourth layer.
  - [**1 points**] Repeat the previous step, adding support for a fifth layer. 
  - [**2 points**] Implement an adaptive learning technique that was discussed in lecture and use it on the five layer network (choose either RMSProp or AdaDelta). Discuss which adaptive method you chose. Compare the performance of your five layer model with and without the adaptive learning strategy. **Do not use AdaM for the adaptive learning technique as it is part of the exceptional work.**
- Exceptional Work (**1 points total**)
  - 5000 level student: You have free reign to provide additional analyses.
  - One idea (**required for 7000 level students**):  Implement adaptive momentum (AdaM) in the five layer neural network and quantify the performance compared to other methods.  
