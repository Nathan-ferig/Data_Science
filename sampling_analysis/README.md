
# Data Sampling and Cleaning Analysis

This notebook demonstrates various sampling methods and compares the samples with the original dataset. It also includes a cleaning section to free memory after execution.

## 1. Dataset Loading

The notebook loads a dataset (`census.csv`) and checks its first few rows, dimensions, and null values.

## 2. Sampling Methods

Different sampling methods are implemented:
- **Random Sampling**: Selects a random sample from the dataset.
- **Systematic Sampling**: Samples based on a calculated interval.
- **Group Sampling**: Samples from random groups within the dataset.
- **Stratified Sampling**: Samples based on a stratification variable (e.g., income).
- **Reservoir Sampling**: Samples from data in a streaming fashion.

## 3. Comparisons

The notebook compares the mean of the sample versus the population for each sampling method, and calculates the percentage difference. It also checks the distribution of values for each method.

## 4. Memory Cleanup

The notebook cleans up variables to free memory and optimize execution.

## How to Run

1. Ensure Python and necessary libraries (pandas, numpy) are installed.
2. Load the `census.csv` dataset.
3. Run the notebook cells to process the data.
4. View the results of the sampling comparisons.

## 📎 Connect with Me

If you found this project useful or want to collaborate, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/nathanferig/).

