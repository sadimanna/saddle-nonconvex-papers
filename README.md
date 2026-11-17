## 01 · Foundations

| # | Paper | Authors | Venue | Year |
|:--:|---|---|:--:|:--:|
| 01 | [Identifying and Attacking the Saddle Point Problem in High-Dimensional Non-Convex Optimization](https://proceedings.neurips.cc/paper/2014/hash/04192426585542c54b96ba14445be996-Abstract.html) | Dauphin et al. | **NeurIPS** | 2014 |
| 02 | [Escaping From Saddle Points – Online Stochastic Gradient for Tensor Decomposition](https://proceedings.mlr.press/v40/Ge15.html) | Ge, Huang, Jin & Yuan | **COLT** | 2015 |
| 03 | [Gradient Descent Only Converges to Minimizers](https://proceedings.mlr.press/v49/lee16.html) | Lee, Simchowitz, Jordan & Recht | **COLT** | 2016 |
| 04 | [Cubic Regularization of Newton Method and Its Global Performance](https://doi.org/10.1007/s10107-006-0706-8) | Nesterov & Polyak | *Mathematical Programming* | 2006 |

## 02 · Efficient saddle-point escape

| # | Paper | Authors | Venue | Year |
|:--:|---|---|:--:|:--:|
| 05 | [How to Escape Saddle Points Efficiently](https://proceedings.mlr.press/v70/jin17a.html) | Jin, Ge, Netrapalli, Kakade & Jordan | **ICML** | 2017 |
| 06 | [Gradient Descent Can Take Exponential Time to Escape Saddle Points](https://papers.neurips.cc/paper_files/paper/2017/hash/f79921bbae40a577928b76d2fc3edc2a-Abstract.html) | Du et al. | **NeurIPS** | 2017 |
| 07 | [Escaping Saddles with Stochastic Gradients](https://proceedings.mlr.press/v80/daneshmand18a.html) | Daneshmand, Kohler, Lucchi & Hofmann | **ICML** | 2018 |
| 08 | [First-order Stochastic Algorithms for Escaping From Saddle Points in Almost Linear Time](https://proceedings.neurips.cc/paper_files/paper/2018/hash/217e342fc01668b10cb1188d40d3370e-Abstract.html) | Xu, Jin & Yang | **NeurIPS** | 2018 |
| 09 | [NEON2: Finding Local Minima via First-Order Oracles](https://proceedings.neurips.cc/paper/2018/hash/d4b2aeb2453bdadaa45cbe9882ffefcf-Abstract.html) | Allen-Zhu & Li | **NeurIPS** | 2018 |
| 10 | [SSRGD: Simple Stochastic Recursive Gradient Descent for Escaping Saddle Points](https://proceedings.neurips.cc/paper_files/paper/2019/hash/addfa9b7e234254d26e9c7f2af1005cb-Abstract.html) | Li | **NeurIPS** | 2019 |

## 03 · Constrained and manifold optimization

| # | Paper | Authors | Venue | Year |
|:--:|---|---|:--:|:--:|
| 11 | [Escaping Saddle Points in Constrained Optimization](https://papers.neurips.cc/paper_files/paper/2018/hash/069654d5ce089c13f642d19f09a3d1c0-Abstract.html) | Mokhtari, Ozdaglar & Jadbabaie | **NeurIPS** | 2018 |
| 12 | [Escaping from Saddle Points on Riemannian Manifolds](https://proceedings.neurips.cc/paper/2019/hash/24e01830d213d75deb99c22b9cd91ddd-Abstract.html) | Sun, Flammarion & Fazel | **NeurIPS** | 2019 |
| 13 | [Efficiently Escaping Saddle Points on Manifolds](https://proceedings.neurips.cc/paper/2019/hash/7486cef2522ee03547cfb970a404a874-Abstract.html) | Criscitiello & Boumal | **NeurIPS** | 2019 |
| 14 | [Escape Saddle Points by a Simple Gradient-Descent Based Algorithm](https://papers.nips.cc/paper_files/paper/2021/hash/47bd8ac1becf213f155a82244b4a696a-Abstract.html) | Zhang & Li | **NeurIPS** | 2021 |

## 04 · Deep learning and generalization

| # | Paper | Authors | Venue | Year |
|:--:|---|---|:--:|:--:|
| 15 | [Escaping Saddle Points for Effective Generalization on Class-Imbalanced Data](https://proceedings.neurips.cc/paper_files/paper/2022/hash/8f4d70db9ecec97b6723a86f1cd9cb4b-Abstract-Conference.html) | Rangwani et al. | **NeurIPS** | 2022 |

---

## ✧ Suggested reading path

| Step | Read | What to focus on |
|:--:|---|---|
| 01 | Dauphin et al. · NeurIPS 2014 | Hessian spectrum, negative curvature and saddle-free Newton |
| 02 | Ge et al. · COLT 2015 | Strict-saddle property |
| 03 | Lee et al. · COLT 2016 | Stable-manifold argument and almost-sure saddle avoidance |
| 04 | Jin et al. · ICML 2017 | Perturbed gradient descent and escape efficiency |
| 05 | Du et al. · NeurIPS 2017 | Why ordinary gradient descent can escape slowly |
| 06 | Daneshmand et al. · ICML 2018 | Stochastic noise as a source of negative-curvature exploration |
| 07 | Allen-Zhu & Li · NeurIPS 2018 | First-order methods for finding negative-curvature directions |
| 08 | Zhang & Li · NeurIPS 2021 | Gradient-based saddle escape |

> **Scope.** This bibliography concerns saddle points in non-convex minimization and methods for finding approximate second-order stationary points or local minima. It does not cover the distinct minimax setting \(\min_x \max_y f(x,y)\).
