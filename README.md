# NBA Rookie Career Prediction Project

## Overview

This project aims to predict the career outcomes of NBA players based on their performance during their rookie years (first four years after being drafted). By analyzing player statistics and award achievements during this period, the project provides a strategic framework for teams to assess player value accurately. The findings have significant implications for player scouting and team management in professional basketball.

## Project Structure

### Data

The project utilizes two primary datasets:

- `team_stats.csv`: Contains player performance statistics.
- `player_stats.csv`: Contains award information.

These datasets have been merged into a panel dataset that includes 900 unique players spanning 14 years of NBA drafts (2007-2015). The dataset records player performance statistics and award achievements for each season on a yearly basis.

### Data Preprocessing

The data preprocessing involved:

- **Season Standardization**: Adjusted statistics from seasons with fewer games (e.g., the 2011 lockout season) to match the standard 82-game season.
- **Stats Averaging**: Averaged performance metrics across the first four years of a player's career.
- **Labeling**: Created season-level and career-level outcomes based on a player's achievements.

### Career Outcome Classification

Players are classified into six categories based on their career outcomes:

1. **Elite**: Won any All-NBA award, MVP, or DPOY.
2. **All-Star**: Selected as an All-Star.
3. **Starter**: Started in at least 41 games or played at least 2000 minutes in a season.
4. **Rotation**: Played at least 1000 minutes in a season.
5. **Roster**: Played at least 1 minute but did not meet any of the above criteria.
6. **Out of the League**: Not in the NBA in that season.

For simplification, a three-category system was also created:

- **Top Class**: Career outcome is either Elite or All-Star.
- **Middle Class**: Career outcome is Starter, Rotation, or Roster.
- **Incompatible**: Career outcome is Out of the League.

### Machine Learning Methods

The project employs several machine learning methods:

- **K-means Clustering**: Used for exploring the data and determining the optimal number of clusters.
- **Logistic Regression**: Applied for initial classification, both with the six-category and simplified three-category systems.
- **Random Forest**: Used for robust classification, especially after addressing class imbalances using SMOTE.

### Results

- **Logistic Regression**: Achieved moderate success with the simplified three-category system, highlighting the importance of data interpretability and model simplicity.
- **Random Forest**: Demonstrated high accuracy (83%) in predicting career outcomes, proving effective for this complex dataset.

## Conclusion

The study successfully created a predictive model for NBA player career outcomes based on rookie-year performance. While the Random Forest model showed strong results, further refinement is possible, especially for predicting top-tier outcomes. The findings hold significant implications for NBA teams in scouting and evaluating players, providing a valuable tool for decision-making under wage cap constraints.

## Files
- `team_stats.csv`: Contains player performance statistics.
- `player_stats.csv`: Contains award information.
- `report.pdf`: is my summary of the job.
- `award_project_template.ipynb`: contains code for data cleaning and quantitative analysis
- `model_training.ipynb`: contains code for benchmarking the best regression classification algorithms.
- `240 final presentation.pdf` contains a pptx file for speech purposes.

## References

The study references various works in sports analytics, machine learning, and NBA data analysis. Please see the full paper for detailed citations.
