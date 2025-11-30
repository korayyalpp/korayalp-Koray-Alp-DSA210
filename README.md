Koray Alp — DSA210 Term Project

Do Defenders Receive More Disciplinary Cards Than Other Football Players?

⸻

Introduction

This project investigates whether defenders receive more disciplinary cards (yellow and red) compared to players in other positions in professional football leagues. By creating a numerical “Card Score” metric and analyzing position groups, the study assesses whether disciplinary tendencies differ structurally across roles on the field.

The aim is to determine whether the defensive role—often involving physical challenges, last-ditch tackles, and high-pressure defensive actions—results in defenders accumulating more cards over a season compared to midfielders, attackers, and goalkeepers.

By applying exploratory data analysis (EDA) and statistical hypothesis testing, the project provides an evidence-based conclusion on whether defenders are statistically more prone to disciplinary actions.

⸻

Motivation

Football is a physically demanding sport where disciplinary outcomes significantly impact match performance and team strategy. Defenders, due to their tactical responsibilities, frequently engage in high-risk situations such as:
	•	Tackling attacking players
	•	Stopping fast counterattacks
	•	Defending critical zones
	•	Committing tactical fouls

These game dynamics raise the question:

Do defenders inherently receive more cards than other player roles?

This project aims to:
	•	Compare the average card score of defenders vs. other players
	•	Quantify disciplinary differences between positions
	•	Understand whether defensive responsibilities statistically increase card risk
	•	Provide actionable insights into the relationship between player role and discipline

⸻

Data Source

The dataset used in this project is a CSV file containing official player statistics, including:
	•	Name
	•	Position
	•	Yellow cards
	•	Red cards

The data was imported into a Google Colab notebook and processed using Python for further analysis.

A custom metric—Card Score—was constructed to quantify disciplinary impact:
	•	2 points per yellow card
	•	3 points per red card

This allows a unified comparison across players and positions.

⸻

Hypothesis Testing

Disciplinary Difference Between Defenders and Other Positions

To determine whether defenders receive more cards, we formally test:

H₀ (Null Hypothesis):

Defenders and non-defenders have equal average card scores.

H₁ (Alternative Hypothesis):

Defenders have a significantly higher average card score than other players.

Method:
A Welch’s Two-Sample t-test (independent samples with unequal variances) is applied to compare the card score distributions of defenders and other positions.

Interpretation Rule:
If p-value < 0.05, reject H₀ → defenders receive significantly more cards.
If p-value ≥ 0.05, fail to reject H₀ → no statistical difference.

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

1. Data Collection
	•	Import CSV file into Google Colab
	•	Select relevant columns (Name, Position, Yellow cards, Red cards)

2. Cleaning
	•	Verified column integrity
	•	Checked for missing values
	•	Standardized positions into two groups:
	•	Defender
	•	Other

3. Feature Creation
	•	Constructed Card Score = 2 × Yellow + 3 × Red
	•	Labeled each player as Defender or Other

4. Grouping
	•	Aggregated summary statistics for each group
	•	Prepared datasets for t-test and visualization

⸻

Data Analysis & Visualizations

The following EDA techniques were applied:

1. Histogram

Shows distribution of card scores for Defenders vs Others.

2. Box Plot

Compares median and spread of card scores across groups.

3. Violin Plot

Displays density and distribution shape.

4. Correlation Heatmap

Shows the relationships between:
	•	Yellow cards
	•	Red cards
	•	Card score

5. Group Summary

Analyzed count, means, variance for each position group.

These visualizations help determine whether defenders statistically accumulate more cards.

⸻

Hypothesis Test Results

The Welch t-test compares mean card scores between the two groups.

Output metrics:
	•	t-statistic
	•	p-value

Interpretation is based on a 0.05 significance level.

A statistically significant p-value indicates defenders indeed receive more cards on average.

⸻

Limitations & Future Work

Limitations
	•	Data includes only one league dataset; results may not generalize globally.
	•	Positional labels are simplified into Defender vs Other.
	•	Card severity is standard-weighted (2 for yellow, 3 for red), but alternative scoring could be explored.
	•	The dataset does not include contextual match details such as foul type, minute, or referee behavior.

Future Work
	•	Expand the dataset across multiple leagues (La Liga, Serie A, Bundesliga).
	•	Analyze card patterns by specific defensive sub-roles (CB, RB, LB).
	•	Include fouls committed and duels lost for deeper disciplinary modeling.
	•	Implement predictive modeling (e.g., logistic regression) to estimate card probability.
	•	Explore referee and match-level effects on card issuance.

⸻

Conclusion

This project provides a structured statistical approach to understanding whether defenders receive more cards than other football players. Through EDA and hypothesis testing, we evaluate disciplinary trends and determine whether player position plays a significant role in card accumulation.
