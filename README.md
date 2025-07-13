Purpose:
This lab demonstrates data visualization, preprocessing, and statistical analysis techniques on a synthetic weather dataset using Python in a simulated Jupyter Notebook setting. It covers loading data, visualizing relationships and distributions, cleaning (missing, outliers), reducing data, scaling/discretization, and computing statistical measures.Key Insights:  Visualizations: No strong correlation between temperature and humidity; temperature distribution is normal with mean ~23°C after cleaning.  
Statistical Measures: Temperature has a mean of ~10.6°C range, low variance (8.36), and negligible correlation with humidity (-0.14), confirming independent variables in this dataset.

Challenges Faced or Decisions Made:  
Since the environment prohibits internet access, I generated a synthetic dataset instead of using real one from Kaggle. This allowed control over features like missing values and outliers.  
For visualizations, outputs are text-based, so insights are derived from data rather than visual inspection.  
Randomness in data generation and sampling means results are illustrative, not fixed. Decisions like filling with mean and using 1.5*IQR for outliers were chosen for standard practice.

