Task 1: Data Quality Issues
The dataset contains no missing values. The numerical columns (math score, reading score, writing score) are already in the correct format. The categorical columns are stored as object type, which is appropriate. Therefore, no major data quality issues were found.

Task 2: Missing Value Strategy
Median imputation was used to handle missing values in math score. This method is preferred because it is more robust to outliers and provides a better representation of the central value compared to the mean.

Task 3: Outliers (IQR)
Outliers were detected using the IQR method. Values below Q1 − 1.5×IQR or above Q3 + 1.5×IQR were considered outliers. These outliers were handled by removing them to reduce their impact on the analysis.

Task 4: Normalization
Min-Max normalization scales values between 0 and 1, preserving the relative relationships between data points. Z-score normalization standardizes the data to have a mean of 0 and a standard deviation of 1. Both methods help ensure that features are on a similar scale and prevent one feature from dominating others.

Task 5: PCA
The correlation between math score and reading score is approximately 0.82, indicating a strong positive relationship. Since the features are highly correlated, PCA was applied to reduce redundancy and transform them into principal components while preserving most of the variance.
PCA reduces dimensionality by converting the original features into new uncorrelated components. The first principal component captures the maximum variance, while the second captures the remaining variance.
