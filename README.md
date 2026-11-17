# Papers on Saddle-Point Efficiency in Non-Convex Optimization

A bibliography of papers related to saddle-point identification,
avoidance, and efficient escape in non-convex optimization.

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
               No. Paper                                                                                                                         Authors        Venue                      Year
  ---------------- ----------------------------------------------------------------------------------------------------------------------------- -------------- -------------- ----------------
                 1 [Identifying and Attacking the Saddle Point Problem in High-Dimensional Non-Convex                                            Yann N.        NeurIPS                    2014
                   Optimization](https://proceedings.neurips.cc/paper/2014/hash/04192426585542c54b96ba14445be996-Abstract.html)                  Dauphin et al.                

                 2 [Escaping From Saddle Points -- Online Stochastic Gradient for Tensor                                                         Rong Ge,       COLT                       2015
                   Decomposition](https://proceedings.mlr.press/v40/Ge15.html)                                                                   Furong Huang,                 
                                                                                                                                                 Chi Jin, and                  
                                                                                                                                                 Yang Yuan                     

                 3 [Gradient Descent Only Converges to Minimizers](https://proceedings.mlr.press/v49/lee16.html)                                 Jason D. Lee,  COLT                       2016
                                                                                                                                                 Max                           
                                                                                                                                                 Simchowitz,                   
                                                                                                                                                 Michael I.                    
                                                                                                                                                 Jordan, and                   
                                                                                                                                                 Benjamin Recht                

                 4 [Cubic Regularization of Newton Method and Its Global Performance](https://doi.org/10.1007/s10107-006-0706-8)                 Yurii Nesterov Mathematical               2006
                                                                                                                                                 and Boris T.   Programming    
                                                                                                                                                 Polyak                        

                 5 [How to Escape Saddle Points Efficiently](https://proceedings.mlr.press/v70/jin17a.html)                                      Chi Jin, Rong  ICML                       2017
                                                                                                                                                 Ge, Praneeth                  
                                                                                                                                                 Netrapalli,                   
                                                                                                                                                 Sham M.                       
                                                                                                                                                 Kakade, and                   
                                                                                                                                                 Michael I.                    
                                                                                                                                                 Jordan                        

                 6 [Gradient Descent Can Take Exponential Time to Escape Saddle                                                                  Simon S. Du et NeurIPS                    2017
                   Points](https://papers.neurips.cc/paper_files/paper/2017/hash/f79921bbae40a577928b76d2fc3edc2a-Abstract.html)                 al.                           

                 7 [Escaping Saddles with Stochastic Gradients](https://proceedings.mlr.press/v80/daneshmand18a.html)                            Ashkan         ICML                       2018
                                                                                                                                                 Daneshmand,                   
                                                                                                                                                 Jonas Kohler,                 
                                                                                                                                                 Aurelien                      
                                                                                                                                                 Lucchi, and                   
                                                                                                                                                 Thomas Hofmann                

                 8 [First-order Stochastic Algorithms for Escaping From Saddle Points in Almost Linear                                           Pan Xu, Fred   NeurIPS                    2018
                   Time](https://proceedings.neurips.cc/paper_files/paper/2018/hash/217e342fc01668b10cb1188d40d3370e-Abstract.html)              Roosta, and                   
                                                                                                                                                 Michael W.                    
                                                                                                                                                 Mahoney                       

                 9 [NEON2: Finding Local Minima via First-Order                                                                                  Zeyuan         NeurIPS                    2018
                   Oracles](https://proceedings.neurips.cc/paper/2018/hash/d4b2aeb2453bdadaa45cbe9882ffefcf-Abstract.html)                       Allen-Zhu and                 
                                                                                                                                                 Yuanzhi Li                    

                10 [SSRGD: Simple Stochastic Recursive Gradient Descent for Escaping Saddle                                                      Zhize Li       NeurIPS                    2019
                   Points](https://proceedings.neurips.cc/paper_files/paper/2019/hash/addfa9b7e234254d26e9c7f2af1005cb-Abstract.html)                                          

                11 [Escaping Saddle Points in Constrained                                                                                        Aryan          NeurIPS                    2018
                   Optimization](https://papers.neurips.cc/paper_files/paper/2018/hash/069654d5ce089c13f642d19f09a3d1c0-Abstract.html)           Mokhtari,                     
                                                                                                                                                 Asuman                        
                                                                                                                                                 Ozdaglar, and                 
                                                                                                                                                 Ali Jadbabaie                 

                12 [Escaping from Saddle Points on Riemannian                                                                                    Hongyi Sun,    NeurIPS                    2019
                   Manifolds](https://proceedings.neurips.cc/paper/2019/hash/24e01830d213d75deb99c22b9cd91ddd-Abstract.html)                     Nicolas                       
                                                                                                                                                 Flammarion,                   
                                                                                                                                                 and Maryam                    
                                                                                                                                                 Fazel                         

                13 [Efficiently Escaping Saddle Points on                                                                                        Antonio        NeurIPS                    2019
                   Manifolds](https://proceedings.neurips.cc/paper/2019/hash/7486cef2522ee03547cfb970a404a874-Abstract.html)                     Criscitiello                  
                                                                                                                                                 and Nicolas                   
                                                                                                                                                 Boumal                        

                14 [Escape Saddle Points by a Simple Gradient-Descent Based                                                                      Guodong Zhang  NeurIPS                    2021
                   Algorithm](https://papers.nips.cc/paper_files/paper/2021/hash/47bd8ac1becf213f155a82244b4a696a-Abstract.html)                 and Q. Li                     

                15 [Escaping Saddle Points for Effective Generalization on Class-Imbalanced                                                      A. Rangwani et NeurIPS                    2022
                   Data](https://proceedings.neurips.cc/paper_files/paper/2022/hash/8f4d70db9ecec97b6723a86f1cd9cb4b-Abstract-Conference.html)   al.                           
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Suggested reading order

1.  Dauphin et al. --- NeurIPS 2014
2.  Ge et al. --- COLT 2015
3.  Lee et al. --- COLT 2016
4.  Jin et al. --- ICML 2017
5.  Du et al. --- NeurIPS 2017
6.  Daneshmand et al. --- ICML 2018
7.  Allen-Zhu and Li --- NeurIPS 2018
8.  Zhang and Li --- NeurIPS 2021

**Scope note:** This list focuses on non-convex minimization and
escaping undesirable stationary points. It does not cover the separate
minimax saddle-point literature (for example, optimization of
(`\min`{=tex}\_x `\max`{=tex}\_y f(x,y))). Verify bibliographic metadata
against the publisher proceedings before formal citation.
