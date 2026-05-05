# Search algorithms
**Iterative deepening** repeats depth-limited DFS with limit 0, 1, 2 and combines BFS-like completeness with DFS-like space
#### Solving problems by search with heuristics:
$f[n] = g[n] + h[n]$:
$g[n]$ is the exact cost from the root to node $n$
$h[n]$ is a heuristic estimate from current node to $n$
A heuristic is called admissible if $h[n]$ <= actual cost
if $h[n] = 0$ for every node, the search become uniform-search
A*: DFS but frontier order is lowest $g[n] + h[n]$
IDA*: A* but bounded about a estimate value, if $f$ > threshold, cut the branch and find. If found, return; else update threshold = min($f$ s.t. $f$ > threshold) and restart the search.
A good heuristic sits in between: informative enough to prune, cheap enough to compute
# CSP / COP
## Constraint Satisfaction Problems:
A solution is a complete assignment that satisfies all constraints
## Constraint Optimization Problems:
Is a CSP but the target is to find the best solution

The representation is declarative: we specify the structure of the problem, not the solving steps
## Solving Paradigms:
Mathematical Progarmming: IP, MIP, column generation, SDP,...
Dynamic Programming
Local Search: tabu search, simulated anneling,...
Greedy algo, Ant Colony Opt, greedy randomized,...
Constraint Programming:
- Perturbative - Constructive
- Systematic vs Incomplete
## Heuristics and metaheuristics
#### Heu:
- Choose the next solution in the neighborhood
- Based on local info: the current and the next sol
- Drive the search toward local optimum
- Memoryless
#### Metaheu:
- Collect info on the exe sequence(s)
- Aim at escaping from local optima
- Drive the search toward global optimality
- Typically include memory or learning
## Local search: from CSP to COP:
$F[x] = cost[x] + a * penalty[x]$
$F[x]$ is the new target function
$cost[x]$ is the original target function
$a$ is coefficience of penalty (usally a very large number)
We run local search, sometimes goes into a bad assignment to seek a better solution later
## Search: branching strategy
- Standard branching strat: labelling
	- Label a variable and creates one branch per candidate value
- How to choose the variable?
	- *Domain heuristic* chooses the variable with the smallest domain: minimize the size of the search tree
	- *Degree heuristic* chooses the variable involved in the largest number of constraints: drive the search to a fail node if the CSP has no solution
- How to order the values?
	- Lexicographic static order
	- Choose a value that is more likely to reac h a solution