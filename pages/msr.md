- literature
  collapsed:: true
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
	- **Strategies for Literature Search**:(TCJO)
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
- experiments
  collapsed:: true
	- ### **Overview**
	  
	  This document discusses:
	- **Why experiments are vital in scientific inquiry.**
	- **Theoretical and practical aspects of experimental design.**
	- **Examples of experiments involving computers and humans.**
	- **Strategies to mitigate errors, biases, and confounds.**
	- **The importance of research planning and sampling.**
	  
	  ---
	- ### **Why Experiments?**
	- **Purpose**:
		- A controlled way to test hypotheses about causal relationships.
		- Gather data in a structured, reproducible manner.
		- Provide incremental insights into complex systems.
	- **Hypothesis Testing**:
		- A hypothesis is a testable proposition about how the world works.
		- Experiments cannot "prove" a hypothesis but can assess its likelihood.
	- **Importance of Experimental Theory**:
		- Guides effective experimental design.
		- Ensures appropriate use of statistical tools.
		- Improves communication through shared terminology.
		  
		  ---
	- ### **Experiment Design Examples**
	- #### **1. Computer-Based Experiment**
	- **Research Question**: What is the fastest increment operation in C++?
		- **Independent Variable**: Type of increment (`i++`, `++i`, `i += 1`).
		- **Dependent Variable**: Execution time measured in processor cycles.
		- **Findings**: While slight differences were observed initially, repeated measurements revealed no significant differences.
	- **Key Issues**:
		- **Variability and Noise**: Repeated trials are required to calculate confidence intervals.
		- **Order Effects**: The position of conditions in the testing sequence influenced results. Addressed by randomizing the order of operations.
		- **Confounds**: Systematic biases like background processes affected results.
	- #### **2. Human-Based Experiment**
	- **Research Question**: What is the optimal button size for a mobile app?
		- **Independent Variable**: Button size (large, intermediate, small).
		- **Dependent Variables**:
			- Objective: Selection time and error rate.
			- Subjective: User satisfaction (measured via Likert scale).
	- **Experimental Designs**:
		- **Within-Subjects**: Each participant tests all conditions, reducing variability by controlling for individual differences.
		- **Between-Subjects**: Each participant experiences only one condition, avoiding potential learning or fatigue effects.
	- **Pretesting and Fine-Tuning**:
		- Pre-tests assess participant familiarity with apps or tasks.
		- Pilot studies refine the experimental design and analysis.
		  
		  ---
	- ### **Core Concepts in Experimental Theory**
	- **Key Variables**:
		- **Independent Variables**: Factors manipulated by the experimenter.
		- **Dependent Variables**: Outcomes measured to assess the impact of manipulations.
	- **Noise and Bias**:
		- **Noise**: Random variability unrelated to experimental conditions, manageable with statistical techniques.
		- **Bias**: Systematic distortions, such as confounding variables or observer/participant biases, which must be eliminated.
	- **Null Hypothesis**:
		- Often posits no effect or difference between conditions.
		- Experiments are designed to reject the null hypothesis, avoiding confirmation bias.
	- **Qualitative vs. Quantitative Analysis**:
		- Qualitative: Identifies measurable properties and potential manipulations.
		- Quantitative: Collects data, applies statistics, and refines or rejects hypotheses.
	- **Empirical Cycle**:
		- Formulate hypotheses → Design experiments → Collect data → Analyze results → Revise theories.
		  
		  ---
	- ### **Sampling Strategies**
	- **Types of Sampling**:
		- **Random Sampling**: Ensures representativeness but is challenging to achieve.
		- **Non-Random Sampling**:
			- Accidental: Convenient but potentially biased.
			- Quota: Ensures representation of specific groups.
			- Purposive: Targets specific expertise or traits.
	- **Practical Approaches**:
		- **Cluster Sampling**: Hierarchical random sampling (e.g., city → school → student).
		- Adjustments for population structure can improve generalizability.
		  
		  ---
	- ### **The Research Plan**
	- **Purpose**:
		- Prevents opportunistic or poorly structured research.
		- Guides systematic execution and facilitates reporting.
	- **Steps**:
		- Familiarize yourself with the field through literature and discussions.
		- Define a focused, feasible research question.
		- Operationalize the question into measurable components.
		- Plan data analysis methods.
		- Obtain ethical permissions, especially for human subjects.
		- Conduct pilot experiments and fine-tune setups.
		- Execute the full experiment.
	- **Ethical Considerations**:
		- Recruitment methods, participant consent, and privacy must meet ethical standards.
		- Universities often require approval from ethics committees.
		  
		  ---
	- ### **Mitigating Experimental Issues**
	- **Pilot Experiments**:
		- Validate measurements, participant behavior, and analysis methods.
		- Identify and address issues with internal validity.
	- **Randomization**:
		- Prevents systematic biases by evenly distributing potential confounds.
	- **Control Groups**:
		- Essential for distinguishing treatment effects from other influences.
		- Randomized Controlled Trials (RCTs) provide robust evidence by comparing treatment and control groups.
		  
		  ---
	- ### **Key Takeaways**
	- Experiments allow precise, controlled investigations into hypotheses.
	- Thoughtful design mitigates noise, bias, and confounds.
	- Clear research planning ensures ethical and effective execution.
	- Statistical analysis is crucial for interpreting results and assessing variability.
	  
	  
	  <!--EndFragment-->
- statistics
  collapsed:: true
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
- writing
  collapsed:: true
	- ### 1.  **Introduction to Scientific Writing**
	- **Characteristics**: Scientific writing has a neutral, impersonal style and follows a fixed organizational pattern.
	- **Learning Approach**:
		- Read scientific and popular scientific texts.
		- Refer to style manuals and guidelines.
		- Practice writing, both scientific and non-scientific texts.
		  
		  ---
	- ### 2.  **Preparation**
	- **Purpose**: Define the purpose of your writing (e.g., project report, proposal, review, etc.).
	- **Audience**: Understand your target audience (e.g., colleagues, professors, broader scientific community).
	- **Venue**: Tailor the length and detail to the type of publication (journal, thesis, or conference paper).
	- **Message**: Clearly outline the core message, conclusions, and contributions of your work.
	- **Background**: Assess the knowledge level of your audience and avoid assumptions.
	- **Storyline**: Draft a schematic structure of your content to maintain logical flow and coherence.
	  
	  ---
	- ### 3.  **Organization of Scientific Texts**
	- **Canonical Structure**:
		- Abstract
		- Introduction
		- Methods
		- Results
		- Discussion/Conclusion
	- **Chapters**: Keep chapters evenly distributed and readable in one sitting. Use headings judiciously to avoid excessive sub-levels.
	- **Abstract**: Self-contained, concise, and includes the research question, method essence, and main results.
	- **Keywords**: Use specific and field-relevant keywords for easy classification and search.
	- **Introduction**: Sets the scientific context, research questions, and summarizes methods and objectives.
	- **Methods & Results**: Methods detail procedures for reproducibility; results focus on factual findings, avoiding interpretation.
	- **Conclusion**: Summarizes findings and links them to research questions.
	- **Discussion**: Compares results with prior work, highlights broader implications, and suggests future work.
	- **Acknowledgments and Appendices**: Recognize contributors and provide supplementary material as needed.
	  
	  ---
	- ### 4.  **Writing the Text**
	- **Parallel Process**: Writing should proceed alongside research to identify gaps and weaknesses early.
	- **Iterative Process**: Writing, revising, and seeking feedback are critical for improvement.
	- **Style**: Maintain consistency in perspective (e.g., first-person plural) and optimize paragraph structure for clarity and logical flow.
	- **Advice**:
		- Avoid jargon and overly complex sentences.
		- Strive for simplicity without losing precision.
		- Read widely to adopt good practices.
		  
		  ---
	- ### 5.  **Illustrations and Non-Text Elements**
	- **Diagrams**: Use clear, spacious, and relevant vector graphics to explain concepts.
	- **Graphs**: Choose appropriate types (line graphs, bar charts, etc.), ensure clarity with proper labels, titles, and readable formatting.
	- **Tables**: Reserve for simple, quickly interpretable data. Complex data is better visualized as graphs or in appendices.
	- **Algorithms and Equations**: Use pseudocode for clarity and ensure all symbols in equations are well-defined and explained.
	- **Color Usage**: Optimize for both color and grayscale readability, ensuring accessibility for color-blind readers.
	  
	  ---
	- ### 6.  **General Recommendations**
	- **Quality Improvement**: Regular reading, writing, and critiquing enhance skill.
	- **Presentation**: Aim for clarity, aesthetics, and utility in every aspect of the document.
	- **Learning by Doing**: Practical experience and iterative refinement are emphasized as essential components of mastering scientific writing.
	  
	  
	  <!--EndFragment-->
- review
  collapsed:: true
	- ### 1.  **Introduction to the Review Process**
	- **Purpose**: Peer review acts as the quality control system for science, ensuring published work is reliable and well-vetted.
	- **Involvement**: All scientists contribute as reviewers or editors, requiring mastery of various aspects of the discipline.
	- **Discussion**: While essential, the process invites debates on its effectiveness and fairness.
	  
	  ---
	- ### 2.  **Theoretical Foundations**
	- **Reliability**: Publications must meet criteria of clarity, completeness, correctness, validity, and sometimes relevance.
	- **Broad Application**: Peer review applies not only to publications but also to grants, tenure decisions, and other resource allocations.
	- **Process**:
		- Peers, typically three per paper, evaluate the work anonymously.
		- Reviewers provide constructive feedback, improving both accepted and rejected manuscripts.
		  
		  ---
	- ### 3.  **Practical Implementation**
	- **Participants**:
		- Reviewers: Often experienced and overworked, they can lean conservative.
		- Authors: Must adhere to submission guidelines.
		- Editors: Oversee both scientific and administrative aspects, often multitasking across roles.
	- **Workflow**:
		- Manuscript Submission: Authors prepare and electronically submit papers.
		- Administrative Screening: Initial filtering by editors for alignment with the journal's scope.
		- Reviewer Selection: Editors choose reviewers based on expertise, keywords, or author suggestions.
		- Review Process: Reviewers assess manuscripts for clarity, validity, relevance, and methodological soundness.
		- Feedback: Reviewers submit reports, including numerical evaluations and open comments for authors and editors.
		- Editorial Decision: Based on reviews, the editor decides to accept, request revisions, or reject the paper.
	- **Review Outcomes**:
		- Accept, minor/major revisions, resubmit, or outright rejection.
		- Revisions may require extensive effort and detailed response letters from authors.
		  
		  ---
	- ### 4.  **Characteristics of a Good Review**
	- **Structure**:
		- Summarize the paper's content succinctly.
		- Provide an opinion with justifications.
		- Suggest improvements in both content and presentation.
	- **Engagement**: Reviewers should actively engage with the scientific aspects, offering insights into the literature, methodology, and findings.
	- **Diplomacy**: Feedback should be constructive and professional, avoiding unnecessary criticisms on trivial details.
	  
	  ---
	- ### 5.  **Challenges and Criticisms of Peer Review**
	- **Human Bias**:
		- Personal biases (e.g., institutional reputation, nationality, gender) can influence decisions.
		- Conformist research often fares better than innovative or interdisciplinary work.
	- **Expertise Limitations**: Finding qualified reviewers for niche or interdisciplinary topics is difficult.
	- **Social Engineering**:
		- Networking or favoritism can unfairly influence the process.
		- Groups may manipulate journal quality by collectively supporting each other's work.
	- **Fraud**: Ethical breaches include delaying reviews, rejecting competitors’ work, or stealing ideas.
	  
	  ---
	- ### 6.  **Alternatives to Peer Review**
	- **No Review**: Publishing without peer review or limited to checking for methodological soundness.
	- **Open Review**: Reviewers and authors openly identify themselves.
	- **Non-Anonymous Peer Review**: Transparency but potential for retaliation or bias.
	- **Double-Blind Peer Review**: Concealing both author and reviewer identities, though it doesn't eliminate all biases.
	  
	  ---
	- ### 7.  **Key Takeaways**
	- **Strengths**: Peer review ensures quality, offers improvement opportunities, and validates research credibility.
	- **Weaknesses**: It is prone to human error, biases, and systemic inefficiencies.
	- **Alternatives**: While promising, they also have drawbacks and require further refinement.
- ---
	- ### **Literature ("Now You Know" Solutions)**
	  collapsed:: true
		- **Reasons to Use Literature**:
			- To understand prior research and avoid redundancy.
			- To identify open questions and guide your research direction.
			- To provide a foundation for situating your work within the field.
		- **Reasons to Refer to Literature**:
			- To acknowledge others' contributions.
			- To situate your research in the broader context of previous findings.
			- To prevent plagiarism by properly crediting sources.
		- **What a Literature Review Is**:
			- A structured discussion of relevant works that highlights their contributions to a specific research question.
			- Includes historical context, major trends, and open questions.
		- **How to Start Looking for Literature**:
			- Use textbooks, journals, conferences, and citation networks (e.g., Google Scholar).
			- Read abstracts and introductions to assess relevance.
		- **How to Assess Literature Quality**:
			- Check journal impact factors and reputation.
			- Consider biases in citations (e.g., popularity vs. substance).
			- Account for field-specific publishing norms.
		- **How to Refer to Different Types of Sources**:
			- Follow specific citation styles (e.g., APA, MLA) and use tools like EndNote or Zotero.
			- Ensure completeness with DOIs, publication years, and journal names.
		- **How to Avoid Plagiarism**:
			- Properly paraphrase and cite sources.
			- Avoid copying directly without quotes or attribution.
			- Cite all data, figures, and code when used.
			  
			  ---
	- ### **Experiments ("Now You Know" Solutions)**
	  collapsed:: true
		- **Introduction Section**:
			- **Why Scientists Do Experiments**:
				- To test hypotheses and establish causal relationships in a controlled manner.
				- To gather reliable data in a reproducible format.
			- **The Importance of Experimental Theory**:
				- Guides experiment design and statistical analysis.
				- Standardizes terminology for effective communication.
		- **Computer Experiment Example**:
			- **Basic Terminology**:
				- **Independent Variables**: Factors manipulated (e.g., increment type).
				- **Dependent Variables**: Factors measured (e.g., execution time).
			- **Issues When Designing Experiments**:
				- Noise requires statistical analysis to establish confidence intervals.
				- Confounds (e.g., order effects) must be randomized or eliminated.
		- **Human Experiment Example**:
			- **Working with Human Participants**:
				- Consider subjective and objective measurements (e.g., usability scores vs. task performance).
				- Account for variability in participants through pre-testing and sampling.
			- **Within- and Between-Subject Designs**:
				- Within-subjects: Participants experience all conditions, reducing inter-participant variability.
				- Between-subjects: Participants experience only one condition, avoiding fatigue or learning effects.
			- **Randomized Controlled Trials**:
				- Randomize participants into treatment and control groups for unbiased comparisons.
		- **Theory Section**:
			- **Noise vs. Bias**:
				- **Noise**: Random variability manageable through statistics.
				- **Bias**: Systematic error requiring elimination (e.g., confounds, observer bias).
			- **Experimental Design Goals**:
				- Minimize noise and eliminate bias to improve reliability.
		- **Sampling Section**:
			- **Types of Sampling**:
				- Random sampling ensures representativeness but is challenging.
				- Non-random methods (e.g., quota, purposive) have specific applications but may introduce bias.
			- **Practical Approaches to Random Sampling**:
				- Cluster sampling helps achieve representative sub-samples.
		- **Research Plan Section**:
			- **Steps in Research Planning**:
				- Familiarize with the field and define a focused research question.
				- Operationalize variables, design pilot studies, and refine experimental setups.
				- Seek ethical approval for human studies.
		- **Why Planning is Crucial**:
			- Prevents disorganized or opportunistic research.
			- Facilitates data analysis and report writing.
	- ### **Statistics ("Now You Know" Solutions)**
	  collapsed:: true
		- ### **Now You Know**
		- #### **Why we need descriptive statistics**
		- Descriptive statistics summarize raw data to make it comprehensible.
			- **Measures of central tendency** (e.g., mean, median) provide insights into the "center" of data.
			- **Measures of spread** (e.g., range, standard deviation) describe variability.
			- Visual tools like histograms, boxplots, and scatterplots reveal patterns and distributions.
			  
			  ---
		- #### **The different measurement scales**
			- **Nominal**: Categories without an inherent order (e.g., gender, colors).
			- **Ordinal**: Categories with an order but unequal intervals (e.g., Likert scales[disagree, somewhat agree, agree]) no difference.
			- **Interval**: Ordered categories with meaningful intervals but no true zero (e.g., temperature in Celsius, dates) you can calculate differences.
			- **Ratio**: Ordered categories with meaningful intervals and a true zero (e.g., weight, height, temp in kelvin).
		- #### **A little bit about distributions**
			- Distributions show how data points are spread.
				- Common distributions include **normal distribution** (bell curve) and **skewed distributions**.
				- **Probability Density Function (PDF)** describes the likelihood of values within a range.
				- **Cumulative Distribution Function (CDF)** shows cumulative probabilities up to a value.
				- Quantile the opposite of CDF
				- ---
		- ### **Now You Know**
		- #### **Several measures of central tendency and their use**
		- **Mean**: Average value; sensitive to outliers.
		- **Median**: Middle value; robust to outliers.
		- **Mode**: Most frequent value; useful for categorical data.
		  
		  ---
		- #### **Several measures of spread and their use**
		- **Range**: Difference between the highest and lowest values.
		- **Variance**: Average squared deviation from the mean.
		- **Standard Deviation**: Square root of variance; shows average deviation.
		- **Interquartile Range (IQR)**: Range of the middle 50% of data; resistant to outliers.
		  
		  ---
		- #### **A few other measures of a distribution’s shape**
		- **Skewness**: Measures asymmetry in the data distribution.
			- Positive skew: Tail on the right.
			- Negative skew: Tail on the left.
		- **Kurtosis**: Measures "peakness" or tail heaviness(how frequent extreme values occur).
		- **Outliers**: Extreme values that lie far from most data.
		  
		  ---
		- ### **Now You Know**
		- #### **What a confidence interval is**
		- A confidence interval (CI) provides a range within which the true population parameter is likely to lie.
		- Confidence intervals are often used to indicate how uncertain a measurement is.
		- ---
		- #### **How to use it and interpret it**
		- Use CIs to express **uncertainty** in estimates.
		- Narrow intervals indicate **high precision**, while wide intervals suggest more variability.
		  
		  ---
		- #### **How not to use it**
		- Do not interpret a CI as the probability that the true value is in the range (the true value is either inside or outside).
		- Avoid using CIs without considering the context or effect size.
		  
		  ---
		- ### **Now You Know**
		- #### **What an effect size is**
		- Effect size measures the strength or magnitude of a relationship or difference.(how well a independent predicts the dependent variable)
			- **Cohen’s d**: Used for mean differences.
			- **η² (Eta-squared)**: Used for variance explained.
			- **Odds Ratio (OR)**: Used for binary outcomes.
			  
			  ---
		- #### **To look out for them when we go through the individual tests**
		- Effect sizes complement p-values by showing practical significance.
		- A significant p-value with a small effect size might indicate limited practical importance.
		- Significance is about the sample.
		- Effect shouldn't really change even then the sample becomes bigger.
		- ---
		- ### **Now You Know**
		- #### **Analyzing data from nominal and interval independent variables with interval dependent variables**
		- **Nominal Independent Variable**:
			- **Two values**: Use a **t-test**.
			- **Multiple values**: Use **ANOVA**.
		- **Interval Independent Variable**:
			- Use **linear regression** to test relationships.
			  
			  ---
		- #### **Interpreting a fitted linear model**
		- **Coefficients**: Show the relationship between predictors and the dependent variable.
		- **R²**: Proportion of variance explained by the model.
		- **Residuals**: Check if assumptions (e.g., normality) are met.
		  
		  ---
		- ### **Now You Know**
		- #### **Analyzing data with interval independent and dependent variables**
		- Use **correlation** to test linear relationships.
		- Use **linear regression** for predictive modeling.
		- Effect size: **Pearson’s r** (e.g., r = 0.1 is small, r = 0.5 is medium, r = 0.8 is large).
		  
		  ---
		- #### **Calculating sample size**
		- Use **power analysis** based on:
			- Expected effect size.
			- Desired significance level (α).
			- Power (1 - β, where β is the Type II error rate).
			  
			  ---
		- ### **Now You Know**
		- #### **Analyzing data with interval independent and nominal dependent variables**
		- Use **logistic regression** for binary outcomes.
		- Effect size: **Odds Ratio (OR)** (e.g., OR > 1 indicates increased likelihood).
		  
		  ---
		- ### **Now You Know**
		- #### **Analyzing data with nominal independent variables (2 or more values) and interval dependent variables**
		- **Two values**: Use **independent or paired t-tests**.
		- **More values**: Use **ANOVA** or **repeated-measures ANOVA**.
		- Effect size: **Cohen’s d** for t-tests, **η²** for ANOVA.
		  
		  ---
		- ### **Now You Know**
		- #### **Analyzing data with ordinal or non-normal interval dependent variables**
		- Use non-parametric tests:
			- **Mann-Whitney U** (for two groups).
			- **Kruskal-Wallis** (for multiple groups).
		- Effect size: **Rank-Biserial Correlation** for Mann-Whitney U.
		  
		  ---
		- ### **Now You Know**
		- #### **Analyzing data with ordinal independent and dependent variables**
		- Use **Spearman’s rank correlation**.
		- Effect size: Spearman’s rho (ranges from -1 to 1).
		  
		  ---
		- ### **Useful plots**
			- #### **Different types of plots and when to use them**
			  collapsed:: true
				- **Histograms**: Show frequency distributions.(bar chart)
				- **Boxplots**: Visualize medians and IQRs, highlighting outliers, whiskers indicating extent of the dataset.
				- **Scatterplots**: Explore relationships between two variables.
					- if scatterplot is too crowded use hexbin plot
			- #### **Using quantile-quantile (Q-Q) plots**
			  collapsed:: true
				- Compare data distribution to a theoretical distribution (e.g., normal).
				- Deviations from the diagonal line indicate departures from normality.
			- Independent variable: Horizontal axis
			  Dependent variable: Vertical axis
			- I: nominal, D: interval -> use boxplot
			- I: interval, D: interval -> scatterplot
			- I: nominal, D: interval -> hexbin plot
			- I: nominal, D: ratio -> histogram
			- I: nominal, D: nominal -> bubble plot in table format
			- I: interval, D: nominal(binary) -> scatter plot
			- ---
		- ### **Now You Know**
		- #### **Steps of a statistical test**
		- Define null and alternative hypotheses.
		- Select the appropriate test.
		- Compute the test statistic and p-value.
		- Compare the p-value to the significance threshold (α).
		- Draw conclusions.
		  
		  ---
		- #### **Why steps matter even with software**
		- Understanding steps ensures proper test selection and interpretation.
		- Helps diagnose issues like violations of assumptions.
		  
		  ---
		- #### **What a p-value is (and is not)**
		- **Is**: Probability of observing results as extreme as the sample, assuming H₀ is true. (the area under the curve that you consider is unacceptable)
		- **Is not**: The probability that H₀ is true or the probability of the observed data.
		  
		  ---
		- ### **Power and Significance**
		- #### **What power and significance are**
		- **Significance (α)**: Probability of Type I error (false positive).
		- **Power (1 - β)**: Probability of correctly rejecting H₀ (avoiding a Type II error).
		  
		  ---
		- #### **Relation to Type I and Type II errors**
		- Lower α reduces Type I errors but increases Type II errors.
		- High power reduces Type II errors but requires larger sample sizes.
		  
		  ---
		- #### **Using power analysis**
		- Plan sample size for adequate power.
		- Avoid using power analysis post hoc to justify results.
		- It is useful to think about the power of an experimental
		  approach, especially if it is to be used many times
			- For instance a setup for testing user interfaces
		-
		- Neyman and Pearson
			- not good for science
			- good for finding false positives(covids test, quality control)
	- ### **Writing ("Now You Know" Solutions)**
	  collapsed:: true
		- Here’s a detailed solution for the **"Now You Know" sections** from the **Writing Guide ("Methods of Scientific Research")**:
		  
		  ---
		- ### **Preparation**
		- **Key Points**:
			- **Purpose**:
				- Define the purpose of your text (e.g., reporting results, reviewing, proposing).
				- Tailor the content based on this purpose.
			- **Audience**:
				- Determine whether the audience is academic, professional, or lay.
				- Adjust background detail and technicality accordingly.
			- **Venue**:
				- Understand the publication format (journal, thesis, conference).
				- Align word count, tone, and level of detail with the venue's requirements.
			- **Message**:
				- Clearly articulate the key message and conclusion of your work.
				- Highlight your contribution and ensure relevance to the target audience.
			- **Background**:
				- Provide sufficient context to bridge the audience's knowledge gaps.
				- Avoid assumptions; cite references to clarify methods and sources.
			- **Storyline**:
				- Sketch a logical flow of ideas to prevent redundancy and confusion.
				  
				  **Solution**:
		- Invest time in defining these parameters before writing.
		- Use preparation to streamline your work and enhance clarity.
		  
		  ---
		- ### **Organization**
		- **Key Points**:
			- **Canonical Structure**:
				- Follow the standard scientific structure:
					- **Abstract**: Condense the essence of the study.
					- **Introduction**: Present the context and research questions.
					- **Methods**: Detail replicable procedures.
					- **Results**: Present factual findings without interpretation.
					- **Discussion/Conclusion**: Interpret results and propose implications.
			- **Chapter Management**:
				- Keep chapters balanced and logically ordered.
				- Avoid excessive subsections; keep headings clear and informative.
			- **Supplementary Elements**:
				- Use appendices for detailed data or background information.
				- Include acknowledgments and bibliographies appropriately.
				  
				  **Solution**:
		- Use the canonical structure to organize both reading and writing effectively.
		- Ensure chapters flow cohesively, aiding comprehension.
		  
		  ---
		- ### **Writing Text**
		- **Key Points**:
			- **Parallel Process**:
				- Write alongside research to identify gaps and refine questions.
				- Use writing to document and clarify your methodology and findings.
			- **Iterative Process**:
				- Write drafts, review them with time, and seek feedback.
				- Edit and revise to maintain consistency and clarity.
			- **Feedback**:
				- Accept critiques from supervisors and colleagues.
				- Address feedback constructively to improve quality.
			- **Style**:
				- Avoid jargon, over-complicated language, and inconsistent voice.
				- Write concise, precise, and reader-friendly paragraphs.
				  
				  **Solution**:
		- Embrace writing as a continual and reflective process.
		- Prioritize clarity and responsiveness to feedback to enhance the final text.
		  
		  ---
		- ### **Illustrations**
		- **Key Points**:
			- **Diagrams and Graphs**:
				- Use clear, labeled visuals that add value to the text.
				- Ensure readability in both color and grayscale.
			- **Tables**:
				- Include tables only when they convey information succinctly.
				- Simplify data presentation; move complex data to appendices if necessary.
			- **Algorithms and Equations**:
				- Present algorithms as pseudocode for clarity.
				- Define all symbols and number equations for easy referencing.
			- **Style and Accessibility**:
				- Avoid overly complex visuals, poor formatting, or illegible designs.
				- Use formats and color schemes that accommodate colorblind readers.
				  
				  **Solution**:
		- Use non-text elements thoughtfully to complement and enhance your writing.
		- Maintain aesthetic and functional quality in all visuals.
	- ### **Review ("Now You Know" Solutions)**
	  collapsed:: true
		- ### **Why Peer Review?**
		- Peer review ensures quality control in science by vetting research for clarity, validity, relevance, and correctness. It provides a system of checks to maintain the reliability of published work.
		  
		  ---
		- ### **How Peer Review Works**
			- **The Process**:
				- Authors submit manuscripts.
				- Editors filter for suitability and select reviewers based on expertise.
				- Reviewers evaluate and provide structured feedback.
				- Editors decide based on reviewer input, leading to acceptance, revision, or rejection.
			- **The Actors**:
				- Reviewers: Assess the paper’s quality and suggest improvements.
				- Editors: Facilitate and oversee the review process.
				- Authors: Address feedback constructively and resubmit if necessary.
				  
				  ---
		- ### **What a Good Review Should Contain**
			- **Summary**: Briefly outline what the paper is about and its key contributions.
			- **Opinion**: Provide reasoned judgments about its significance and validity.
			- **Suggestions**: Offer constructive criticism for improving content, methodology, and presentation.
			- **Engagement**: Actively engage with the science, contributing insights rather than focusing on trivial issues.
			  
			  ---
		- ### **The Weaknesses of Peer Review**
			- **Bias**: Mitigate biases (personal, institutional, or cultural) by using double-blind or open review systems.
			- **Expertise**: Match manuscripts with appropriately skilled reviewers, especially for interdisciplinary work.
			- **Social Engineering**: Increase transparency to discourage favoritism or retaliatory behavior.
			- **Fraud**: Implement stricter oversight and accountability to curb unethical practices like idea theft.
			  
			  ---
		- ### **Alternatives to Peer Review**
			- Evaluate alternatives such as **open review** (transparent identities) and **double-blind review** (anonymity for both authors and reviewers).
			- Consider "soundness-only" review, focusing on methodological validity over novelty.
			- Balance the trade-offs of these systems to address biases and improve fairness while maintaining rigorous standards.
-