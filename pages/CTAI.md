- The document "**Causal Federated Learning For Neuroimaging**" by Alvaro Vargas Guerrero explores how Federated Learning (FL) can address the unique challenges of applying AI in the medical sector, specifically for neuroimaging research.
- ### **The Problem: Why AI Lags in Medicine**
  Despite advancements in LLMs and multimodal AI, healthcare AI remains largely theoretical due to several critical barriers:
  *   **Data Issues:** Medical data often suffers from **data imbalance** (non-IID conditions), a **lack of overall data**, and **biased data** sets.
  *   **Privacy and Legal Constraints:** Regulations like **GDPR** and the complexity of data consent make sharing raw, private patient data between institutions extremely difficult.
  *   **Institutional "Agendas":** Different types of hospitals (government, private, non-profit) have varying legal definitions and incentives, further complicating data centralization.
- ### **The Solution: Federated Learning (FL)**
  Federated Learning is presented as a privacy-preserving alternative to traditional centralized training. Instead of moving data to a central server, the model is moved to the data.
  *   **Mechanism:** Local institutions (hospitals, research centers) train **local models** on their own private data. They then send only **model updates or weights** to a central **Federated Server**. The server aggregates these updates to create a **Global Model**, which is then redistributed back to the participants.
  *   **Key Advantage:** It allows for collaboration and massive data scaling without ever exchanging raw, sensitive patient information—summarized by the phrase, **"We’re not exchanging data, your Honor"**.
- ### **Open Challenges of FL**
  While FL solves privacy issues, it introduces new technical and security hurdles:
  *   **Model Security:** The system is vulnerable to **poisoning attacks** (where an adversary corrupts local data or models), **man-in-the-middle attacks**, and **DDoS** attacks.
  *   **Overhead:** There is significant **computation overhead** (running local training loops) and **communication overhead** (frequently uploading and downloading model updates).
  *   **Heterogeneity and Fairness:** "Client drift" occurs when data across different hospitals is too diverse. Furthermore, smaller institutions with less data may feel excluded if **incentive mechanisms** and **fairness** (e.g., FairFed) are not properly managed.
- ### **The Intersection of FL and Causality**
  The document argues that the "Achilles heel" of current machine learning is its reliance on **correlation rather than causation**. 
  *   **The Ladder of Causation:** Drawing on Judea Pearl’s work, the author notes that standard AI only operates on the first rung (**Association/Seeing**). 
  *   **Goal:** To reach higher rungs like **Intervention (Doing)** and **Counterfactuals (Imagining)**, researchers are developing **Federated Causal Discovery**.
  *   **Application:** This approach is being used by the AIMS group at VUB to study cognitive deterioration in Multiple Sclerosis (MS) across an international network, allowing for **explainable-by-design** models that support causal interventions.
  
  
  
  
  
  **Syrtis** is a unified **control-plane for enterprise AI**, designed as a platform to design, test, deploy, and monitor AI services with the reliability of software engineering. It acts as an orchestrator for **Generative AI architecture**, specifically helping organizations move beyond "prototype purgatory" where 95% of AI projects typically fail due to a lack of control architecture.
- ### **Core Vision and Methodology**
  The primary mission of Syrtis is to help organizations turn critical workflows into **trustworthy AI services** quickly, without compromising sovereignty, security, or control. 
  
  *   **Skill Blending Process (SBP):** Syrtis employs a methodology that rethinks workflows as **hybrid intelligence systems**. This process articulates human skills and compute skills along a common algorithm defined with the human operators.
  *   **Resource Optimization:** The platform focuses on optimizing three key resources: **Time** (freeing up quantitative hours), **Information** (ensuring 24/7 availability and coherence), and **Knowledge** (transforming static info into dynamic assets).
  *   **AI as an Optimizer:** The philosophy behind Syrtis is that AI should not replace existing systems but rather optimize them and fix "broken workflows".
- ### **The Technical Full-Stack Platform**
  Syrtis provides an end-to-end production line for enterprise-grade AI through a multi-step architecture:
  
  1.  **Ingest:** Accepts diverse data types including CSV, SQL, PDFs, and APIs.
  2.  **Index & Enrich (Content-Aware Indexing):** Converts structured and unstructured data into a live knowledge layer grounded in verifiable sources using **Retrieval-Augmented Generation (RAG)**.
  3.  **Design (Visual Scenario Builder):** Features a drag-and-drop interface with modular "Agent Blocks" allowing teams to build specialized agents (e.g., for HR or Ops) in hours rather than months.
  4.  **Test:** Includes built-in source-backed evaluations and automated accuracy tests to eliminate hallucinations and provide a clear citation trail.
  5.  **Deploy:** Offers one-click rollout to **EU Sovereign Cloud** or on-premises environments, ensuring no data leaves the customer's perimeter (GDPR by default).
  6.  **Monitor:** Provides real-time dashboards to track latency, token costs, drift alerts, and carbon footprint while maintaining logs ready for **EU AI-Act compliance**.
- ### **Key Features and Infrastructure**
  *   **Multi-Agent Systems (MAS):** Syrtis architecture allows for the seamless integration of traditional programming (code) and AI agents that collaborate to produce precise user experiences.
  *   **Model-Agnostic:** It allows organizations to mix and match models from OpenAI, Anthropic, or various open-source LLMs within the same graph without rewiring the entire system.
  *   **Auditability:** The platform places auditability at its core, providing full request "waterfalls" and data lineage for every interaction.
- ### **Real-World Impact: The FIBA Use Case**
  A major application of Syrtis is the **"DRAZEN" Expert Assistant** developed for **FIBA (International Basketball Federation)**. 
  *   **The Problem:** Traditional LLMs struggled with factual mistakes and instability when processing large, 15,000-line game files.
  *   **The Syrtis Solution:** By using a fully controllable orchestration layer that combined Python code with LLM interpreters, Syrtis built an automated game report generation service.
  *   **Results:** The system reduced the editorial cycle time by **97%** (from 3 hours to 5 minutes) and allowed for the production of **3,000 reports per year**, a feat described as impossible with standard ChatGPT.
- ### **The Organization**
  Syrtis is led by CEO **Maxime Favier** (a PhD and entrepreneur) and CTO **Romain Weeger** (a lead system architect with 25+ years of experience). The project is the result of over two years of R&D, supported by advisors from the **Vrije Universiteit Brussel (VUB)** and financed by **Innoviris**.
  
  
  
  
  
  
  
  Arnau Dillen’s presentation and research focus on the evolution of **Brain-Computer Interfaces (BCI)** as an alternative interaction modality to standard tools like mice and keyboards, which often exclude individuals with motor impairments or are inefficient in specialized environments like industrial floors.
- ### **I. Fundamentals of Brain-Computer Interfaces**
  BCI technology works by measuring the electrical activity generated by neurons in the brain. These signals can be captured through several methods:
  *   **Non-Invasive Methods:** The most common is the **Electroencephalogram (EEG)**, which is portable and has high temporal resolution but is often noisy with low spatial resolution. Other methods include **Magnetoencephalogram (MEG)** and chemical-based methods like **fMRI**.
  *   **Invasive Methods:** These require surgical implants, such as **Electrocorticography (ECoG)** or **Local Field Potentials (LFP)**, to achieve higher precision, though they carry greater medical risks.
- ### **II. Arnau’s Research: Optimizing BCI for Control**
  Arnau’s PhD research specifically targets **Motor Imagery (MI) BCI**, where a user’s imagined movements (e.g., left hand, right hand, tongue, or feet) are mapped to device actions. Key contributions include:
  *   **Optimal Sensor Set:** While clinical EEG caps often use 64 sensors, Arnau’s study found that **eight sensors** are sufficient to achieve adequate decoding performance, which significantly reduces setup time from 30 minutes to under five.
  *   **Shared Control Strategy:** To simplify the mental load on the user, he developed a **shared control approach**. In this system, the robot (a "cobot" or collaborative robot) is semi-autonomous and spatially aware. The user provides high-level commands via BCI, while the robot handles the precision of the movement.
  *   **Multimodal Interaction:** The system integrates **Augmented Reality (AR)** through a HoloLens 2, allowing users to see a menu of actions overlaid on real-world objects, and **eye tracking** to select which object to interact with.
  *   **Standardized Evaluation:** Arnau established a modular framework to evaluate the **usability** of BCI prototypes, measuring efficiency (completion time), effectiveness (success rate), and user experience.
- ### **III. State-of-the-Art Decoding Trends**
  Modern BCI research is moving beyond standard linear models toward more complex architectures:
  *   **Advanced Features:** **Riemann geometry** is used to map 2D EEG data onto a 3D manifold to better localize brain activity, while **Filter Bank Common Spatial Patterns (FBCSP)** learn which specific frequencies are most informative for an individual.
  *   **Deep Learning:** New models use **Convolutional Neural Networks (CNNs)** to automatically learn spatial and temporal features. More recent trends include using **Transformers** with self-attention to capture long-range dependencies in brain activity.
- ### **IV. Novel and Future Applications**
  Current trends are pushing BCI into diverse fields:
  *   **Generative AI:** Researchers are now using EEG signals as inputs for generative models to **reconstruct images** that a person is looking at or imagining.
  *   **Communication:** **Brain-to-text** applications allow paralyzed individuals to type or "handwrite" text on a screen by imagining the physical motions.
  *   **Bidirectional BCIs:** These systems not only decode movement but also use electrical stimulation to **restore the sense of touch** in prosthetic limbs.
  *   **Next-Gen Hardware:** Companies like **Neuralink** are developing lower-risk implants, while others are creating **dry EEG sensors** that do not require conductive gel, making the technology more "plug-and-play".
  *   **Cognitive Modeling:** Future projects like **MEMOBRAIN** aim to use AI to extract active "brain states" to better understand and diagnose neurological diseases like **Multiple Sclerosis**.
  
  
  
  
  
  
  
  
  This in-depth summary of **counterfactuals** is based on the provided presentation and slides by Dimitris Sakharidis, which explore their role in making machine learning models explainable and fair.
- ### **I. The Theoretical Foundation: The Ladder of Causation**
  Counterfactuals represent the highest level of reasoning in Judea Pearl’s "Ladder of Causation," which describes how humans and machines evolve in their understanding of the world:
  *   **Level 1: Association (Seeing):** Observing correlations and patterns (e.g., "What does a symptom tell me about a disease?").
  *   **Level 2: Intervention (Doing):** Taking actions to observe effects, often through Randomized Controlled Trials (e.g., "If I take aspirin, will my headache be cured?").
  *   **Level 3: Counterfactuals (Imagining):** Reasoning about hypothetical scenarios in imaginary worlds (e.g., "Would the patient have lived if they had been vaccinated?"). This requires **retrospection**—intervening on a world that has already occurred to understand what *might* have been.
- ### **II. Counterfactual Explanations in Machine Learning**
  In the context of AI, a counterfactual explanation describes the **minimal changes** required to an input’s features to flip the model's output to the opposite result.
  
  *   **Mechanics:** If a model takes input $x$ (factual) and produces output $y$ (e.g., "Loan Rejected"), a counterfactual $x'$ is found such that the model produces the opposite output $-y$ ("Loan Approved"). The difference ($x' - x$) serves as the explanation.
  *   **Decision Boundaries:** Visually, this is the process of finding the nearest point on the other side of a model’s **decision boundary**. Since these boundaries are often "black boxes," counterfactuals are generated by making guided changes to data until the outcome flips.
  *   **Diverse Counterfactuals:** Because there are often many ways to change an outcome, models should provide **diverse** options (e.g., "To get a loan, you could either increase your working hours OR get a Master’s degree").
- ### **III. Algorithmic Recourse and Feasibility**
  While a counterfactual is a mathematical explanation, **algorithmic recourse** is a practical plan provided to an individual to help them reverse an unfavorable decision. To be useful, counterfactuals must meet specific criteria:
  *   **Proximity:** The change should be as small as possible.
  *   **Probability:** The suggested counterfactual state must look like realistic data.
  *   **Feasibility:** The changes must be possible to implement; for example, an explanation that requires a user to "decrease their age" is useless.
- ### **IV. Global Counterfactual Explainability**
  Global explainability seeks to understand the behavior of the **entire model** rather than a single instance.
  *   **Summarization:** This involves identifying a small set of "counterfactual actions" that apply to large subpopulations (e.g., "For all foreign workers with few home-years, increasing job experience to four years flips the loan decision").
  *   **Techniques:** Tools like **GLANCE** use joint clustering on both feature and action spaces to find these general rules, while **GLOBE-CE** uses translation-based methods to find global "directions" for local actions.
- ### **V. Counterfactuals for Fairness**
  Counterfactuals are a powerful tool for auditing and ensuring **algorithmic fairness**, moving beyond simple correlation to causal fairness.
  *   **Counterfactual Fairness:** An individual-level metric stating that a decision is fair if it would have been the same even if the person's **protected attribute** (like race or gender) had been different.
  *   **Discovering Unfairness:** If the minimal change required to flip a "Loan Rejected" outcome to "Approved" is simply changing the user's sex from female to male, it is a clear indication of discrimination.
  *   **Fairness of Recourse:** This measures whether it is harder (more "costly") for certain protected groups to achieve a positive outcome than others. For example, a model is unfair if women must increase their income by $20k to get a loan, while men only need to increase it by $5k.
  
  
  
  
  
  
  
  
  
  **AI Attribution** is the process of identifying and quantifying the specific contribution of different factors—whether input features or training data—to a machine learning model's final decision. As AI models tackle harder tasks, their complexity grows, often turning them into **"black boxes"** where the rationale for a specific recommendation or classification is no longer human-interpretable.
- ### **I. Core Types of Attribution**
  There are two primary levels at which attribution is conducted:
  *   **Feature Attribution:** Identifies which input variables (e.g., age, salary, race) were most influential for a specific outcome.
  *   **Data Attribution:** Explains the model through the lens of the **training data** it was built upon. This approach treats the model as a product of its training samples and seeks to identify which specific examples "taught" the model to behave in a certain way.
- ### **II. Local Data Attribution: Explaining Specific Decisions**
  Local attribution focuses on why a model made a specific prediction for a new data point.
  *   **Leave-One-Out (LOO):** The most intuitive method, where a single training sample is removed, the model is retrained, and the change in loss is measured. While conceptually simple, it is **exhaustively expensive** for large datasets.
  *   **Influence Functions:** To avoid the cost of retraining, this method from robust statistics approximates the change in loss by upweighting a training sample by an infinitesimal amount. It uses **gradients** and **Hessian matrices** to calculate influence.
  *   **Robustness and Class Outliers:** Influence-based methods are susceptible to **class outliers**—points that resemble one class but are labeled as another. Researchers suggest using **proximity-based robustness** and **explaining by contrast** (showing what a point is *not*) to improve reliability.
  *   **User Intent:** Explanations should be customized to what the user needs: interpreting a correct prediction (using "supporters") or investigating a wrong one (identifying "opposers").
- ### **III. Shapley Values and Efficiency**
  Derived from game theory, **Shapley values** provide a mathematically fair way to allocate "credit" to inputs in a coalition. 
  *   **The 2^N Problem:** Calculating exact Shapley values requires $2^N$ model calls, which is computationally impossible for most ML scenarios.
  *   **Approximation Methods:** 
    *   **Kernel-SHAP:** Trains a linear surrogate model to predict the loss based on random coalitions of data.
    *   **TMC-Shapley:** Uses a Monte-Carlo approach to shuffle data permutations and compute average marginal contributions, employing **truncation** to stop when the change in loss becomes negligible.
- ### **IV. Global Data Attribution: Understanding Model Behavior**
  Global attribution aims to explain the overall behavior of a model rather than a single instance.
  *   **Data Prototypes:** These are representative points that summarize the entire dataset.
  *   **Prototypical Self-Explainable Models:** These models find prototypes within the model’s own **embedding space** and use them for classification, ensuring the explanation is highly faithful to the model's internal logic.
  *   **InfProto:** This hybrid approach bridges local and global explainability by using a single process to generate both **prototypes** (showing what a model generally thinks) and **influential instances** (showing what specific samples caused a fluke or pattern).
- ### **V. Attribution in the Era of LLMs and RAG**
  In **Retrieval-Augmented Generation (RAG)**, attribution is critical for determining which retrieved documents actually influenced an LLM's answer.
  *   **ContextCite:** A popular method that trains a linear surrogate model to approximate how an LLM's response changes as parts of the context are ablated (removed). 
  *   **Inter-Document Relationships:** A major limitation of linear models like ContextCite is that they struggle to account for complex relationships between documents:
    *   **Redundancy:** Multiple documents providing the same information.
    *   **Complementarity:** Documents answering different parts of a multi-part query.
    *   **Synergy (Multi-hop):** Cases where two or more documents must be combined to reach an answer.
  *   **FACILE:** To address these interactions, **FACILE** uses **Factorization Machines** (polynomial models) as a surrogate. This allows the system to model **pairwise interactions** and identify cases of synergy or redundancy more accurately and cost-effectively than linear methods.
  
  
  
  
  
  
  
  **Datashift** is a consultancy specializing in helping organizations realize real value from AI while managing its inherent risks through a **Responsible AI** framework. With 175 employees across four locations in Belgium and the Netherlands, the organization has seen 40% year-over-year growth. Their core philosophy is that while AI is incredibly useful today, scaling alone will not lead to Artificial Super Intelligence (ASI), and organizations must move "beyond the algorithm" to achieve sustainable success.
- ### **I. The Responsible AI Philosophy**
  Datashift defines Responsible AI as the practice of developing AI in a way that **maximizes value while managing risk** and avoiding harm. They advocate for a shift in focus from simply optimizing machine learning models to answering broader strategic questions:
  *   **Should we build this system?** (Ethical and value alignment).
  *   **How should we build it?** (Technical and safety considerations).
  *   **How do we do this consistently?** (Scalability and governance).
- ### **II. Framework for AI Risk Management**
  Datashift proposes a "101" approach to risk management, defining **risk** as the probability of a negative outcome multiplied by the severity of its harm. Their framework involves three continuous steps across the AI lifecycle (Design, Build, and Operate):
  1.  **Identify:** Map potential organizational risks to individual use-cases.
  2.  **Measure:** Evaluate the probability of occurrence and the potential impact.
  3.  **Manage:** Take deliberate actions to **avoid, mitigate, transfer, or accept** risks based on clear trade-offs.
- ### **III. Strategic Trade-offs**
  A central theme of the Datashift approach is making deliberate choices throughout the AI lifecycle:
  *   **Ambition vs. Exposure:** Deciding if a project’s scope is worth the potential risk exposure (e.g., testing a chatbot internally before a customer rollout).
  *   **Budget vs. Risk Mitigation:** Determining how much to invest in safety tools, such as software to measure bias.
  *   **Benefits vs. Risks:** Assessing if a "high-risk" solution can be deployed temporarily to ensure business continuity.
- ### **IV. Key Risks and Recommended Controls**
  Datashift identifies a specific taxonomy of risks and provides corresponding technical and organizational (ORG) controls:
  *   **Accuracy:** Mitigated by performance and user testing.
  *   **Fairness:** Addressed by changing training/test data or adapting model architecture to avoid discrimination.
  *   **Safety & Security:** Managed through **input/output filters**, adversarial testing, and **prompt injection detection**.
  *   **Compliance:** Ensuring adherence to regulations like the **EU AI Act** and **GDPR** by controlling where data is processed.
  *   **Environment:** Monitoring the carbon footprint of AI training and deployment.
- ### **V. Implementing Responsible AI at Scale**
  For organizations managing 100+ use-cases, Datashift recommends building **foundational blocks** to standardize workflows:
  *   **AI Governance Policy:** Defining organizational rules and accountability.
  *   **AI Inventory:** Maintaining an overview of all active AI projects and their risk levels (e.g., prohibited, high, limited, or minimal risk).
  *   **Responsible AI Principles:** Providing high-level guidance for all employees.
  *   **Standardized Workflows:** Using risk assessment questionnaires and operational templates to ensure consistency.
  
  Datashift concludes that AI should be viewed simultaneously as a **tool** for value, a **fool** that can hallucinate or fail (like the Dutch Tax authority's biased models), and a **target** for adversaries, requiring constant vigilance and human oversight.
  
  
  
  
  
  
  
  This in-depth summary of the **CTAI** (Current Trends in AI) presentation explores the evolving relationship between society and algorithms, focusing on the concept of "Algocracy" and the role of the FARI institute.
- ### **I. Core Concept: Algocracy**
  The presentation centers on the theme of **Algocracy**, questioning whether society is ready to give significant power to algorithms. It explores how algorithms move beyond simple tools to become systems that exert power over human behavior and societal structures.
- ### **II. Taxonomy of Algorithmic Power**
  The source categorizes algorithmic presence into two distinct levels of influence:
  *   **Algorithms that Recommend (Influence):** These are pervasive in daily life, guiding choices through platforms like **Netflix** for entertainment, **Waze** for navigation, **Google** for information, and apps like **Tinder** or **Vinted** for social and commercial interactions.
  *   **Algorithms that Oblige (Control):** These systems impose specific outcomes or require compliance. Examples include:
    *   **Public Administration:** Platforms like **Tax-on-web** for mandatory fiscal declarations.
    *   **Access and Eligibility:** **Credit scoring** systems and physical **turnstiles** that control entry based on algorithmic verification.
    *   **Infrastructure:** **Smart electricity meters** that monitor and potentially regulate home energy use.
- ### **III. FARI: AI for the Common Good**
  FARI is presented as a major collaborative institute between **ULB and VUB** designed to bridge the gap between public institutions, industry, research, and civil society. 
  *   **Key Infrastructure:** 
    *   **Test & Experience Center:** A 600m² facility with over 15 demonstrations showcasing the potential impact of AI and robotics.
    *   **CAVE (Computer Augmented Virtual Environment):** Belgium's largest CAVE (147 sqm), featuring 4K projectors and dual GPU clusters for immersive, real-time interaction with complex digital environments.
  *   **Flagship Programs:** FARI focuses on six critical domains: **Health & Wellbeing**, **Energy**, **Mobility**, **Media/Democracy**, **Public Sector & Administration**, and the **Green Deal**.
  *   **Impact:** To date, FARI has awarded 15 PhD grants for "AI for the Common Good" and engaged with over 4,000 participants through various community events.
- ### **IV. The CITICOD Project: Democratic Algorithm Design**
  To legitimize the use of algorithms in the public sector, the **CITICOD project** advocates for **Citizen Coding**—implicating the public in the design of systems that affect them.
  *   **Collaborative Development:** It proposes a tripartite group of developers: domain and law experts, randomly selected citizens, and elected politicians to resolve ideological conflicts.
  *   **Algorithmic Applications:** This "social coding" approach is applied to high-stakes use cases, such as:
    *   **School Access:** Using the **Gale-Shapley (stable marriage) algorithm** to match students to schools or universities fairly.
    *   **Resource Management:** Designing algorithms for **collective mobility** and **neighborhood energy pooling**.
- ### **V. Critical Case Studies: Successes and Failures**
  *   **The Covid-19 Contact Tracing Failure:** The source critiques early contact tracing apps as failures because they were developed by tech companies with **no transparency, efficiency, or citizen participation**. It argues these companies often fail when they impose technology on domains they do not understand, such as public health, without listening to experts or the public.
  *   **Brussels Vaccination Strategy:** Conversely, FARI demonstrated success by helping develop a vaccination strategy that used algorithms to match patients with the most efficient testing and vaccination centers.
  *   **Energy and Mobility:** Other projects include retrofitting homes with smart meters to detect appliance patterns (e.g., dishwashers) and developing "Mobility as a Service" solutions.
  
  
  
  
  
  
  
  The provided slides, titled **"Current Trends: A Hands-on Introduction to Hierarchical Pattern-Based Sequence Learning"** by Patrick Van der Spiegel, offer a technical deep dive into time series analysis, focusing on how to represent and learn from sequential data to detect anomalies.
- ### **I. Fundamentals of Sequence Data**
  The presentation defines **sequence data** as ordered sets of elements (continuous or discrete) generated by observing processes or systems over time via sensors or event logs. 
  *   **Time Series:** An ordered sequence of observations ($S = (s_{t_1}, \dots, s_{t_n})$) where each point is observed at a specific time. These can be **univariate** (single variable) or **multivariate** (multiple variables).
  *   **Sliding Windows:** This is the primary method for extracting local parts of a sequence. A window of fixed length $k$ slides across a sequence of length $n$ to extract all possible contiguous subsequences.
- ### **II. Measuring Similarity: Distances and Profiles**
  Determining similarity is the foundation of sequence learning. The slides focus on **z-normalised Euclidean distance** as a core dissimilarity measure.
  *   **Distance Profile:** For a specific "query" segment, a distance profile calculates the distance between that query and every other subsequence in the time series.
  *   **Motifs and Discords:**
    *   **Motifs:** Recurring subsequences that have a very low distance to each other.
    *   **Discords:** Subsequences that are maximally different from all others, often indicating an anomaly.
  *   **Matrix Profile:** This is a meta-structure that stores the distance to the **nearest neighbor** for every segment in a time series. It is the primary tool used to identify motifs (low-distance groups) and discords (highest-distance segments).
- ### **III. Dimensionality Reduction: Piecewise Approximations**
  Calculating distances for every segment in massive datasets is computationally "not manageable". To solve this, the slides introduce **Piecewise Approximations**, which reduce dimensionality by partitioning a sequence into non-overlapping frames and approximating each frame with a small number of values.
  *   **Piecewise Linear Approximation (PLA):** Represents frames using lines (slopes/intercepts).
  *   **Piecewise Aggregate Approximation (PAA):** Uses the average value of each frame.
  *   **Symbolic Aggregate Approximation (SAX):** Discretizes values into a symbolic (alphabet-based) representation.
  *   **Trade-off:** These methods trade accuracy for speed. Increasing the number of frames improves the accuracy of the distance profile approximation but increases computational cost.
- ### **IV. Sequence Learning and Anomaly Detection**
  The slides define three main sequence learning tasks: **Recognition** (identifying known patterns), **Prediction** (forecasting future values), and **Generation** (producing synthetic data).
  *   **Time Series Anomaly Detection (TSAD):** This is the process of flagging data points or subsequences that deviate from "normal" behavior.
  *   **The "No One-Size-Fits-All" Rule:** Anomaly detection is context-dependent; what is an anomaly in one domain (e.g., a sudden drop in power load) might be normal in another.
  *   **Benchmarks:** The **UCR time series anomaly archive** (250 datasets) is cited as a gold standard for testing detection algorithms because it contains diverse, real-world data with ground-truth anomalies.
- ### **V. Hierarchical Pattern Matching (HPM)**
  The core contribution of the slides is the **HPM algorithm**, a multi-granular approach to anomaly detection implemented through the `pbsf-lib` library. 
  *   **The Workflow:** 
    1.  **Segmenter:** Splits input into ordered segments (e.g., via SlidingWindow).
    2.  **Discretiser:** Converts segments into **Chains**, which are multiple approximations of varying granularity (from coarse-grained to fine-grained).
    3.  **Model (PatternTree):** A hierarchical structure where nodes are segment approximations.
  *   **The PatternTree Logic:**
    *   **Root Nodes:** Store coarse-grained approximations (low number of frames).
    *   **Leaf Nodes:** Store fine-grained approximations (high number of frames).
  *   **Training vs. Testing:** During training, the tree is populated with "legitimate" chains from a training set. During testing, new chains are compared against the tree; if a chain (or its specific approximations) is **not present** in the tree, it is marked as an anomaly.
  
  
  
  
  
  
  
  
  
  
  
  This in-depth summary covers the presentation **"Beyond ChatGPT: LLMs, Retrieval-Augmented Generation, and Agents,"** delivered by **Cédric Gilon** on May 22, 2026. The session explores the technical evolution of Large Language Models (LLMs), the mechanics of Retrieval-Augmented Generation (RAG), and the shift toward autonomous agents.
- ### **I. The LLM Landscape (2020–2026)**
  The materials trace a rapid trajectory from the release of GPT-3 in 2020 to the advanced landscape of 2026.
  *   **Key Milestones:** Highlights include the 2022 release of ChatGPT (reaching 100M users in two months), the 2023 rise of multimodal reasoning in GPT-4, and the 2024 emergence of high-performance "open-weights" models like Llama and Mistral.
  *   **Thinking Models:** A major shift occurred in late 2024 with "thinking" models like **OpenAI o1** and **DeepSeek R1**. These models generate hidden "inference tokens" to reason internally before providing a final answer. The philosophy is that **"thinking more" is better than "knowing more,"** as longer inference times lead to significantly higher answer quality.
  *   **Efficiency via MoE:** Models like **DeepSeek V3** utilize **Mixture of Experts (MoE)**, where tokens are routed to specific "experts". While the model may have 671B parameters, only about 37B are activated per token, optimizing compute for faster inference.
- ### **II. Fundamentals and Training Mechanics**
  At their core, LLMs follow a simple mathematical objective: **predicting the next token** based on all previous tokens in a sequence.
  *   **Tokens:** LLMs process sub-word units called tokens, a trade-off that balances vocabulary size with sequence length. Rare words are often split into more tokens.
  *   **Architecture:** Modern LLMs rely on the **Transformer architecture** and its **self-attention mechanism**, which allows tokens to identify correlations with other tokens in the same sentence (e.g., matching the word "it" to the correct subject).
  *   **The Training Pipeline:**
    1.  **Pre-training:** Gathering trillions of tokens from the internet (e.g., the 44TB **FineWeb** dataset) to teach the model language and knowledge.
    2.  **Fine-tuning:** Training the model on question-and-answer datasets to teach it to act as an assistant.
    3.  **Post-training (Alignment):** Using **Reinforcement Learning with Human Feedback (RLHF)** or more stable alternatives like **Direct Preference Optimization (DPO)** to ensure the model is helpful, harmless, and follows editorial boundaries.
- ### **III. Context and the "Lost in the Middle" Problem**
  Context windows have expanded dramatically, from 128K tokens to **Gemini's 2M+ tokens** (roughly 6,000 pages). 
  *   **Imperfect Recall:** Despite larger windows, models suffer from being **"lost in the middle,"** finding it easier to retrieve information from the very start or very end of a long prompt than from the center.
  *   **Use Cases:** Massive context allows for putting a full codebase, entire books, or complex legal documents into a single prompt.
- ### **IV. Retrieval-Augmented Generation (RAG)**
  RAG is the primary technical solution for **hallucinations** (false information) and the **knowledge cutoff** (information newer than the model's training data).
  *   **Workflow:** Documents are split into **chunks**, converted into dense **vectors (embeddings)**, and stored in a **Vector DB**. When a user asks a question, the system retrieves the "top-k" chunks with the highest semantic similarity to provide as context for the LLM's answer.
  *   **Advanced Techniques:** To improve quality, developers use **Re-ranking** (filtering retrieved chunks for accuracy), **HyDE** (generating a fake answer first to improve document retrieval), and **Query Decomposition** (breaking one complex question into multiple sub-questions).
  *   **Evaluation:** The **RAGAS** framework is used to automatically evaluate RAG systems based on **faithfulness** (grounding claims in context), **relevance**, and **context recall**.
- ### **V. From LLMs to Autonomous Agents**
  The industry is shifting from static chatbots to **AI Agents** that operate in **"agentic loops"**.
  *   **ReAct Loop:** Based on the **Reason and Act** framework, agents follow a cycle of **Observe -> Reason -> Act**.
  *   **Capabilities:** Agents can use external tools to search the web, execute code, call APIs, and read or write files.
  *   **Multi-Agent Systems:** Complex projects now use teams of specialized agents (e.g., a **Main Orchestrator** managing a **Developer**, **Security Officer**, and **Tester**).
  *   **Coding Agents:** Tools like **Claude Code** and **Devin** can now write, debug, and refactor codebases autonomously, showing high proficiency on benchmarks like **SWE-bench**.
- ### **VI. Sovereignty and Societal Impact**
  The rise of AI brings new challenges regarding data control and workforce development.
  *   **Sovereignty & AI Act:** Organizations must choose between **Closed APIs** (where data leaves the infrastructure) and **Open-weights models** (which allow for local deployment and better auditability under the **EU AI Act**).
  *   **The Junior Paradox:** Because agents excel at entry-level tasks (research, first drafts, boilerplate code), there is a risk that **junior roles will disappear**, leaving no clear path for new hires to develop the judgment needed to become seniors.
  *   **Education Reform:** Since AI can easily write essays, universities are moving away from writing as a proxy for learning. **ULB’s action plan** emphasizes integrating AI as a co-author while shifting assessments to **live problem solving**, **portfolios**, and **oral exams**.