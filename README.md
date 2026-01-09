Koray Alp — DSA210 Term Project

Do Defenders Receive More Disciplinary Cards Than Other Football Players?

⸻

Introduction

This project investigates whether defenders receive more disciplinary cards (yellow and red) compared to players in other positions in professional football leagues. By creating a numerical Card Score metric and analyzing position groups, the study assesses whether disciplinary tendencies differ structurally across roles on the field.

The aim is to determine whether the defensive role—often involving physical challenges, last-ditch tackles, and high-pressure defensive actions—results in defenders accumulating more cards over a season compared to midfielders, attackers, and goalkeepers.

By applying exploratory data analysis (EDA), statistical hypothesis testing, and machine learning methods, the project provides an evidence-based evaluation of whether defenders are more prone to disciplinary actions.

⸻

Motivation

Football is a physically demanding sport where disciplinary outcomes significantly impact match performance and team strategy. Defenders, due to their tactical responsibilities, frequently engage in high-risk situations such as:
	•	Tackling attacking players
	•	Stopping fast counterattacks
	•	Defending critical zones
	•	Committing tactical fouls

These game dynamics raise the central research question:

Do defenders inherently receive more cards than other player roles?

This project aims to:
	•	Compare the average card score of defenders vs. other players
	•	Quantify disciplinary differences between positions
	•	Test whether defensive responsibilities statistically increase card risk
	•	Validate findings using both statistical inference and predictive modeling

⸻

Data Source

The dataset used in this project is a CSV file containing official player statistics, including:
	•	Name
	•	Position
	•	Yellow cards
	•	Red cards

The data was imported into a Google Colab notebook and processed using Python.

A custom metric—Card Score—was constructed to quantify disciplinary impact:
	•	2 points per yellow card
	•	3 points per red card

This unified score allows consistent comparison across players and positions.

⸻

Hypothesis Testing

Disciplinary Difference Between Defenders and Other Positions

To determine whether defenders receive more cards, the following hypotheses are tested:

H₀ (Null Hypothesis):
Defenders and non-defenders have equal average card scores.

H₁ (Alternative Hypothesis):
Defenders have a significantly higher average card score than other players.

Method:
A Welch’s Two-Sample t-test (independent samples with unequal variances) is applied to compare card score distributions.

Decision Rule:
	•	If p-value < 0.05 → Reject H₀
	•	If p-value ≥ 0.05 → Fail to reject H₀

⸻

Tools & Technologies
	•	Python
	•	pandas — data loading and cleaning
	•	numpy — numerical operations
	•	matplotlib — visualization
	•	seaborn — statistical graphics
	•	scipy.stats — hypothesis testing
	•	Google Colab — analysis environment

⸻

Data Processing

Data Collection
	•	Imported CSV file into Google Colab
	•	Selected relevant columns (Name, Position, Yellow cards, Red cards)

Cleaning
	•	Verified column integrity
	•	Checked for missing values
	•	Standardized positions into two groups:
	•	Defender
	•	Other

Feature Creation
	•	Constructed Card Score = 2 × Yellow + 3 × Red
	•	Labeled each player as Defender or Other

Grouping
	•	Aggregated summary statistics by position group
	•	Prepared datasets for hypothesis testing, visualization, and ML modeling

⸻

Data Analysis & Visualizations

The following EDA techniques were applied:
	•	Histogram — distribution of card scores for Defenders vs Others
	•	Box Plot — comparison of median and spread
	•	Violin Plot — density and distribution shape
	•	Correlation Heatmap — relationship between yellow cards, red cards, and card score
	•	Group Summary Statistics — count, mean, variance by position

These visualizations provide intuitive insight into disciplinary differences across roles.

⸻

Machine Learning Extension

In addition to statistical analysis, supervised machine learning methods are implemented to assess whether player position can predict disciplinary risk.

Problem Formulation

The task is formulated as a binary classification problem.

Target Variable
	•	High Card Risk
	•	1 → Card Score above a predefined threshold
	•	0 → Card Score below or equal to the threshold

The threshold is selected based on the empirical distribution of Card Score to ensure class balance.

Features
	•	Position (Defender vs Other)
	•	Yellow cards
	•	Red cards

The Card Score itself is excluded from the feature set to prevent data leakage.

⸻

Data Splitting

The dataset is divided into:
	•	Training set: 70%
	•	Validation set: 15%
	•	Test set: 15%

This structure supports robust model training, tuning, and unbiased evaluation.

⸻

Models Implemented
	•	Logistic Regression
	•	Baseline interpretable classifier
	•	Measures positional effect on disciplinary risk
	•	Decision Tree Classifier
	•	Captures non-linear decision boundaries
	•	Offers transparent rule-based interpretation
	•	Random Forest Classifier
	•	Ensemble learning method
	•	Improves predictive accuracy and stability

⸻

Model Evaluation Metrics

Models are evaluated using:
	•	Accuracy
	•	Precision
	•	Recall
	•	F1-score
	•	Confusion Matrix

These metrics provide insight into both overall performance and class-level prediction quality.

⸻

Key Findings from Machine Learning
	•	Player position contributes meaningfully to predicting high card risk
	•	Defenders exhibit higher predicted probabilities of exceeding the card score threshold
	•	Ensemble methods (Random Forest) outperform simpler classifiers
	•	Logistic regression results align with hypothesis testing outcomes

⸻

Interpretation & Contribution

Machine learning results reinforce the statistical findings by:
	•	Providing predictive validation of disciplinary trends
	•	Demonstrating consistency between inferential and predictive approaches
	•	Strengthening confidence in the conclusion that defensive roles are structurally associated with higher disciplinary exposure

⸻

Conclusion

This project provides a comprehensive analytical framework to evaluate whether defenders receive more disciplinary cards than other football players. By combining exploratory data analysis, hypothesis testing, and machine learning, the study demonstrates that player position—particularly defensive roles—plays a significant role in disciplinary outcomes.

The integration of predictive modeling enhances the robustness of the findings and shows that disciplinary behavior in football can be both statistically analyzed and algorithmically modeled.
