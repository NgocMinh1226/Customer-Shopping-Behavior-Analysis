# Customer Shopping Behavior Analysis
A data science project to segment and classify customer shopping behavior using K-Means, Hierarchical Clustering, SVM, and KNN, with insights for targeted marketing strategies.

## Overview 
This project focuses on analyzing customer shopping behavior using classification and clustering algorithms. The goal is to segment customers based on their purchasing patterns and predict behaviors such as promo code usage, enabling businesses to tailor marketing strategies effectively.

#### Objectives
- **Classification**: Predict whether customers use promo codes based on demographic and behavioral features using Support Vector Machine (SVM) and K-Nearest Neighbors (KNN) algorithms.
- **Clustering**: Group customers into segments based on numerical features like age, purchase amount, and frequency using K-Means and Hierarchical Clustering algorithms.
- **Evaluation**: Assess model performance using metrics such as Accuracy, Precision, Recall, F1-Score for classification, and Silhouette Score and Davies-Bouldin Index for clustering.

<img src="image/system_operation_process.png" 

#### Dataset
The dataset, sourced from [shopping_behavior_updated](https://www.kaggle.com/code/a10101100/ecommerce-trends-viz), is a synthetic collection simulating real-world customer shopping behavior at a mall. It includes 3,900 records with attributes such as:

Customer ID
Age
Gender
Purchase Amount (USD)
Payment Method
Frequency of Purchases
Review Rating
Promo Code Used
And more (see the full list in the report)

<img src="image/data_set_structure.png" 


#### Methodology
- **Data Preprocessing**
	- Cleaning: Removed irrelevant features (e.g., Customer ID) and handled missing values.
	- Encoding: Applied One-Hot Encoding to categorical variables (e.g., Payment Method, Gender) and Label Encoding for ordinal data (e.g., Frequency of Purchases).
	- Scaling: Standardized numerical features to ensure uniform contribution to model training.

#### Algorithms
**Classification**:
- **SVM**: Utilized a linear kernel to predict promo code usage, achieving higher accuracy but lower recall for non-promo users.
- **KNN**: Employed with k=5 neighbors, offering balanced precision and recall but lower overall accuracy (70.90%).
**Clustering**:
- **K-Means**: Determined optimal clusters (k=5) using the Elbow method. Achieved a Silhouette Score of 0.1479 and Davies-Bouldin Index of 1.6535.
- **Hierarchical** Clustering: Used Agglomerative Clustering with a dendrogram to identify 5 clusters. Recorded a Silhouette Score of 0.0880 and Davies-Bouldin Index of 2.0147.

#### Evaluation
**Classification:**
- SVM outperformed KNN in accuracy and F1-Score for promo code users but struggled with non-promo user recall.
- KNN provided balanced performance across classes.
**Clustering:**
- K-Means produced clearer, more distinct clusters compared to Hierarchical Clustering, which showed overlapping clusters.
- Both clustering methods indicated room for improvement due to low Silhouette Scores and high Davies-Bouldin Indices.

#### Conclusions
- SVM is more effective for classifying promo code usage, while KNN offers simplicity and balanced performance.
- K-Means outperforms Hierarchical Clustering in creating distinct customer segments, but both methods suggest the data may not have clear natural clusters.
- Visualizations revealed no significant spending differences by gender, with younger customers (18-40) showing higher density but lower purchase amounts.

#### Limitations
- Clustering results were suboptimal, with low Silhouette Scores indicating poor cluster separation.
- Hierarchical Clustering produced overlapping clusters, possibly due to unsuitable data structure or parameter choices.
- The dataset's synthetic nature may limit real-world applicability.

### Contributors
- **Group 10:** 6 members


## Clone Repository
Clone this Repository using,

	git clone https://github.com/NgocMinh1226/Customer-Shopping-Behavior-Analysis.git


## Usage
Install `jupyter` from [here](http://jupyter.readthedocs.io/en/latest/install.html) or use

	pip install jupyter

After installing jupyter notebook Just run `jupyter notebook` in terminal and you can visit the notebook in your web browser.


## Create Environment

Create an environment using the `requirements.txt` using pip by using following command so you dont have to install dependencies one by one,


	pip -r requirements.txt

If you need to use conda to create the environment,
Read conda docs on managing environments [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)


## Dependencies

* [Pandas](https://pandas.pydata.org/docs/)
* [NumPy](https://numpy.org/devdocs/user/index.html)
* [Matplotlib](https://matplotlib.org/3.3.3/contents.html)
* [Seaborn](https://seaborn.pydata.org/)
* [Sklearn](https://scikit-learn.org/stable/)

Install missing dependencies using,

	pip install pandas numpy matplotlib seaborn sklearn


