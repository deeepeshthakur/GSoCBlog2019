---
layout: post
title: First Evaluation Report
---

The Julia Community is simply amazing. Along the way I had my share of genuine but sometimes stupid and irritating doubts, everybody was really helpful. Slack is very active and very well organised. I'm really grateful to be a part of this community.

I spent the first last week of May going through literature on S-ROCK methods which I proposed to implement during my GSoC. After the first week I tried fixing bugs and getting the benchmarks for ROCK methods ready. I worked towards optimising memory usage in ROCK-methods, RKC, IRKC, and SERK-methods. Also we put in place certain step size limits to prevent the solver from going unstable. Also During this period I implemented SERK2 and ESERK4 which are similar SERK methods that I proposed but have ordrs 2 and 4 replectively.

With this IRKC and SERK-methods are almost complete and only their benchmarking remains.

## List of Contributions

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

## Performance for the above Stabilized Methods
   1. ### Non-Stiff Problems
       * [Fitzhugh-Nagumo](https://nextjournal.com/deeepeshthakur/fitzhugh-nagumo-work-precision-diagrams)
       * [Lotka-Volterra](https://nextjournal.com/deeepeshthakur/lotka-volterra-work-precision-diagrams)
       * [Linear 100x100](https://nextjournal.com/deeepeshthakur/linear-100x100-work-precision-diagrams)
       * [Rigid Body](https://nextjournal.com/deeepeshthakur/rigid-body-work-precision-diagrams)

  2. ### Stiff Problems
       * [Orego](https://nextjournal.com/deeepeshthakur/orego-work-precision-diagrams)
       * [Hires](https://nextjournal.com/deeepeshthakur/hires-work-precision-diagrams)
       * [Filament](https://nextjournal.com/deeepeshthakur/filament-work-precision-diagrams)
       * [Comparing Stabilized Methods for Filament with TRBDF2](https://nextjournal.com/deeepeshthakur/filament-work-precision-diagrams-comparison-with-trbdf2)

## Future Work
Going forward after discussing with my mentor I've decided to postpone benchmarking of SERK-methods to prioritize implementation of SROCK-methods. I plan to implement some basic stochastic solvers in [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl), and then start with SROCK methods as detailed in my proposal.

**All the problems for benchmarking purposes are taken from [DiffEqBenchmarks.jl](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl)**
