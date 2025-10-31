# Koray Alp DSA210 Term Project
The Impact of Injuries on the Career Longevity of Professional Football Players On Premier League

## Introduction
This project focuses on analyzing how **injuries affect the career longevity of football players in the English Premier League (EPL)**.  
The goal is to determine whether players who experience frequent or long-term injuries tend to have **shorter professional careers** compared to those with fewer or minor injuries.  
By examining detailed **injury and career data** from Premier League players, the project aims to highlight the long-term effects of physical health and recovery management on career duration.

## Motivation
The **English Premier League** is one of the most competitive and physically demanding football leagues in the world.  
Players face intense match schedules, high physical pressure, and frequent injuries that can limit their long-term participation.  
This project aims to:
- **Measure the impact of injury frequency** on total career years within the Premier League.  
- **Explore the relationship** between recovery duration and a player's professional longevity.  
- **Understand the long-term cost of recurring injuries** on player stability and performance.  
- **Provide evidence-based insights** for how clubs and medical teams can help extend player careers through better injury management.  

## Data Source
The dataset will be collected exclusively from **English Premier League players** using the following sources:  
- **Transfermarkt.com** – For detailed injury history, recovery duration, and career timelines.  
- **Maçkolik.com** – For verifying player match appearances and activity per season.  
- **Official Premier League & Club Websites** – For cross-checking injury data and retirement information.  

## Hypothesis Testing
- **Injury–Career Length Relationship (Premier League):**  
  - **H₀:** Injuries have no effect on a Premier League player's career length.  
  - **H₁:** Frequent or severe injuries significantly shorten a player’s Premier League career.  
  - **Method:** Correlation and linear regression analysis using player-level injury and career data.  
  - **Interpretation:** If *p-value < 0.05*, injuries have a statistically significant negative effect on career duration in the EPL.

## Tools & Technologies
- **Python**
  - `pandas` – Data cleaning and structuring  
  - `numpy` – Statistical calculations   
- **Jupyter Notebook** – For analysis and visual presentation  
- **Excel** – For collecting and organizing raw player data  

## Data Processing
- **Data Collection:** Extract injury and career data for Premier League players from Transfermarkt, Maçkolik, and official club websites.  
- **Cleaning Data:** Remove duplicate entries and fill missing values.  
- **Feature Creation:**  
  - Calculate **total injuries per player**.  
  - Compute **average recovery duration** (days missed per injury).  
  - Determine **career length** within the Premier League (final season – debut season).  
- **Standardization:** Use consistent units for time (days) and ensure all players belong to EPL clubs.  
- **Grouping:** Analyze players by **position** (forwards, midfielders, defenders, goalkeepers) to identify role-based patterns.  

## Data Analysis & Visualizations
- **Injury Frequency vs. Career Duration:** Use **scatter plots** and **regression lines** to measure the relationship between injury count and career length.  
- **Recovery Duration Impact:** Visualize recovery times with **box plots** to identify outliers and patterns.  
- **Position-Based Comparison:** Compare injury effects across player positions using **bar and violin plots**.  
- **Correlation Heatmap:** Display relationships between injuries, matches missed, and career duration.  
- **Predictive Modeling (Future Work):** Develop a **regression model** to predict expected career length based on injury data for Premier League players.  

## Limitations & Future Work
- **League-Specific Limitation:** Focused only on the Premier League — results may not generalize to other leagues.  
- **Data Availability:** Some historical injury details may be incomplete or inconsistent.  
- **Medical Record Access:** Reliance on public data limits accuracy of injury severity classification.  
- **Future Work:**  
  - Expand to include **Championship** or **European leagues** for comparison.  
  - Integrate **injury severity categories** (minor, moderate, severe).  
  - Add **seasonal workload metrics** (minutes played, matches per season).  
  - Create an **interactive dashboard** visualizing player injury timelines and career length predictions.  

