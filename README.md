# Project 2: Mall Customer Segmentation

##  Team Members
* Shuai Liu
* Zhuoxi Zhong
* Sinan Huang

##  Project Goal

> The purpose is to analyze the dataset "mall customers" and discover patterns and relationships in retail data, such as how income and age relate to spending behavior, how distinct customer groups emerge, and how those groups can guide marketing or service strategies.

##  Dataset

* **Name:** Mall Customers
* **Source:** [Kaggle](https://www.kaggle.com/datasets/shwetabh123/mall-customers)
* **Features Used for Clustering:**
    * `Annual Income (k$)`
    * `Spending Score (1-100)`

##  Project Pipeline
│
├── 1.  Data Exploration
│   ├── Correlation Heatmap
│   ├── Feature Distributions
│   └── Pair Plots
│
└── 2.  Clustering Analysis
    │
    ├──  K-Means Clustering
    │   ├── Elbow Method 
    │   └── Visualization 
    │
    ├──  Hierarchical Clustering
    │   ├── Dendrogram 
    │   └── Visualization 
    │
    └──  density DBSCAN
        ├── K-Distance Plot 
        └── Visualization 
##  Results & Visualizations

### 1. Exploratory Data Analysis (EDA)

| Correlation Heatmap | Feature Distributions |
| :---: | :---: |
| `` | `` |

### 2. Clustering Model Comparison

We implemented three distinct algorithms to understand the customer groups from different perspectives.

| K-Means (K=5) | Hierarchical (K=5) | DBSCAN |
| :---: | :---: | :---: |
| `` | `` | `` |
| K-Means found 5 clear, spherical clusters. | Hierarchical clustering found 5 very similar clusters to K-Means. | DBSCAN successfully identified core groups and flagged several points as "noise" (in black). |

**Plots Used for Parameter Selection:**

| K-Means (Elbow Plot) | Hierarchical (Dendrogram) | DBSCAN (K-Distance Plot) |
| :---: | :---: | :---: |
| `` | `` | `` |

##  How to Run

1.  **Dowload the file and unpack it or use git**
    ```bash
    git clone https://github.com/Hsin-thefirst/Datamining-Project-2.git
    cd Datamining-Project-2
    ```

2.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Notebook**
    Open and run the .ipynb files.

### `requirements.txt`
```text
pandas
numpy
matplotlib
seaborn
scikit-learn
kneed