# DataFest-2024: Student Performance Clustering



## Project Overview

This project performs K-Means clustering on student data to identify distinct groups based on their performance metrics and engagement with learning materials.  The analysis uses data from three sources: student performance scores, video viewing habits, and page interaction data. The goal is to gain insights into student learning patterns and potentially inform targeted interventions.


## Main Features and Functionality

The Jupyter Notebook (`src/main.ipynb`) implements the following functionalities:

* **Data Loading:** Loads student performance data, video viewing data, and page interaction data from CSV files.
* **Data Preprocessing:**  Selects relevant features for clustering (average cost, average intrinsic motivation, average expectancy).  No explicit scaling is performed, although the code contains commented-out lines suggesting MinMaxScaler was considered.
* **K-Means Clustering:** Applies the K-Means algorithm to cluster students into groups based on the chosen features. The optimal number of clusters (3) is determined visually using the elbow method (plotting within-cluster sum of squares (WCSS) against the number of clusters).
* **3D Visualization:** Creates a 3D scatter plot to visualize the clusters in the feature space (average cost, average intrinsic motivation, average expectancy).
* **Cluster Analysis:** Calculates the average values of various performance metrics and engagement measures for each cluster.  This includes the number of students in each cluster, average performance scores across several dimensions, average video viewing time, and average page interaction metrics (number of reviewed pages, number of retries, and sum of engaged time).
* **Output:** Presents the average metrics for each cluster, providing a comparative analysis of the student groups identified.




## Data Techniques

This project employs the following data analysis techniques:

* **Data Loading and Preprocessing:**  Raw data from three CSV files (student performance, video views, page interactions) is loaded using Pandas.  Feature selection focuses on `average cost`, `average intrinsic motivation`, and `average expectancy` for clustering.  While MinMaxScaler was considered, no explicit data scaling is currently implemented. Missing value handling and further preprocessing steps (e.g., outlier detection) are not explicitly detailed.

* **K-Means Clustering:** The K-Means algorithm from scikit-learn is used to cluster students based on the selected features.  The number of clusters (k=3) is determined visually using the elbow method by observing the within-cluster sum of squares (WCSS).

* **Cluster Analysis:** Descriptive statistics (mean, count) are calculated for each cluster to characterize the student groups identified.  These statistics include average performance scores, video viewing time, and page interaction metrics.

* **Data Visualization:** A 3D scatter plot using Matplotlib visualizes the clusters in the three-dimensional feature space.


## Tech Stack

* **NumPy:** For numerical computing.
* **Pandas:** For data manipulation and analysis.
* **Matplotlib:** For creating visualizations.
* **Scikit-learn:** For the K-Means clustering algorithm.


