# ML-Powered Game Analytics (Chess Game)

## Executive Summary

This project applies machine learning to analyze player behavior using data from 50 online chess games. The goal is to predict player outcomes, identify behavior patterns, and generate design insights that could enhance gameplay experiences. Using decision tree classification and k-means clustering, we visualized player groups and provided automated recommendations based on common play patterns and outcomes.

---

## Introduction

Game analytics powered by machine learning can uncover meaningful insights into player behavior. This project focuses on chess due to its structured, turn-based nature and clear win conditions. Our aim was to build a simple yet insightful system that uses actual game data to predict winners, analyze strategies, and generate design suggestions using accessible ML tools.

---

## Methodology

### Game and Data Selection
We used a dataset of 50 chess matches, stored in a CSV file. The dataset includes fields such as player ratings, number of moves, win/loss status, and opening strategies.

### Data Preparation
We dropped rows with missing data and selected features such as `turns`, `white_rating`, `black_rating`, and `opening_ply`. The target label for prediction was the `winner` column.

### Analytics Dashboard and Visualization
We visualized key insights using multiple plots:
- A histogram with KDE for game length (turns)
- A clustered scatter plot of player ratings

These plots helped illustrate the distribution of game types and segmentation of players.

### Machine Learning Implementation
- **Winner Prediction:** We used a Decision Tree Classifier to predict the game winner based on features.
- **Player Clustering:** Using KMeans clustering, we grouped players into 3 behavior clusters and visualized them.

---

## Results and Analysis

- The Decision Tree model provided reasonable accuracy in predicting winners based on ratings and moves.
- KMeans clustering identified three distinct player groups, generally based on rating similarity.
- Visualization showed that most short games were won by higher-rated players.
- Games with fewer than 30 turns were often lost by lower-rated players.

---

## Machine Learning Insights

- Players with high rating disparity finished games more quickly.
- Short games (<30 moves) frequently resulted in resignation or loss.
- Players with lower black_rating values tend to resign more often.

---

## Automated Design Recommendations

- Add beginner tutorials for games where rating disparity is large.
- Provide dynamic hints for players struggling early in games.
- Adjust difficulty or suggestions based on early player moves.

---

## Technical Challenges

- Small dataset (only 50 games) limited the robustness of predictions.
- Lack of time-stamped moves reduced our ability to extract deep patterns.
- Data cleaning required careful checking to ensure input consistency.

---

## Future Improvements

- Scale up the dataset to include hundreds or thousands of games.
- Add session-based analytics (return visits, time per move, etc.).
- Explore advanced models like Random Forest or Neural Networks.
- Implement a real-time dashboard with user-level feedback.

---

## Conclusion

This project successfully demonstrates how machine learning can enhance game analytics. By using simple models and clear features, we gained insights into player behavior and suggested ways to improve game design. These methods can be extended to other games and more complex datasets in future work.

---

## References

- [Scikit-learn documentation](https://scikit-learn.org/)
- Lichess Open Database (for chess data structure reference)
- Tutorials: Machine Learning for Games (various online courses)
