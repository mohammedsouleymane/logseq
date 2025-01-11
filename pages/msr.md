- literature
- statistic
  collapsed:: true
  
  ---
	- ### **Overview**
	- The document explores basic concepts, principles, and applications of statistics in analyzing experimental data.
	- Emphasis is placed on using statistics for hypothesis testing, modeling relationships, and interpreting results, with applications in various fields.
	  
	  ---
	- ### **Key Concepts**
	- **Statistics and Its Purpose**:
		- **Descriptive Statistics**: Tools to summarize and describe data (e.g., means, medians, histograms).
		- **Inferential Statistics**: Tools to generalize findings from a sample to a population using hypothesis testing and confidence intervals.
	- **Measurement Scales**:
		- **Nominal**: Categories without order (e.g., gender, colors).
		- **Ordinal**: Ordered categories without meaningful intervals (e.g., Likert scales).
		- **Interval**: Ordered categories with meaningful intervals but no true zero (e.g., temperature in Celsius).
		- **Ratio**: Ordered categories with meaningful intervals and a true zero (e.g., weight, height).
		  
		  ---
	- ### **Descriptive Statistics**
	- Use plots like histograms to visualize distributions and patterns.
	- Measures of central tendency:
		- **Mean**: Average of values.
		- **Median**: Middle value, robust to outliers.
		- **Mode**: Most frequent value.
	- Measures of spread:
		- **Range**, **Variance**, **Standard Deviation**: Quantify data variability.
		- **Quantiles**: Extend the idea of the median (e.g., quartiles).
		  
		  ---
	- ### **Distributions**
	- Data is often modeled with distributions (e.g., Normal, Beta).
	- Probability Density Function (PDF) and Cumulative Distribution Function (CDF) are tools to describe data likelihood and cumulative probabilities.
	  
	  ---
	- ### **Statistical Hypotheses**
	- **Null Hypothesis (H₀)**: Assumes no effect or no difference.
	- **Alternative Hypothesis (H₁)**: Represents an effect or difference.
	- Test results are interpreted through p-values, confidence intervals, and effect sizes.
	  
	  ---
	- ### **Inferential Statistics**
	- **Testing Relationships**:
		- **Independent vs. Dependent Variables**: Relationship analyzed depends on variable types.
		- Common variable pairings:
			- Nominal → Interval: t-tests, ANOVA.
			- Interval → Interval: Correlation and Regression.
			- Interval → Nominal: Logistic Regression.
			- Nominal → Nominal: Chi-square tests.
	- **Effect Sizes**:
		- Quantifies the magnitude of relationships or differences (e.g., Cohen's d, η²).
		- Independent of p-values, effect sizes highlight the importance of results.
	- **Confidence Intervals**:
		- Provide a range within which the true population parameter lies with a certain probability (e.g., 95%).
		  
		  ---
	- ### **Statistical Methods by Variable Type**
	- **Nominal → Interval (Two Groups)**:
		- Use t-tests (independent or paired).
		- Example: Comparing experimental vs. control groups.
	- **Nominal → Interval (Multiple Groups)**:
		- Use ANOVA to test if means differ across groups.
		- Post-hoc tests (e.g., Tukey's HSD) identify specific group differences.
	- **Interval → Interval**:
		- Use correlation (e.g., Pearson’s r) to measure linear relationships.
		- Regression models predict one variable based on another.
	- **Interval → Nominal**:
		- Logistic Regression: Models probabilities of categorical outcomes.
		- Example: Predicting crash probability based on temperature.
	- **Nominal → Nominal**:
		- Chi-square tests examine associations between categories.
		- Odds ratios quantify effect size in contingency tables.
	- **Ordinal Variables**:
		- Use non-parametric tests like the Wilcoxon Rank Sum, Kruskal-Wallis, or Sign tests for skewed or non-normal data.
		  
		  ---
	- ### **Advanced Topics**
	- **General Linear Models (GLMs)**:
		- Extend basic regression/ANOVA to handle multiple independent variables and interactions.
	- **Generalized Linear Models (GzLMs)**:
		- Include non-linear relationships or restricted dependent variable ranges (e.g., probabilities in logistic regression).
		  
		  ---
	- ### **Practical Application in R**
	- Statistical software like R is used for analysis.
	- Common commands:
		- `t.test()`: Performs t-tests.
		- `aov()`: Performs ANOVA.
		- `lm()`: Fits linear models.
		- `glm()`: Fits logistic or generalized models.
		- `pwr.t.test()`: Calculates required sample size.
		  
		  ---
	- ### **Conclusion**
	- The document stresses understanding statistical principles, rather than manual calculations.
	- Core objectives:
		- Analyze data to validate hypotheses.
		- Use appropriate tests for data types.
		- Interpret statistical results critically.
		  
		  <!--EndFragment-->
-