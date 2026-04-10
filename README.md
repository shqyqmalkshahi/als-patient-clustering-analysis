# als-patient-clustering-analysis
Applied K-Means clustering and PCA to healthcare data to identify patient subgroups, using feature engineering, scaling, and model evaluation techniques.

# ALS Patient Clustering Analysis

## Overview
This project applies unsupervised machine learning techniques to cluster ALS patients based on clinical and laboratory features. The goal is to identify meaningful patient subgroups and uncover hidden patterns in high-dimensional healthcare data.

---

## Objective
To identify patient groupings using K-Means clustering and evaluate cluster quality, while using PCA to visualize complex patterns in reduced dimensions.

---

## Dataset
- ALS clinical dataset  
- 2,223 patient records  
- 100+ clinical features (lab values, functional scores, vital signs) :contentReference[oaicite:1]{index=1}  

---

## Methodology

### Data Preparation
- Removed identifier columns (ID, SubjectID)  
- Removed redundant features using correlation filtering (>|0.90|)  
- Dropped constant variables  
- Handled missing values using median imputation  
- Standardized all numerical features using z-score scaling  

---

### Feature Engineering
- Selected numeric clinical variables  
- Reduced dimensional redundancy  
- Prepared dataset for clustering  

---

### Clustering (K-Means)
- Tested k values from 2 to 10  
- Used silhouette score to determine optimal cluster count  
- Final model:
  - k = 2  
  - Silhouette score = 0.081 :contentReference[oaicite:2]{index=2}  

---

### Dimensionality Reduction (PCA)
- Reduced data to 2 principal components  
- Captured ~18% of total variance  
- Used for visualization of cluster separation :contentReference[oaicite:3]{index=3}  

---

### Cluster Analysis
- Cluster sizes:
  - Cluster 0 → 1105 patients  
  - Cluster 1 → 1118 patients :contentReference[oaicite:4]{index=4}  

- Generated cluster profiles using feature averages  
- Compared clinical variables across clusters  

---

## Key Insights

- Patients can be grouped into two distinct clusters based on clinical features  
- Clusters show differences in ALS functional scores and lab measurements  
- Overlap between clusters is expected due to complexity of medical data  
- PCA visualization shows partial separation between groups  
- Clustering reveals potential patient profiles or disease patterns  

---

## Model Evaluation

- Silhouette Score: 0.081  
  - Indicates weak but meaningful structure (common in healthcare data)  
- PCA explained variance: ~18%  
  - Suggests high complexity and dimensionality  

---

## Business / Research Value

- Supports exploratory patient segmentation  
- Helps identify potential disease progression patterns  
- Provides foundation for personalized treatment strategies  
- Can guide further clinical research  

---

## Limitations

- Low silhouette score indicates overlapping clusters  
- PCA captures limited variance  
- Clusters are not clinically validated  
- Results require expert interpretation  

---

## Future Improvements

- Apply advanced clustering (Gaussian Mixture, DBSCAN)  
- Test cluster stability across multiple runs  
- Incorporate domain knowledge from clinicians  
- Use additional feature selection techniques  

---

## Project Structure

- `.ipynb` → clustering and analysis  
- `.pdf` → full report  
- `.csv` → PCA-transformed dataset  

---

## Tools Used

- Python  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  

---

## Author
Shaghayegh Malekshahi  
Master’s in Data Science  
