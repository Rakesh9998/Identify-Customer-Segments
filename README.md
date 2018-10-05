# Identify-Customer-Segments

Project Details
Below, you will find an outline of the steps that you will take in this project.
Step 0: The Data
There are a number of files used for this project.Due to the the agreement issue, I am not including the dataset here as the data are proprietary. The files available for the project are:

Udacity_AZDIAS_Subset.csv: Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
Udacity_CUSTOMERS_Subset.csv: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
Data_Dictionary.md: Information file about the features in the provided datasets.
AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographic data.
Identify_Customer_Segments.ipynb: Jupyter Notebook divided into sections and guidelines for completing the project. The notebook provides more details and tips than the outline given here.

Step 1: Preprocessing
When I start an analysis, I must first explore and understand the data that I am working with. In this (and the next) step of the project, I’ll be working with the general demographics data. As part of my investigation of dataset properties, I attended to a few key points:

How are missing or unknown values encoded in the data? Are there certain features (columns) that should be removed from the analysis because of missing data? Are there certain data points (rows) that should be treated separately from the rest?
Consider the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric). What assumptions must be made in order to use each feature in the final analysis? Are there features that need to be re-encoded before they can be used? Are there additional features that can be dropped at this stage?
I created a cleaning procedure that I applied first to the general demographic data, then later to the customers data.

Step 2: Feature Transformation
Now that my data is clean, I use dimensionality reduction techniques to identify relationships between variables in the dataset, resulting in the creation of a new set of variables that account for those correlations. In this stage of the project, I attended to the following points:

The first technique that I should perform on your data is feature scaling. What might happen if we don’t perform feature scaling before applying later techniques you’ll be using?
Once I’ve scaled my features, I can then apply principal component analysis (PCA) to find the vectors of maximal variability. How much variability in the data does each principal component capture? Can you interpret associations between original features in your dataset based on the weights given on the strongest components? How many components will you keep as part of the dimensionality reduction process?
I use the sklearn library to create objects that implement your feature scaling and PCA dimensionality reduction decisions.

Step 3: Clustering
Finally, on the transformed data, I apply clustering techniques to identify groups in the general demographic data. I then apply the same clustering model to the customers dataset to see how market segments differ between the general population and the mail-order sales company. You will tackle the following points in this stage:

Use the k-means method to cluster the demographic data into groups. How should you make a decision on how many clusters to use?
Apply the techniques and models that you fit on the demographic data to the customers data: data cleaning, feature scaling, PCA, and k-means clustering. Compare the distribution of people by cluster for the customer data to that of the general population. Can you say anything about which types of people are likely consumers for the mail-order sales company?
sklearn will continue to be used in this part of the project, to perform your k-means clustering. In the end, you will export the completed notebook with your work as an HTML file, which will serve as a report documenting your approach and findings.
