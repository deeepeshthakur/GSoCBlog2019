---
layout: post
title: Third Evaluation Report
---

With the addition of `KomBurSROCK2` and `SROCKC2` all the methods mentioned in StochasticDiffEq.jl [Issue #73](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/73) are complete. `KomBurSROCK2` is similar to `SROCK2` for Stratonovich Problems.

| Solver | Description |
|:--------------:|:--------:|
| **KomBurSROCK2** | This is an explicit strong order 1 and weak order 2 solver for stiff Stratonovich type problems. This method is similar to SROCK2 for Stratonovich Problems. It is compatible with 1-D, Diagonal, Commutative, and General Noise cases. |
| **SROCKC2** | This is an explicit strong order 1 solver for stiff Ito type problems. It has convergence of strong order 1 for 1-Dimensional, Diagonal and Commutative Noise. |

With this in place, I refactored the SROCK methods I implemented to only use vector type calculation. Further adding Tracked Array compatibility and fixing some bugs in general noise case in `SROCKEM`. Along with these I added Diagonal noise compatibility in 3-stage Split-step Milstein Methods and fixed bugs in error calculation in RKMilCommute when using adaptive setting.

### Approximating Iterated Integrals
Now StochasticDiffEq has functionality for estimating Double Stochastic Integrals using iterative techniques as used in [SDELAB](https://doi.org/10.1016/j.cam.2006.05.037) with accuracy of order 1. These are required to get order 1 convergence in Milstein Methods for general noise case. The original paper was by Wiktorsson that is [Joint Characteristic Function and Simultaneous Simulation of Iterated Itô Integrals for Multiple Independent Brownian Motions](https://www.jstor.org/stable/2667257). Apart from this we use take advantage of Diagonal and Commutative noise cases to approximate these using less computational effort.

Apart from this I also made contirbutions to OrdinaryDiffEq.jl and DiffEqDevTools.jl where I fixed bugs in ROCK Method in case of negative `dt`, and fix noise type when noise is non-diagonal in `analyticless_test_convergence`. I also refactered SERK methods adding step-size limits to `ESERK4`.

## List of Contributions during Weeks 9 - 13

### StochasticDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Diagonal Noise Case Three Stage Split-step Milstein Methods | [#184](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/184) | Merged |
| Implemented KomBurSROCK2 | [#186](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/186) | Merged |
| Vector Format for SROCK Methods | [#192](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/192) | Merged |
| Implemented SROCKC2 | [#204](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/204) | Merged |
| Implemented Iterated Integrals | [#209](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/209) | Merged |
| Fix Error Calculation RKMilCommute | [#218](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/218) | Merged |
| SROCKEM General Noise Bug Fix | [#227](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/227) | Merged |
| SROCK Methods Tracked Arrays Compatibility | [#228](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/228) | Open |

### OrdinaryDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| SERK Cleanup | [#808](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/808) | Merged |
| Bug Fix ROCK Methods | [#848](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/848) | Merged |

### DiffEqDevTools.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Fix Noise Type in Analyticless Convergence Test | [#46](https://github.com/JuliaDiffEq/DiffEqDevTools.jl/pull/46) | Merged |


## Future Work
With iterated_integrals.jl in place, I want to add Milstein Methods that take advantage of this to get strong order 1 convergence in case of general noise. Also, I want to add Benchmarks to show the performance of these solvers to the community and I SROCK method `KomBurSROCK1` which has strong order 1 convergence using iterated_integrals.jl.

## Refrences
   1. [SDELAB](https://doi.org/10.1016/j.cam.2006.05.037)
   2. [SDELAB2](https://github.com/tonyshardlow/SDELAB2)
   3. [Wiktorsson, Magnus. Joint Characteristic Function and Simultaneous Simulation of Iterated Itô Integrals for Multiple Independent Brownian Motions. The Annals of Applied Probability, vol. 11, no. 2, 2001, pp. 470–487. JSTOR](www.jstor.org/stable/2667257)
