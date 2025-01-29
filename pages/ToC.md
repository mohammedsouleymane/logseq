# TQBF and FQBF: PSPACE-Complete Problems
collapsed:: true
	- ## 1. Definition of the TQBF Problem
	- **TQBF (True Quantified Boolean Formula)** is the problem of determining whether a given quantified Boolean formula (QBF) is true.
	- A **quantified Boolean formula (QBF)** is a Boolean formula with leading **existential (∃)** and **universal (∀)** quantifiers. Each variable in the formula must be within the scope of a quantifier.
	- A QBF is either **TRUE** or **FALSE**. For example:
		- **Example QBF**: ∀x∃y (x ∨ y) ∧ (¬x ∨ ¬y) is a QBF.
		- **Non-QBF Example**: (x ∨ y) ∧ (¬x ∨ ¬y) is a Boolean formula but not a QBF because it is not quantified.
	- The **TQBF problem** is formally defined as:
	  
	  \[ TQBF = \{ \langle \phi \rangle \ | \ \phi \text{ is a QBF that is TRUE} \} \]
	  
	  ---
	- ## 2. Complexity of TQBF
	- **TQBF is PSPACE-complete.**
	- **PSPACE** is the class of decision problems solvable by a deterministic Turing machine using polynomial space.
	- PSPACE-completeness means a problem is among the "hardest" problems in PSPACE.
	- ### PSPACE-Completeness Criteria
	  1. **TQBF is in PSPACE:**
		- A recursive algorithm can determine if a QBF is true using polynomial space.
		- If the QBF has no quantifiers, it evaluates to either TRUE or FALSE.
		- If the QBF is of the form ∃x ψ, evaluate ψ with x = TRUE and x = FALSE recursively, and accept if either evaluates to TRUE.
		- If the QBF is of the form ∀x ψ, evaluate ψ with x = TRUE and x = FALSE recursively, and accept if both evaluate to TRUE.
		- The recursion depth is at most n (the input length), implying TQBF is in SPACE(n) and therefore in PSPACE.
		  
		  2. **All problems in PSPACE are polynomial-time reducible to TQBF:**
		- Given a language **A** in PSPACE, construct a polynomial-time reduction from **A** to TQBF.
		- Let **M** be a Turing machine deciding **A** in space **n^k**.
		- Construct a QBF **ϕ** that simulates **M** on input **w** such that **ϕ** is TRUE if and only if **M** accepts **w**.
		- The QBF **ϕ** represents the computation history of **M** on **w**, with a tableau of at most **n** columns (max configuration size) and **d(n^k)** rows (max steps taken by **M**), where **d** is a constant.
		- Define configurations recursively using **ϕ(c₁, c₂, b)**, which asserts that **M** transitions from configuration **c₁** to **c₂** in **b** steps.
		- The reduction is computable in **O(n^{2k})** time.
		  
		  ---
	- ## 3. Complexity of the FQBF Problem
	- **FQBF (False Quantified Boolean Formula)** is the problem of determining whether a given QBF is **false**.
	- **FQBF is PSPACE-complete**, as it is the complement of TQBF.
	- Since PSPACE = coPSPACE, if a problem is in PSPACE, its complement is also in PSPACE.
	- Because TQBF is PSPACE-complete and FQBF is its complement, **FQBF is also PSPACE-complete**.
	- If a polynomial-time algorithm were found for FQBF, it would imply **P = PSPACE**, a major open problem in complexity theory.
	  
	  ---
	- ## Summary
	- **TQBF is a PSPACE-complete problem**, meaning it is one of the hardest problems in PSPACE. The problem is to determine if a quantified Boolean formula is **true**.
	- **FQBF is the complement of TQBF**. Since PSPACE = coPSPACE, **FQBF is also PSPACE-complete**.
	- Both problems remain fundamental in computational complexity, with important implications for theoretical computer science.
- # Undecidability, the Recursion Theorem, and the Halting Problem
  collapsed:: true
	- ## 1. Decidability of the Given Problem
	- **Problem Statement:** Given a Turing machine (TM) **M**, does **M** halt on input **⟨M⟩** (its own encoding)?
	- **This problem is undecidable.**
	- This is a variation of the **Halting Problem**, where instead of testing if a TM halts on a given input, we test if it halts on its own encoding.
	- The **Halting Problem** (HALT_TM = {⟨M, w⟩ | M halts on input w}) is **undecidable**.
	- ### Proof by Reduction
	  1. Assume there exists a TM, **R**, that decides the given problem. That is, **R** accepts **⟨M⟩** if **M** halts on input **⟨M⟩** and rejects otherwise.
	  2. Construct a TM **S** to decide HALT_TM, which is known to be undecidable:
		- **S =** "On input ⟨M, w⟩:
		  1. Modify **M** to create a new TM **M'** that ignores its input and runs **M** on input **w**.
		  2. Run **R** on ⟨M'⟩.
		  3. Accept if **R** accepts, and reject if **R** rejects."
		  3. If **R** decides the given problem, then **S** decides HALT_TM:
		- If **M** halts on **w**, then **M'** halts on any input, so **M'** halts on **⟨M'⟩**, so **R** accepts ⟨M'⟩, so **S** accepts.
		- If **M** does not halt on **w**, then **M'** does not halt on any input, so **M'** does not halt on **⟨M'⟩**, so **R** rejects ⟨M'⟩, so **S** rejects.
		  4. Since no decider exists for the Halting Problem, we have a contradiction. Therefore, the given problem is **undecidable**.
		  
		  ---
	- ## 2. Formal Statement of the Recursion Theorem
	- **The Recursion Theorem:** "Let **T** be a Turing machine that computes a function **t : Σ* × Σ* → Σ***. Then, there exists a Turing machine **R** that computes a function **r : Σ* → Σ*** such that for every input **w**, **r(w) = t(⟨R⟩, w)**."
	- **Intuition:** There exists a TM **R** that can access its own description, **⟨R⟩**, and use it in its computation.
	- This theorem enables self-referential behavior in TMs.
	  
	  ---
	- ## 3. Using the Recursion Theorem to Prove Undecidability
	- **We prove that ATM = {⟨M, w⟩ | M accepts w} is undecidable.**
	- **Assumption:** Suppose ATM is decidable. Let **H** be a decider for ATM:
		- **H(⟨M, w⟩) accepts** if **M** accepts **w**.
		- **H(⟨M, w⟩) rejects** if **M** does not accept **w**.
	- ### Construction of TM **T**
	  1. **T(⟨M⟩, w):**
	   1. Run **H** on input **⟨M, w⟩**.
	   2. If **H** accepts, reject.
	   3. If **H** rejects, accept.
	  2. By the **Recursion Theorem**, there exists a TM **R** such that **R(w) = T(⟨R⟩, w)**.
	  3. Analyzing **R(w):**
		- **R(w) = T(⟨R⟩, w) =** If **H(⟨R, w⟩) accepts, reject**; if **H(⟨R, w⟩) rejects, accept**.
		- Since **H(⟨R, w⟩) accepts if R accepts w and rejects if R does not accept w**, we reach a **contradiction**.
	- ### Conclusion
	- The assumption that **H** exists is incorrect.
	- Therefore, **ATM is undecidable**.
	  
	  ---
	- ## Summary
	- The problem of determining if a TM halts on its own encoding is **undecidable**, shown via reduction from the Halting Problem.
	- The **Recursion Theorem** allows a TM to access its own description, enabling self-reference.
	- The theorem is crucial for proving the undecidability of problems like **ATM**.
- # Logarithmic Space Complexity Classes: L and NL
  collapsed:: true
	- Definitions of L and NL:
		- **L (Logarithmic Space):** L is the class of decision problems that can be solved by a deterministic Turing machine using a logarithmic amount of space. This means that the amount of memory (tape cells) the Turing machine uses is bounded by O(log n), where n is the size of the input. The input itself is read-only and doesn't count toward the space used [1].
		- **NL (Nondeterministic Logarithmic Space):** NL is the class of decision problems that can be solved by a nondeterministic Turing machine using a logarithmic amount of space [1]. Similar to L, the space used is bounded by O(log n), but the machine is nondeterministic, meaning it can explore multiple computation paths simultaneously, and again the input is read-only and does not count toward the space used [1].
	- Relationship between L and NL:
		- L is a subset of NL because any deterministic Turing machine is also a nondeterministic Turing machine, meaning any problem solvable deterministically in logarithmic space is also solvable nondeterministically in logarithmic space [1].
		- The precise relationship between L and NL is unknown; specifically, it is not known if L = NL or if L is a strict subset of NL [2].
		- It is known that NL = coNL, meaning if a problem is in NL, then its complement is also in NL. This follows from the Immerman-Szelepcsényi theorem, which states that for every function f with f(n) ≥ log(n), NSPACE(f(n)) = coNSPACE(f(n)), implying NL is closed under complementation [2].
	- Relationship to other complexity classes:
		- **NL is a subset of P:** A log-space Turing machine has a limited number of configurations (specifically, O(n^k) for some constant k), so it can only run for a polynomial amount of time before repeating a configuration and looping [3]. Because any problem in NL is solvable by a Turing machine that runs in polynomial time, NL is a subset of P.
		- **L is a subset of P:** Since L is a subset of NL and NL is a subset of P, L is also a subset of P.
		- **NL is a subset of PSPACE:** P is a subset of PSPACE, and since NL is a subset of P, it follows that NL is also a subset of PSPACE.
		- **NL is a subset of SPACE(log^2(n)):** By Savitch's theorem, NSPACE(f(n)) is a subset of SPACE(f(n)^2). For log-space, this implies NL is a subset of SPACE(log^2(n)) [3].
	- NL-completeness and an example:
		- **Definition:** A language B is NL-complete if:
			- B is in NL [4].
			- For all languages A in NL, A is log-space reducible to B, meaning if we have a solution to B, we can solve all other problems in NL [4].
		- Log-space reducibility means there exists a function f computable in logarithmic space that transforms an instance of problem A to an instance of problem B such that the answer to A is "yes" if and only if the answer to B is "yes" [5]. This requires a log-space transducer with a read-only input tape, a read/write work tape using at most O(log n) space, and a write-only output tape [5].
		- **Example:** The problem PATH is NL-complete. PATH is the set of all tuples 〈G, s, t〉 such that G is a directed graph with a path from node s to node t [6, 7]. The proof of PATH being NL-complete shows that PATH is in NL, and all languages in NL are log-space reducible to PATH [7]. It also constructs a log-space transducer to perform this reduction [7, 8].
		- Another example of an NL-complete problem is **2SAT**, the set of satisfiable Boolean formulas in 2CNF (conjunctive normal form with exactly 2 literals per clause) [8, 9].
		  
		  In summary, L and NL are complexity classes defined by the amount of space a Turing machine uses. NL is the nondeterministic counterpart of L, and it is contained in $P, SPACE(log^2(n))$, and PSPACE. NL-complete problems are the "hardest" problems in NL, as any other problem in NL can be reduced to them using a log-space reduction.
		  
		  <!--EndFragment-->
- # NP, coNP, and Certificates
  collapsed:: true
	- ### 1. Definitions of the Class NP:
	- **Direct Definition**: NP is the class of decision problems that can be solved by a nondeterministic Turing machine (NTM) in polynomial time. This means there exists an NTM that, for any input of size *n*, halts in at most *n^k* steps for some constant *k*. If at least one of the computation branches of the NTM accepts the input, then the input is considered to be in the language.
	- **Certificate-Based Definition**: A language *A* is in NP if there exists a polynomial-time verifier *V* such that:
		- *A = {w | V accepts ⟨w, c⟩ for some c}*
		- This means that for any string *w* in *A*, there exists a string *c* (the "certificate") such that *V* can verify that *w* is in *A* in polynomial time, based on *c*.
		- The size of the certificate must also be polynomial in the length of *w*.
	- ### 2. Intuitive Explanation of Equivalence:
	- The two definitions of NP are equivalent because the "certificate" definition effectively captures the power of nondeterminism.
	- **Nondeterministic TM Perspective**: An NTM can "guess" a potential solution (e.g., a path in HAMPATH or a factor in COMPOSITES) and then verify that the guess is correct in polynomial time.
	- **Polynomial-Time Verifier with a Certificate**: The certificate is the "guess" that the NTM makes. The verifier then checks if the guess is a valid solution in polynomial time.
	- Essentially, the NTM's ability to explore all possible computation paths simultaneously is mirrored by the verifier's ability to check any potential certificate in polynomial time. The certificate provides the specific "path" or "choice" that would have led the NTM to accept.
	- ### 3. Certificates for the Class coNP:
	- **coNP Definition**: The class coNP is the set of languages whose complements are in NP. If *A* is in coNP, then the complement of *A*, denoted as *Ā*, is in NP.
	- **Certificates for coNP**:
		- A language *A* is in coNP if there exists a polynomial-time verifier *V* such that *w* ∈ *A* if and only if for all certificates *c*, *V(⟨w, c⟩)* rejects.
		- In other words, for an input *w* in *A* (a coNP language), no certificate can convince *V* that *w* is not in *A*.
		- Conversely, *w* is not in *A* if and only if there exists a certificate *c* for which *V(⟨w, c⟩)* accepts.
	- **Example**:
		- *TAUTOLOGY* = {⟨ϕ⟩ | all assignments satisfy ϕ} is a coNP problem.
		- To show that *ϕ* is a tautology, we must show that no assignment falsifies *ϕ*, meaning that a certificate proving *ϕ* is not a tautology cannot exist.
	- ### 4. Certificates for Problems in NP ∪ coNP:
	- For problems in **NP**, there exist polynomial-size certificates that can be used to efficiently verify that a given input is in the language.
	- For problems in **coNP**, there is no such certificate that directly shows an input is in the language, but if an input *w* is **not** in the language, then there exists a certificate proving that *w* is in the complement language (which is an NP language).
	- **Key Difference**:
		- NP problems have certificates for membership.
		- coNP problems have certificates for non-membership (i.e., certificates for membership in their complement).
	- It is not known if all problems in **NP ∪ coNP** have certificates for both membership and non-membership, since it is not known whether **NP = coNP**.
	- It is known that **P ⊆ NP ∩ coNP**. If NP = coNP, then all problems in NP ∪ coNP would have certificates for both membership and non-membership.
	- ### **Summary:**
	- NP problems can be defined using nondeterministic Turing machines or with polynomial-time verifiers that take certificates, capturing the notion of efficiently verifiable solutions.
	- coNP is the complementary class, characterized by the existence of certificates that demonstrate an input is **not** in the language.
	- The relationship between NP and coNP is an open question, and whether every problem in NP ∪ coNP has both types of certificates is unknown.
	  
	  <!--EndFragment-->
- # PSPACE, NPSPACE, and their Relationship to Time Complexity
  collapsed:: true
	- **Defining PSPACE and NPSPACE:**
		- **PSPACE (Polynomial Space):** PSPACE is the class of decision problems that can be solved by a deterministic Turing machine using a polynomial amount of space. This means that the amount of memory (tape cells) the Turing machine uses is bounded by a polynomial function of the input size *n*.
		- **NPSPACE (Nondeterministic Polynomial Space):** NPSPACE is the class of decision problems that can be solved by a nondeterministic Turing machine using a polynomial amount of space. Similar to PSPACE, the space used is bounded by a polynomial function of the input size, but the machine is nondeterministic, meaning it can explore multiple computation paths simultaneously.
	- **Relationship between PSPACE and NPSPACE:**
		- The sources state that PSPACE = NPSPACE. This is a significant result, and it is a consequence of Savitch's theorem.
		- **Sketch of Proof (Savitch's Theorem):** Savitch’s theorem demonstrates that any problem solvable by a nondeterministic TM using *f(n)* space can be solved by a deterministic TM using *f(n)^2* space. The conversion of an NTM *N* to a deterministic TM *M* involves using a recursive algorithm to test if a configuration of *N* can reach another configuration within a given number of steps. The deterministic algorithm needs to keep track of configurations in the recursion, requiring *O(f(n))* space per level of recursion and a recursion depth of *O(f(n))*, thus the total space is *O(f(n)^2)*. When *f(n)* is a polynomial function, then *f(n)^2* is also a polynomial function, so this shows NPSPACE is a subset of PSPACE. Because a deterministic TM is also a nondeterministic TM, we also have that PSPACE is a subset of NPSPACE, so we can conclude that PSPACE = NPSPACE.
	- **Relationship to Time Complexity Classes:**
		- **PSPACE contains P:** The class P (polynomial time) is a subset of PSPACE because a Turing machine that runs in polynomial time can use, at most, a polynomial amount of space. A TM that uses *t(n)* time can use, at most, *t(n)* space.
		- **PSPACE contains NP:** As shown above, P is a subset of PSPACE, and it is known that NP contains P. We also know that NP is a subset of PSPACE because any problem in NP can be verified using a polynomial amount of space. So it is true that PSPACE also contains NP.
		- **PSPACE is a subset of EXPTIME:** A TM that uses *t(n)* space cannot use more than *2^{O(t(n))}* time without repeating a configuration and looping. Therefore, PSPACE is a subset of EXPTIME (exponential time) because a Turing machine that runs in polynomial space is limited to an exponential number of possible configurations and thus will halt in exponential time.
		- **TIME(t(n)) ⊆ SPACE(t(n))**: Any Turing Machine that uses *t(n)* steps can use at most *t(n)* space. This means a TM that runs in polynomial time must also run in polynomial space.
		- **SPACE(t(n)) ⊆ TIME(2^{O(t(n))})**: A Turing machine that runs in *t(n)* space can be simulated in *2^{O(t(n))}* time.
		  
		  In summary, PSPACE and NPSPACE are complexity classes that relate to the amount of memory a Turing Machine uses. They are equivalent, as stated by Savitch's Theorem. They encompass polynomial time classes like P and NP and are contained within exponential time classes like EXPTIME.
		  
		  <!--EndFragment-->