## Information Theory - Off the top of your head
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
- WPO
	- Here is an explanation of the numbers and concepts for each part of the code:
	  
	  ---
	- ### **1. Self-Information for Each Symbol**
	  
	  **Formula:**
	  
	  I(x)=−log⁡2(p(x))I(x) = -\log_2(p(x))
	- **Purpose**: Measures how much information is gained when observing a specific symbol xx with probability p(x)p(x).
	- **Interpretation**: Higher self-information means the symbol is less likely to occur.
	  
	  Example:
	  
	  If pi=0.27p_i = 0.27,
	  
	  I(x)=−log⁡2(0.27)≈1.8928 bits.I(x) = -\log_2(0.27) \approx 1.8928 \text{ bits.}
	  
	  The values printed for each symbol represent their respective self-information.
	  
	  ---
	- ### **2. Entropy of the Information Source**
	  
	  **Formula:**
	  
	  H(X)=−∑ipi⋅log⁡2(pi)H(X) = -\sum_{i} p_i \cdot \log_2(p_i)
	- **Purpose**: Entropy quantifies the average uncertainty (or information) of the information source.
	- **Interpretation**: This value represents the theoretical lower bound of the average number of bits needed to encode the symbols.
	  
	  Example:
	  
	  For pi=[0.27,0.27,0.25,0.14,0.07]p_i = [0.27, 0.27, 0.25, 0.14, 0.07],
	  
	  H(X)=−(0.27⋅log⁡2(0.27)+0.27⋅log⁡2(0.27)+… )≈2.0654 bits.H(X) = -(0.27 \cdot \log_2(0.27) + 0.27 \cdot \log_2(0.27) + \dots) \approx 2.0654 \text{ bits.}
	  
	  ---
	- ### **3. Average Length of the Binary Codes**
	  
	  **Formula:**
	  
	  L=∑ipi⋅liL = \sum_{i} p_i \cdot l_i
	  
	  Where lil_i is the length of the code for symbol xix_i.
	- **Purpose**: Compute the expected number of bits per symbol in a specific encoding.
	- **Interpretation**: Average length should ideally approach the entropy H(X)H(X) for optimal codes.
	  
	  Example:
	  
	  For code1=["1","10","10","001","000"]code1 = ["1", "10", "10", "001", "000"], code lengths are [1,2,2,3,3][1, 2, 2, 3, 3], and
	  
	  L=0.27⋅1+0.27⋅2+0.25⋅2+0.14⋅3+0.07⋅3=1.9600 bits.L = 0.27 \cdot 1 + 0.27 \cdot 2 + 0.25 \cdot 2 + 0.14 \cdot 3 + 0.07 \cdot 3 = 1.9600 \text{ bits.}
	  
	  ---
	- ### **4. Efficiency of the Binary Codes**
	  
	  **Formula:**
	  
	  η=H(X)L\eta = \frac{H(X)}{L}
	- **Purpose**: Measures how close the encoding is to the theoretical minimum.
	- **Interpretation**: A perfectly efficient code will have η=1\eta = 1.
	  
	  Example:
	  
	  For code1code1, with H(X)=2.0654H(X) = 2.0654 and L=1.9600L = 1.9600,
	  
	  η=2.06541.9600≈1.0539.\eta = \frac{2.0654}{1.9600} \approx 1.0539.
	  
	  ---
	- ### **5. Prefix Codes**
	- **Definition**: A prefix code ensures no code is a prefix of another code.
	- **Purpose**: Guarantee unique decodability.
	- **Method**: Check if any code in the set is a prefix of another.
	  
	  Example:
	  
	  For code1=["1","10","10","001","000"]code1 = ["1", "10", "10", "001", "000"],
	- "1" is not a prefix of "10" or "001", and so on. Thus, **`code1` is a prefix code**.
	  
	  ---
	- ### **6. Shannon Binary Encoding**
	  
	  **Formula:**
	  
	  Ni=⌈−log⁡2(pi)⌉N_i = \lceil -\log_2(p_i) \rceil
	- **Purpose**: Calculate the codeword lengths required for a Shannon-optimal code.
	- **Interpretation**: −log⁡2(pi)-\log_2(p_i) gives the minimum number of bits needed to encode a symbol, and ⌈⋅⌉\lceil \cdot \rceil ensures integer values.
	  
	  Example:
	  
	  For pi=0.27p_i = 0.27,
	  
	  Ni=⌈−log⁡2(0.27)⌉=2 bits.N_i = \lceil -\log_2(0.27) \rceil = 2 \text{ bits.}
	  
	  The average length NavgN_{avg} is calculated as
	  
	  Navg=∑ipi⋅Ni.N_{avg} = \sum_{i} p_i \cdot N_i.
	  
	  ---
	- ### **7. Shannon's Fundamental Source Coding Theorem**
	  
	  **Theorem:**
	  
	  H(X)≤Navg≤H(X)+1H(X) \leq N_{avg} \leq H(X) + 1
	- **Purpose**: Validate if a given encoding satisfies the bounds set by Shannon's theorem.
	- **Interpretation**: If NavgN_{avg} lies within this range, the encoding is valid.
	  
	  Example:
	  
	  If H(X)=2.0654H(X) = 2.0654 and Navg=2.2000N_{avg} = 2.2000,
	  
	  2.0654≤2.2000≤3.06542.0654 \leq 2.2000 \leq 3.0654
	  
	  The theorem is **fulfilled**.
	  
	  ---
	- ### **8. Kraft-McMillan Inequality**
	  
	  **Formula:**
	  
	  ∑i2−li≤1\sum_{i} 2^{-l_i} \leq 1
	- **Purpose**: Validate if a set of code lengths is uniquely decodable.
	- **Interpretation**: If the sum is ≤1\leq 1, the code satisfies the Kraft-McMillan inequality.
	  
	  Example:
	  
	  For code1=["1","10","10","001","000"]code1 = ["1", "10", "10", "001", "000"],
	  
	  ∑i2−li=2−1+2−2+2−2+2−3+2−3=0.875≤1.\sum_{i} 2^{-l_i} = 2^{-1} + 2^{-2} + 2^{-2} + 2^{-3} + 2^{-3} = 0.875 \leq 1.
	  
	  This means **`code1` satisfies the Kraft-McMillan inequality**.
	  
	  ---
	  
	  These detailed steps ensure the code covers all aspects of information theory for the given problem.
	  
	  <!--EndFragment-->
-