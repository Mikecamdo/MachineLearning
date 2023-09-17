# Lab Assignment One: Exploring Table Data

You are to perform preprocessing and exploratory analysis of a data set: exploring the statistical summaries of the features, visualizing the attributes, and addressing data quality.
This report is worth 10% of the final grade. Please upload a report (one per team) with all code used, visualizations, and text in a rendered Jupyter notebook. 
Any visualizations that cannot be embedded in the notebook, please provide screenshots of the output. Only the rendered HTML notebook is acceptable. 

You should analyze table data. The requirements and rubric for each are explained below.

<i>**A note on grading:** This lab is mostly about visualizing and understanding your dataset. The largest share of the points is from how you interpret the visuals that you make. 
Making the visuals is not enough to satisfy each of the rubrics below—you should appropriately explain what the implications of the visualizations are. In other words, expect about 20% of the available points for visuals that have no substantive discussion.</i>

<i>**Graded Example from previous offering:** https://www.dropbox.com/sh/yinn3v3qnzlbep5/AAA-i1u-4ylyxwiCb8nyEDY7a?dl=0</i>

# Table Data 
**Dataset requirements:** Choose a dataset that is mostly ready to be analyzed. That is, it is already in the format of table data. The following requirements should be met:

1. The data includes categorical features (it can also include other forms of data, but must have categorical data)
2. The data must be 1,000 rows or larger
3. The data is not strictly image or text data (but could have these data)
4. The dataset should have some prediction task associated with it (i.e., labels to learn, classification)
 
**Table Data Grading Rubric**

- Business Understanding (**1.5 points total**).  
  - [**1.5 points**] In your own words, give an overview of the dataset. Describe the purpose of the data set you selected (i.e., why and how was this data collected in the first place?). What is the prediction task for your data and why are other third parties interested in the result? Once you begin modeling, how well would your prediction algorithm need to perform to be considered useful to these third parties?
    - Be specific and use your own words to describe the aspects of the data.
- Data Understanding (**3 points total**)
  - [**1.5 points**] Load the dataset and appropriately define data types. What data type should be used to represent each data attribute? Discuss the attributes collected in the dataset. For datasets with a large number of attributes, only discuss a subset of relevant attributes.  
  - [**1.5 points**] Verify data quality: Explain any missing values or duplicate data. Visualize entries that are missing/complete for different attributes. Are those mistakes? Why do these quality issues exist in the data? How do you deal with these problems? Give justifications for your methods (elimination or imputation).  
- Data Visualization (**4.5 points total**)
  - [**2 points**] Visualize basic feature distributions. That is, plot the dynamic range and exploratory distribution plots (like boxplots, histograms, kernel density estimation) to better understand the data. Describe anything meaningful or potentially useful you discover from these visualizations. These may also help to understand what data is missing or needs imputation. **Note:** You can also use data from other sources to bolster visualizations. Visualize at least five plots, at least one categorical. 
  - [**2.5 points**] Ask three interesting questions that are relevant to your dataset and explore visuals that help answer these questions. Use whichever visualization method is appropriate for your data.  **Important:** Interpret the implications for each visualization. 
- Exceptional Work (**1 point total**)
  - [**0.4 points**] The overall quality of the report as a coherent, useful, and polished product will be reflected here. Does it make sense overall? Do your visualizations answer the questions you put forth in your business analysis? Do you properly and consistently cite sources and annotate changes made to base code? Do you provide specific reasons for your assumptions? Do subsequent questions follow naturally from initial exploration?
  - [**0.6 Points**] Additional analysis:
    - **5000 level students**: You have free rein to provide any additional analyses. 
    - **7000 level students**: Implement dimensionality reduction using uniform manifold approximation and projection (UMAP), then visualize and interpret the results. Give an explanation of UMAP dimensionality reduction methods. You may be interested in the following information:
    - https://github.com/lmcinnes/umap
    - https://pair-code.github.io/understanding-umap/
