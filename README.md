# MNIST-Unsupervised-Clustering
# MNIST Unsupervised Learning: Comparative Analysis of Clustering Techniques

## Overview

This project presents a comparative analysis of three unsupervised learning clustering techniques:

- K-Means
- DBSCAN
- Spectral Clustering

The experiments are performed on the MNIST handwritten digit dataset. Since MNIST is a high-dimensional dataset with 784 pixel features per image, dimensionality reduction techniques are applied before clustering.

## Objectives

1. To study unsupervised clustering techniques on high-dimensional data.
2. To compare K-Means, DBSCAN and Spectral Clustering.
3. To apply PCA, t-SNE and UMAP for dimensionality reduction and visualization.
4. To evaluate clustering performance using ARI, NMI, Silhouette Score and Davies-Bouldin Index.
5. To compare the computational time of the clustering algorithms.

## Dataset

The project uses the standard MNIST handwritten digit dataset.

- Number of images: 70,000
- Number of classes: 10
- Image size: 28 × 28 pixels
- Features per image: 784
- Classes: digits 0–9

The dataset is automatically downloaded using `fetch_openml()` in the Python notebook.

## Methodology

The overall workflow is:

```text
MNIST Dataset
      ↓
Data Preprocessing
      ↓
Standardization
      ↓
Dimensionality Reduction
      ↓
PCA / t-SNE / UMAP
      ↓
Clustering
      ↓
K-Means / DBSCAN / Spectral Clustering
      ↓
Evaluation
      ↓
ARI / NMI / Silhouette / Davies-Bouldin
      ↓
Comparison
```

## Data Preprocessing

The MNIST images contain 784 pixel features.

The following preprocessing steps are performed:

1. Load MNIST dataset.
2. Select a practical subset for computation.
3. Standardize the features using `StandardScaler`.
4. Reduce dimensionality using PCA and UMAP.
5. Use t-SNE and UMAP for two-dimensional visualization.

## Clustering Algorithms

### K-Means

K-Means partitions the dataset into a predefined number of clusters. Since MNIST contains ten digit classes, ten clusters are used.

### DBSCAN

DBSCAN is a density-based clustering algorithm. It can identify dense regions and classify isolated points as noise.

### Spectral Clustering

Spectral Clustering uses relationships between neighboring data points to identify clusters. It can capture complex structures but is more computationally expensive.

## Evaluation Metrics

| Metric | Description | Better Value |
|---|---|---|
| ARI | Agreement between predicted clusters and true labels | Higher |
| NMI | Shared information between clusters and true labels | Higher |
| Silhouette Score | Cluster compactness and separation | Higher |
| Davies-Bouldin Index | Similarity between clusters | Lower |
| Execution Time | Computational efficiency | Lower |

## Results

The notebook generates a comparison table containing:

- Adjusted Rand Index
- Normalized Mutual Information
- Silhouette Score
- Davies-Bouldin Index
- Execution Time

The exact numerical results depend on the sample size, parameters and execution environment.

## Project Structure

```text
MNIST-Unsupervised-Clustering/
│
├── README.md
├── requirements.txt
├── MNIST_Unsupervised_Clustering.ipynb
│
├── dataset/
│   └── README.md
│
├── results/
│   ├── results.csv
│   ├── ari_comparison.png
│   ├── nmi_comparison.png
│   ├── silhouette_comparison.png
│   └── execution_time.png
│
└── .gitignore
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/MNIST-Unsupervised-Clustering.git
```

Move into the project directory:

```bash
cd MNIST-Unsupervised-Clustering
```

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

## Running the Project

The project can be executed using Google Colab or Jupyter Notebook.

Open:

```text
MNIST_Unsupervised_Clustering.ipynb
```

Run the cells sequentially.

The MNIST dataset will be downloaded automatically using OpenML.

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- UMAP

## Reference

This implementation is based on the methodology presented in:

**"Unsupervised Learning: Comparative Analysis of Clustering Techniques on High-Dimensional Data"**

The implementation is a practical reproduction/extension and does not claim to reproduce the paper's exact numerical results.

## Author

**Sanika**

Computer Engineering  
Pimpri Chinchwad College of Engineering
