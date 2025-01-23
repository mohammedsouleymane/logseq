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
	- **Problem with Ordinary Lists**: Manipulating lists from one end is inefficient, especially for long lists. Operations like `append/3` take O(n) time.
	- **Difference Lists**: A difference list is represented as the difference between two lists (e.g., `[a,b,c|X]-X`). This allows constant-time append operations.
	- **Usage**: Difference lists are useful for improving programs that use `append/3`. However, they cannot be unified directly due to variable naming issues.
- ### 2. **Definite Clause Grammars (DCGs)**
	- **Purpose**: DCGs are used in Prolog to define languages according to grammar rules, making it easy to parse and generate sentences.
	- **Syntax**: DCGs use the `-->` operator instead of `:-`. They allow for the inclusion of Prolog code within `{}`.
	- **Expansion**: Prolog expands DCG rules into standard Prolog predicates, using difference lists to avoid the need for `append/3`.
	- **Applications**: DCGs can be used to parse command languages, generate syntax trees, and translate between languages.
- ### 3. **Meta-Programming in Prolog**
	- **Concept**: Meta-programming involves writing programs that manipulate other programs. In Prolog, this is facilitated by the fact that program syntax and term syntax are identical.
	- **Representations**:
		- **Non-ground representation**: Variables are used to represent variables, allowing Prolog to handle unification.
		- **Ground representation**: Ground terms represent variables, requiring explicit handling of unification and variable bindings.
	- **Examples**:
		- **Solve Interpreter**: Simulates Prolog execution, allowing for custom computation rules.
		- **Breadth-first Execution**: Modifies the solve interpreter to execute goals in a breadth-first manner.
		- **Reasoning about Agents' Knowledge**: Extends the solve interpreter to handle multiple databases and common knowledge.
- ### 4. **Flexible Computation in Prolog**
	- **Problem of Floundering**: Negation as failure in Prolog can lead to incorrect results due to fixed clause ordering.
	- **Solution**: Use of `when/2` to delay execution until certain conditions (e.g., groundness) are met.
	- **Example**: The British Museum Sort algorithm, which can be improved by delaying the checking of ordered-ness until the list is non-variable.
- ### 5. **Prolog Meta-Programming Facilities**
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
  
  By focusing on these key areas, you should be well-prepared to tackle exam questions on declarative programming, difference lists, DCGs, and meta-programming in Prolog.