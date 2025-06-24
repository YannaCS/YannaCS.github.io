---
layout: project
title: Clustering Analysis and 3D Visualization Dashboard
date: 2024-10-01
screenshot:
  src: /assets/img/projects/cluster/cluster_0_10s.gif
  srcset:
    1920w: /assets/img/projects/cluster/cluster_0_10s.gif
    960w: /assets/img/projects/cluster/cluster_0_10s.gif
    480w: /assets/img/projects/cluster/cluster_0_10s.gif
description: >
  A dashboard for analyzing datasets by using K-means and Hierarchical clustering algorithms. This tool helps determine the <b>optimal number of clusters</b> and provides detailed <b>3d visualizations</b> and comparisons of clustering results.  
  <br><br><br>
  
  <a href="https://clustering-and-3d-plot.streamlit.app/" target="_blank" onclick="event.stopPropagation();">🎯Click here and Try it out </a>  
  
  (plz get it back up and wait it waking up for a moment)
links:
  - title: Repository
    url: https://github.com/YannisCS/Clustering-and-3D-Visualization
featured: true
--- 

## Project Details

Here's more detailed information about it:

- **Multiple Data Sources**: Analyze built-in sample datasets or upload your own CSV files
- **Custom Dataset Mapping**: For uploaded files, map columns to appropriate features  
  <img src="{{ '/assets/img/projects/cluster/cluster_15_25s.gif' | relative_url }}" alt="" style="width: 100%; max-width: 750px;">
- **Interactive 3D Visualizations**: Compare original data with K-means and Hierarchical clustering results
- **Optimal Cluster Detection**: Automated determination of the optimal number of clusters using:
  - Elbow Method
  - Silhouette Score
  - Calinski-Harabasz Method
  - Ensemble approach combining all methods  
  <img src="{{ '/assets/img/projects/cluster/cluster_27_37s.gif' | relative_url }}" alt="" style="width: 100%; max-width: 750px;">

- **Comprehensive Performance Metrics**:
  - Precision, Recall, Jaccard Index
  - Rand Index
  - Fowlkes-Mallows Score  
  <img src="{{ '/assets/img/projects/cluster/cluster_38_48s.gif' | relative_url }}" alt="" style="width: 100%; max-width: 750px;">



### Technology Stack

- Python 
- Streamlit
- Pandas 
- NumPy  
- Plotly 
- Scikit-learn 
- SciPy
- kneed 