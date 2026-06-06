# Customer Segmentation using K-Means & DBSCAN

Unsupervised learning project to segment customers based on purchasing behavior, demographics, and campaign responses.

## Dataset

- Customer data (ID, Birth Year, Income, Children, Spending, Campaign acceptance)
- Target: Group customers into meaningful segments

## Preprocessing & Feature Engineering

- Handle missing values (Income imputed with mean)
- Create new features:
  - Age (from Year_Birth)
  - Total_Children (Kidhome + Teenhome)
  - AcceptedCmp_Total (sum of 5 campaign responses)
  - Total_Mnt (sum of spending on 6 product categories)
- Encode categorical variables (LabelEncoder)
- Drop unnecessary columns (ID, Dt_Customer)

## Exploratory Analysis

- Distributions: Age, Income, Total Spending, Kidhome
- Income vs Kidhome scatter
- Correlation heatmap after feature engineering

## Clustering Algorithms

### K-Means
- StandardScaler for normalization
- 5 clusters (based on business logic)
- Silhouette Score for evaluation
- PCA visualization (2D)

### DBSCAN
- eps = 2, min_samples = 5
- Handles noise points automatically
- Silhouette Score (excluding noise)

## Results

- K-Means Silhouette Score: ~0.17
- DBSCAN Silhouette Score: ~0.15 (excluding noise)

