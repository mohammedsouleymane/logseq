- literature
  ---
	- ### **Overview**
	  
	  This document focuses on the importance of literature in scientific research, covering the following topics:
	- **Why literature is essential**.
	- **How to find, assess, and reference literature**.
	- **Avoiding plagiarism and proper citation practices**.
	- **Different types of sources and reference styles**.
	  
	  ---
	- ### **Why Literature?**
	- **Purpose of Reading Literature**:
		- Understand previous work in the field.
		- Gain new ideas and identify open research questions.
		- Learn new methods and skills.
		- Find relevant data for tuning or testing models.
		  
		  > 
		  
		  *Science is an incremental process, building on the work of predecessors.*
	- **Importance of Referencing Literature**:
		- Acknowledge prior work and prevent duplication.
		- Situate new work within the broader research landscape.
		- Enhance the replicability and verifiability of research.
		- Avoid plagiarism and demonstrate subject-matter expertise.
	- **What is a Literature Review?**
		- It introduces and discusses research relevant to a topic.
		- Not a simple list of papers but a discussion of how these works relate to the research question.
		- Reviews historical progress, identifies key players, and highlights gaps or controversies in the field.
		  
		  ---
	- ### **Finding Literature**
	- **Strategies for Literature Search**:
		- **Textbooks**: Offer foundational knowledge but may not reflect the latest advancements.
		- **Conferences**: Provide cutting-edge work and identify active researchers.
		- **Journals**: Contain polished and peer-reviewed work; many journals specialize in review articles.
		- **Online Tools**: Use resources like Google Scholar, Citeseer, or ISI Web for citation analysis and reference tracking.
	- **Using Citation Networks**:
		- Citation analysis helps trace the influence of a paper (forward and backward).
		- Central or highly cited articles often represent pivotal works in the field.
	- **Paper Structure**:
		- Papers follow a standard structure: Introduction, Methods, Results, Discussion, and Conclusion.
		- Different sections reference related work, methodological sources, and impactful results.
	- **Sources Based on Research Stage**:
		- **Workshops**: Early-stage ideas and discussions.
		- **Conferences**: Refined work, but not as mature as journal publications.
		- **Reports and Journals**: Comprehensive and conclusive results.
		- **Books**: Summarize extensive research or provide educational overviews.
		  
		  ---
	- ### **Assessing Literature Quality**
	- **Evaluating Sources**:
		- Trace arguments and data back to their origins, verify from multiple sources.
		- Assess the reputation of the publication venue (e.g., Nature, IEEE).
	- **Impact Factors**:
		- Measure average citations per paper over two years.
		- Journals with higher impact factors often have stricter acceptance criteria.
		- Caution: High impact factors do not always equate to quality (e.g., controversial or widely publicized papers).
	- **Field-Specific Norms**:
		- Computer science relies heavily on conferences.
		- Linguistics emphasizes books.
		- Physics uses preprint archives for rapid dissemination.
		  
		  ---
	- ### **Referencing in Text**
	- **Reference Styles**:
		- **Author-Year (e.g., Smith, 2020)**: Common in social and natural sciences.
		- **Numbered Notes [e.g., 12]**: Often used in technical disciplines.
		- Include additional details like sections, not page numbers, for ease across editions.
	- **Special Cases**:
		- Cite unpublished manuscripts or personal communications explicitly.
		- For anonymous sources, attribute to organizations where possible.
	- **Automating References**:
		- Use tools like EndNote, Zotero, or BibTeX for efficient reference management.
		- Always verify automated references for completeness and accuracy.
		  
		  ---
	- ### **The Reference List**
	- **Purpose**:
		- Provides all necessary information to locate and credit sources.
		- Includes author names, publication year, journal/book details, volume, issue, pages, DOI, and ISBN.
	- **Formats**:
		- Different fields and journals adopt varying formats (e.g., APA, MLA, Chicago).
		- Use reference managers to handle these formats efficiently.
	- **Source Types**:
		- **Journal Articles**: The most common and reliable source type.
		- **Books**: Include ISBN if relevant, though not a mark of quality.
		- **Websites**: Include retrieval dates and organization names when authors are unavailable.
		- **Conference Papers**: Often in proceedings; ensure citation completeness.
		- **Theses and Datasets**: Follow standard referencing rules for these less common sources.
		  
		  ---
	- ### **Plagiarism and Ethical Practices**
	- **What is Plagiarism?**
		- Copying or paraphrasing someone else’s work without proper acknowledgment.
		- Applies to text, ideas, figures, tables, and even code.
	- **Avoiding Plagiarism**:
		- Use proper citation formats for all borrowed material.
		- Paraphrase only after fully understanding the source content.
		- When quoting, use quotation marks for short texts or indent for long passages.
	- **Citing Correctly**:
		- Always include the source in the reference list.
		- Err on the side of over-citing to avoid accidental omissions.
		  
		  ---
	- ### **Conclusion**
	  
	  This guide equips researchers with the skills to:
	- Find relevant literature.
	- Evaluate its quality.
	- Incorporate it responsibly into their own work.
	- Avoid plagiarism while giving credit to original authors.
	  
	  
	  <!--EndFragment-->
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