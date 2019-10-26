# Fall 2019 228A Lecture notes 

## General information

Lin Lin. https://math.berkeley.edu/~linlin/

Office Hours: Tue 3:30PM-4:30PM Evans 1083 



**Recommended Textbook (you DO NOT need to buy them, electronic versions available for all books via Berkeley library access)**

**[Lev]** R. J. LeVeque, Finite difference methods for ordinary and partial differential equations, steady state and time dependent problems, SIAM, 2007. [[Link for electronic version (need Berkeley library access)](http://oskicat.berkeley.edu/search~S1?/XFinite+difference+methods+for+ordinary+and+partial+differential+equations&searchscope=1&SORT=DZ/XFinite+difference+methods+for+ordinary+and+partial+differential+equations&searchscope=1&SORT=DZ&extended=0&SUBKEY=Finite+difference+methods+for+ordinary+and+partial+differential+equations/1%2C42%2C42%2CB/frameset&FF=XFinite+difference+methods+for+ordinary+and+partial+differential+equations&searchscope=1&SORT=DZ&2%2C2%2C)]

**[Ise]** A. Iserles, A first course in the numerical analysis of differential equations, Second Edition, Cambridge Univ. Press, 2009 [[Link for electronic version (need Berkeley library access)](http://oskicat.berkeley.edu/search~S1?/Xa+first+course+in+the+numerical+analysis+of+differential+equations&searchscope=1&SORT=D/Xa+first+course+in+the+numerical+analysis+of+differential+equations&searchscope=1&SORT=D&SUBKEY=a+first+course+in+the+numerical+analysis+of+differential+equations/1%2C39%2C39%2CB/frameset&FF=Xa+first+course+in+the+numerical+analysis+of+differential+equations&searchscope=1&SORT=D&2%2C2%2C)]

**[Hai]** E. Hairer, S. P. Norsett and G. Wanner, Solving ordinary differential equations, Second Edition (2 vols.), Springer, 2008. [[Link for electronic version (need Berkeley library access)](http://oskicat.berkeley.edu/search~S1?/XSolving+ordinary+differential+equations&searchscope=1&SORT=DZ/XSolving+ordinary+differential+equations&searchscope=1&SORT=DZ&SUBKEY=Solving+ordinary+differential+equations/1%2C211%2C211%2CB/frameset&FF=XSolving+ordinary+differential+equations&searchscope=1&SORT=DZ&8%2C8%2C)]

**[Saa]** Y. Saad, Iterative methods for sparse linear systems, SIAM, 2003 [[Link for electronic version (need Berkeley library access)](http://oskicat.berkeley.edu/search~S1?/X+Iterative+methods+for+sparse+linear+systems&searchscope=1&SORT=DZ/X+Iterative+methods+for+sparse+linear+systems&searchscope=1&SORT=DZ&extended=0&SUBKEY=+Iterative+methods+for+sparse+linear+systems/1%2C89%2C89%2CB/frameset&FF=X+Iterative+methods+for+sparse+linear+systems&searchscope=1&SORT=DZ&3%2C3%2C)]

 **Related materials**

**[Gu]** M. Gu, Lecture notes Math 228A Fall 2014 [(web)](http://math.berkeley.edu/~mgu/MA228A)

**[Per]** P. Persson, Lecture notes Math 228A Fall 2013
[(web)](http://persson.berkeley.edu/228A)

**[Wil]** J. Wilkening, Lecture notes Math 228A Fall 2007 [(pdf)](https://math.berkeley.edu/~linlin/2015Fall_228A/wilkening_228A_notes.pdf)

[General information of the class (pdf)](lectures/228A_Note_general.pdf)

## Lecture 1 (8/29)

General discussion on ordinary differential equations.

Introducing Julia. 

[Lecture note 1 (pdf)](lectures/Lec1.pdf)

**Reading**: [LeV] 5.1, 5.2 [Hai] I.7,I.8



<span style="color:red">IMPORTANT</span>: In this class, everyone who chooses to use Julia **MUST use Julia v1.2**. (This would greatly simplify the unnecessary work for the GSI. Homework submission with any other version of Julia are NOT accepted). Other programming languages such as `python` and `MATLAB` are also accepted. Please discuss with the GSI about the acceptable versions of these languages.



### How to install Julia

1. Download the binary file (**version 1.2, used in this class**)
   
   (Linux): https://julialang-s3.julialang.org/bin/linux/x64/1.2/julia-1.2.0-linux-x86_64.tar.gz
   

(Windows) https://julialang-s3.julialang.org/bin/winnt/x64/1.2/julia-1.2.0-win64.exe

   (Mac) https://julialang-s3.julialang.org/bin/mac/x64/1.2/julia-1.2.0-mac64.dmg

2. Untar / install

3. Run (e.g. Linux)

   ``` bash
   linlin@forum:~/.julia/environments$ julia
                  _
      _       _ _(_)_     |  Documentation: https://docs.julialang.org
     (_)     | (_) (_)    |
      _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
     | | | | | | |/ _` |  |
     | | |_| | | | (_| |  |  Version 1.2.0 (2019-08-20)
    _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
   |__/                   |
   
   julia>
   ```

   

### How to upgrade your local version of Julia (from 0.7+)

From version 0.7+, the package management system has changed.

```bash
linlin@forum:~$ cd ~/.julia/environments/
linlin@forum:~/.julia/environments$ ls
v0.7  v1.1
linlin@forum:~/.julia/environments$ cp -r v0.7 v1.2
linlin@forum:~/.julia/environments$ julia
               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.2.0 (2019-08-20)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia>
```

Now press ] to enter the package mode

```bash
(v1.2) pkg> update; precompile
  Updating registry at `~/.julia/registries/General`
  Updating git-repo `https://github.com/JuliaRegistries/General.git`
  Updating git-repo `https://github.com/JuliaPy/Conda.jl.git`
  Updating git-repo `https://github.com/JuliaLinearAlgebra/GenericLinearAlgebra.jl`
  Updating git-repo `https://github.com/JuliaPy/PyCall.jl.git`
  Updating git-repo `https://github.com/JuliaPy/PyPlot.jl.git`
 Resolving package versions...
 Installed Distances ────── v0.8.2
 Installed NLSolversBase ── v7.4.1
 Installed IJulia ───────── v1.20.0
 Installed MbedTLS ──────── v0.7.0
 Installed BandedMatrices ─ v0.10.1
 Installed DataFrames ───── v0.19.3
 Installed OrdinaryDiffEq ─ v5.15.0
...
```

Now your previously installed package should be ready to be used. For example, try `Arpack` (solving sparse eigenvalue problems)

```julia
using Arpack
using LinearAlgebra
A = Diagonal(1:4);
λ, ϕ = eigs(A, nev = 2);
display(λ)

2-element Array{Float64,1}:
 4.0
 3.0
```



Once you have installed Julia, [get started from here with the Julia documentation](https://docs.julialang.org/en/v1/manual/getting-started/) .



### Notebook mode of julia

First, you need to install the `IJulia` package from Julia.

Then, download the [Jupyter](https://jupyter.org/install) software. The classic Jupyter Notebook comes together with the `Anaconda` python distribution and is perhaps the easiest. In fact, `Anaconda` installs both Jupyter Notebook and Jupyter Lab:

![](lectures/assets/AnacondaNavigator.png)

Launch either JupyterLab or Jupyter Notebook, and you should be able to create a new IJulia notebook, with the version matching the version of Julia for which `IJulia` is installed. 

Another way to get access to the Jupyter lab is to use your browser, the default address http://localhost:xxxx/tree leads to the classic the notebook, and http://localhost:xxxx/lab leads to the Jupyter Lab.

You might also find it handy to have the cheat sheets for 

- [keyboard shortcuts for JupyterLab](https://raw.githubusercontent.com/Jakeler/jupyter-shortcuts/master/outputs/Shortcuts.png)
- [keyboard shortcuts for Jupyter Notebook](https://www.cheatography.com/weidadeyue/cheat-sheets/jupyter-notebook/)



### Console mode of julia

- Running a script

  ```julia
  include(“name.jl”)
  ```

- Different modes

  - **Command** mode
  - **Help** mode (type “?”)
  - **Shell** mode (type “;”)
  - **Package** mode (type “]”)

- Package mode:

  - Add a package: `]add packagename`
  - Update the package list: `]update` 
  - **Update and precompile** (otherwise the precompilation process will occur when you execute `using package` for the first time) :
     `]update; precompile`
  - Build a package (some packages need to be built before used): `]build packagename` 



### Julia packages used in this course (this list will keep updating throughout the course)

- `Plots/PyPlot/Gadfly`: Plotting: 

  Useful link https://julialang.org/downloads/plotting.html

- `IJulia`: Notebook (now in the Jupyter notebook)

- `DifferentialEquations`: See everything we will talk about in this class about ODEs. [http://docs.juliadiffeq.org](http://docs.juliadiffeq.org/)

- `LinearAlgebra`: Nearly all basic linear algebra related packages

- `SpecialFunctions`: Special functions such as Bessel, Hankel, Airy, error,etc.

- `Flux/DiffEqFlux`: Machine learning related packages





### If you have used Julia v0.6 (or earlier versions) but not v0.7+

First of all,  Julia v0.7 (released 08/2018, equivalent to v1.0 other than additional warning messages helping the transition) introduced many breaking changes. This will not be a problem if you start afresh, but may require you to adapt your old code to the new version. Here are a few tips that might help you with the transition.

- Always only refer to the latest manual

- The package mode has been changed. `Pkg.add("package name")` no longer works.  The new way is to type `]` which gives `|pkg>`

- `@printf` is deprecated.  Need to load the package `using Printf`

- Many linear algebra routines were moved from `Base` to `LinearAlgebra` package.

- `eye(N)` for identity matrix is deprecated.  Now it is `Matrix(1.0I,N,N)`.

- `diagm(vec,n)` to create a matrix with `vec` on its n-th sub-diagonal (if n=0 it is the diagonal) is      deprecated.  Now it is `diagm(n=>vec)`.

- Matrix functions such as `expm` and `logm` are deprecated. Now they can be invoked by `exp` and `log` directly. Note that this is very different behavior from `MATLAB`.

- Diagonalization routine `eig` is replaced by `eigen`

- `qr` does not return the QR factors `(q,r)`, but a structure.  So if `F=qr(A)` is called, `F.Q` and `F.R` are needed to retrieve the Q and R factors.

- `full(A)` is deprecated. Now it becomes `Matrix(A)`.

- Special functions such as `erf` are now in the `SpecialFunctions` package.

- In a local scope, such as a `for`-loop, global variables are only inherited for reading but not for      writing. For example

  ``` julia
  z = 1.0
  for i = 1 : 3
      # Only read the values of the global variable z
      println(z)
  end
  
  # output
  1.0
  1.0
  1.0
  ```

  However,

  ``` julia
  z = 1.0
  for i = 1 : 3
      # Also write to the global variable z
      z = z + i
  end
  
  # output 
  ERROR: UndefVarError: z not defined
  ```

  There are two ways getting around this problem.

  The first is to put an explicit `global` in front of the assignment

  ``` julia
  z = 1.0
  for i = 1 : 3
      # Also write to the global variable z
      global z = z + i
  end
  println(z)
  
  # output 
  7.0
  ```

  The second way is to wrap everything in a "global local scope" using a `let` block, or any other function or subroutine. Then the global variable becomes a local variable

  ``` julia
  z = 1.0
  let
      z = 1.0
      for i = 1 : 3
          z = z + i
      end
      println(z)
  end
  
  # output 
  7.0
  ```

  **Note (8/10/2019):** It appears that in the latest version of JupyterLab / Jupyter Notebook, **this problem is fixed**, i.e. you **can** modify the values of global variables in the **Notebook environment (only)**. I strongly agree with this modification, since it is rather annoying to put `let` blocks in a notebook everywhere which messes up with the indent. I guess the rationale for the very strict scoping rule is to discourage users from using global variables when writing production level codes (which I agree). The scope issue apparently went through [a hot debate](https://discourse.julialang.org/t/another-possible-solution-to-the-global-scope-debacle/15894), but I do not know whether a definitive answer has been reached at this point.



### Other materials

Here is a notebook introducing some basic features of Julia.

[Notebook: Julia tutorial](notebooks/Basics.ipynb) Last update: 8/28/2019

Here are a few other online documents.

[Learn X in Y minutes](https://learnxinyminutes.com/docs/julia/)

[The Julia Express (pdf)](http://bogumilkaminski.pl/files/julia_express.pdf)

[MATLAB–Python–Julia cheatsheet](https://cheatsheets.quantecon.org/)

[Julia user manual](https://docs.julialang.org/)



## Lecture 2 (9/3)

### DifferentialEquations.jl

The [DifferentialEquations](http://docs.juliadiffeq.org/) package can be a useful tool in this class for checking the accuracy of your solution, learning more advanced solvers, and comparing for performance of different solvers.

It has a nicely written [tutorial](http://docs.juliadiffeq.org/latest/tutorials/ode_example.html) section, and I also recommend this [Youtube video](https://www.youtube.com/watch?v=KPEqYtEd-zY&feature=youtu.be) given by the developer [Chris Rackauckas](http://chrisrackauckas.com/) on the basics of numerical ODEs, together with some useful practical programming skills (such as avoiding the allocation of large arrays, broadcast etc) that will not be covered in detail in this class. There is also an [accompanying notebook](http://tutorials.juliadiffeq.org/html/introduction/01-ode_introduction.html).

[Notebook: Overview of integrators using DifferentialEquations.jl ](notebooks/Overview.ipynb) 



Lipschitz continuity; Euler's method

[Lecture note 2 (pdf)](lectures/Lec2.pdf)

[Notebook: Forward Euler method](notebooks/ForwardEuler.ipynb)

**Reading**: [Wil] pp 26-30, 41-44 

[![](http://img.youtube.com/vi/v-pbGAts_Fg/0.jpg)](https://www.youtube.com/watch?v=v-pbGAts_Fg)

Why we should study Euler's method: Euler's Method scene in Hidden Figures

## Lecture 3 (9/5)

[Lecture note 3 (pdf)](lectures/Lec3.pdf)

Convergence of Euler's method

Second order Taylor method

**Reading**: [LeV] 6.1-6.3, [LeV] 5.3-5.6 [Ise] 1.2-1.4



## Lecture 4 (9/10)

Adams-Bashforth method and Adams-Moulton method

Convergence of trapezoidal rule; Fixed point problem and fixed point iteration

[Lecture note 4 (pdf)](lectures/Lec4.pdf)

**Reading**: [Ise] 2.1 (Adams method); [Hai] III.1 (Multistep method)

[Tobias von Petersdorff's notes on contraction mapping (with some numerics)](others/ContractionMapping.pdf)

## Lecture 5 (9/12)

Consistency of linear multistep method.  Adaptive time stepping. 

[Lecture note 5 (pdf)](lectures/Lec5.pdf)

**Reading**: [Ise] 2.2 (Consistency of AB/AM) ; 6.1-6.2 (Milne device)

## Lecture 6 (9/17)

[Notebook: Zero stability of LMM](notebooks/LMM.ipynb)

[Details of the proof of general convergence theory of LMM (pdf)](lectures/LMMConvergence.pdf)

[Lecture note 6 (pdf)](lectures/Lec6.pdf)

Zero stability of LMM; Convergence of general LMM

**Reading**: [LeV] 6.1-6.4 (Zero stability); [Hai] III.3-4 (Zero stability, first Dahlquist theorem); [Wil] pp 61-77 (Convergence of LMM)



## Lecture 7 (9/19)

[Lecture note 7 (pdf)](lectures/Lec7.pdf)

Runge-Kutta method. Consistency of Runge-Kutta method. Taylor expansion.

**Reading**: [Ise] 3.1-3.3. [Hai] II.2 (Order Conditions for Runge-Kutta)



## Lecture 8 (9/24)

[Handout for order condition of Runge-Kutta method (pdf)](lectures/RKOrderCondition.pdf)

[Notebook: Check the order condition of GL2](notebooks/RKOrderCondition.ipynb)

Consistency of Runge-Kutta method. Diagram method. 

**Reading**: [Wil] pp 95-107. 

## Lecture 9 (9/26)

Embedded Runge-Kutta method. Zero stability of Runge-Kutta method. 

**Reading**: [Ise] 6.3 (Embedded Runge-Kutta). [Hai] II.3 (Convergence of Runge-Kutta)

## Lecture 10 (10/1)

Absolute stability, LMM

[Notebook: Stability region](notebooks/StabilityRegion.ipynb)

[Lecture note 10 (pdf)](lectures/Lec10.pdf)

**Reading**: [LeV] 7.1-7.4 (Absolute stability)

## Lecture 11 (10/3)

Absolute stability, Runge-Kutta method; Stiff equations

[Notebook: Stiff equations](notebooks/StiffEquation.ipynb)

[Lecture note 11 (pdf)](lectures/Lec11.pdf)

**Reading**: [LeV] 7.5-7.7 (Plotting region of absolute stability); [Ise] 4.1-4.4 (Stiff equations).



## Lecture 12 (10/8)

Stiff equations

[Lecture note 12 (pdf)](lectures/Lec12.pdf)

**Reading**: [LeV] 8.1-8.3. (Stiff equations). [Hai] IV.1. 

## Lecture 13 (10/10)

Canceled due to PG&E shutdown

## Lecture 14 (10/15)

Nonlinear equations. 

**Reading**: [Ise] 7.1-7.3 (Solving nonlinear algebraic systems)

[Notebook: Nonlinear equations](notebooks/NonlinearEquations.ipynb)

## Lecture 15 (10/17)

Nonlinear equations. 

## Lecture 16 (10/22)

Hamiltonian system. 

**Reading**:  [Ise] 5.4.

[Notebook: Symplectic integrator](notebooks/Symplectic.ipynb)

[Lecture Note 16 (pdf)](lectures/Lec16.pdf)

Some excellent reading materials given by Ernst Hairer:

https://www.unige.ch/~hairer/poly_geoint/week1.pdf

https://www.unige.ch/~hairer/poly_geoint/week2.pdf

https://www.unige.ch/~hairer/poly_geoint/week3.pdf

## Lecture 17 (10/24)

Hamiltonian system. 

(Note is also in Lecture Note 16)