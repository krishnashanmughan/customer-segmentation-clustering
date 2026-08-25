# Customer Segmentation (Clustering)

Segments ~2.2K grocery-store customers into distinct, actionable groups
using unsupervised learning — turning raw transaction and demographic
data into marketing insight.

## Approach
- **Feature Engineering:** derived Age, Customer tenure ("Customer_For"),
  total Spend, and household features from raw fields.
- **EDA:** PDF plots, boxplots (with outlier removal on Income/Age),
  and a correlation matrix.
- **Preprocessing:** encoding + StandardScaler, then **PCA** to 3
  components for visualization and clustering.
- **Clustering:** compared **K-Means++** (Elbow + Dunn Index), **DBSCAN**
  (grid-searched on eps/min_samples), and **Hierarchical/Agglomerative**
  (grid-searched, silhouette-scored).
- **Selection:** K-Means with k=4 gave the cleanest, best-separated groups.

## Results
4 clear segments along income vs. spending, e.g.:
- High income / high spend  →  star customers
- Low income / low spend     →  budget-conscious
- (plus two mid-tier groups)

Profiled each segment and reviewed past campaign response to guide
targeted marketing.

## Tech Stack
Python · pandas · scikit-learn · SciPy · seaborn · matplotlib

## License
MIT
