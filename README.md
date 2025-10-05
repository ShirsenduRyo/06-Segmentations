# 06-Segmentations
An attempt to create a new segmentation technique

## Dataset Description

This project uses the **Bank Marketing dataset** (bank-full.csv) made publicly available by Moro et al. (2011).  
The dataset contains the results of **direct marketing campaigns** (phone calls) carried out by a Portuguese banking institution.  
The classification goal in the original paper was to predict whether a client would subscribe to a term deposit (`y` = yes/no).  

For this project, we focus on applying **segmentation algorithms** (e.g., K-Means, K-Means++, GMM, Hierarchical Clustering) to group clients into meaningful clusters.

### Dataset Details
- **Number of instances**: 45,211  
- **Number of attributes**: 17 input variables + 1 output (binary)  

#### Features:
- **Client attributes**:  
  - `age` : numeric  
  - `job` : categorical (e.g., admin, technician, unemployed)  
  - `marital` : categorical (married, single, divorced)  
  - `education` : categorical  
  - `default` : has credit in default? (yes/no)  
  - `housing` : has housing loan? (yes/no)  
  - `loan` : has personal loan? (yes/no)  

- **Campaign-related attributes**:  
  - `contact` : type of communication (cellular, telephone)  
  - `month`, `day_of_week` : last contact date  
  - `duration` : last contact duration (in seconds)  
  - `campaign` : number of contacts performed during this campaign  
  - `pdays` : days since last contact from a previous campaign  
  - `previous` : number of contacts before this campaign  
  - `poutcome` : outcome of the previous campaign  

- **Social & economic context attributes**:  
  - `emp.var.rate` : employment variation rate (quarterly indicator)  
  - `cons.price.idx` : consumer price index (monthly indicator)  
  - `cons.conf.idx` : consumer confidence index (monthly indicator)  
  - `euribor3m` : euribor 3-month rate  
  - `nr.employed` : number of employees  

- **Target variable**:  
  - `y` : has the client subscribed to a term deposit? (binary: `yes`, `no`)  

### Notes
- The dataset is **imbalanced** (~11% “yes” vs. ~89% “no”).  
- It contains a mix of **numeric, categorical, and temporal variables**.  
- For segmentation tasks, categorical variables usually need encoding (e.g., one-hot encoding).  
- `duration` is highly predictive but not known before the call ends (so often excluded in predictive tasks, though may be used in descriptive clustering).  

### Citation
Please cite the following paper if you use this dataset:  

> Moro, S., Laureano, R., & Cortez, P. (2011).  
> *Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology.*  
> In P. Novais et al. (Eds.), Proceedings of the European Simulation and Modelling Conference - ESM'2011, pp. 117-121, Guimarães, Portugal. EUROSIS.  
> [PDF](http://hdl.handle.net/1822/14838) | [BibTeX](http://www3.dsi.uminho.pt/pcortez/bib/2011-esm-1.txt)


## Similar Works

| **Algorithm** | **Authors** | **Silhoette Score** | **No. of Clusters** |
|:-----------:|:-----------:|:-----------:|
| K-Means | Abbas & Asghar | 0.54 | 4 |
| Hierarchical Clustering (Ward Linkage) | Mishra & Reddy | 0.49 | 4 |
| DBSCAN + Hierarchical (Hybrid) (Ward Linkage) | Sahu & Gupta | 0.67 | 6 |
| **Autoencoder + K-Means** | **Rahman & Akter** | **0.69** | **5**|
| XGBoost + K-Prototypes | Qureshi et al. | 0.64 | 5|
