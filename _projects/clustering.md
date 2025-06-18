---
layout: project
title: Clustering Analysis and 3D Visualization Dashboard
date: 2024-10-01
screenshot:
  src: /assets/img/projects/cluster_0_10s.gif
  srcset:
    1920w: /assets/img/projects/cluster_0_10s.gif
    960w: /assets/img/projects/cluster_0_10s.gif
    480w: /assets/img/projects/cluster_0_10s.gif
description: >
  A dashboard for analyzing datasets using K-means and Hierarchical clustering algorithms. This tool helps determine the optimal number of clusters and provides detailed 3d visualizations and comparisons of clustering results.  
  🎯 [Click here and Try it out (plz wait it waking up for a moment)](https://clustering-and-3d-plot.streamlit.app/) 
links:
  - title: Repository
    url: https://github.com/YannisCS/Clustering-and-3D-Visualization
featured: true
--- 

## Project Details

Here's more detailed information about it:

- **Multiple Data Sources**: Analyze built-in sample datasets or upload your own CSV files
- **Interactive 3D Visualizations**: Compare original data with K-means and Hierarchical clustering results
- **Optimal Cluster Detection**: Automated determination of the optimal number of clusters using:
  - Elbow Method
  - Silhouette Score
  - Calinski-Harabasz Method
  - Ensemble approach combining all methods  
- **Comprehensive Performance Metrics**:
  - Precision, Recall, Jaccard Index
  - Rand Index
  - Fowlkes-Mallows Score  
- **Custom Dataset Mapping**: For uploaded files, map columns to appropriate features

### Technology Stack

- Python 
- Streamlit
- Pandas 
- NumPy  
- Plotly 
- Scikit-learn 
- SciPy
- kneed 