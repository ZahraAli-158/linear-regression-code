# linear-regression-code
1. Importing Libraries and Reading the Dataset
The notebook begins by importing the pandas library, which is commonly used for data manipulation and analysis. The dataset is then read using the read_csv() function from a local file path and stored in a DataFrame for further processing.

2. Initial Data Exploration
To get an overview of the dataset, the first few rows (head()), the last few rows (tail()), and a few random samples (sample()) are displayed. The shape (shape) and number of dimensions (ndim) of the dataset are checked to understand its structure. Summary statistics like mean, min, max, and standard deviation are obtained using the describe() function.

3. Checking for Missing Values
The info() function is used to understand the data types and non-null counts of each column. The presence of missing values is checked using isnull() and sum(). The total number of missing values is calculated with isnull().sum().sum() to ensure the dataset is clean and ready for analysis.

4. Handling Missing Data
If any missing values are present, the code uses the mean() of numerical columns to fill them using the fillna() method. This step ensures that missing data does not negatively impact model training. After imputation, the cleaned numeric and non-numeric data are combined again using concat().

5. Removing Duplicates and Verifying Cleaned Data
The dataset is further cleaned by removing any duplicate rows using the drop_duplicates() method. After this step, the shape of the dataset is checked again to confirm changes. The goal here is to ensure the data is unique and free of redundancy.

6. Outlier Detection and Removal
To handle outliers, the Interquartile Range (IQR) method is applied. The first (Q1) and third quartiles (Q3) are computed, and the IQR is calculated. Rows with values outside the acceptable range (Q1 - 1.5*IQR or Q3 + 1.5*IQR) are identified as outliers and removed. Boxplots are created before and after outlier removal to visualize the effect.

7. Feature Scaling
In the final part of the notebook, a second dataset (Thyroid_Diff.csv) is loaded to demonstrate feature scaling. Both Min-Max Scaling (MinMaxScaler) and Standardization (StandardScaler) are applied to the numeric features to normalize the data. This is important for ensuring features are on the same scale before applying machine learning models.
