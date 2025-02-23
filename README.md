# Palmer Penguins

### Overview

The Palmer Penguins Dataset contains data on penguin species from the Palmer Archipelago in Antarctica. This dataset includes physical attributes such as body mass, flipper length, and culmen dimensions for three penguin species: Adelie, Chinstrap, and Gentoo. The project focuses on exploratory data analysis (EDA), data cleaning, feature transformation, and building a machine learning model to classify penguin species based on these physical attributes.

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

Machine Learning:
- Train a model to classify penguin species based on physical attributes.
- Evaluate model performance using precision, recall, and F1-score.
- Identify the most important features influencing the classification.

### EDA Questions

I want to answer the following questions:

1. What is the distribution of penguin body mass across the dataset?
2. How does body mass vary between different species?
3. What is the correlation between physical features of the penguins (culmen length, culmen depth, flipper length, and body mass)?
4. How are penguin species distributed across different islands?
5. Are there any patterns or differences in the body mass of penguins based on species?

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

![screenshot-github com-2025 01 27-13_35_33](https://github.com/user-attachments/assets/054a55cf-6894-4fbd-9b87-8a9f05c92d43)

- Body Mass Distribution: A histogram to visualize the distribution of penguin body mass across the dataset.
- Boxplots by Species: Boxplots for comparing the body mass distribution for different species (Gentoo and Chinstrap).
- Species Comparison: A side-by-side boxplot comparing the body mass of Chinstrap and Gentoo species.
- Species Distribution Across Islands: Countplots to visualize the distribution of species across the three islands.

### Correlation Analysis

A heatmap was generated to display the correlation between the numerical features (culmen length, culmen depth, flipper length, and body mass). Significant correlations were found between:

- Flipper length and body mass: Strong positive correlation (r = 0.87).
- Culmen length and body mass: Moderate positive correlation (r = 0.60).
- Culmen depth: Exhibited a weak negative correlation with body mass.

### Species Distribution Across Islands

A groupby operation was performed to calculate the number of penguins of each species present on each island. The results show that Gentoo penguins are predominantly found on Biscoe and Dream islands, while Chinstrap penguins are mainly found on Dream island.

### Machine Learning Model

**Model Performance**:
- The classifier performed very well for Gentoo (100% precision and recall), Adelie (98% precision, 96% recall), and Chinstrap (89% precision, 94% recall).
- Overall accuracy of the model was 97%, indicating a robust classification system.

**Feature Importance**:
- Culmen length (beak length) was the most important feature for species classification.
- Flipper length and culmen depth were also significant, while body mass played a lesser role in distinguishing species.

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

- Species Distribution Across Islands:
    - Gentoo penguins were found mainly on Biscoe and Dream islands, while Chinstrap penguins were most commonly observed on Dream island.

- Feature Importance:
    - The model relied most heavily on culmen length to classify species, followed by flipper length and culmen depth.

### Source

Dataset: [Palmer Archipelago Antarctica Penguin Dataset on Kaggle](https://www.kaggle.com/datasets/parulpandey/palmer-archipelago-antarctica-penguin-data)
