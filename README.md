This lab demonstrates the application of data visualization, preprocessing, and statistical analysis techniques using Jupyter Notebook. A synthetic weather dataset was created to explore data patterns, clean inconsistencies (such as missing values and outliers), reduce dataset size, scale and discretize features, and compute key statistical measures. The dataset includes variables like Date, Temperature, Humidity, Rainfall, and WindSpeed for 20 days in January 2024, with intentional missing values and an outlier introduced for demonstration.Key Insights from Visualizations and Statistical MeasuresVisualizations:Scatter Plot (Temperature vs Humidity): The plot reveals a weak positive relationship between temperature and humidity, with points scattered across the range (temperature 15–50°C, humidity 45–75%). No strong linear trend is evident, consistent with the low correlation coefficient of 0.1388.
Histogram (Temperature Distribution): The distribution is approximately normal but right-skewed, with the highest frequency (around 8) in the 20–25°C bin. Frequencies decrease toward higher temperatures, with sparse data in 35–40°C and a single outlier bin at 45–50°C before removal.

Statistical Measures (computed after handling missing values and removing the outlier, on 19 rows):

General Overview: 
The dataset has 19 entries post-cleaning. Temperature ranges from 15.87°C to 33.11°C, Humidity from 48.51% to 74.25%, Rainfall from 0.48 to 9.89 mm/in, and WindSpeed from 1.01 to 15.55 m/s.

Central Tendency (Temperature): 
Minimum: 15.87°C, Maximum: 33.11°C, Mean: 24.69°C, Median: 23.70°C, Mode: 15.87°C (indicating mostly unique values).

Dispersion (Temperature): 17.25°C, Quartile 1 (Q1): 22.64°C, Quartile 3 (Q3): 26.80°C, Interquartile Range (IQR): 4.16°C, Variance: 22.27, Standard Deviation: 4.72°C.

Correlation Analysis: 
Temperature shows weak correlations with Humidity (0.14), negligible with Rainfall (-0.0005), and moderate with WindSpeed (0.34). Other pairs like Humidity-Rainfall (-0.04) are also low, suggesting independent variables in this dataset.

Challenges Faced or Decisions MadeChallenges:
The synthetic nature of the data (generated via NumPy random functions without a seed) results in variability across runs, making exact reproduction tricky. Identifying and managing the outlier (temperature of 50°C) skewed initial visualizations, and missing values (one each in Temperature, Humidity, and Rainfall) required careful imputation to avoid distorting statistics. The code interpreter environment limits external data access, so a synthetic dataset was necessary.

Decisions: 
Missing values were filled using column means (e.g., Temperature NaN replaced with ~24.69°C). Outliers were detected and removed using the IQR method (1.5 × IQR bounds: 14.53–36.24°C), eliminating one row. Data reduction involved sampling to 10 rows and dropping less relevant columns (Rainfall, WindSpeed). Scaling used Min-Max normalization for Temperature (0–1 range), and discretization binned it into 'Low', 'Medium', 'High' categories for categorical analysis. Statistical analysis was performed post-cleaning but pre-reduction to capture full insights, with visualizations highlighting pre- and post-processing differences. All code was modularized into separate Jupyter cells for step-by-step execution and debugging.

