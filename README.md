# Palmer-Penguins

### Overview

The Palmer Penguins Dataset consists of data on penguin species from the Palmer Archipelago in Antarctica. The dataset includes various physical attributes like body mass, flipper length, and culmen dimensions for different penguin species. This dataset is great for exploratory data analysis, statistical modeling, and machine learning.

### Objectives

Data Exploration: 
- Understanding the structure, missing values, and outliers in the dataset.

Data Cleaning:
- Impute missing values (median imputation for numerical features, mode imputation for categorical features).
- Remove outliers using Z-scores.

Data Transformation:
- One-hot encode the categorical variable species.

Data Analysis:
- Investigate relationships between physical characteristics and species.
- Explore the distribution of penguins across islands.
- Create visualizations to compare species and their characteristics.

### Datasets

penguins_size.csv - This simplified version of the dataset contains the following variables:
- species: The species of penguin (Adelie, Chinstrap, Gentoo).
- culmen_length_mm: The length of the penguin’s culmen (in mm).
- culmen_depth_mm: The depth of the penguin’s culmen (in mm).
- flipper_length_mm: The length of the penguin’s flipper (in mm).
- body_mass_g: The body mass of the penguin (in grams).
- island: The island where the penguin was observed (Biscoe, Dream, Torgersen).
- sex: The sex of the penguin (male or female).

penguins_lter.csv - The original combined data for the three penguin species, aggregated from individual datasets.

### Data Cleaning & Imputation

1. Missing Values:
- Numerical columns (culmen length, culmen depth, flipper length, body mass) are imputed with the species-specific median values.
- Categorical column sex is imputed with the mode value.

2. Outlier Removal:
- Z-scores are calculated to identify outliers in the numerical columns. Data points with Z-scores greater than 3 are removed.

3. One-Hot Encoding:
- The species column is one-hot encoded into binary columns for Chinstrap and Gentoo species. The Adelie species serves as the reference group.
  
### Key Visualizations

- Body Mass Distribution: A histogram to visualize the distribution of penguin body mass across the dataset.
- Boxplots by Species: Boxplots for comparing the body mass distribution for different species (Gentoo and Chinstrap).
- Species Comparison: A side-by-side boxplot comparing the body mass of Chinstrap and Gentoo species.
- Species Distribution Across Islands: Countplots to visualize the distribution of species across the three islands.

### Correlation Analysis

A heatmap was generated to display the correlation between the numerical features (culmen length, culmen depth, flipper length, and body mass). Significant correlations were found between:

- flipper length and body mass (strong positive correlation).
- culmen length and body mass (moderate positive correlation).

### Species Distribution Across Islands

A groupby operation was performed to calculate the number of penguins of each species present on each island. The results show that Gentoo penguins are predominantly found on Biscoe and Dream islands, while Chinstrap penguins are mainly found on Dream island.

### Key Findings

- Missing Values: The dataset had missing values in numerical features (culmen dimensions, flipper length, and body mass) and the categorical feature sex.

- Outliers: Outliers were identified and removed to improve data quality, ensuring better modeling performance.

- Correlation Analysis:
  - Flipper length showed the strongest positive correlation with body mass (r = 0.87).
  - Culmen length had a moderate positive correlation with body mass (r = 0.60).
  - Culmen depth exhibited a weak negative correlation with body mass.

- Species Distribution Across Islands:
  - Gentoo penguins were predominantly found on Biscoe and Dream islands.
  - Chinstrap penguins were mainly observed on Dream island.

- One-Hot Encoding: Binary columns for Chinstrap and Gentoo species were created for effective model integration.

### Future Work

Advanced Modeling:
- Build classification models such as Logistic Regression, Random Forest, and Gradient Boosting to predict penguin species.
- Use regression models to predict numerical characteristics like body mass.

Hyperparameter Optimization:
- Experiment with tuning model hyperparameters to improve accuracy and performance.

Feature Engineering:
- Create interaction terms between culmen dimensions and flipper length to capture non-linear relationships.

Cross-Validation:
- Perform k-fold cross-validation to ensure robust evaluation of models.

Comparative Analysis:
- Compare the penguin dataset with similar datasets from different regions to identify global trends in penguin morphology.

### Source

https://www.kaggle.com/datasets/parulpandey/palmer-archipelago-antarctica-penguin-data
