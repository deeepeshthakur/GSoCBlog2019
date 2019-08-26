---
layout: post
title: Second Evaluation Report
---

I have completed the implementation of `ESERK4` method. I also worked towards making the ROCK and SERK solvers GPU compatible. This allows using DifferentialEquations.jl problem type mixed with neural networks. These methods are a very promising option in training data generation, for example `ROCK2` taking 3 minutes against 40 minutes with `BS3`.[1]

I also started the implementation of Stochastic-ROCK solvers. These solvers boast similar benifits for SDEs like ROCK methods for ODEs. The three methods that I've implemented so far are `SROCK1` both for Stratonovich and Ito type problems and `SROCK2` for Ito type problems.

| Solver | Description |
|:--------------:|:--------:|
| **SROCK1{:Ito}** | This is an explicit strong order 1 solver for stiff Ito type problems. It gives strong order 1 for 1-Dimensional Noise and Diagonal Noise and strong order 1/2 for General Noise case. It can be configured to get strong order 1 for Commutative Noise with some extra calculation but this is not yet implemented. Also this methods gives weak order 1 convergence for all the above Noise cases. |
| **SROCK1{:Stratonovich}** | This is an explicit strong order 1 solver for stiff Stratonovich type problems. It has convergence of strong order 1 for 1-Dimensional, Diagonal and Commutative Noise and strong order 1/2 for General Noise cases. Also we get weak order 1 for the above mentioned noise cases. |
| **SROCK2** | This is an explicit solver with weak order 2 for Ito type problems. |

The above mentioned solvers are compatible with 1-D, Diagonal, Commutative and General Noise. Note that `SROCK1{:Ito}` is also compatible with Commutative Noise but with strong order 1/2.

Apart from these I've also added Three stage split-step Explicit Milstein Methods mentioned in StochasticDiffEq.jl [Issue #65](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/65). These solvers are compatible with 1-D noise and Diagonal Noise.

In addition to the above solver I've added Benchmark files for `ROCK2` and `ROCK4` ODE solvers.


## List of Contributions during Weeks 1 - 4

### StochasticDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Implemented SROCKEM | [#168](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/168) | Merged |
| RKMilCommute GPU Compatibility | [#169](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/169) | Merged |
| SROCK1 General Noise and Optimisation | [#170](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/170) | Merged |
| RKMilCommute Memory Optimisation | [#173](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/173) | Merged |
| Implemented SKSROCK | [#174](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/174) | Merged |
| Fix Commutative Tests | [#175](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/175) | Merged |
| Implemented Tang Xaio SROCK2W2Ito | [#177](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/177) | Merged |

### DiffEqDocs.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Added Docs for ODE and SDE Solvers | [#233](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/233) | Merged |


## Future Work
Right now I'm focusing on implementing and optimising all the SROCK solvers mentioned in [Issue #73](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/73) of [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl). I also plan to add benchmarks for these solvers.

**All the problems for benchmarking purposes are taken from [DiffEqBenchmarks.jl](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl)**

## Refrences
   1. [Neural Jump SDEs (Jump Diffusions) and Neural PDEs](http://www.stochasticlifestyle.com/neural-jump-sdes-jump-diffusions-and-neural-pdes/)
