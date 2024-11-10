# Palmer-Penguins

### Overview

The Palmer Penguins Dataset consists of data on penguin species from the Palmer Archipelago in Antarctica. The dataset includes various physical attributes like body mass, flipper length, and culmen dimensions for different penguin species. This dataset is great for exploratory data analysis, statistical modeling, and machine learning.

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

### Key Tasks:

- Data Inspection: Exploring the structure of the data (columns, data types, missing values).
- Data Cleaning: Handling missing data, if any, and converting categorical data into numerical representations.
- Exploratory Data Analysis (EDA).
  
### Analysis Performed

Correlation Matrix:
- Identifying strong correlations between numerical variables. For example, body mass (body_mass_g) is strongly correlated with flipper length (flipper_length_mm), with a correlation coefficient of 0.87.
- Other correlations were also identified, such as culmen_length_mm with body_mass_g (0.60), and culmen_depth_mm with flipper_length_mm (-0.58).

Species Distribution Across Islands:
- Adelie species are spread across all three islands, with the highest count on the Dream island.
- Chinstrap species are primarily found on Dream Island.
- Gentoo species are concentrated on Biscoe Island.

### Visualizations

- Histograms and Boxplots for the distribution of body mass across different penguin species.
- Correlation Heatmap to show the relationships between numerical variables.
- Species distribution by island using a countplot.

### Source

https://www.kaggle.com/datasets/parulpandey/palmer-archipelago-antarctica-penguin-data
