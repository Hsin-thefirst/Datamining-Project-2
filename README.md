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
├── 1.  Data Exploration(dataset overview)  
│   ├── Correlation Heatmap  
│   ├── Feature Distributions  
│   └── Pair Plots  
│  
└── 2.  Clustering Analysis  
│   │  
│  ├──  K-Means Clustering  
│   │   ├── Elbow Method   
│   │   └── Visualization   
│   │  
│   ├──  Hierarchical Clustering  
│   │   ├── Dendrogram   
│   │   └── Visualization   
│   │  
│   └──  density DBSCAN  
│       ├── K-Distance Plot   
│       └── Visualization 
│  
└── 3.  Overall model evaluation and comparison

##  Results & Visualizations

### 1. Exploratory Data Analysis (EDA)

| Correlation Heatmap | Feature Distributions | ...  

### 2. Clustering Model Comparison

We implemented three distinct algorithms to understand the customer groups from different perspectives.

| K-Means (K=5) | Hierarchical (K=5) | DBSCAN |  
| K-Means found 5 clear, spherical clusters. | Hierarchical clustering found 5 very similar clusters to K-Means. | DBSCAN successfully identified core groups and flagged several points as "noise" (in black). |

### 3. Model Evaluation & Comparison

#### Internal Metrics Comparison
* **Conclusion:** All models (DBSCAN, K-Means, Hierarchical, GMM) performed excellently on the Silhouette Score (~0.55), indicating a clear cluster structure. DBSCAN performed best on the Davies-Bouldin Index (lower is better).

| Model | Silhouette (Higher) | Calinski-Harabasz (Higher) | Davies-Bouldin (Lower) |
| :--- | :---: | :---: | :---: |
| **K-Means (K=5)** | 0.555 | 248.65 | 0.572 |
| **Hierarchical (K=5)**| 0.554 | 244.41 | 0.578 |
| **DBSCAN (Optimal)** | **0.558** | 245.36 | **0.511** |
| **GMM (K=5)** | 0.554 | 244.94 | 0.576 |

#### PCA 2D Visualization Comparison
To compare all models on a 2D plane, we used PCA for dimensionality reduction. This clearly shows how different algorithms partition the data.

#### Similarity Matrix (Distance Matrix)
The heatmap will display the (200x200) distance matrix, sorted by cluster label. The **5 dark squares** along the diagonal clearly indicate that intra-cluster distance is low (high similarity), while the brighter areas indicate high inter-cluster distance.

**Plots Used for Parameter Selection:**

| K-Means (Elbow Plot) | Hierarchical (Dendrogram) | DBSCAN (K-Distance Plot) |

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