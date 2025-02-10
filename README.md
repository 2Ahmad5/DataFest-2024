# DataFest 2024 Winning Project: Student Performance Clustering
This project analyzes student performance data to identify distinct clusters of students based on their learning behaviors and engagement metrics.  The goal is to provide insights into student learning patterns to improve pedagogical strategies and support systems. The project was completed by Ahbab Abeer, Ahmad Choudhary, Darren Li, and Chirag Biswas, with assistance from Islam Tayeb for data processing.


<div align="center">
<img src="https://github.com/2Ahmad5/DataFest-2024/blob/main/data/image-1739221194746.png?raw=true" alt="image-1739221194746.png" />
</div>


## Features
* **K-Means Clustering:** Employs the K-Means algorithm to group students into distinct clusters based on key performance indicators.
* **Data Visualization:** Generates 3D scatter plots to visualize the clusters in three-dimensional space, allowing for a better understanding of cluster characteristics.
* **Data Aggregation:** Aggregates various data points (average attempts, EOC scores, engagement metrics, page views) per cluster to understand each group’s traits.
* **Student Identification:**  Provides the ability to identify the individual student IDs associated with each cluster.

## Usage
This project is implemented as a Jupyter Notebook.  To run the notebook:

1. Ensure you have the necessary dependencies installed (see below).
2. Clone the repository.
3. Navigate to the `src` directory.
4. Open `main.ipynb` in Jupyter Notebook or JupyterLab.
5. Execute the cells sequentially.

## Installation
1.  Clone the repository:
    ```bash
    git clone <repository_url>
    ```
2.  Create a virtual environment (recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Technologies Used
* **Python:** The primary programming language for data analysis and manipulation.
* **Jupyter Notebook:** An interactive computing environment used for creating and sharing the analysis.
* **NumPy:**  Provides support for large, multi-dimensional arrays and matrices.  Used for numerical computations.
* **Pandas:** Provides high-performance, easy-to-use data structures and data analysis tools. Used for data manipulation and cleaning.
* **Matplotlib:** Used for creating static, interactive, and animated visualizations in Python. Used to generate the 3D scatter plots.
* **Scikit-learn (sklearn):** A machine learning library.  The `KMeans` clustering algorithm is from this library.
* **MinMaxScaler (from sklearn.preprocessing):** Used for feature scaling in the data preprocessing step (although it was commented out in the provided code).

## Statistical Analysis
The project employs K-Means clustering to segment students into groups based on their performance on various metrics.  The input data includes:

* `avg_attempts`: Average number of attempts per question.
* `eoc_crct/poss`: Ratio of correct answers to total possible answers on end-of-course (EOC) assessments.
* `eoc_crct/atmp`: Ratio of correct answers to total attempts on EOC assessments.
* `avg_cost`: Average cost (likely related to cognitive load or effort).
* `avg_expectance`: Average expectancy (likely related to student perceived success rate).
* `avg_intrinsic`: Average intrinsic motivation.
* `avg_utility`: Average utility (likely related to perceived usefulness).
* `num_reviewed`: Number of pages/resources reviewed.
* `num_retry`: Number of retry attempts.
* `Sum engaged`: Total engagement time.


The K-Means algorithm iteratively assigns data points to clusters to minimize the within-cluster sum of squares (WCSS). The optimal number of clusters was determined using the elbow method (although the ElbowVisualizer code is commented out).  The resulting clusters are then visualized using 3D scatter plots, showing the distribution of students across the `avg_cost`, `avg_intrinsic`, and `avg_expectance` dimensions.  The average values of all features are then calculated for each cluster, providing a summary of each cluster's characteristics. Finally, individual student IDs are assigned to their respective clusters allowing further targeted analysis.

## Dependancies
To install the python libraries used in the project, you'll need to have Python 3 installed.  Then, use pip to install each package individually:

```bash
pip install numpy pandas matplotlib scikit-learn
```

*README.md was made with [Etchr](https://etchr.dev)*