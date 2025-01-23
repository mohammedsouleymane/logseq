- First order term unification
  to unify two term
	- compare **their functors**, if they do not match fail, otherwise...
	- if the terms have different **number of arguments** then fail otherwise...
	- if they have **no arguments** succeed, otherwise...
	- for each arguments
		- if one is a variable, let it be identical to the other, otherwise
		- unify them using this procedure
- meta predicates
	- **var** is a meta-predicate which tests whether or not its
	  argument is a variable
	- **ground/1**, which succeeds if its argument is fully instantiated
	- **findall/3** is exactly analogous to running a query and asking for all the solutions by hitting ; at the prompt
- dlist
	- Difference lists are likely to help in improving any program
	  which uses append – but. . . you cannot unify them!!!
	- Writing [a|X]-X = [a|Y]-Y has unpredictable results, because X and Y may have
	  different values
- To effectively summarize the content of the document for an exam, focus on the key concepts and their applications. Here's a structured summary:
- ### 1. **Difference Lists**
  collapsed:: true
	- **Problem with Ordinary Lists**: Manipulating lists from one end is inefficient, especially for long lists. Operations like `append/3` take O(n) time.
	- **Difference Lists**: A difference list is represented as the difference between two lists (e.g., `[a,b,c|X]-X`). This allows constant-time append operations.
	- **Usage**: Difference lists are useful for improving programs that use `append/3`. However, they cannot be unified directly due to variable naming issues.
- ### 2. **Definite Clause Grammars (DCGs)**
  collapsed:: true
	- **Purpose**: DCGs are used in Prolog to define languages according to grammar rules, making it easy to parse and generate sentences.
	- **Syntax**: DCGs use the `-->` operator instead of `:-`. They allow for the inclusion of Prolog code within `{}`.
	- **Expansion**: Prolog expands DCG rules into standard Prolog predicates, using difference lists to avoid the need for `append/3`.
	- **Applications**: DCGs can be used to parse command languages, generate syntax trees, and translate between languages.
- ### 3. **Meta-Programming in Prolog**
  collapsed:: true
	- **Concept**: Meta-programming involves writing programs that manipulate other programs. In Prolog, this is facilitated by the fact that program syntax and term syntax are identical.
	- **Representations**:
		- **Non-ground representation**: Variables are used to represent variables, allowing Prolog to handle unification.
		- **Ground representation**: Ground terms represent variables, requiring explicit handling of unification and variable bindings.
	- **Examples**:
		- **Solve Interpreter**: Simulates Prolog execution, allowing for custom computation rules.
		- **Breadth-first Execution**: Modifies the solve interpreter to execute goals in a breadth-first manner.
		- **Reasoning about Agents' Knowledge**: Extends the solve interpreter to handle multiple databases and common knowledge.
- ### 4. **Flexible Computation in Prolog**
  collapsed:: true
	- **Problem of Floundering**: Negation as failure in Prolog can lead to incorrect results due to fixed clause ordering.
	- **Solution**: Use of `when/2` to delay execution until certain conditions (e.g., groundness) are met.
	- **Example**: The British Museum Sort algorithm, which can be improved by delaying the checking of ordered-ness until the list is non-variable.
- ### 5. **Prolog Meta-Programming Facilities**
  collapsed:: true
	- **Term/Instantiation Testing**: Predicates like `var/1`, `nonvar/1`, and `ground/1` are used to check the instantiation of terms.
	- **Term Manipulation**: Predicates like `functor/3`, `arg/3`, and `=../2` are used to construct and deconstruct terms.
	- **Database Access/Manipulation**: Predicates like `clause/2`, `assert/1`, `retract/1`, and `retractall/1` allow for dynamic manipulation of the Prolog database.
	- **Meta-level Identity Testing**: Predicates like `==/2` and `\==/2` are used to test syntactic identity at the meta-level.
- ### Key Points to Remember:
- **Difference Lists**: Understand how they work and why they are more efficient for certain operations.
- **DCGs**: Know how to write and expand DCG rules, and understand their applications in parsing and translation.
- **Meta-Programming**: Be familiar with the concepts of non-ground and ground representations, and how to write meta-interpreters.
- **Flexible Computation**: Understand the problems with fixed clause ordering and how to use `when/2` to delay execution.
- **Meta-Predicates**: Be able to use and understand the purpose of key meta-predicates in Prolog.
  
  ---
- ### **1. Understand the Key Concepts**
  collapsed:: true
	- **Difference Lists**:
		- Know how they work and why they are more efficient than regular lists.
		- Be able to write and explain the `append/3` operation for difference lists.
		- Understand why unification can be problematic with difference lists.
	- **Definite Clause Grammars (DCGs)**:
		- Be able to write simple DCG rules for parsing or generating sentences.
		- Understand how DCGs are expanded into Prolog predicates using difference lists.
		- Know how to add arguments to DCGs for more complex tasks (e.g., translation or syntax trees).
	- **Meta-Programming**:
		- Understand the difference between **non-ground** and **ground representations**.
		- Be able to explain how meta-programming allows programs to manipulate other programs.
		- Know how to write a simple meta-interpreter (e.g., `solve/1`) and modify it (e.g., for breadth-first execution).
	- **Flexible Computation**:
		- Understand the problem of **floundering** and how to use `when/2` to delay execution.
		- Be able to explain how delayed goals can improve efficiency (e.g., in sorting algorithms).
	- **Meta-Predicates**:
		- Know the purpose of key meta-predicates like `var/1`, `nonvar/1`, `ground/1`, `functor/3`, `arg/3`, `=../2`, `clause/2`, `assert/1`, and `retract/1`.
		- Understand how to use `==/2` and `\==/2` for meta-level identity testing.
		  
		  ---
- ### **2. Practice Applying the Concepts**
  collapsed:: true
	- **Difference Lists**:
		- Write a Prolog program that uses difference lists to concatenate two lists in constant time.
		- Explain why `[a,b,c|X]-X` represents a difference list and how it can be used.
	- **DCGs**:
		- Write a DCG to parse a simple language (e.g., commands like `start 2 players` or `save game`).
		- Add arguments to a DCG to build a syntax tree or translate between languages.
	- **Meta-Programming**:
		- Write a meta-interpreter (`solve/1`) and modify it to handle breadth-first execution or multiple databases.
		- Explain how meta-programming can be used to reason about agents' knowledge (e.g., the "Three Wise Men" problem).
	- **Flexible Computation**:
		- Write a Prolog program that uses `when/2` to delay execution until a variable is ground.
		- Explain how delayed goals can prevent floundering in negation-as-failure.
	- **Meta-Predicates**:
		- Use `functor/3` and `arg/3` to deconstruct and reconstruct terms.
		- Write a program that dynamically adds or removes clauses from the Prolog database using `assert/1` and `retract/1`.
		  
		  ---
- ### **3. Be Prepared for Different Types of Exam Questions**
  collapsed:: true
	- **Theoretical Questions**:
		- Explain the difference between difference lists and ordinary lists.
		- Describe how DCGs are expanded into Prolog predicates.
		- Discuss the advantages and disadvantages of non-ground vs. ground representations in meta-programming.
	- **Practical Questions**:
		- Write a Prolog program using difference lists or DCGs.
		- Modify a given meta-interpreter to change its execution strategy.
		- Use meta-predicates to manipulate terms or the Prolog database.
	- **Problem-Solving Questions**:
		- Solve a problem using flexible computation (e.g., improve a sorting algorithm by delaying goals).
		- Reason about a meta-programming scenario (e.g., how to handle common knowledge in multi-agent systems).
		  
		  ---
- ### **4. Review the Document for Details**
  collapsed:: true
	- While the summary covers the main points, make sure to review the document for **specific examples** and **details** that might be tested. For example:
		- The exact syntax for writing DCG rules and adding arguments.
		- The trace of how `append/3` works with difference lists.
		- The specific behavior of meta-predicates like `=../2` or `clause/2`.
- ---
- ### **1. Constraint Logic Programming (CLP)**
	- **Problem with Traditional Prolog**: Traditional Prolog programs can waste time searching through impossible solutions because constraints are checked after generating a solution (e.g., British Museum Sort).
	- **Solution**: Use **constraints** to reduce the search space by reasoning about the data logically. Constraints are integrated into the unification process, allowing early failure when constraints are violated.
	- **Benefits**: Constraints can drastically reduce the search space and even change the algorithm's behavior (e.g., improving sorting algorithms).
	  
	  ---
- ### **2. Finite Domains (FD) in Prolog**
	- **Concept**: Finite domains allow you to associate a set of allowed values with a variable. Any attempt to unify the variable with a value outside its domain will fail immediately.
	- **Syntax**:
		- `X in 1..10`: Defines a domain for `X` (integers from 1 to 10).
		- `X #> Y + 2`: Posts an arithmetic constraint.
	- **Examples**:
		- `?- X in 1..10, X #> Y + 8, Y = 1.` → `X = 10`.
		- `?- X in 1..10, X #> Y + 8, Y = -2.` → `X in 7..10`.
	- **Residue**: Constraints can leave a residue (e.g., `X in 7..10`) that further constrains the variable.
	  
	  ---
- ### **3. Domain Specification**
	- **Domain Terms**: Domains can be specified using integers, ranges (e.g., `1..10`), sets (e.g., `{1,2,3}`), or unions/intersections of ranges.
	- **Predefined Constraints**:
		- `in/2`: Associates a range with a variable.
		- `#=/2`, `#>/2`, `#</2`, etc.: Arithmetic constraints.
		- `all_different/1`: Ensures all variables in a list have different values.
		  
		  ---
- ### **4. Labeling and Search Control**
	- **Labeling**: The `labeling/2` predicate is used to enumerate solutions for constrained variables.
		- **Control Options**: You can specify the order in which variables are instantiated (e.g., `ffc` for "first fail, smallest domain first") and whether to maximize or minimize certain variables.
		- **Example**:
		  ```prolog
		  ?- X in 1..10, Y in 2..15, X #< Y + 2, labeling([max(X)], [X, Y]).
		  ```
		  This maximizes `X` while satisfying the constraints.
	- **Indomain/1**: Enumerates values for a single variable.
	  
	  ---
- ### **5. Example: SEND + MORE = MONEY**
	- **Problem**: Solve the cryptarithmetic puzzle where each letter represents a unique digit.
	- **Solution**:
		- Use `add/3` to define the addition constraint.
		- Use `all_different/1` to ensure all digits are unique.
		- Use `labeling/2` to find solutions.
	- **Efficiency**: The constraint-based solution is ~2,800 times faster than a generate-and-test approach.
	  
	  ---
- ### **6. Reasoning About Domains**
	- **Meta-Predicates**:
		- `fd_inf/2`: Finds the minimum value in a domain.
		- `fd_size/2`: Returns the size of a domain.
		- `fd_dom/2`: Retrieves the entire domain of a variable.
	- **Use Cases**: These predicates are useful for controlling search strategies, such as instantiating variables with the smallest domain first.
	  
	  ---
- ### **7. Propositional and Reified Constraints**
	- **Propositional Constraints**: Allow logical combinations of constraints (e.g., `#\/` for OR, `#/\` for AND, `#==>` for implication).
		- Example: `X #= 1 #==> Y in 1..10` means "if `X = 1`, then `Y` must be between 1 and 10."
	- **Reified Constraints**: Associate a truth value (0 or 1) with a constraint.
		- Example: `(A #= B) #<==> R` means `R = 1` if `A = B`, and `R = 0` otherwise.
		- Useful for meta-programming and optimizing constraint satisfaction.
		  
		  ---
- ### **8. Combinatorial Constraints**
	- **all_different/1**: Ensures all variables in a list have different values.
	- **element/3**: Constrains `Y` to be the `X`th element of a list.
	- **relation/3**: Constrains `Y` based on a list of integer/range pairs associated with `X`.
	  
	  ---
- ### **9. Constraints Over Other Domains**
	- **Booleans**: Simple Boolean algebra constraints.
	- **Reals**: Constraints over real numbers (floating-point approximations).
	- **Rationals**: Constraints over rational numbers (fractions).
	- **Example**:
	  ```prolog
	  ?- {X < 2.0, Y > 1.0, Y = X + 1.0}.
	  ```
	  This constrains `X` and `Y` over real numbers.
	  
	  ---
- ### **10. Resource Allocation Example**
	- **Problem**: Stack boxes of varying heights in a limited space, ensuring the largest boxes are at the bottom.
	- **Solution**:
		- Use `constrain_boxes/3` to define physical constraints.
		- Use `link_boxes/1` to define relationships between boxes.
		- Use `labeling/2` to find a valid stacking solution.
		  
		  ---
- ### **Key Points to Remember**
	- **Constraints**: Understand how to define and use constraints to reduce search space.
	- **Finite Domains**: Know how to specify domains and use predicates like `in/2`, `#=/2`, and `all_different/1`.
	- **Labeling**: Be able to use `labeling/2` to enumerate solutions and control search strategies.
	- **Propositional and Reified Constraints**: Understand how to combine constraints logically and associate truth values with them.
	- **Applications**: Be familiar with classic problems like SEND + MORE = MONEY and resource allocation.