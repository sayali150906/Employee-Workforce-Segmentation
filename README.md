# Workforce Segmentation and Retention-Risk Analytics

Segmentation of the IBM HR Analytics workforce (1,470 employees) with PCA, K-Means, multi-linkage Hierarchical clustering, department sub-segments and model-based retention-risk tiers.

## Repository contents
| File | Description |
|---|---|
| `Workforce_Segmentation_Notebook.ipynb` | Full notebook (feature engineering, PCA, clustering, analysis) |
| `Employee_Segmentation_Report.docx` | Segmentation findings and recommendations |
| `PCA_Summary.docx` | PCA variance, loadings and visualisation |
| `Workforce_Analytics_Dashboard.html` | Interactive dashboard with a department filter |

## Approach
- 20 features including 4 engineered ones (IncomeToLevel, TenureRatio, PromotionGap, SatisfactionIndex)
- PCA to 13 components (about 93% of variance)
- K-Means with k = 4; Hierarchical clustering compared across Ward, Average and Complete linkage
- Separate 3-group K-Means inside each department
- Performance index (rating, involvement, salary hike, training) split into three groups
- Out-of-fold logistic-regression risk scores to form High, Medium and Low retention-risk tiers

## Key findings
- Four segments: Entry-Level Early Career, Experienced Newcomers, Stable Mid-Career, Senior Veterans
- Entry-Level Early Career has 23.5% attrition (company average 16.1%)
- The High risk tier (top 20% of scores) has 52% attrition and holds about 65% of leavers
- Low performers leave more often (21.8%) than core and high performers (13.3%)

## How to run
1. Upload `Workforce_Segmentation_Notebook.ipynb` to Google Colab.
2. Click Runtime > Run all (the dataset downloads automatically).
3. Open `Workforce_Analytics_Dashboard.html` in a browser.
