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
  
  ---
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