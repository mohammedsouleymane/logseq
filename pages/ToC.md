# TQBF and FQBF: PSPACE-Complete Problems
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
-
-