Fire Damage vs Distance from Fire Station — Simple Linear Regression Project

This project investigates whether the distance between a home and its nearest fire station affects the amount of fire damage the home suffers during a residential fire. Using a real dataset of 15 suburban fires and applying statistical tools in Simple Linear Regression (SLR), the analysis explores trends, model validity, prediction capability, and key statistical inferences.

⸻

Project Overview

Residential fires are costly and dangerous. Emergency response time plays a major role in determining how much damage a fire ultimately causes, and distance from the fire station is a key factor affecting response time.

This project:
	•	Uses real-world suburban fire data
	•	Builds a simple linear regression model
	•	Tests model assumptions
	•	Compares a linear model vs a quadratic model
	•	Estimates confidence intervals
	•	Analyzes influential points
	•	Uses predictions to quantify expected damage

⸻

Dataset Summary

The dataset contains 15 residential fires, with two recorded variables:
	•	Distance from nearest fire station (in miles)
	•	Damage in property loss (in thousands of dollars)

Example:

DISTANCE   DAMAGE
   3.4        31
   5.3        43
   2.6        20

Distance is measured in miles.
Damage is measured in thousands of USD.

⸻

Key Research Question

Does the distance to a fire station significantly affect fire damage?
More specifically:
Does fire damage increase for homes located farther from fire stations?

⸻

Statistical Model

A Simple Linear Regression (SLR) model is used:

y = \beta_0 + \beta_1 x + \epsilon

Where:
	•	y = fire damage
	•	x = distance from the fire station
	•	\beta_1 = expected change in fire damage per mile
	•	\epsilon \sim N(0,\sigma^2)

Assumptions checked:
	•	Linearity
	•	Normality of residuals
	•	Constant variance
	•	Independence
	•	Zero mean errors

All assumptions were validated using residual plots, Q-Q plots, Shapiro-Wilk tests, and diagnostics.

⸻

Model Results

Estimated Regression Equation

\hat{y} = 10.2779 + 4.9193x

Interpretation:
	•	A home next to the fire station is predicted to suffer ~$10,278 in damage.
	•	Every additional mile adds approximately $4,919 in expected fire damage.

Statistical Significance

Both coefficients had very small p-values:
	•	Intercept p-value: 6.59e-06
	•	Slope p-value: 1.25e-08

Distance is a highly significant predictor of damage.

Model Fit
	•	Multiple R² = 0.9235
	•	Adjusted R² = 0.9176

About 92% of variation in fire damage is explained by distance.

⸻

🔍 Model Comparison

A quadratic model was also tested:

y = \beta_0 + \beta_1 x + \beta_2 x^2 + \epsilon

Results:
	•	Adjusted R² was slightly worse than the linear model.
	•	Quadratic term was not statistically meaningful.
	•	No strong curvature in data.

Linear model is preferred.

⸻

Diagnostic Checks
	•	Residuals vs Fitted: No pattern → constant variance holds
	•	Q-Q Plot: Points near line → normality holds
	•	Shapiro-Wilk: p-value > 0.05 → normality not rejected
	•	Leverage / Cook’s Distance:
	•	Point 13 slightly influential
	•	Not extreme enough to remove

Model assumptions are solid.

⸻

Confidence Intervals

95% CI for slope:

4.07 \le \beta_1 \le 5.77

We are 95% confident that each additional mile increases expected fire damage by $4,070–$5,770.

Example Prediction (distance = 5 miles):

Value	Amount
Prediction	$34,875
95% CI	$32,925 – $36,824


⸻

Conclusion

Final Answer: YES — distance from a fire station significantly affects fire damage.
	•	Houses farther away suffer more damage, with a strong and statistically significant linear trend.
	•	Each extra mile adds roughly $4,920 in expected losses.
	•	The linear regression model is highly accurate and explains over 92% of variation.
	•	Results are statistically robust and supported by all assumption checks.

This demonstrates how emergency response planning and station placement can meaningfully affect public safety and financial outcomes.
