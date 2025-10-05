# 06-Segmentations

<!-- #### Features:
- **Client attributes**:  
  - `age` : numeric  
  - `job` : categorical (e.g., admin, technician, unemployed)  
  - `marital` : categorical (married, single, divorced)  
  - `education` : categorical  
  - `default` : has credit in default? (yes/no)  
  - `housing` : has housing loan? (yes/no)  
  - `loan` : has personal loan? (yes/no)   -->

## K-Means

| **Name** | **Silhouette Score** | **No. of Clusters** | **Description** |
|:-----------:|:-----------:|:-----------:|:-------------------:|
| Simple |  | 0.0919 | 3 | Simple Data, no changes |
| Filtered through Correlations | 0.1637 | 7 | Features in the feature pair with high corr, and the one with a lower corr. with target(y), filtered |
| VIF /& Corr. Filters | 0.1810 | 7 | The above filter, along with extra filtra for VIF, to counter multi-Collinearity |




