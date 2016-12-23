# DPLL-Algorithm-CNF

The DPLL algorithm is designed to evaluate satisfiability of a
propositional logic formula in conjunctive normal form (CNF). 
A logical expression in CNF can be represented in Python as a list of sets of integers. 

For example:
clauses = [{1,2,3}, {-1,3}, {4}, {-4, -3}]

Each integer represents a literal, which is negative if the literal is negated and positive
otherwise. The absolute value of the integer identifies the atomic sentence. So the above
represents:

(P1 v P2 v P3) ^ (-P1 v P3) ^ P4 ^ (-P4 v -P3)

-> init (self, cnf) accepts as input a CNF formula as a list of sets
-> solve(self) returns True if cnf is satisfiable and False otherwise
