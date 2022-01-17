In this manuscript, the authors propose a genetic algorithm based on symbolic trees and regression (SGA-PDE) to identify/uncover PDEs from data.
Previous approaches are employing sparse
regression based on a dictionary of predefined functions. The success of such approaches depends
on the dictionary selection, and the function components underlying the dynamics of the data need
to be part of this dictionary for previously proposed methods to succeed. The current manuscript,
alleviates this requirement by proposing a genetic algorithm that operates on symbolic trees that
represent the PDE.

SGA-PDE includes a crossover operator to reorganize different trees together (generating new
solution candidates), and special mutation and replacement operators to internally change certain
function terms, introducing new candidate solutions in the tree level. The effectiveness of the
proposed approach is demonstrated on three standard benchmarks for methods uncovering PDEs
(Burgers, KdV, Chafee-Infante), and two additional problems constructed by the authors (PDE
compound, PDE divide) where previous methods fail and SGA-PDE succeeds.
The language of the paper is clear. The proposed approach is very interesting and useful. The
findings are clearly explained, and supported by the results. As the interest in approaches uncovering PDEs from data is raising, the proposed method is an interesting contribution, augmenting
the arsenal of tools.

There are two main issues: first the authors do not compare with previous approaches (see comment later) and do not clearly report disadvantages of the proposed approach and the robustness
to hyperparameters (see comments later). Additional minor issues are included in the comments
that follow.

## 1 Comments
1. The literature review is good, especially with respect to recent works, but some references
from very early (older) approaches on genetic programming applied for scientific discovery
would enhance the manuscript, e.g. [1].

2. In page 4, the authors state that “Nevertheless, it is difficult to construct a method for effectively calculating the gradient between the loss and the structure of the equation, which
restricts the application of gradient-based methods and reinforcement learning in PDE discovery.” Reinforcement Learning, however, does not necessarily require that the loss (reward)
has a gradient. The reward is considered an observation. The gradient is computed on the
policy, which is something different. There are even completely gradient-free methods for
RL. There are some very early approaches towards this direction [2, 3] (I am not an author
of any of these works).

3. The abbreviation AIC is stated in page 8, although introduced much later.

4. In equation (3), the explanation of the parameter λ, the regularization coefficient is not
provided. The selection of this parameter can affect the results, especially the sparsity of the
solution, and this parameter has to be tuned together with tol.

5. The authors should clearly state the complete set of hyperparameters of their method, as
tuning all these hyperparameters is an additional complexity. For example, maximum tree
width, length, tol, λ, AIC threshold, etc. These are stated in the appendix, but some reference
to them (e.g. a table with all hyperparams, and default values) needs to be made in the main
text.

6. The authors do not report how they tuned the hyperparameters of their method for the
problems they consider. They do not offer a recipe on how to select them, even a heuristic
one. They state this information in the appendix, although some reference in the main text is
needed. For the reported results they do not report which hyperparameter combination leads
to these results. More importantly the robustness of their approach to the hyperparameter
selection is not analysed. The results are thus not reproducible from the information in the
main text.

7. Although the merits of the proposed approach are clear, the disadvantages compared to
other approaches (time to solution, biases included in the operands and how to select them,
additional implementation/design of the "rules" complexity, number of hyperparameters to
tune, robustness of results based on random seed) are not clearly analysed.

8. In page 13, the authors state that “Since the operators are basic, there is no need to make
many assumptions about the equation structure in SGA- PDE, which indicates the ability of
SGA-PDE to discover new equations from the data without prior knowledge of the mechanism
of the problem.”. Their method requires, however, the definition of (1) double operators, (2)
single operators, and (3) operands, which may not be clear for any dataset. So the "bias" is
shifted from other methods. In other methods some dictionary is built which includes some
bias, whereas in the proposed SGA-PDE this "architectural/expert" bias is in the operands,
etc. which seems smaller, but is not completely removed.

9. The problems that SGE-PDE solves, where previous methods (DLGA-PDE) fail, at least the
ones taken into account in this study, are artificially generated problems. Demonstrating that
the method works on a "physical" PDE or something more realistic where other methods
fail, would strengthen the paper.

10. The additional complexity of the proposed method compared to previous literature needs to
be clearly emphasized. The proposed method is solving multiple ridge regression problems
(to compute the fitness function) at every iteration.

11. Adding comparisons with previous approaches regarding time to solution would strengthen
the paper.

12. The authors are open-sourcing the data and code that assists reproducibility of the results
(if the hyper-parameters in the code are the same as the ones selected in the paper).

13. Please report in the main article that the algorithm is implemented in Python.

## 2 Typos - Rephrasing
1. (Suggestion) In page 2, the authors state that “It is impossible to find the function terms
that do not exist in the candidate set from the data in these methods. ” Please reformulate
the sentence to “It is not possible to find function terms that do not exist in the candidate
set with these methods, even if they are part of the underlying equations that generated the
data.”

2. Page 4, towards the end “the diffusion terms can be preset → present ...”

3. Page 10, “Since the mutation in SGA-PDE is to find” → “Since the goal of the mutation in
SGA-PDE is to find”

## References
[1] Maarten Keijzer. Scientific discovery using genetic programming. IMM, Informatik og Matematisk Modellering, Danmarks Tekniske Universitet, 2001.  
[2] A Lozano-Durán and M Bassenne. Towards model discovery with reinforcement learning.  
[3] Maxime Bassenne and Adrián Lozano-Durán. Computational model discovery with reinforcement learning. arXiv preprint arXiv:2001.00008, 2019.
