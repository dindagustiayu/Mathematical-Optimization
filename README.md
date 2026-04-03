[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

# Mathematical Optimization
Optimization comes from the same root as optimal, which means _best_. When you optimize something, you are __making it best__. But _best_ can vary. 

_People optimize_. If you are a football player, you might want to maximiza your running yards, and also minimize your fumbles. Both maximizing and minimizing are types of optimization problems. 

_Nature optimize_. Physical systems tend to a state of minimum energy. The molecules in an isolated chemical system react with each other until the total potential energy of their electrons is minimized. Rays of light follow paths that minimize their travel time.

Optimization is an important tool in decision science and in the analysis of physical systems. The process is:
1. We must first identify some _objective_, a quantitative measure of the performance of the system under study (time, potential energy, or any values).
2. The objective depends on certain characteristics of the systems, called _variables_ or _unknowns_.
3. Often the variables are restricted, or _constrained_, in some way. For instance, such as electron density in a molecule and the interest rate on a loan, cannot be negative.
4. The process of identifying objective, variables and constraints for a given problem is known as _modelling_.
5. Once the model has been formulated, an optimization algorithm can be used to find its solution.
6. After optimization, we must be able to recognize whether it has succeeded in its task of finding a solution. In many cases, there are ellegant mathematical expression known as _optimally conditions_ for checking that the current set of variables is indeed the solution of the problem.

## Prerequisites
- Linear Algebra
- Calculus I (Derivatives)
- Computer programming skills

## Mathematical Formula
In mathematics, optimization is the minimization or maximization of a function subject to constraints on its variables. We use the following notation:

- $x$ is the vector of _variables_, also called _unknowns_ or _parameters_.
  Variables, $x_1 \ x_2 \ x_3$ and so on, which are the __inputs__ things we can control. They abbreviated $x_n$ to refer to individuals or $x$ to refer to them as a group.
  
- $f$ is the _objective function_, a function of x that we want to maximize or minimize. The objective function, $f(x)$, which is the __output__ we are trying to maximize or minimize.

- $c$ is the vector of _constraints_ that the unknowns must satisfy. This is a vector function of the variables $x$. The number of components in $c$ is the number of individual restrictions that we place on the variables. _Constraints_, which are equations that place limits on how big or small some variables can get.

    - Equality constraints are noted $h_n (x)$
    - Inequality constraints are noted $g_n (x)$


The optimization problem can then be written as 
<p align='center'>
    $$ \begin{align} \min_{x \ \in \ R^n} \ f(x) \quad \mbox{subject \ to} \ \left \{\begin{array} \\ c_i (x) = 0, \quad i \ \in \ \varepsilon \\ c_i(x) \geq 0, \quad i \ \in \ \imath \end{array} \right \} \end{align}$$
</p>
    
## Example
Here $f$ and each $c_i$ are scalar-valued functions of the variables $x$, and $\mathcal{I}, \ \mathcal{I}$ are sets of indices. As a simple example, consider the problem
<p align='center'>
    $$\begin{align} \mbox{min} \ (x_1 - 2)^2 + (x_2 - 1)^2 \quad \mbox{subject \ to} \ \left \{\begin{array} \\ x_1^2 - x_2 \quad \leq \ 0 \\ x_1 + x_2 \quad \leq \ 2 \end{array} \right \} \end{align}$$ 
</p>

## Solution
- The objective function $f(x)$
<p align='center'>
    $$f(x_1, \ x_2) = (x_1 -2)^2 + (x_2 -1)^2$$
</p>
    Often, it is more natural or convenient to label the unknowns with two or three subscripts, or to use different variables by completely different names, so that relabeling is necessary to achieve the standard form.
    
- Calculate the constraints $c(x)$ with $\mathcal{E} = 0$ and $\mathcal{I} = [1, \ 2]$, these consraints are __inequality__ so $c_i (x) \geq 0$. We can write this problem by defining the constraints,

    Another common difference is that we are required to _maximize_ rather than _minimize_ $f$, but we can accommodate this change easily by _minimizing_ $-f$ in this formulation.

    - constraint 1: $-x_1^2 + x_2 \geq 0$
    - constraint 2: $-x_1 - x_2 + 2 \geq 0$


<p align='center'>
    $$\begin{align} f(x) &= (x_1 - 2)^2 + (x_2 -1)^2, \quad x =\left  [\begin{array} \ x_1 \\ x_2 \end{array} \right] \\ c(x) &= \left [\begin{array} \ c_1 (x) \\ c_2 (x) \end{array} \right] = \left [\begin{array} \ -x_1^2 + x_2 \\ -x_1 - x_2 + 2 \end{array} \right], \quad \imath= \{ 1, \ 2 \}, \quad \varepsilon = 0  \end{align}$$
</p>
