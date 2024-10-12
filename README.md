# **Exploratory Data Analysis (EDA) on Car Sales Data**

**Objective**

The primary objective of this project is to perform exploratory data analysis (EDA) on a dataset containing information about cars and their associated sales prices (MSRP). This analysis aims to uncover patterns, spot anomalies, and establish relationships between various attributes. A linear regression analysis was performed to evaluate the predictive power of one variable (horsepower) on the sales price.

**About the Dataset**

The dataset P5-CarData.csv consists of 11,925 entries across 16 columns, detailing various characteristics of cars.

**Key Features**

Make: Manufacturer of the car
Model: Specific model name
Year: Year of manufacture
HP: Engine horsepower
Cylinders: Number of engine cylinders
Transmission: Type of transmission (automatic/manual)
Driven_Wheels: Type of drivetrain
MPG_H: Highway miles per gallon
MPG_C: City miles per gallon
Popularity: Popularity score
MSRP: Manufacturer's suggested retail price

**Methodology**

Data Importation:

Utilized Pandas to read the CSV file into a DataFrame.
Data Inspection:

Used .info() to assess the structure and data types within the dataset.
Data Cleaning:

Dropped columns deemed insignificant for analysis: 'Engine Fuel Type', 'Market Category', 'Vehicle Style', 'Number of Doors', 'Vehicle Size'.
Renamed columns for clarity: 'Engine HP' to 'HP', 'Engine Cylinders' to 'Cylinders', etc.
Checked for and removed duplicate entries, leading to a reduced dataset of 10,925 rows.
Identified and addressed missing values:
Filled missing values in the 'Cylinders' column with zeros.
Filled missing values in the 'HP' column with the mean horsepower.
Descriptive Statistics:

Generated summary statistics using the .describe() method.
Calculated maximum horsepower, minimum city MPG, maximum highway MPG, and maximum MSRP.
Outlier Detection and Removal:

Utilized box plots to visually assess the distribution of key variables and identify outliers.
Applied the Interquartile Range (IQR) method to set cutoff values for detecting outliers in 'HP' and 'MSRP', leading to a refined dataset of 4,065 rows after outlier removal.

**Data Visualization:**

Created histograms to visualize the distributions of 'HP' and 'MSRP'.
Developed box plots to illustrate the cleaned data distributions for 'HP' and 'MSRP'.
Generated bar plots to show the count of each car make in the dataset.

**Correlation and Regression Analysis:**

Created a pairplot to visualize relationships between numeric variables.
Conducted a linear regression analysis to explore the relationship between horsepower (HP) and MSRP, calculating the R-squared value to assess the model's explanatory power.
Improved the regression model by filtering out remaining low-end MSRP outliers, resulting in an enhanced R-squared value.

**Results**

Summary Statistics
Maximum Horsepower (HP): 1,001
Minimum City MPG: 7
Maximum Highway MPG: 354
Maximum MSRP: $2,065,902
Outlier Identification
HP Cutoff Values:
Lower: -19.5
Upper: 496.5
MSRP Cutoff Values:
Lower: -9,962.5
Upper: 75,257.5

**Visualization Outcomes**

Histograms showed the distribution of horsepower and MSRP, highlighting skewness in the data.
Box Plots visually confirmed the removal of outliers, resulting in more representative data distributions.
Bar Plot indicated the popularity of different car makes, with Chevrolet (401), Ford (418), and Toyota (273) being the most prevalent in the dataset.

**Regression Analysis**

Initial R-squared: 0.231075 (before filtering outliers).
Improved R-squared (after filtering): 0.277382, indicating a better fit for the model after removing low-end MSRP outliers.

**Conclusion**

This exploratory data analysis has provided valuable insights into the car sales dataset. The EDA techniques employed allowed for effective identification of patterns, anomalies, and relationships between variables. The linear regression analysis demonstrated that horsepower has a measurable impact on sales price, albeit with room for improvement in the model's predictive capabilities. Future analyses could further enhance the model by incorporating additional relevant variables or exploring advanced regression techniques.


