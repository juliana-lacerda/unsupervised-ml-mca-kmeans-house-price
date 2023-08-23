# unsupervised-ml-mca-kmeans-house-price
Unsupervised machine learning applied to a house price data set with numeric and categorical features.

The data set is composed of qualitative and quantitative features related to houses along with the property value (target). The target variable is removed from the data set as a unsupervised techniques are performed and the target is used only in the end to validade the models' output.

# Data Set
Data set: https://www.kaggle.com/datasets/elakiricoder/jiffs-house-price-prediction-dataset (house_price_dataset_original_v2_cleaned.csv)

# Multiple Correspondency Analysis and Kmeans Clustering
* The following steps are performed in the notebook:
    * The data frame is devided into quantitative and qualitative.
    * MCA (Multiple Correspondency Analysis) is performed at the quantitative data frame where the first three coordinates is returned for each observation (with explained variance of ~50%). MCA is performed only using qualitative variables that present statistically significant association with at least one other.
    * This data frame is then merged with the quantitative one and KMeans is performed. The inertia and silhouette score are used to pick the most appropriate number of clusters. An F test is performed to check the contribution of the features to the cluster formation.
    * The metrics of the houses' variables are then calculated for the resulting clusters and their property value is also compared.

# Requirements
The required packages are listed in  requirements.txt
