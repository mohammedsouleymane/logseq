- Derived from cooperative game theory and proposed by Nobel laureate **Lloyd Shapley**, **Shapley values** provide a mathematically fair way to allocate "credit" or payoffs among members of a coalition. In modern AI, this framework is used for **attribution**, helping to identify and quantify the specific contribution of different factors—such as input features or training data—to a machine learning model's final decision.
- ### **Core Mechanism**
  
  The fundamental logic of Shapley values is to determine the **marginal contribution** of a specific member (a feature or data point) by comparing outcomes across all possible combinations (coalitions) of other members.
- **The Calculation:** For a specific factor $i$, the system calculates the difference in the model's output (e.g., the loss or the probability of a correct answer) when $i$ is included versus when it is excluded ($v(S \cup {i}) - v(S)$).
- **Averaging:** This marginal contribution is averaged across every possible subset of the other factors to ensure a fair distribution of influence.
- ### **Applications in AI**
- **Feature Attribution:** Identifying which input variables (like age, race, or salary) were most influential for a specific prediction, such as a loan rejection.
- **Data Attribution:** Explaining a model's behavior by identifying which specific **training samples** most influenced the model's parameters.
- **Retrieval-Augmented Generation (RAG):** In the era of Large Language Models (LLMs), Shapley values help determine which specific retrieved documents actually influenced an LLM's final response, which is critical for identifying the root of factual errors or hallucinations.
- ### **The Feasibility Challenge ($2^N$ Problem)**
  
  A major drawback of calculating exact Shapley values is that it is **exhaustively expensive**. Because it requires testing every possible coalition, the number of required model calls grows exponentially as $2^N$ (where $N$ is the number of features or documents). For example, while 10 documents require roughly 1,000 LLM calls, 30 documents would require **1 billion calls**, making exact calculation impossible for large datasets.
- ### **Approximation Methods**
  
  To overcome these computational costs, researchers use several approximation techniques:
- **Kernel SHAP:** This method trains a simple **linear surrogate model** on a random sample of coalitions to predict the loss and treat the resulting weights as Shapley values.
- **TMC-Shapley (Truncated Monte Carlo Shapley):** This approach shuffles data permutations and computes average marginal contributions, using **truncation** to stop the process when the change in output becomes negligible.
- **ContextCite:** A specific application for RAG that uses linear surrogate models to provide attribution scores for sentences or documents in a context window.
  
  <!--EndFragment-->
-
-
- Based on the sources provided, the distinction between **causality and correlation** is central to overcoming the "Achilles heel" of modern machine learning, which currently relies almost entirely on associative patterns.
- ### **Correlation (Association)**
- **Definition:** Correlation, or **Association**, is the first rung on Judea Pearl’s **Ladder of Causation** and involves **"seeing"** or observing patterns in data.
- **Nature of reasoning:** It answers the question, **"What if I see...?"** by identifying how variables are related statistically, such as the probability of a reaction given a vaccination ($P(R | A)$).
- **Limitations:** Correlation **does not imply causation**; a model might incorrectly infer that ice cream sales cause sunburns simply because they frequently occur together due to a hidden **confounder**—the sun.
- **Vulnerability to Bias:** Standard machine learning models are susceptible to **spurious correlations**, such as identifying a "cow" based on the presence of green grass in the background rather than the animal itself.
- **The "Cancer Gene" Debate:** Historically, opponents of causal reasoning argued that smoking and cancer were merely correlated due to a "cancer gene" that influenced both, illustrating how correlation cannot distinguish between a direct cause and a shared latent factor.
- ### **Causality (Intervention and Counterfactuals)**
- **Definition:** Causality involves higher rungs of reasoning—**Intervention** ("Doing") and **Counterfactuals** ("Imagining")—to understand the actual mechanisms of cause and effect.
- **Intervention ($do$-calculus):** This level answers **"What if I do...?"** by manipulating a variable to observe its effect, often through **Randomized Controlled Trials (RCTs)**.
- **Mathematical notation:** While correlation is expressed as $P(Y | X)$, causality is expressed as **$P(Y | do(X))$**, where the variable $X$ is artificially fixed, breaking its dependence on other factors.
- **Counterfactuals:** This is the highest level of causal reasoning, involving **retrospection** and answering, **"What if I had acted differently?"**. It allows for reasoning about hypothetical scenarios that did not occur in reality.
- **Explainability and Fairness:** Causal models are **"explainable by design"** because they provide a graph structure showing how features influence outcomes, rather than offering a "black-box" probability.
- **Causal Fairness:** In AI auditing, causality helps determine if a protected attribute (like race or gender) **directly caused** a decision, rather than just being correlated with it.
- ### **Summary Comparison**
  
  | Feature | Correlation (Association) | Causality (Intervention/Counterfactual) |
  | **Activity** | **Seeing**/Observing | **Doing**/Intervening and **Imagining** |
  | **Question** | What does a symptom tell me about a disease? | Will taking aspirin cure my headache? |
  | **AI Status** | Where current ML models reside | The goal for robust, human-like AI |
  | **Risk** | Misled by **confounders** and bias | **Robust** to environmental changes |
  | **Output** | Probabilistic associations ($P(Y \mid X)$) | Direct causal effects ($P(Y \mid do(X))$) |
  
  <!--EndFragment-->
-
-
-
- The **Ladder of Causation**, proposed by Judea Pearl, describes three levels of reasoning that humans and machines use to understand the world. The smoking example is frequently used in the sources to illustrate the limitations of standard statistics (correlation) and the power of causal reasoning.
- ### **Rung 1: Association (Seeing)**
- **Activity:** Observing and looking for patterns or correlations.
- **Question:** "What if I see...?".
- **The Smoking Example:** At this level, we observe a statistical relationship: **people who smoke tend to have higher rates of lung cancer**.
- **The Challenge (The "Cancer Gene" Debate):** Historically, statistical giants like Karl Pearson and Ronald Fisher—who were themselves heavy smokers—argued that this association did not prove smoking *caused* cancer. They posited that a **latent confounder** (a "cancer gene") existed, which both made people more likely to become addicted to smoking and more prone to developing cancer. Because Rung 1 only looks at "seeing" existing data, it cannot mathematically distinguish between a direct cause and a shared genetic factor.
- ### **Rung 2: Intervention (Doing)**
- **Activity:** Actively manipulating the environment to observe the effect.
- **Question:** "What if I do...?" or "How can I make $Y$ happen?".
- **The Smoking Example:** This level uses **$do$-calculus** to artificially fix a variable. In the smoking context, an intervention would ask: **"What if we ban cigarettes?"**.
- **Mechanism:** By performing **Randomized Controlled Trials (RCTs)**, researchers take a random group of people and force some to smoke and others to stop. This "doing" breaks the influence of the "cancer gene" because smoking is no longer a choice based on genetics—it is an external assignment. If the treated group still shows higher cancer rates, the link is causal.
- ### **Rung 3: Counterfactuals (Imagining)**
- **Activity:** Reasoning about hypothetical scenarios in imaginary worlds that did not actually occur.
- **Question:** "What if I had acted differently?" or "Why?".
- **The Smoking Example:** This rung involves **retrospection** for a specific individual. If a person who smoked for 20 years is diagnosed with lung cancer, a counterfactual question would be: **"Would this specific person be healthy today if they had not smoked for the last 2 years?"**.
- **Mechanism:** AI currently struggles here because it is trained on "real" data, not "imaginary" data. Counterfactual reasoning requires a mental or mathematical model of the world to estimate what *would have happened* to the same individual in a different version of reality.
- ### **Summary of the Ladder**
  
  | Rung | Activity | Smoking Example Question |
  | **1. Association** | Seeing | Does smoking increase the probability of cancer? |
  | **2. Intervention** | Doing | Will cancer rates drop if we ban cigarettes? |
  | **3. Counterfactuals** | Imagining | Would I have avoided cancer if I hadn't smoked? |
  
  <!--EndFragment-->
-
-
- **Influence functions** are a method from robust statistics used in AI attribution to identify which specific training data points most influenced a machine learning model's prediction for a new test sample. They serve as a computationally efficient alternative to the "Leave-One-Out" (LOO) method, which requires retraining a model multiple times to measure the impact of removing individual data points.
- ### **Core Mechanism**
  
  Instead of physically removing a data point and retraining the model—which is "exhaustively expensive" for large datasets—influence functions approximate the change in model parameters by **upweighting** a specific training sample ($z_{train}$) by an infinitesimal amount ($\epsilon$).
  
  The influence of a training point on the test loss is mathematically decomposed into an expression involving:
- **Gradients of Test Loss:** Measuring how the loss on a specific test sample changes with respect to model parameters.
- **Gradients of Training Data Loss:** Measuring the model's error on the training sample being investigated.
- **Hessian Matrix ($H$):** A matrix of second-order derivatives that describes the local geometry of the loss function. Because explicitly constructing this matrix is "super expensive," researchers use specialized products to compute it without full construction.
- ### **Limitations and Challenges**
- **Computational Cost:** While more efficient than retraining, calculating the Hessian matrix remains a significant hurdle.
- **Susceptibility to Outliers:** Influence-based methods are highly sensitive to **class outliers**—data points that look like one class but are labeled as another, or are ambiguous. These outliers often show high influence across many test points because the model's decision boundary "tries too hard" to fit them, leading to potentially misleading explanations.
- ### **Advanced Applications and Robustness**
  
  To address these limitations, researchers have developed more stable versions and applications:
- **InfProto:** This method bridges local and global explainability by providing a **robust version of the influence function**. It identifies both prototypes (general patterns) and influential instances (specific influencers) in a single process, which is preferred by 68% of users over standard local or global explanations.
- **Federated Learning:** In decentralized systems, local gradient calculations are used to measure the influence of a specific client's update. This helps detect **client drift**, where an update from a participant with a massive amount of data might bias the global model away from the true optimum.
- **User Intent Customization:** Modern attribution frameworks allow users to customize how they view influence based on their needs, such as investigating a wrong prediction by looking at "opposers" (points that would have pushed the model toward the correct answer).
  
  <!--EndFragment-->
-
- For a school implementing an **autonomous AI grading system**, the Responsible AI lifecycle would be governed by the three high-level stages of **Design, Build, and Operate**. Crucially, because the **EU AI Act** specifically classifies "exam correction with AI" as a **High-Risk AI system**, the school would face strict transparency and auditability obligations throughout this cycle.
- ### **I. Design Phase: Strategic Alignment and Risk Assessment**
  
  Before development begins, the school must answer the fundamental question: **"Should we build this system?"**.
- **Risk Identification:** The school must map organizational risks to this specific use-case, identifying potential harms such as **accuracy errors** (misinformed grades) and **fairness issues** (discrimination against specific student groups).
- **Democratic Development:** Following the "Citicode" project's approach, the school should involve three groups in the design: domain experts (teachers), students (the "citizens" affected), and school leadership (the "politicians" resolving ideological conflicts over grading criteria).
- **Establishment of Governance:** An **AI Governance Policy** must be created to define accountability and rules for usage, ensuring the system is included in an official **AI Inventory**.
- ### **II. Build Phase: Mitigation and Evaluation**
  
  During the building stage, the focus shifts to technical controls to minimize intrinsic risks.
- **Debiasing and Fairness:** The system must undergo **fairness audits** to ensure it does not discriminate based on **protected attributes** like race or gender. Developers should use causal models to ensure these attributes do not "directly influence" the grade.
- **Attribution and Explainability:** The system should use **attribution methods** (like Shapley values or ContextCite) to trace a grade back to specific evidence in a student's answer, preventing "black-box" decisions.
- **Adversarial Testing:** The model should be subjected to **adversarial testing** to ensure students cannot "jailbreak" or manipulate the grading criteria through prompt injection.
- **Skill Blending Process (SBP):** Rather than full autonomy, the school might design a **hybrid intelligence system** where the AI processes the initial data but results are sent for **Human Validation** before being finalized.
- ### **III. Operate Phase: Monitoring and Recourse**
  
  Once deployed, the system requires continuous oversight to remain compliant and ethical.
- **Transparency and Disclosure:** Under the EU AI Act, students must be informed that an AI system is correcting their exams.
- **Audit-Ready Logging:** The school must maintain "trust-and-trace" documentation, including **request waterfalls** and **data lineage**, to satisfy auditors and prove every grade is grounded in verifiable sources.
- **Algorithmic Recourse:** If a student receives an unfavorable grade, the system should provide **algorithmic recourse**—a clear plan or set of instructions explaining the "minimal changes" needed to have achieved a different outcome.
- **Right to Human Review:** Students must be granted the right to request a **human verification** of their exam that is independent of the AI system's assessment.
- **Performance Monitoring:** The school must use real-time dashboards to monitor for **model drift** or a drop in accuracy that might occur as the curriculum evolves.
  
  <!--EndFragment-->
-
-
-
- **What is federated learning?**
  Federated learning is a privacy-preserving approach where multiple institutions train local machine learning models on their own private data and only share the model weights with a central server. The central server aggregates these local updates into a **global model**, allowing for collaboration without ever exchanging the raw, sensitive data itself.
- **What are its challenges?**
  Major challenges include model security vulnerabilities such as **poisoning** and man-in-the-middle attacks, alongside significant **computation and communication overhead** during the iterative training process. Additionally, the system faces "**client drift**" where diverse local datasets bias the model, and it struggles with incentive mechanisms to ensure fairness among contributors.
- **Why would you not want your company to use it?**
  A company might reject this approach because the constant back-and-forth transfer of large model updates can lead to **massive payloads** and extremely slow training times. There is also the critical risk that sophisticated adversaries could **inverse model weights** to reconstruct original proprietary data points, potentially compromising corporate secrets or user privacy.
- <!--EndFragment-->
-
- The evolution of Large Language Models (LLMs) from 2020 to 2026 has been defined by a shift from simple text prediction to complex reasoning and autonomous action, all accelerated by the architectural breakthrough of the **Transformer**.
- ### **The Foundation: The Transformer Breakthrough (2017)**
  
  The current era of AI began with the landmark paper **"Attention is all you need" (Vaswani, 2017)**, which introduced the **Transformer architecture**.
- **Self-Attention Mechanism:** Unlike previous sequential models, Transformers use an **attention block** to map correlations between all tokens in a sentence simultaneously. This allows the model to understand context dynamically—for example, correctly identifying that the word "it" refers to an "animal" and not a "street" based on surrounding descriptors like "tired."
- **Capturing Long-Range Dependencies:** By using attention to identify relationships between distant tokens, Transformers significantly improved the ability to process complex sequential data.
- **Stackability and Scale:** This architecture allowed researchers to stack hundreds of attention layers (e.g., **GPT-2 had 48 layers**, while **Llama 3 has 80**), enabling models to process trillions of data points and develop "emergent" abilities.
- ### **The Timeline of Evolution (2020–2026)**
- **2020: The Scaling Era (GPT-3):** With **175 billion parameters**, GPT-3 demonstrated that massive scale enables **few-shot learning**, allowing models to perform tasks based on just a few examples in a prompt.
- **2022: Accessibility and Alignment (ChatGPT):** This year brought LLMs to the mainstream, utilizing **Reinforcement Learning from Human Feedback (RLHF)** to ensure models were helpful, harmless, and followed editorial boundaries.
- **2023: Multimodal Reasoning (GPT-4):** Models evolved to process and discuss **images, audio, and video** alongside text, expanding their interaction modalities.
- **2024: Thinking Models and Efficiency:**
	- **Inference Tokens:** Models like **OpenAI o1** and **DeepSeek R1** began generating hidden **inference tokens** to "think step-by-step" before answering, following the philosophy that **"thinking more" is better than "knowing more."**
	- **Mixture of Experts (MoE):** Architecture like **DeepSeek V3** optimized compute by routing tokens to specific experts; a 671B parameter model might only activate **37B parameters per token**, maintaining speed at scale.
- **2025: The Rise of AI Agents:** Models moved beyond static chat into **AI Agents** that use the **ReAct (Reason and Act)** framework to observe environments, use tools (via protocols like MCP), and execute actions like coding and testing autonomously.
- **2026: Frontier Models and Massive Context:** Current iterations like **GPT-5.5**, **Gemini 3.1**, and **Claude 4.7** feature **context windows** of millions of tokens, allowing them to process entire codebases or 6,000-page documents in a single prompt.
- ### **The Impact of Transformers on Acceleration**
  
  The Transformer's efficiency has led to a dramatic expansion in what models can handle:
- **Context Engineering:** Larger context windows allow for "Context Engineering," where full legal documents or books are used as inputs without the need for traditional chunking.
- **Bridging Local and Global Knowledge:** Through **Retrieval-Augmented Generation (RAG)**, the Transformer's attention mechanism helps ground LLM answers in external, verifiable documents to prevent hallucinations.
- **The "Junior Paradox":** As Transformer-based agents automate entry-level tasks like boilerplate coding and research, the industry faces a challenge in training new hires to develop the high-level judgment that AI cannot yet replicate.
  
  <!--EndFragment-->
-
- **Sequence learning** involves creating mathematical models based on "legitimate" or normal sequences of data to perform three primary tasks: **recognition** (identifying known patterns), **prediction** (forecasting future values), and **generation** (producing synthetic data). In the context of time series, this often requires breaking a long sequence into smaller, contiguous parts using a **sliding window**.
- ### **The Matrix Profile for Anomaly Detection**
  
  The **Matrix Profile** is a powerful meta-structure used to identify patterns and irregularities within these sequences. It is constructed by calculating a "distance profile" for every possible segment in a time series, which measures how similar each segment is to every other part of the data.
- **Motifs:** These are recurring subsequences that have a very **low distance** to each other in the matrix profile. They represent "normal" or expected behavior.
- **Discords (Anomalies):** These are subsequences that are maximally different from all others. In the matrix profile, a discord is the segment with the **highest distance** to its nearest neighbor, indicating it is an outlier that does not match any known pattern.
- ### **Illustration: Ice Cream Sales**
  
  Imagine a dataset of daily ice cream sales over a summer.
- **Motifs:** A typical "legitimate" sequence might show a pattern where sales are low in the morning, peak during the heat of the afternoon, and taper off in the evening. Because this happens almost every day, these segments will have a low distance to each other, forming a **motif**.
- **Discords:** If sales suddenly drop to zero in the middle of a blazing hot Tuesday afternoon, this specific segment will be unlike any other "hot afternoon" segment in the history. In the matrix profile, this segment will show a very **high distance** to its nearest neighbor and be flagged as a **discord** (anomaly).
- ### **Robustness to Shifting Peaks**
  
  A critical question in sequence learning is whether the model is robust if a peak (such as the highest point of sales) occurs at different times on different days.
- **Distance Sensitivity:** Standard **Euclidean distance** is highly sensitive to the exact timing of data points; if two identical shapes are slightly shifted in time, the Euclidean distance between them will be large.
- **Dimensionality Reduction:** To mitigate some of this sensitivity and improve speed, practitioners use **Piecewise Approximations** (like PAA or SAX), which partition sequences into non-overlapping frames and approximate them with average values or symbols. This helps summarize the general "shape" of the data rather than focusing on exact point-by-point matches.
- **The "No One-Size-Fits-All" Rule:** Ultimately, sequence learning's robustness depends on the training data. If your "legitimate" training set includes days where peaks naturally shift (e.g., due to changing weather patterns), the model will learn that these shifts are **normal** behavior. However, if the model has only ever seen peaks at 2:00 PM, a shift to 5:00 PM will likely be flagged as an anomaly because it deviates from the "expected normal behavior" described in its training sequences.
  
  <!--EndFragment-->
-
-
- The **Brain-Computer Interface (BCI) decoding pipeline**, as illustrated on slide 31 of Arnau Dillen's presentation, follows a sequential process to translate neural activity into physical actions.
- ### **The BCI Pipeline Stages**
- **Signal Acquisition:** Capturing brain activity, typically through **Electroencephalography (EEG)**, which measures electrical impulses using sensors placed on the scalp.
- **Pre-processing:** EEG signals are inherently noisy and must be cleaned. This involves **filtering** the data (usually between 8-35 Hz for motor imagery) and removing "bad data" or artifacts caused by muscle movements.
- **Feature Extraction:** Identifying specific patterns related to the user's intent. A standard technique used is **Common Spatial Patterns (CSP)**, which localizes where brain activity is strongest for a particular imagined movement.
- **Classification:** Using machine learning models to interpret the extracted features. Standard pipelines often employ **Linear Discriminant Analysis (LDA)** to categorize the brain signals into specific classes, such as "left hand" or "right hand" movements.
- **Action Execution:** The final classification result is sent to a device (such as a robot arm or "cobot") to perform the requested physical action.
  
  ---
- ### **Potential Drawbacks of This Pipeline**
  
  While functional, this specific pipeline faces several significant challenges and drawbacks:
- **Extreme Signal Noise:** EEG signals are very weak and easily corrupted by **artifacts**, such as the electrical activity from tensing facial muscles or blinking.
- **High Variability:** Brain activity is unique to every individual and **changes over time**. A model trained on one person rarely works for another, and a model that works for a user in the morning may become unreliable just one hour later.
- **Complexity Limits:** It is difficult to distinguish between many different movements; currently, a classifier that can accurately recognize just **four different movements** is considered a major achievement.
- **User Fatigue:** The process requires intense mental focus, which leads to significant **fatigue**. Users often find the necessary calibration phase (10–15 minutes) both exhausting and boring.
- **Skill Acquisition:** Using a BCI is a skill that must be learned. Users require extensive training sessions to learn how to reliably generate the brain signals that the model is designed to decode.
- **Extensive Setup Time:** Standard pipelines using "wet" electrodes require the application of conductive gel to every sensor, which can take up to **30 minutes of preparation** before an experiment can even begin.
  
  <!--EndFragment-->
-
-
-
- **Explainable AI (XAI)** is a field dedicated to providing human-understandable explanations for the outcomes of algorithmic decision-making systems. Its primary goals are to **build user trust**, allow for error correction, detect hidden biases, and ensure compliance with transparency regulations like the **EU AI Act**.
- ### **How We Achieve Explainability**
  
  Explainability can be achieved through different lenses depending on the scope of the explanation and what part of the model is being examined:
- #### **1. Local vs. Global Explainability**
- **Local Explainability:** Focuses on explaining a **specific, individual prediction**. For a rocket, this would answer: *"Why was this specific launch on Tuesday aborted?"*.
- **Global Explainability:** Seeks to provide a **general understanding** of how the model behaves across all data. For a rocket, this would answer: *"What are the most important factors the model generally considers for a successful launch?"*
- #### **2. Features vs. Training Data (Attribution)**
- **Feature Attribution:** Identifies which **input variables** (e.g., fuel levels, wind speed, temperature) were most influential in a specific decision.
- **Data Attribution:** Explains a decision by identifying which specific **training samples** from the past most influenced the model's current behavior. It points to the "experiences" the model learned from.
  
  ---
- ### **Example: A Rocket Launch Model**
  
  Imagine an AI model designed to decide whether a rocket is "Clear to Launch" or must be "Aborted" based on real-time sensor data.
- **Association (Seeing):** At the lowest level of the **Ladder of Causation**, the model simply sees patterns. It might notice that when the "Fuel Pressure" light is green, launches are usually successful, but it doesn't necessarily understand the physical "why".
- **Intervention (Doing):** On the second rung, we can test the model by **manipulating variables**. If we artificially increase the "Wind Speed" value in the simulation, we can observe exactly at what point the model changes its decision to "Abort".
- **Counterfactual Explanation (Local/Feature):** If a launch is aborted, a counterfactual provides the operator with a "lever" for understanding. The AI might explain: **"If the wind speed had been 5 km/h lower (the minimal change), the rocket would have been cleared for launch"**.
- **Data Attribution (Local):** If the AI aborts a launch despite seemingly good conditions, data attribution could reveal that the model is being influenced by **three specific historical test flights** in its training data where similar atmospheric conditions led to a catastrophic failure.
- **Global Explainability:** The system provides a summary dashboard showing that, across all 500 simulated launches, "Engine Temperature" is the **most significant feature** influencing the model's safety threshold.
- **Algorithmic Recourse:** This provides the engineers with a **plan of action**. It doesn't just say "Abort"; it provides instructions on what specific parameters (like fuel mix or launch angle) need to be adjusted to reach the "Clear to Launch" state.
  
  <!--EndFragment-->
-