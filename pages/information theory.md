## Questions
	- #### 1: p 15
	  collapsed:: true
		-
		- p 15
		- ---
		- ### **Shannon's Axioms for Entropy**
		  
		  Shannon introduced the concept of **entropy** for independent discrete sources based on the following three axioms:
		- #### **Axiom 1: Continuity**
		  
		  The entropy \( H \) must be a continuous function of the probabilities of each event \( p(x_i) \).
		  
		  This means that small changes in the probability distribution of the source should result in small changes in the entropy. Mathematically, if \( p(x_i) \) changes continuously, then the entropy function \( H(X) \) should also change continuously.
		- #### **Axiom 2: Monotonicity with Number of Events**
		  
		  If all events are equally likely (\( p(x_i) = \frac{1}{n} \)), then the entropy should **monotonically increase** as the number of events \( n \) increases. In other words, there is more uncertainty when there are more equally likely events.
		  
		  This means that the entropy \( H \) should increase as the number of equally likely outcomes increases. If each outcome is equally probable, the uncertainty or information content should be greater when there are more possible outcomes.
		- #### **Axiom 3: Additivity for Successive Choices**
		  
		  If a choice is broken down into two successive choices, the original entropy \( H \) should be the weighted sum of the individual entropy values for each choice.
		  
		  Mathematically, this axiom states that the total entropy of a system involving two choices should be the sum of the individual entropies of the two choices. This property reflects how entropy is additive for independent events.
		  
		  ---
		- ### **Shannon's Entropy Formula and Its Compliance with Axioms**
		  
		  Shannon’s entropy formula is:
		  
		  $$ H(X) = - \sum_{i} p(x_i) \log p(x_i) $$
		  
		  Let’s now demonstrate how this formula satisfies the three axioms.
		- #### **Axiom 1: Continuity**
		- The formula \( H(X) = - \sum_{i} p(x_i) \log p(x_i) \) is continuous because both the logarithm function and the summation operation are continuous. If the probabilities \( p(x_i) \) change continuously, the entropy \( H(X) \) will also change continuously. Therefore, **Axiom 1** is satisfied.
		- #### **Axiom 2: Monotonicity with Number of Events**
		- When \( p(x_i) = \frac{1}{n} \) for all \( i \), the entropy formula becomes:
		  
		  $$ H(X) = - \sum_{i} \frac{1}{n} \log \frac{1}{n} = \log n $$
		- This expression shows that the entropy is equal to \( \log n \), which increases monotonically with \( n \). Therefore, as the number of equally likely events increases, the entropy also increases. Hence, **Axiom 2** is satisfied.
		- #### **Axiom 3: Additivity for Successive Choices**
		- Consider two independent choices, each with its own entropy \( H_1 \) and \( H_2 \). The total entropy of the system can be expressed as:
		  
		  $$ H_{\text{total}} = H_1 + H_2 $$
		- Expanding the formula for two successive choices results in the same expression as the original formula for \( H \). This property can be demonstrated by considering the entropy of two independent sources and applying the summation and logarithmic operations.
		- This can be proven using the example for \( n = 3 \) and generalized for any \( n \) using induction. Therefore, **Axiom 3** is satisfied.
		  
		  ---
		- ### **Conclusion**
		  
		  Shannon's entropy formula:
		  
		  $$ H(X) = - \sum_{i} p(x_i) \log p(x_i) $$
		  
		  satisfies all three of Shannon's axioms:
		- **Axiom 1**: Continuity of entropy as a function of probabilities.
		- **Axiom 2**: Monotonic increase in entropy as the number of equally likely events increases.
		- **Axiom 3**: Additivity of entropy for successive independent choices.
		  
		  Thus, Shannon’s entropy formula is a valid and consistent measure of information based on these fundamental principles.
		  
		  ---
	- #### 2: p19
	  collapsed:: true
		- p19
		- ---
		- ### **1. Define Self-Information**
		  
		  The **self-information** of a symbol \( x_i \) is a function of its probability of occurrence \( p(x_i) \). This function, \( S(x_i) = f(p(x_i)) \), should fulfill these properties:
		  
		  **Non-negativity:** The information contribution of each message should be non-negative:
		    $$ 0 \leq f(p(x_i)) $$
		  
		  **Zero information for certain events:** If a message is certain (\( p(x_i) = 1 \)), its self-information is zero because there is no uncertainty:
		    $$ \lim_{p(x_i) \to 1} f(p(x_i)) = 0 $$
		  
		  **Decreasing information with increasing probability:** Less probable messages carry more information:
		    $$ f(p(x_i)) > f(p(x_j)) \quad \text{if} \quad p(x_i) < p(x_j) $$
		  
		  **Additivity for independent events:** The information of a message composed of two independent messages is the sum of their individual information:
		    $$ f(p(x_i, x_j)) = f(p(x_i)) + f(p(x_j)) $$
		  
		  The **logarithmic function** \( f(x) = -\log(x) \) satisfies all these conditions, making it the suitable function for defining self-information:
		  $$ S(x_i) = -\log(p(x_i)) $$
		  
		  ---
		- ### **2. Average Self-Information over All Symbols**
		  
		  To describe the information content of a source that can produce multiple symbols, the **average self-information**, or **entropy** \( H(X) \), is calculated.
		- Consider a source \( X \) with \( n \) statistically independent symbols.
		- A long message with \( N \) symbols will contain the \( i \)-th symbol approximately \( N p(x_i) \) times.
		- The total information in this long message is:
		  $$ \sum_{i} (N p(x_i) S(x_i)) $$
		- The average information per symbol, or entropy, is then:
		  $$ H(X) = \frac{\sum_{i} (N p(x_i) S(x_i))}{N} = \sum_{i} p(x_i) S(x_i) $$
		  
		  ---
		- ### **3. Entropy Formula**
		  
		  Substituting the self-information formula into the entropy definition yields:
		  $$ H(X) = - \sum_{i} p(x_i) \log p(x_i) $$
		  
		  This formula represents the **entropy of the source \( X \)**, expressed in **bits per symbol**, and it is derived from the concept of self-information by averaging the information content of all possible symbols produced by the source.
		  
		  ---
		  
		  This derivation provides a way to quantify the uncertainty in a source that produces a sequence of independent symbols, where the entropy serves as a measure of the average amount of uncertainty or information per symbol.
	- #### 3: p21
	  collapsed:: true
		- p21
		-
		- ---
		- ### **Binary Entropy Function \( H_b(p) \)**
		  
		  The **binary entropy function**, denoted as \( H_b(p) \), quantifies the uncertainty associated with a Bernoulli process. A Bernoulli process is characterized by a random variable \( X \) that can take on two values:
		  \( X = 1 \) (success) with probability \( P[X = 1] = p \)
		  \( X = 0 \) (failure) with probability \( P[X = 0] = 1 - p \)
		  
		  ---
		- ### **Derivation of the Binary Entropy Function**
		  
		  Recall the general formula for the entropy of a discrete source:
		  
		  $$
		  H(X) = - \sum_{i} p(x_i) \log p(x_i)
		  $$
		  
		  For a Bernoulli process, we apply this formula to the two possible outcomes (success and failure), leading to:
		  
		  $$
		  H_b(p) = - \left[ p \log p + (1 - p) \log (1 - p) \right]
		  $$
		  
		  This expression defines the **binary entropy function** \( H_b(p) \) as the entropy of a Bernoulli process with probability of success \( p \).
		  
		  ---
		- ### **Sketch and Key Points of \( H_b(p) \)**
		  
		  The graph of \( H_b(p) \) plotted against \( p \) takes a concave shape. The key points of the binary entropy function are:
		- **Minimums:** \( H_b(p) = 0 \) at \( p = 0 \) and \( p = 1 \). This means that if the outcome is certain (either always success or always failure), there is no uncertainty, and hence the entropy is zero.
		- **Maximum:** \( H_b(p) = 1 \) at \( p = 1/2 \). This implies that the uncertainty is maximized when both success and failure are equally likely.
		  
		  ---
		- ### **Derivation of the Maximum**
		  
		  To find the maximum of \( H_b(p) \), we take its derivative and set it to zero:
		  
		  $$
		  \frac{\partial H_b(p)}{\partial p} = \log \left( \frac{1 - p}{p} \right) = 0
		  $$
		  
		  This equation is satisfied when \( p = 1/2 \), confirming that the **maximum entropy of the binary entropy function occurs at** \( p = 1/2 \), where \( H_b(1/2) = 1 \) bit/symbol.
		  
		  ---
		- ### **General Bounds for the Entropy of a Discrete Source**
		  
		  For a discrete source with an alphabet of length \( n \), the **entropy is bounded by**:
		  
		  $$
		  0 \leq H(X) \leq \log n
		  $$
		- The **lower bound (0)** signifies no uncertainty, meaning the source consistently produces the same symbol. This occurs when all probabilities are zero except for a single symbol with \( p(x_j) = 1 \).
		- The **upper bound \( \log n \)** represents maximum uncertainty, occurring when all symbols are equally likely (\( p(x_i) = 1/n \) for all \( i \)) and statistically independent. This condition leads to:
		  
		  $$
		  H_{\text{max}}(X) = - \sum_{i} \left( \frac{1}{n} \right) \log \left( \frac{1}{n} \right) = \log n
		  $$
		  
		  Therefore, a **discrete source reaches its maximum entropy when all its symbols are equally likely and statistically independent**, resulting in maximum uncertainty about the next symbol produced by the source.
		  
		  ---
	-
		- p23,24
		- ---
		- ### **Information Rate and Its Relationship with Entropy**
		  
		  The **information rate**, \( R(X) \), quantifies the average amount of information a source \( X \) transmits per unit of time, typically expressed in bits per second (bit/s). It is directly related to the **entropy**, \( H(X) \), which measures the average information content per symbol in bits per symbol.
		  
		  ---
		- ### **General Formula for Information Rate**
		  
		  In general, the information rate is calculated as:
		  
		  $$
		  R(X) = \sum_i f(x_i) S(x_i)
		  $$
		  
		  Where:
		- \( f(x_i) \) is the average frequency of occurrence of the \( i \)-th symbol (in symbols per second),
		- \( S(x_i) \) is the self-information of the \( i \)-th symbol (in bits per symbol).
		  
		  ---
		- ### **Relationship with Entropy**
		  
		  The average frequency of occurrence can be expressed in terms of the probability of the symbol \( p(x_i) \) and the **average duration of a symbol** \( \langle \tau \rangle \):
		  
		  $$
		  f(x_i) = \frac{p(x_i)}{\langle \tau \rangle}
		  $$
		  
		  Substituting this expression into the information rate formula:
		  
		  $$
		  R(X) = \frac{\sum_i p(x_i) S(x_i)}{\langle \tau \rangle}
		  $$
		  
		  Since \( H(X) = \sum_i p(x_i) S(x_i) \), we can express the information rate as:
		  
		  $$
		  R(X) = \frac{H(X)}{\langle \tau \rangle}
		  $$
		  
		  This equation highlights the **direct relationship between the information rate and entropy**. A higher entropy implies more information per symbol, leading to a higher information rate. However, a longer average symbol duration will decrease the information rate.
		  
		  ---
		- ### **Information Rate for Binary Coders**
		  
		  For **binary coders**, where symbols \( x_i \) are translated into sequences of \( N(x_i) \) bits, the average duration of a symbol can be expressed in terms of the sampling period \( T_s \):
		  
		  $$
		  \langle \tau \rangle = T_s \times N(x_i)
		  $$
		  
		  Where:
		- \( N(x_i) \) is the average number of bits per symbol.
		  
		  Therefore, the information rate for binary coders becomes:
		  
		  $$
		  R(X) = \frac{H(X)}{T_s \times N(x_i)}
		  $$
		  
		  This formula shows that the information rate for binary coders is inversely proportional to both the average number of bits per symbol \( N(x_i) \) and the sampling period \( T_s \).
		  
		  ---
		- ### **Key Concepts Summary**
		  
		  **Information rate** \( R(X) \) quantifies the rate of information transmission in bits per second.
		  **Entropy** \( H(X) \) measures the average information content per symbol.
		  **Average symbol duration** \( \langle \tau \rangle \) is the average time to transmit a symbol.
		  For binary coders, \( \langle \tau \rangle = T_s \times N(x_i) \), where \( N(x_i) \) is the number of bits per symbol.
		  
		  The information rate is **directly proportional to entropy** and **inversely proportional to the average symbol duration**. In the case of binary coders, the information rate is also inversely proportional to the average number of bits per symbol and the sampling period.
		  
		  ---
- ## Information Theory - Off the top of your head
  collapsed:: true
	- The entropy $H(X)$ of the discrete source $X$ equals. #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:37:15.686Z
	  card-last-reviewed:: 2025-01-07T18:37:15.686Z
	  card-last-score:: 5
	  id:: 67715a6c-c1fd-4702-9ae9-481c4032493c
		- $$H(X) = - \sum^n_{i=1}{p(x_{i})\cdot logp(x_{i})}$$
	- The self-information of a symbol $x_{i}$ equals #card
	  card-last-interval:: 4
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2025-01-11T18:16:47.484Z
	  card-last-reviewed:: 2025-01-07T18:16:47.484Z
	  card-last-score:: 5
	  id:: 67715b3c-9208-4242-8fff-6539540892ba
		- $$S(x_{i}) = - log(p(x_i)$$
	- The entropy of a discrete source $X$ is maximal for a uniform distribution with #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:36:41.388Z
	  card-last-reviewed:: 2025-01-07T18:36:41.388Z
	  card-last-score:: 5
	  id:: 67715b6a-eee7-4021-81cf-d7c40a4ef0cd
		- $$p(x_i) = \frac{1}{n} \; \; \; \forall{i}$$
	- The entropy of a discrete source with alphabet length n is bounded by #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:10:31.741Z
	  card-last-reviewed:: 2025-01-07T18:10:31.742Z
	  card-last-score:: 5
	  id:: 67715bd3-b751-4785-9054-4abf3eada6aa
		- $$0 \leq H(X) \leq log n$$
	- The information rate $R(X)$ equals #card
	  card-last-interval:: 4
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2025-01-11T18:17:33.140Z
	  card-last-reviewed:: 2025-01-07T18:17:33.140Z
	  card-last-score:: 5
	  id:: 67715e8d-c80c-41d3-89f7-3991d8e47d54
		- $$R(X) = - \sum^n_{i=1} f(x_i)logp(x_i)$$
	- The information rate $R(X)$ equals #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:37:34.683Z
	  card-last-reviewed:: 2025-01-07T18:37:34.684Z
	  card-last-score:: 5
	  id:: 67716c19-1f8e-4cba-a042-2e40e19d4f3a
		- $$R(X) = \frac{1}{<T>} H(X)$$
	- The Markov property demands that #card
	  id:: 67716ce4-1ab7-4474-96d5-196734cd8a91
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:27:54.804Z
	  card-last-reviewed:: 2025-01-07T18:27:54.805Z
	  card-last-score:: 5
		- $$p(x_j(k) | x_{i_{k-1}}(k-1) \cap ... \cap x_{i_{1}}(1) )  = p(x_j(k)|x_{i_{k-1}}(k-1 )    )$$
	- A stationary Markov process that has a state-transitio probability which staties #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:22:02.391Z
	  card-last-reviewed:: 2025-01-07T18:22:02.391Z
	  card-last-score:: 5
	  id:: 67716d12-1091-49f7-8247-9e0366a4cdd4
		- $$P_{ij}(k) = p(x_j(k) | x_{i_{k-1}} (k-1) ) = P_{ij}  \; \;\; \forall{k}$$
	- The joint entropy of two random variables X and Y: #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:22:46.445Z
	  card-last-reviewed:: 2025-01-07T18:22:46.445Z
	  card-last-score:: 5
	  id:: 67716d51-3b01-4420-97e5-9c5f3a6b7755
		- $$H(X,Y) = \sum\sum p(x_i,y_i) log p(x_i, y_i)$$
	- X and Y are statistically independent if and only if #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:26:52.286Z
	  card-last-reviewed:: 2025-01-07T18:26:52.287Z
	  card-last-score:: 5
	  id:: 67716d9c-9b37-4ebc-aff2-6e24d25c4cf4
		- $$H(X,Y) = H(X) + H(Y)$$
	- The conditional entropy of two random variables X and Y #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:28:36.975Z
	  card-last-reviewed:: 2025-01-07T18:28:36.976Z
	  card-last-score:: 5
	  id:: 67716dc0-ac27-4b92-a439-1fb1f917846b
		- $$H(Y|X) = \sum\sum{p(x_i,y_i) logp(y_i | x_i)}$$
	- Relation between entropy definitions #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:14:10.287Z
	  card-last-reviewed:: 2025-01-07T18:14:10.287Z
	  card-last-score:: 5
	  id:: 67715f18-b821-474f-9081-cab98bab3a6f
		- $$H(Y|X) = H(X,Y) - H(X)$$
	- Conditional entropy for an ideal channel #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:29:34.937Z
	  card-last-reviewed:: 2025-01-07T18:29:34.937Z
	  card-last-score:: 5
	  id:: 67716e41-b8bc-4208-8b9d-d8c01121006a
		- $$H(Y|X) = H(X|Y) = 0$$
	- Conditional entropy for independent random variables #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:19:13.155Z
	  card-last-reviewed:: 2025-01-07T18:19:13.156Z
	  card-last-score:: 5
	  id:: 67716e64-6384-45bb-a3aa-d9a4987d6aa5
		- $$H(Y|X) = H(Y) \; and \; H(X|Y) = H(X)$$
	- The condition entropy H(Y|X) is bounded #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:18:45.116Z
	  card-last-reviewed:: 2025-01-07T18:18:45.116Z
	  card-last-score:: 5
	  id:: 67716e98-b458-482f-b9ff-8163d7d666c2
		- $$0 \leq H(Y|X) \leq H(Y)$$
	- H(X,Y) is bounded #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:20:37.704Z
	  card-last-reviewed:: 2025-01-07T18:20:37.704Z
	  card-last-score:: 5
	  id:: 67716ece-6786-43d0-952c-52d434ed23b4
		- $$0 \leq max([H(X), H(Y)]) \leq H(X,Y) \leq H(X) + H(Y)$$
	- The mutual information is defined as #card
	  card-last-interval:: 11.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2025-01-18T22:19:55.520Z
	  card-last-reviewed:: 2025-01-07T18:19:55.520Z
	  card-last-score:: 5
	  id:: 67716f1b-f50d-4438-8eb3-465fc59f328e
		- $$I(X;Y) = H(X) - H(X|Y)$$
	- For two discrete random variables X and Y , the mutual information equals #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2025-01-11T18:42:05.921Z
	  card-last-reviewed:: 2025-01-07T18:42:05.921Z
	  card-last-score:: 3
	  id:: 677bfca3-bee5-4268-aee6-9910e362dcf7
		- $$\sum \sum p(x_i,y_j) log(\frac{p(x_i,y_j)}{p(x_i)p(y_j)})$$
	- Mutual information for an ideal channel #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2025-01-11T18:19:48.091Z
	  card-last-reviewed:: 2025-01-07T18:19:48.091Z
	  card-last-score:: 3
	  id:: 677bfd59-9ca1-4568-9621-ccf3587037ce
		- $$I(X;Y) = H(X) = H(Y)$$
	- Mutual information for independent random variables #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:20:17.351Z
	  card-last-reviewed:: 2025-01-07T18:20:17.351Z
	  card-last-score:: 5
	  id:: 677bfd7d-818a-4dd5-a313-ae5002bb8911
		- $$I(X;Y) = 0$$
	- The mutual information is bounded #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:27:11.719Z
	  card-last-reviewed:: 2025-01-07T18:27:11.719Z
	  card-last-score:: 5
	  id:: 677bfda5-7ff6-451e-a1c1-a1c06f6d6e01
		- $$0 \leq I(X;Y) \leq H(X)$$
	- The channel capacity is defined as #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:26:36.016Z
	  card-last-reviewed:: 2025-01-07T18:26:36.017Z
	  card-last-score:: 5
	  id:: 677bfe1f-2177-4a96-b7ba-bad6e2fd1c75
		- $$\sup\limits_{X} I(X; Y)$$
		  where the supremum is taken over all possible choices of $X$.
	- A transducer with input X and output Y satisfies #card
	  card-last-interval:: 4
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2025-01-11T18:32:31.320Z
	  card-last-reviewed:: 2025-01-07T18:32:31.321Z
	  card-last-score:: 5
	  id:: 677c4158-2e4f-4f39-8e6b-44122ca18736
		- $$R(Y) \leq R(X)$$
	- Shannon theorem (1): If $R \leq C$ there exists a coding system resulting in an arbitrary small frequency of errors #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:31:45.085Z
	  card-last-reviewed:: 2025-01-07T18:31:45.085Z
	  card-last-score:: 5
	  id:: 677c410f-aa87-4e73-9523-c38df3427319
	- Shannon theorem (2): If $R > C$ it is possible to encode the source such that the frequency of errors is less than $R - C + \epsilon$ #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:29:58.438Z
	  card-last-reviewed:: 2025-01-07T18:29:58.438Z
	  card-last-score:: 5
	  id:: 677c41df-c450-4cfe-968a-78a33866b448
	- Shannon theorem (3): There is no encoding system which give a frequency of errors less than $R - C$. #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:14:33.899Z
	  card-last-reviewed:: 2025-01-07T18:14:33.899Z
	  card-last-score:: 5
	  id:: 677c4224-ad4e-4b89-9929-27ef384cc0bb
	- The entropy of a continuous distribution with pdf $f_X (x)$ #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:10:10.350Z
	  card-last-reviewed:: 2025-01-07T18:10:10.350Z
	  card-last-score:: 5
	  id:: 677c4278-5be8-44f0-8f92-efc4687ed30e
		- $$H(X) - \int^{+\infty}_{-\infty} f_{X}(x) logf_{X}(x) dx$$
	- The joint entropy of continuous distributions equals #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:09:24.848Z
	  card-last-reviewed:: 2025-01-07T18:09:24.849Z
	  card-last-score:: 5
	  id:: 677c4330-3456-429d-9c03-47d476355467
		- $$H(X,Y) = - \int^{+\infty}_{-\infty} \int^{+\infty}_{-\infty} f(x,y) log f(x,y) dxdy$$
	- The conditional entropy of continuous distributions equals #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:13:49.124Z
	  card-last-reviewed:: 2025-01-07T18:13:49.124Z
	  card-last-score:: 5
	  id:: 677c4393-9da1-44c9-bcea-48240683b881
		- $$H(Y|X) = - \int^{+\infty}_{-\infty} \int^{+\infty}_{-\infty} f(x,y)log\frac{f(x,y)}{f(x)} dxdy$$
	- A uniform distribution maximizes the entropy under bounded amplitude constraint. #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-11T18:14:43.561Z
	  card-last-reviewed:: 2025-01-07T18:14:43.562Z
	  card-last-score:: 5
	  id:: 677c442f-90ba-40a8-91a2-48517c1ebf42
	- The entropy of a uniform distribution in $[-a,a]$ equals #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:40:02.414Z
	  card-last-reviewed:: 2025-01-07T18:40:02.414Z
	  card-last-score:: 5
	  id:: 677c4479-c08e-4dfc-ab56-a87314721e3e
		- $$H(X) = log(2a)$$
	- A Gaussian distribution maximizes the entropy under fixed power constraint. #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:17:49.213Z
	  card-last-reviewed:: 2025-01-07T18:17:49.214Z
	  card-last-score:: 5
	  id:: 677c449f-ae14-40f0-8053-b6ae773a173f
	- The entropy of a single variable Gaussian distribution equals #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:38:04.766Z
	  card-last-reviewed:: 2025-01-07T18:38:04.767Z
	  card-last-score:: 5
	  id:: 677c44bb-4261-48b1-86f5-0cbfcb7cc8cb
		- $$H(X) = \frac{1}{2} log(2\pi e \sigma^2)$$
	- Nyquist-Shannon sampling theorem: #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:39:46.571Z
	  card-last-reviewed:: 2025-01-07T18:39:46.571Z
	  card-last-score:: 5
	  id:: 677c54e6-ee4e-495b-be0a-363c47aa4bfb
		- $x(t)$ can be perfectly reconstructed by
		  $$x(t) = \sum^{\infty}_{k=-\infty} x(nT)sinc(\frac{t}{T_s} - k)$$
		  with
		  $$sinc(x) = \frac{sin \pi x}{ \pi x}$$
		  if $x(t)$ is band limited with $f_{max} \leq W$ and $T_s = \frac{1}{(2W)}$
	- Nyquist Inter Symbol Interference (ISI) criterion #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:18:10.336Z
	  card-last-reviewed:: 2025-01-07T18:18:10.336Z
	  card-last-score:: 5
	  id:: 677d3903-c5f3-4f78-8620-1fc1c4398f77
		- $$
		  h(nT_s) =
		  \begin{cases} 
		  1 & n = 0 \\
		  0 & n \neq 0 
		  \end{cases}
		  $$
	- The band-pass signal #card
	  card-last-interval:: 4.59
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T08:31:34.177Z
	  card-last-reviewed:: 2025-01-07T18:31:34.177Z
	  card-last-score:: 5
	  id:: 677d4408-9c6d-44ca-b82d-0bbe864dd267
		- $$X_{BP} = I(t)cos(2\pi f_e t) - Q(t)sin(2 \pi f_e t)$$
		  can be represented efficiently using its equivalent baseband representation
		  $$ Z(t) = I(t) + jQ(t)$$
		  with
		  $$X_{BP} = \Re(Z(t)e^{j2\pi f_e t})$$
	- Channel capacity for additive noise channel $Y = X + N$ #card
	  card-last-interval:: 11.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2025-01-18T22:32:18.442Z
	  card-last-reviewed:: 2025-01-07T18:32:18.443Z
	  card-last-score:: 5
	  id:: 677d4c51-87a6-4f0e-8ad6-de9adce42678
		- $$C = \sup\limits_{X} (H(Y)) - H(N)$$
	- Shannon-Hartley theorem for independent continuous variables (as a function of the SNR) #card
	  card-last-interval:: 4
	  card-repeats:: 2
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T12:58:58.780Z
	  card-last-reviewed:: 2025-01-08T12:58:58.781Z
	  card-last-score:: 5
	  id:: 677d4cad-e2c8-4bfd-b7a6-2691261d4088
		- $$C = \frac{1}{2} log(1 + SNR)$$
	- Shannon-Hartley theorem: #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T16:05:22.761Z
	  card-last-reviewed:: 2025-01-07T22:05:22.762Z
	  card-last-score:: 5
	  id:: 677d7639-1e93-42b1-8dbc-4efab9f60636
		- The band-limited Gaussian channel $Y (t) = X(t) + N (t)$ with bandwidth
		  W and noise power spectral density $N_0$ has the capacity
		  $$C = Wlog(1 + \frac{P}{N_0 W})$$
		  which is attained when X(t) is zero-mean Gaussian distributed with power P.
	- Shannon’s limit of the channel capacity #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T16:05:04.418Z
	  card-last-reviewed:: 2025-01-07T22:05:04.419Z
	  card-last-score:: 5
	  id:: 677d8c94-fdc2-43c3-abac-d4d54024f72e
		- $$R \leq C = W log (1 + SNR)$$
	- The average length of the output symbol $\langle N \rangle$ and the entropy of the source are related by #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T16:05:14.895Z
	  card-last-reviewed:: 2025-01-07T22:05:14.895Z
	  card-last-score:: 5
	  id:: 677d8cc4-36ae-40b1-866d-f895816cd10d
		- $H(X) \leq \langle N \rangle$.
	- Shannon's fundamental source coding theorem: the average code length $\langle N \rangle$ to binary encode (m = 2) a single symbols of X with entropy H(X) #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T16:04:25.427Z
	  card-last-reviewed:: 2025-01-07T22:04:25.427Z
	  card-last-score:: 5
	  id:: 677d8d9e-821e-4382-aac2-b4ac141ad2b5
		- $$H(X) \leq \langle N \rangle < H(X) + 1$$
	- General Shannon's source coding theorem: the average code length $\langle N \rangle$ (per symbol) to binary encode (m = 2) a block with entropy $H(X)$ satisfies #card
	  card-last-interval:: 4.75
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2025-01-12T16:04:02.387Z
	  card-last-reviewed:: 2025-01-07T22:04:02.388Z
	  card-last-score:: 5
	  id:: 677d8e21-0840-4440-97a2-e940f0e079b7
		- $$H(X) \leq \langle N \rangle < H(X) + \epsilon$$