## CONTENTS

| Section | Focus |
|:--:|---|
| [01](#01--major-topics-to-add) | Major topics missing from the original roadmap |
| [02](#02--additional-mathematical-theory) | Mathematical theory to master |
| [03](#03--algorithmic-families) | Algorithmic families |
| [04](#04--research-areas) | Research areas in non-convex optimization |
| [05](#05--additional-resources) | Books, monographs, lecture notes and papers |
| [06](#06--how-to-extend-the-original-roadmap) | Three levels of expertise |
| [07](#07--recommended-final-study-roadmap) | Recommended study order |
| [08](#08--expertise-milestones) | What becoming an expert means |

# 01 · Major topics to add

The existing roadmap provides a strong foundation in **smooth, unconstrained non-convex optimization and saddle-point escape**. To broaden it into a more comprehensive study of non-convex optimization, add the following areas.

| No. | Topic | Important concepts to study | Why it matters |
|:--:|---|---|---|
| 01 | **Variational analysis** | Subgradients, generalized derivatives, normal cones, tangent cones, subdifferentials | Provides a rigorous foundation for nonsmooth and constrained non-convex optimization |
| 02 | **Nonsmooth optimization** | Clarke subdifferential, directional derivatives, weak convexity, prox-regularity | Many modern optimization problems involve nonsmooth objectives |
| 03 | **Proximal algorithms** | Proximal operator, proximal point method, proximal gradient, Moreau envelope | Essential for composite and regularized non-convex problems |
| 04 | **Constrained non-convex optimization** | KKT conditions, constraint qualifications, Lagrangian, second-order constrained optimality | A major class of practical and theoretical optimization problems |
| 05 | **Stochastic non-convex optimization** | SGD convergence, stochastic approximation, gradient variance, sample complexity | Essential for modern machine learning optimization |
| 06 | **Variance reduction methods** | SVRG, SAGA, SARAH, SPIDER, STORM | Important for improving stochastic gradient complexity |
| 07 | **Non-convex minimax optimization** | Minimax objectives, gradient descent-ascent, extragradient, game-theoretic equilibria | A separate and substantial branch of non-convex optimization |
| 08 | **Global optimization** | Branch and bound, deterministic global optimization, relaxation methods, computational hardness | Explains the difference between finding local stationary points and global optima |
| 09 | **Structured non-convex optimization** | Low-rank matrix factorization, matrix sensing, phase retrieval, tensor decomposition | Studies problem structures where global solutions may be theoretically attainable |
| 10 | **Optimization geometry** | PL condition, error bounds, gradient dominance, invexity, benign landscapes | Explains when non-convex problems can have favorable global convergence properties |
| 11 | **Continuous-time optimization** | Gradient flow, ODE methods, stochastic differential equations, Lyapunov stability | Provides a dynamical-systems perspective on optimization algorithms |
| 12 | **Modern adaptive optimization** | Momentum, Adam, RMSProp, adaptive learning rates, convergence analysis | Important for understanding practical deep learning optimization |

**Perspective:** These are not merely optional extensions. Several are independent research areas with their own mathematical frameworks. For example, variational analysis, minimax optimization, and global optimization each require substantial additional theory.

# 02 · Additional mathematical theory

Beyond algorithmic topics, the following mathematical concepts are important for reading theoretical optimization papers.

| No. | Mathematical topic | Specific concepts and results to learn | Importance |
|:--:|---|---|:--:|
| 01 | **Lipschitz continuity and smoothness** | Gradient Lipschitzness, Hessian Lipschitzness, Hölder continuity | Essential |
| 02 | **Descent and error bounds** | Descent lemma, quadratic growth, error-bound conditions | Essential |
| 03 | **Polyak–Łojasiewicz (PL) condition** | PL inequality, gradient dominance, convergence without convexity | Essential |
| 04 | **Kurdyka–Łojasiewicz (KL) theory** | KL inequality, Łojasiewicz exponent, finite-length property, convergence of iterates | Essential |
| 05 | **Variational inequalities** | Monotone operators, pseudomonotonicity, equilibrium problems | High |
| 06 | **Duality theory** | Lagrangian duality, weak and strong duality, duality gaps | High |
| 07 | **Constraint qualifications** | LICQ, MFCQ, Slater-type conditions, KKT regularity | High |
| 08 | **Second-order variational analysis** | Second-order directional derivatives, generalized Hessians, curvature of constraints | High |
| 09 | **Concentration inequalities** | Hoeffding, Bernstein, Azuma, Gaussian concentration | High |
| 10 | **Dynamical systems theory** | Lyapunov functions, stability, invariant sets, ODE methods | High |
| 11 | **Random matrix theory** | Spectral distributions, eigenvalue concentration, random Hessians | Intermediate |
| 12 | **Numerical conditioning** | Condition numbers, preconditioning, ill-conditioning, finite precision | Essential |

## 2.1 · Polyak–Łojasiewicz condition

A differentiable function satisfies the PL inequality if

\[
\frac{1}{2}\|\nabla f(x)\|^2
\geq
\mu\big(f(x)-f^\star\big),
\]

for some \(\mu>0\).

An important consequence is that certain non-convex functions can enjoy global convergence guarantees without being convex.

**Study:**

- PL inequality.
- Gradient dominance.
- Linear convergence under PL.
- Relationship between PL and strong convexity.
- Examples of non-convex functions satisfying PL.

## 2.2 · Kurdyka–Łojasiewicz inequality

For an appropriate desingularizing function \(\varphi\), a common form of the KL inequality is

\[
\varphi'(f(x)-f^\star)
\operatorname{dist}(0,\partial f(x))
\geq 1.
\]

It is widely used to establish convergence of optimization sequences, especially in non-convex and nonsmooth problems.

**Study:**

- KL property.
- Łojasiewicz gradient inequality.
- Semi-algebraic functions.
- Sufficient decrease conditions.
- Relative error conditions.
- Finite-length convergence of iterates.

These concepts matter because not every non-convex convergence analysis relies on finding or escaping saddle points.

# 03 · Algorithmic families

The original roadmap primarily covers gradient descent, Newton methods, perturbed gradient descent, and negative-curvature methods. For broader expertise, study the following algorithmic families.

| Algorithm family | Algorithms to study | Main theoretical question |
|---|---|---|
| **First-order methods** | GD, SGD, Momentum, Nesterov acceleration | When do first-order methods converge? |
| **Adaptive methods** | AdaGrad, RMSProp, Adam, AdamW | Under what conditions do adaptive methods converge? |
| **Second-order methods** | Newton, damped Newton, trust-region Newton | How does curvature improve convergence? |
| **Cubic regularization** | Cubic-regularized Newton | How can second-order methods obtain stronger stationarity guarantees? |
| **Proximal methods** | Proximal point, proximal gradient, proximal Newton | How do we optimize composite objectives? |
| **Stochastic variance reduction** | SVRG, SAGA, SARAH, SPIDER, STORM | How can stochastic gradient complexity be reduced? |
| **Coordinate methods** | Coordinate descent, block coordinate descent | How does partial parameter updating affect convergence? |
| **Derivative-free methods** | Random search, evolution strategies, zeroth-order gradient estimation | How can optimization proceed without gradient access? |
| **Minimax methods** | GDA, extragradient, optimistic gradient, proximal point | How do we solve non-convex minimax problems? |
| **Global optimization** | Branch and bound, spatial branch and bound, deterministic relaxations | How can global optimality be established? |

> **Important distinction:** Acceleration in non-convex optimization is not the same as acceleration in convex optimization. The guarantees, assumptions, and stationarity measures can be substantially different.

# 04 · Research areas in non-convex optimization

To become comfortable reading papers from ICML, NeurIPS, COLT, SIOPT, Mathematical Programming, and related journals, study these research areas as distinct branches.

| Research area | Core topics | Representative research direction |
|---|---|---|
| **Non-convex stochastic optimization** | SGD, stochastic approximation, sample complexity | Finding approximate stationary points with limited data |
| **Non-convex finite-sum optimization** | SVRG, SARAH, SPIDER, variance reduction | Improving gradient-oracle complexity |
| **Non-convex minimax optimization** | Minimax equilibrium, GDA, extragradient | Convergence in adversarial learning and games |
| **Low-rank optimization** | Matrix factorization, matrix sensing, matrix completion | Understanding benign non-convex landscapes |
| **Tensor optimization** | Tensor decomposition, CP decomposition, tensor power methods | Strict-saddle structures and global recovery |
| **Phase retrieval** | Nonlinear inverse problems, spectral initialization, gradient methods | Global recovery guarantees |
| **Bilevel optimization** | Hypergradients, implicit differentiation, nested optimization | Optimization involving inner and outer objectives |
| **Nonsmooth non-convex optimization** | Clarke stationarity, proximal algorithms, weak convexity | Optimization with nonsmooth regularizers |
| **Global optimization** | Branch and bound, convex relaxations, deterministic guarantees | Establishing global rather than local optimality |
| **Online non-convex optimization** | Online gradient methods, regret, dynamic regret | Optimization with sequentially changing objectives |

## 4.1 · General versus structured non-convex optimization

A crucial distinction is between general non-convex problems and structured non-convex problems.

| | **Class 1 — General non-convex optimization** | **Class 2 — Structured non-convex optimization** |
|---|---|---|
| Formulation | \(\min_{x\in\mathbb R^d} f(x)\) | A non-convex objective with additional algebraic or statistical structure |
| Examples | General smooth or nonsmooth non-convex objectives | Matrix factorization, matrix sensing, phase retrieval, tensor decomposition |
| Typical difficulty | Many local minima, saddle points, and potentially poor local solutions | Non-convexity may have a favorable landscape under suitable assumptions |
| Common guarantees | Approximate first- or second-order stationarity | Sometimes global recovery or global optimality |
| Main question | Can an algorithm find a sufficiently good stationary point? | Does the problem structure make global recovery possible? |

**Key insight:** Non-convexity does not automatically imply that a problem is computationally difficult in practice or that every local minimum is undesirable.

For broader global-optimization theory, study computational hardness, relaxations, and branch-and-bound methods. General global optimization is substantially more difficult than finding approximate first- or second-order stationary points.

# 05 · Additional resources

The following resources complement the original study roadmap. They are arranged broadly from classical numerical optimization to more specialized theoretical areas.

## 5.1 · Books, monographs and lecture notes

| Order | Resource | Main areas covered | Level |
|:--:|---|---|:--:|
| 01 | [Numerical Optimization — Nocedal & Wright](https://link.springer.com/book/10.1007/978-0-387-40065-5) | Classical numerical and nonlinear optimization | Intermediate |
| 02 | [Nonlinear Programming — Dimitri Bertsekas](https://www.athenasc.com/nonlinbook.html) | Constrained optimization, KKT conditions, duality | Advanced |
| 03 | [First-Order Methods in Optimization — Amir Beck](https://epubs.siam.org/doi/book/10.1137/1.9781611974997) | Proximal methods, composite optimization, convergence | Advanced |
| 04 | [Variational Analysis — Rockafellar & Wets](https://link.springer.com/book/10.1007/978-3-642-02431-3) | Variational analysis, generalized derivatives, optimality | Very advanced |
| 05 | [Convex Analysis and Monotone Operator Theory — Bauschke & Combettes](https://link.springer.com/book/10.1007/978-3-319-48311-5) | Monotone operators, proximal methods, convex analysis | Advanced |
| 06 | [Optimization Methods for Large-Scale Machine Learning — Bottou, Curtis & Nocedal](https://doi.org/10.1561/2200000051) | Stochastic optimization and large-scale learning | Advanced |
| 07 | [Optimization for Machine Learning — Sra, Nowozin & Wright](https://mitpress.mit.edu/9780262028692/optimization-for-machine-learning/) | Optimization algorithms and machine learning applications | Advanced |
| 08 | [University of Washington Optimization Lecture Notes](https://sites.math.washington.edu/~burke/crs/516-21/) | Variational analysis, KL theory, non-convex algorithms | Advanced |

## 5.2 · Papers and surveys

| Paper / resource | Venue / year | Main topic |
|---|---|---|
| [Optimization Methods for Large-Scale Machine Learning](https://doi.org/10.1561/2200000051) — Bottou, Curtis & Nocedal | *SIAM Review*, 2018 | Large-scale and stochastic optimization |
| [SPIDER: Near-Optimal Non-Convex Optimization via Stochastic Path-Integrated Differential Estimator](https://arxiv.org/abs/1807.01695) — Fang et al. | NeurIPS 2018 | Variance reduction |
| [A Proximal-Type Method for Nonsmooth and Nonconvex Constrained Minimization Problems](https://link.springer.com/article/10.1007/s10957-024-02597-x) | *Journal of Optimization Theory and Applications*, 2025 | Nonsmooth constrained optimization |
| [Variational Analysis of a Nonconvex and Nonsmooth Optimization Problem: An Introduction](https://arxiv.org/abs/2411.04317) — Royset | 2024 preprint; check current publication record | Variational analysis and nonsmooth non-convex optimization |

*Bibliographic note: Verify publication status, final title, author list, and venue against the publisher or proceedings record before citing these resources formally.*

# 06 · How to extend the original roadmap

Rather than treating every topic as equally important, organize your preparation into three levels.

| Level | Areas | Expected expertise |
|:--:|---|---|
| **I · Core foundations** | Linear algebra, multivariate calculus, matrix analysis, convex analysis, smooth optimization, non-convex stationary-point theory, convergence analysis | Understand standard non-convex optimization papers |
| **II · Advanced theory and algorithms** | Saddle-point escape, stochastic optimization, variance reduction, proximal methods, nonsmooth analysis, constrained optimization, KL theory, PL conditions, minimax optimization | Read and critically evaluate theoretical optimization papers |
| **III · Research specialization** | Global optimization, low-rank optimization, tensor optimization, bilevel optimization, adaptive methods, online optimization, random matrix theory, derivative-free optimization | Understand specialized research directions and develop new algorithms |

# 07 · Recommended final study roadmap

This is the recommended sequence for developing broad expertise in non-convex optimization.

| Priority | Study module | Topics to master | Main resources |
|:--:|---|---|---|
| 01 | **Mathematical foundations** | Linear algebra, matrix analysis, multivariate calculus, probability | MIT 18.06, MIT 18.02 |
| 02 | **Classical optimization** | GD, SGD, Newton, quasi-Newton, trust regions, line search | Nocedal & Wright |
| 03 | **Convex analysis** | Convexity, duality, smoothness, proximal operators | Boyd & Vandenberghe |
| 04 | **Smooth non-convex optimization** | Stationarity, descent lemma, convergence rates, strict saddles | Goodfellow et al., non-convex lecture notes |
| 05 | **Second-order optimization** | Hessian analysis, negative curvature, cubic regularization | Nesterov & Polyak |
| 06 | **Saddle-point theory** | Stable manifolds, strict-saddle property, PGD, NEON | Ge, Lee, Jin, Du |
| 07 | **Stochastic optimization** | SGD, stochastic approximation, sample complexity | Bottou et al., Fang et al. |
| 08 | **Nonsmooth optimization** | Subgradients, Clarke derivatives, weak convexity | Beck; Rockafellar & Wets |
| 09 | **Proximal optimization** | Proximal gradient, proximal point, Moreau envelope | Beck; Bauschke & Combettes |
| 10 | **Constrained optimization** | KKT, constraint qualifications, augmented Lagrangian | Bertsekas |
| 11 | **Convergence frameworks** | PL, KL, error bounds, gradient dominance | Washington optimization notes |
| 12 | **Minimax optimization** | GDA, extragradient, variational inequalities | Specialized minimax literature |
| 13 | **Structured non-convex optimization** | Matrix sensing, phase retrieval, tensor decomposition | Specialized research papers |
| 14 | **Global optimization** | Global optimality, branch and bound, relaxations | Global optimization literature |
| 15 | **Advanced algorithms** | Adaptive optimization, variance reduction, bilevel and derivative-free methods | Recent ICML, NeurIPS and mathematical optimization papers |

# 08 · Expertise milestones

Use these milestones to assess your progress rather than counting the number of books or papers you have read.

| Milestone | You should be able to... |
|---|---|
| **Mathematical understanding** | Derive first- and second-order optimality conditions independently |
| **Algorithmic understanding** | Explain how GD, SGD, Newton, proximal and trust-region methods work |
| **Convergence analysis** | Reproduce convergence proofs under stated assumptions |
| **Complexity analysis** | Derive iteration, gradient-oracle and sample-complexity bounds |
| **Geometric understanding** | Analyze Hessian spectra, negative curvature and optimization landscapes |
| **Stochastic understanding** | Analyze noisy gradients, variance reduction and probabilistic guarantees |
| **General theoretical understanding** | Work with constrained, nonsmooth, minimax and structured non-convex problems |
| **Research capability** | Identify limitations in existing assumptions, convergence guarantees and algorithmic designs |

---

## Final recommendation

The original roadmap is a good specialized foundation for saddle-point efficiency. To broaden it into a serious graduate-level study of non-convex optimization, make these five additions your highest priority:

1. **Variational analysis and nonsmooth optimization.**
2. **Stochastic non-convex optimization and variance reduction.**
3. **Proximal algorithms and composite optimization.**
4. **Constrained non-convex optimization and KKT theory.**
5. **PL/KL inequalities and modern convergence frameworks.**

Then study minimax optimization, structured non-convex problems, and global optimization as separate research branches.

You do not need to master every branch equally. Non-convex optimization is too broad for that. However, you should understand the mathematical language and fundamental guarantees of each branch, so that you can read a paper outside your immediate specialization without having to start learning optimization theory from scratch.

**The target:** Be able to read, derive, compare, and critically evaluate theoretical results across the broader non-convex optimization literature.


