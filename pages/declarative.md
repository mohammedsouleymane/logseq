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