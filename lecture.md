# Fall 2018 228A Lecture notes 

Recommended Textbook (you DO NOT need to buy them)

**[Lev]** R. J. LeVeque, Finite difference methods for ordinary and partial differential equations, steady state and time dependent problems, SIAM, 2007.

**[Ise]** A. Iserles, A first course in the numerical analysis of differential equations, Second Edition, Cambridge Univ. Press, 2009

**[Hai]** E. Hairer, S. P. Norsett and G. Wanner, Solving ordinary differential equations, Second Edition (2 vols.), Springer, 2008.

**[Saa]** Y. Saad, Iterative methods for sparse linear systems, SIAM, 2003

 Related materials

**[Gu]** M. Gu, Lecture notes Math 228A Fall 2014 [(web)](http://math.berkeley.edu/~mgu/MA228A)

**[Per]** P. Persson, Lecture notes Math 228A Fall 2013
[(web)](http://persson.berkeley.edu/228A)

**[Wil]** J. Wilkening, Lecture notes Math 228A Fall 2007 [(pdf)](https://math.berkeley.edu/~linlin/2015Fall_228A/wilkening_228A_notes.pdf)

## Lecture 1 (8/22)

General discussion on ordinary differential equations.

Introducing Julia. 

**Reading**: [LeV] 5.1, 5.2 [Hai] I.7,I.8

[Handout slides](https://github.com/lin-lin/2018Fall_228A/blob/master/others/228A_Note_general.pdf)


**Note**: v0.7 and v1.0 released on 8/8/2018 introduces many breaking
changes. So there is a bit learning curve if you are somewhat familiar
with previous versions of Julia before. I compiled a few things below I
noticed when migrating my old code snippets and notebooks used in the
lecture in this [pdf file](https://github.com/lin-lin/2018Fall_228A/blob/master/others/JuliaChange_v0.7.pdf).

Here is a notebook introducing some basic features of Julia.

[Notebook: Julia tutorial](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/Basics.ipynb), v0.7 compatible

Here are a few other online documents (some information may be
out-of-date).

[Learn X in Y minutes](https://learnxinyminutes.com/docs/julia/)

[The Julia Express](http://bogumilkaminski.pl/files/julia_express.pdf)

[Steven Johnson's Julia-intro](https://github.com/lin-lin/2018Fall_228A/blob/master/others/Julia-intro.pdf) 

[MATLAB–Python–Julia cheatsheet](https://cheatsheets.quantecon.org/)

[Julia manual](https://docs.julialang.org/en/stable/)


## Lecture 2 (8/24)

Lipschitz continuity; Euler's method

[Notebook: Forward Euler method](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/ForwardEuler.ipynb)

**Reading**: [Wil] pp 26-30, 41-44 


## Lecture 3 (8/27)

Convergence of Euler's method


[Lecture Note 1 (pdf)](lectures/228A_Lec1.pdf)

**Reading**: [LeV] 6.1-6.3


## Lecture 4 (8/29)

Adams-Bashforth method and Adams-Moulton method

**Reading**: [LeV] 5.3-5.6 [Ise] 1.2-1.4


## Lecture 5 (8/31)

Convergence of trapezoidal rule; Fixed point problem and fixed point iteration

**Reading**: [Ise] 2.1; [Hai] III.1

[Tobias von Petersdorff's notes on contraction mapping (with some numerics)](https://github.com/lin-lin/2018Fall_228A/blob/master/others/ContractionMapping.pdf)

## Lecture 6 (9/5)

Consistency of linear multistep method.  

[Lecture Note 2 (pdf)](lectures/228A_Lec2.pdf)

**Reading**: [Ise] 2.2; 6.1-6.2

## Lecture 7 (9/7)


[Notebook: Zero stability of LMM](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/LMM.ipynb)

Adaptive time stepping. Zero stability of LMM

**Reading**: [LeV] 6.1-6.4; [Hai] III.3-4

## Lecture 8 (9/10)

[Lecture Note 3 (pdf)](lectures/228A_Lec3.pdf)

[Details of the proof of general convergence theory of LMM (pdf)](lectures/LMMConvergence.pdf)

Zero stability of LMM; Convergence of general LMM

**Reading**: [Wil] pp 61-77


## Lecture 9 (9/12)

Runge-Kutta method. 

**Reading**: [Ise] 3.1-3.3. [Hai] II.2


## Lecture 10 (9/14)

Consistency of Runge-Kutta method. Taylor expansion.

**Reading**: [Hai] II.2

## Lecture 11 (9/17)


Consistency of Runge-Kutta method. Diagram method.

**Reading**: [Wil] pp 95-107

[Lecture Note 4 (pdf)](lectures/228A_Lec4.pdf)

## Lecture 12 (9/19)

Zero stability of Runge-Kutta method. 

**Reading**: [Hai] II.3 


## Lecture 13 (9/21)

Collocation method. Consistency

[Notebook: Gauss quadrature](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/GaussQuadrature.ipynb)

**Reading**: [Ise] 3.1-3.4, [Hai] I.14

## Lecture 14 (9/24)

Gauss quadrature. Lanczos method.

**Reading**: 

[Lecture Note 5 (pdf)](lectures/228A_Lec5.pdf)

[D. Levy's notes on Gauss quadrature](others/GaussianQuad.pdf)

[G. Golub, G. Meurant, Matrices, moments and quadrature, (1993)](others/GM93.pdf)

[G. Golub, J.H. Welsch, Calculation of Gauss Quadrature Rules, (1968) 221–230](others/GM68.pdf)


## Lecture 15 (9/26)

Embedded Runge-Kutta method. Absolute stability

**Reading**: [LeV] 7.1-7.4 


## Lecture 16 (9/28)

Absolute stability

**Reading**: [LeV] 7.5-7.7. [Ise] 4.2-4.4

[Lecture Note 6 (pdf)](lectures/228A_Lec6.pdf)

[Notebook: Stability region](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/StabilityRegion.ipynb)

## Lecture 17 (10/1)

Stiff equations

**Reading**: [LeV] 8.1-8.3. [Ise] 4.1. [Hai] IV.1. 

[Notebook: Stiff equations](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/StiffEquation.ipynb)

## Lecture 18 (10/3)

Stiff equations

**Reading**: [LeV] 8.1-8.3. [Ise] 4.1. [Hai] IV.1. 

[Lecture Note 7 (pdf)](lectures/228A_Lec7.pdf)


## Lecture 19 (10/5)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

[Notebook: Symplectic integrator](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/Symplectic.ipynb)

[Lecture Note 8 (pdf)](lectures/228A_Lec8.pdf)

## Lecture 20 (10/8)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

Some excellent reading materials given by Ernst Hairer:

https://www.unige.ch/~hairer/poly_geoint/week1.pdf

https://www.unige.ch/~hairer/poly_geoint/week2.pdf

https://www.unige.ch/~hairer/poly_geoint/week3.pdf

## Lecture 21 (10/10)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

Recent work on the interesting connection between optimization and symplectic
integration:

M. Betancourt, M.I. Jordan, A.C. Wilson, On Symplectic Optimization, (2018) http://arxiv.org/abs/1802.03653.

## Lecture 22 (10/12)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

[Lecture Note 9 (pdf)](lectures/228A_Lec9.pdf)

## Lecture 23 (10/15)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

## Lecture 24 (10/17)

Exponential time differencing method.

**Reading**: [LeV] 11.6.

[Notebook: Exponential time differencing](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/ExponentialTimeDifferencing.ipynb)


S.M. Cox, P.C. Matthews, Exponential Time Differencing for Stiff Systems, J. Comput. Phys. 176 (2002) 430–455. 

A.-K. Kassam, L.N. Trefethen, Fourth-Order Time-Stepping for Stiff PDEs, SIAM J. Sci. Comput. 26 (2005) 1214–1233.

C. Moler, C. Van Loan, Nineteen Dubious Ways to Compute the Exponential of a Matrix, Twenty-Five Years Later, SIAM Rev. 45 (2003) 3–49.

## Lecture 25 (10/19)

Exponential time differencing method.

**Reading**: [LeV] 11.6.

[Notebook: Matrix exponentials](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/Matrix_exponential.ipynb)

[Lecture Note 10 (pdf)](lectures/228A_Lec10.pdf)

## Lecture 26 (10/22)

Nonlinear equations. 

**Reading**: [Ise] 7.1-7.3  

[Lecture Note 11 (pdf)](lectures/228A_Lec11.pdf)

[Notebook: Nonlinear equations](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/NonlinearEquations.ipynb)


## Lecture 27 (10/24)

Nonlinear equations. 

**Reading**: [Ise] 7.1-7.3  


## Lecture 28 (10/26)

Krylov methods 

**Reading**: 


[Lev]4.1-4.5 [Saa] 6.5-6.12

[Lecture Note 12 (pdf)](lectures/228A_Lec12.pdf)

[Notebook: Krylov 2D example](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/Krylov2D.ipynb)

## Lecture 29 (10/29)

Krylov methods

**Reading**: 

[Lev]4.1-4.5 [Saa] 6.5-6.12

[Notebook: Krylov Laplace equation](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/KrylovLaplace.ipynb)


## Lecture 30 (10/31)


Krylov methods

**Reading**: 

[Lev]4.1-4.5 [Saa] 6.5-6.12


## Lecture 31 (11/2)

Krylov methods

**Reading**: 

[Lev]4.1-4.5 [Saa] 6.5-6.12

[Wen Shen's notes on convergence of CG (pdf)](others/CG_Chebyshev.pdf) (in particular, detailed derivation of the $\sqrt{\kappa}$ convergence using Chebyshev polynomial) 


## Lecture 32 (11/5)

Krylov methods

**Reading**: 

[Lev]4.1-4.5 [Saa] 6.5-6.12

[Notebook: Krylov Helmholtz equation](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/KrylovHelmholtz.ipynb)


## Lecture 33 (11/7)

Krylov methods

**Reading**: 
[Saa] 6.5-6.12

[Lecture Note 13 (pdf)](lectures/228A_Lec13.pdf)



## Lecture 34 (11/9)

Sparse direct methods

**Reading**: 
[Ise] 10.1-10.2

[Notebook: Sparse direct methods](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/SparseDirect.ipynb)
 


## Lecture 35 (11/14)

Sparse direct methods

**Reading**: 
[Ise] 10.1-10.2

[Lecture Note 14 (pdf)](lectures/228A_Lec14.pdf)

## Lecture 36 (11/26)

Sparse direct methods


## Lecture 37 (11/28)

Spectral methods

**Reading**: 
[Notebook: Spectral methods](http://nbviewer.jupyter.org/github/lin-lin/2018Fall_228A/blob/master/notebooks/SpectralMethod.ipynb)

[Lecture Note 15 (pdf)](lectures/228A_Lec15.pdf)

L.N. Trefethen, Is Gauss quadrature better than Clenshaw-Curtis?, SIAM Rev. 50 (2008) 67--87. 
