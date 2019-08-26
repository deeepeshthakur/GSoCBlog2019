---
layout: post
title: First Evaluation Report
---

I have completed the implementation of `ESERK4` method. I also worked towards making the ROCK and SERK solvers GPU compatible. This allows using DifferentialEquations.jl problem type mixed with neural networks. These methods are a very promising option in training data generation, for example `ROCK2` taking 3 minutes against 40 minutes with `BS3`.[1]

I also started the implementation of Stochastic-ROCK solvers. These solvers boast similar benifits for SDEs like ROCK methods for ODEs. The three methods that I've implemented so far are `SROCK1` both for Stratonovich and Ito type problems and `SROCK2` for Ito type problems.

### SROCK1{:Ito}

    This is an explicit strong order 1 solver for stiff Ito type problems. It gives strong order 1 for 1-Dimensional Noise and Diagonal Noise and strong order 1//2 for General Noise case. It can be configured to get strong order 1 for Commutative Noise with some extra calculation but this is not yet implemented. Also this methods gives weak order 1 convergence for all the above Noise cases.

### SROCK1{:Stratonovich}

    This is an explicit strong order 1 solver for stiff Stratonovich type problems. It has convergence of strong order 1 for 1-Dimensional, Diagonal and Commutative Noise and strong order 1//2 for General Noise cases. Also we get weak order 1 for the above mentioned noise cases.

### SROCK2

    This is an explicit solver with weak order 2 for Ito type problems.

The above mentioned solvers are compatible with 1-D, Diagonal, Commutative and General Noise. Note that `SROCK1{:Ito}` is also compatible with Commutative Noise but with strong order 1//2.

Apart from these I've also added Three stage split-step Explicit Milstein Methods mentioned in StochasticDiffEq.jl [Issue #65](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/65). These solvers are compatible with 1-D noise and Diagonal Noise.

In addition to the above solver I've added Benchmark files for `ROCK2` and `ROCK4` ODE solvers.


## List of Contributions during Weeks 1 - 4

### OrdinaryDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Implemented ESERK4 | [#737](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/737) | Merged |
| RKC_utils GPU Compatibility | [#765](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/765) | Merged |

### StochasticDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Implemented Three Stage Split-Step Milstein Methods | [#150](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/150) | Merged |
| Implemented SROCK Method for Stratonovich-type Problems | [#153](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/153) | Merged |
| Optimised Stage-selection for SROCK1 method | [#159](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/159) | Merged |
| Implemented SROCK Method for Ito-type Problems | [#161](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/161) | Merged |
| Bug Fix in RKMilCommute | [#164](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/164) | Merged |
| Implemented SROCK2 Method for Ito-type Problems | [#166](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/166) | Merged |

### DiffEqBenchmarks.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Added Benchmark files for ROCK2 and ROCK4 | [#39](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/39) | Merged |


## Work Precision Diagrams for Stabilized ODE-Solvers including ESERK4
   1. ### Non-Stiff Problems
       * [Fitzhugh-Nagumo (including ESERK4)](https://nextjournal.com/deeepeshthakur/fitzhugh-nagumo-work-precision-diagrams-including-eserk4)
       * [Lotka-Volterra (including ESERK4)](https://nextjournal.com/deeepeshthakur/lotka-volterra-work-precision-diagrams-including-eserk4)
       * [Linear 100x100 (including ESERK4)](https://nextjournal.com/deeepeshthakur/linear-100x100-work-precision-diagrams-including-eserk4)
       * [Rigid Body (including ESERK4)](https://nextjournal.com/deeepeshthakur/rigid-body-work-precision-diagrams-including-eserk4)

  2. ### Stiff Problems
       * [Orego (including ESERK4)](https://nextjournal.com/deeepeshthakur/orego-work-precision-diagrams-including-eserk4)
       * [Hires (including ESERK4)](https://nextjournal.com/deeepeshthakur/hires-work-precision-diagrams-including-eserk4)
       * [Filament (including ESERK4)](https://nextjournal.com/deeepeshthakur/filament-work-precision-diagrams-including-eserk4)


## Future Work
Right now I'm focusing on implementing and optimising all the SROCK solvers mentioned in [Issue #73](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/73) of [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl). I also plan to add benchmarks for these solvers.

**All the problems for benchmarking purposes are taken from [DiffEqBenchmarks.jl](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl)**

## Refrences
   1. [Neural Jump SDEs (Jump Diffusions) and Neural PDEs](http://www.stochasticlifestyle.com/neural-jump-sdes-jump-diffusions-and-neural-pdes/)
