### Fire Damage Linear Regression Model

## This project examines whether the distance between a home and its nearest fire station influences the amount of fire damage sustained during residential fires. A dataset of 15 suburban fires was analyzed using Simple Linear Regression to evaluate this relationship.

## Key Results
	•	Distance shows a strong positive linear relationship with fire damage.
	•	Estimated regression equation:
$$
\hat{y} = 10.2779 + 4.9193x
$$
	•	Interpretation: Homes farther from the fire station tend to experience more damage. Each additional mile increases expected damage by roughly $4,900.
	•	Distance is statistically significant, with very small p-values for both the intercept and slope.
	•	The model explains about 92% of the variation in fire damage (Adjusted R² = 0.9176).

## Model Comparison

A quadratic model was evaluated but did not offer meaningful improvement over the linear model. The linear model fits the data well and is preferred.

## Diagnostics

Residual plots, Q-Q plots, and the Shapiro-Wilk test showed no concerns with normality or constant variance. Cook’s distance identified one moderately influential point, but not enough to invalidate the model.
