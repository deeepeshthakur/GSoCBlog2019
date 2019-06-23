---
layout: post
title: Community Bonding Period
---

The Julia Community is simply amazing. Along the way I had my share of genuine but sometimes stupid and irritating doubts, everybody was really helpful. Slack is very active and very well organised. I'm really grateful to be a part of this community.

I spent the first last week of May going through literature on S-ROCK methods which I proposed to implement during my GSoC. After the first week I tried fixing bugs and getting the benchmarks for ROCK methods ready. I worked towards optimising memory usage in ROCK-methods, RKC, IRKC, and SERK-methods. Also we put in place certain step size limits to prevent the solver from going unstable. Also During this period I implemented SERK2 and ESERK4 which are similar SERK methods that I proposed but have ordrs 2 and 4 replectively.

With this IRKC and SERK-methods are almost complete and only their benchmarking remains.

**List of Contributions**

| Disciption | PR | Status |
|:--------------:|:--------:|:----------:|
| Implemented ESERK5 | [#692](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/692) | Merged |
| IRKC Memory Optimisation | [#723](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/723) | Merged |
| ROCK2 Memory Optimisation | [#729](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/729) | Merged |
| Implemented SERK2 | [#732](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/732) | Merged |
| Fix IRKC Adaptive Version | [#733](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/733) | Merged |
| Fix IRKC Extra Allocation | [#734](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/734) | Merged |
| Implemented ESERK4 | [#737](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/737) | Open |
| Fix ROCK Methods Constants | [#740](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/740) | Merged |
| Cleanup ROCK Methods and ROCK4 Memory Optimisation | [#741](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/741) | Merged |
| Stepsize Limits for ROCK Methods | [#745](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/745) | Merged |
| Stepsize Limtis for SERK Methods and RKC | [#752](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/752) | Merged |
| Fix RKC_utils.jl | [#759](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/759) | Merged |
| RKC_utils GPU Compatibility | [#765](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/765) | Open |


Going forward after discussing with my mentor I've decided to postpone benchmarking of SERK-methods to prioritize implementation of SROCK-methods. I plan to implement some basic stochastic solvers in [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl), and then start with SROCK methods as detailed in my proposal.
