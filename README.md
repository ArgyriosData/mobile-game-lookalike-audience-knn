# Mobile Game Lookalike Audience Modeling with KNN for User Acquisition

## Overview

This project explores how K-Nearest Neighbors (KNN) can be used to identify potential lookalike audiences for mobile game user acquisition (UA).

High-value players are identified using historical revenue, and KNN is applied to find other players with similar behavioral profiles. The resulting audience is compared with the remaining player population to explore differences in historical monetization.

## Methodology

- **Seed audience:** Select the top 2% of players by historical revenue.
- **Data preprocessing:** Handle missing behavioral feature values using median imputation and standardize features.
- **Lookalike modeling:** Apply KNN using behavioral features, excluding player ID and revenue from the model inputs.
- **Audience evaluation:** Compare audience size and historical revenue statistics between lookalikes, standard players, and high-value seeds.

## Key Results

The analysis identified 494 unique lookalike players from 200 high-value seeds.

| Metric | Standard Players | KNN Lookalikes |
|---|---:|---:|
| Player count | 9,306 | 494 |
| Mean revenue | 1.23 | 8.97 |
| Median revenue | 0.89 | 2.88 |

The lookalike audience showed higher historical revenue than the remaining player population, suggesting that behavioral similarity may help identify promising candidates for UA targeting.

## Limitations

This project uses synthetic data and provides an exploratory analysis. Higher historical revenue does not establish future campaign performance. A future-period evaluation or controlled UA experiment would be needed to determine whether targeting the identified audience improves acquisition outcomes.

## Tools

Python, Pandas, NumPy, Scikit-learn
