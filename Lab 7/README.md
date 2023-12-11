# Lab Assignment Seven: Sequential Network Architectures
In this lab, you will select a prediction task to perform on your dataset, evaluate a sequential architecture and tune hyper-parameters. If any part of the assignment is not clear, ask the instructor to clarify. 

This report is worth 10% of the final grade. Please upload a report (**one per team**) with all code used, visualizations, and text in a rendered Jupyter notebook. Any visualizations that cannot be embedded in the notebook, please provide screenshots of the output. The results should be reproducible using your report. Please carefully describe every assumption and every step in your report.

**Dataset Selection**

Select a dataset that is text. That is, the dataset should be text data (or a time series sequence). In terms of generalization performance, it is helpful to have a large dataset of similar sized text documents. It is fine to perform binary classification or multi-class classification. The classification should be "many-to-one" sequence classification. 

**Grading Rubric**

- Preparation (**3 points total**)
  - [**1 points**] Define and prepare your class variables. Use proper variable representations (int, float, one-hot, etc.). Use pre-processing methods (as needed). Describe the final dataset that is used for classification/regression (include a description of any newly formed variables you created). **Discuss methods of tokenization in your dataset as well as any decisions to force a specific length of sequence.** 
  - [**1 points**] Choose and explain what metric(s) you will use to evaluate your algorithm’s performance. You should give a **detailed argument for why this (these) metric(s) are appropriate** on your data. That is, why is the metric appropriate for the task (*e.g.*, in terms of the business case for the task). Please note: rarely is accuracy the best evaluation metric to use. Think deeply about an appropriate measure of performance.
  - [**1 points**] Choose the method you will use for dividing your data into training and testing (*i.e.*, are you using Stratified 10-fold cross validation? Shuffle splits? Why?). **Explain why your chosen method is appropriate or use more than one method as appropriate.** Convince me that your train/test splitting method is a realistic mirroring of how an algorithm would be used in practice. 
- Modeling (**6 points total**)
  - [**3 points**] Investigate at least two different sequential network architectures (e.g., a CNN and a Transformer). Alternatively, you may also choose a recurrent network and Transformer network. Be sure to use an embedding layer (try to use a pre-trained embedding, if possible). Adjust one hyper-parameter of each network to potentially improve generalization performance (train a total of at least four models). Visualize the performance of training and validation sets versus the training iterations, showing that the models converged.
  - [**1 points**] Using the best parameters and architecture from the Transformer in the previous step, add a second Multi-headed self attention layer to your network. That is, the input to the second attention layer should be the output sequence of the first attention layer.  Visualize the performance of training and validation sets versus the training iterations, showing that the model converged.
  - [**2 points**] Use the method of train/test splitting and evaluation criteria that you argued for at the beginning of the lab. Visualize the results of all the models you trained.  Use proper statistical comparison techniques to determine which method(s) is (are) superior.
- Exceptional Work (**1 points total**)
  - You have free reign to provide additional analyses.
  - One idea (**required for 7000 level students to do one of these options**):
    - Use the pre-trained ConceptNet Numberbatch embedding and compare to pre-trained GloVe. Which method is better for your specific application? 
