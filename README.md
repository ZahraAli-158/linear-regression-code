# linear-regression-code
  1. Loading the Data:
	•	Reads a CSV file containing two columns X and Y.
	2.	Basic Exploration:
	•	Shows first few (head), last few (tail), and random (sample) rows.
	•	Checks shape, data types, and statistics like mean, min, max (describe() and info()).
	3.	Missing Values:
	•	Checks for null values and fills them with mean if needed.
	•	Drops rows with missing values as another step.
	4.	Duplicates:
	•	Removes any duplicate rows from the data.
	5.	Outlier Detection:
	•	Uses the IQR method to detect and remove outliers.
	•	Box plots show data before and after outlier removal.
	6.	Data Normalization:
	•	Applies MinMaxScaler to scale values between 0 and 1.
	•	Also shows StandardScaler which standardizes the data (mean=0, std=1).
