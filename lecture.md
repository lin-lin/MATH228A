# Fall 2019 228A Lecture notes 

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

## Lecture 1 (8/29)

General discussion on ordinary differential equations.

Introducing Julia. 

**Reading**: [LeV] 5.1, 5.2 [Hai] I.7,I.8

[Handout slides](others/228A_Note_general.pdf)

**Note**: v0.7 and v1.0 released on 8/8/2018 introduces many breaking changes. So there is a bit learning curve if you are somewhat familiar with previous versions of Julia before. I compiled a few things below I noticed when migrating my old code snippets and notebooks used in the lecture in this [pdf file](others/JuliaChange_v0.7.pdf).

Here is a notebook introducing some basic features of Julia.

[Notebook: Julia tutorial](notebooks/Basics.ipynb), v0.7 compatible

Here are a few other online documents (some information may be out-of-date).

[Learn X in Y minutes](https://learnxinyminutes.com/docs/julia/)

[The Julia Express](http://bogumilkaminski.pl/files/julia_express.pdf)

[Steven Johnson's Julia-intro](Julia-intro.pdf) 

[MATLAB–Python–Julia cheatsheet](https://cheatsheets.quantecon.org/)

[Julia manual](https://docs.julialang.org/en/stable/)

### How to install Julia

1. Download the binary file (**version 1.1.1, used in this class**)
   (Linux): https://julialang-s3.julialang.org/bin/linux/x64/1.1/julia-1.1.1-linux-x86_64.tar.gz
   (Windows) https://julialang-s3.julialang.org/bin/winnt/x64/1.1/julia-1.1.1-win64.exe
   (Mac) https://julialang-s3.julialang.org/bin/mac/x64/1.1/julia-1.1.1-mac64.dmg

2. Untar / install

3. Run (e.g. Linux)

   ``` bash
   linlin@forum:~/Software/julia-1.1.1/bin$ julia
                  _
      _       _ _(_)_     |  Documentation: https://docs.julialang.org
     (_)     | (_) (_)    |
      _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
     | | | | | | |/ _` |  |
     | | |_| | | | (_| |  |  Version 1.1.1 (2019-05-16)
    _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
   |__/                   |
   
   julia>
   ```

   

### Commonly used Julia packages (also in this course, will be updated)

- Plotting: PyPlot/Gadfly

- Notebook (now in the Jupyter notebook): IJulia

  

### How to upgrade your local version of Julia (from 0.7+)

From version 0.7, the package management system has changed.

```bash
linlin@forum:~$ cd ~/.julia/environments/
linlin@forum:~/.julia/environments$ ls
v0.7  v1.0  
linlin@forum:~/.julia/environments$ cp -r v0.7 v1.1
linlin@forum:~/.julia/environments$ julia
               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.1.1 (2019-05-16)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia>
```

Now press ] to enter the package mode

``` bash
(v1.1) pkg> update
  Updating registry at `~/.julia/registries/General`
  Updating git-repo `https://github.com/JuliaRegistries/General.git`
  Updating git-repo `https://github.com/JuliaPy/Conda.jl.git`
  Updating git-repo `https://github.com/JuliaLinearAlgebra/GenericLinearAlgebra.jl`
  Updating git-repo `https://github.com/JuliaPy/PyCall.jl.git`
  Updating git-repo `https://github.com/JuliaPy/PyPlot.jl.git`
 Resolving package versions...
  Updating `~/.julia/environments/v1.1/Project.toml`
  [7d9fca2a] ↑ Arpack v0.3.0 ⇒ v0.3.1
  [8f4d0f93] ↑ Conda v1.1.1+ #master (https://github.com/JuliaPy/Conda.jl.git) ⇒ v1.3.0 #master (https://github.com/JuliaPy/Conda.jl.git)
  [7a1cc6ca] ↑ FFTW v0.2.4 ⇒ v0.3.0
  [14197337] ↑ GenericLinearAlgebra v0.0.0 #master (https://github.com/JuliaLinearAlgebra/GenericLinearAlgebra.jl) ⇒ v0.1.0+ #master (https://github.com/JuliaLinearAlgebra/GenericLinearAlgebra.jl)
  [7073ff75] ↑ IJulia v1.14.1 ⇒ v1.19.0
  [42fd0dbc] ↑ IterativeSolvers v0.7.1 ⇒ v0.8.1
  [c030b06c] ↑ ODE v2.3.0 ⇒ v2.4.0
  [d96e819e] ↑ Parameters v0.10.2 ⇒ v0.11.0
  [f27b6e38] ↑ Polynomials v0.5.1 ⇒ v0.5.2
  [438e738f] ↑ PyCall v1.18.5+ #master (https://github.com/JuliaPy/PyCall.jl.git) ⇒ v1.91.2 #master (https://github.com/JuliaPy/PyCall.jl.git)
  [d330b81b] ↑ PyPlot v2.6.3+ #master (https://github.com/JuliaPy/PyPlot.jl.git) ⇒ v2.8.1+ #master (https://github.com/JuliaPy/PyPlot.jl.git)

```

Now your previously installed package should be ready to be used. For example, try Arpack (solving sparse eigenvalue problems)

``` julia
using Arpack
using LinearAlgebra
A = Diagonal(1:4);
λ, ϕ = eigs(A, nev = 2);
display(λ)

2-element Array{Float64,1}:
 4.0
 3.0
```






## Lecture 2 (9/3)


