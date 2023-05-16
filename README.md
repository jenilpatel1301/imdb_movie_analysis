# imdb_movie_analysis


This repository contains code for analyzing movie data, specifically focusing on factors such as budget, popularity, runtime, and genres. The analysis aims to provide insights into the relationship between these variables and their impact on a movie's success.

## Getting Started

To get started, make sure you have the necessary libraries installed. This code requires the following libraries:

- pandas
- matplotlib
- seaborn
- numpy

You can install these libraries using pip:

```
pip install pandas matplotlib seaborn numpy
```

## Data Wrangling

The data wrangling process involves preparing the dataset for analysis by handling missing data, removing duplicates, and dropping unnecessary columns. Here are the key steps:

- Import the required libraries.
- Load the movie dataset using `pd.read_csv`.
- Perform initial data exploration using functions like `head()`, `shape`, `dtypes`, `nunique()`, `isnull().sum()`, `describe()`, and `info()`.
- Remove duplicates using `drop_duplicates()`.
- Handle missing data by filling in null values with appropriate values. For object-type columns, "missing" is used, while budget values of 0 are replaced with `np.NAN`.
- Drop unuseful columns like 'id', 'imdb_id', 'homepage', and 'overview' using `drop()`.

## Exploration with Visuals and Conclusions

The analysis focuses on answering several questions using visualizations and deriving conclusions. Here's a summary of each question and the corresponding visualizations used:

### Question 1: Does higher budget mean higher popularity? Is there a coefficient relationship?

- Scatter plot: `plt.scatter()` to plot the relationship between budget and popularity.
- Bar chart: Compare the mean popularity of low-budget and high-budget movies.

Conclusion: There is no strong relationship between budget and popularity based on the scatter plot. However, the bar chart shows that higher budget films tend to have higher average popularity.

### Question 2: What length will receive the highest popularity?

- Bar chart: Compare the mean popularity of movies with short, medium, and long runtimes.

Conclusion: Movies with a moderate runtime (neither too short nor too long) tend to have higher average popularity.

### Question 3: Does higher popularity mean higher profits?

- Bar chart: Compare the mean profit of movies with low and high popularity.

Conclusion: Movies with higher popularity tend to generate significantly higher average profits.

### Question 4: Which genres are most popular from year to year?

- Bar chart: Display the occurrences per genre.
- Heatmap: Visualize the budget and revenue for each genre per year.

Conclusion: The top five genres are Drama, Comedy, Thriller, Action, and Romance. The number of movies released has increased over time.

## Conclusion

Based on the analysis conducted, the following conclusions can be drawn:

1. The quantity and range of movies have increased, providing audiences with more choices.
2. A higher budget does not guarantee higher popularity, but movies with larger budgets tend to have higher average popularity.
3. Movies with a runtime of approximately 150 minutes are more likely to be popular.
4. Genres such as Drama, Comedy, Thriller, and Action are popular among audiences.
5. Higher popularity correlates with higher profits.

This analysis provides insights into the factors that contribute to a movie's success, helping filmmakers and producers make informed decisions regarding budget, runtime, and genre selection.

## Reference

https://www.kaggle.com/diegoinacio/imdb-genre-based-analysis
