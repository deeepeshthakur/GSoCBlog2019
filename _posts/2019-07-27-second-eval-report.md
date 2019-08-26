---
layout: post
title: Second Evaluation Report
---

I completed implementing `SROCKEM`, `SKSROCK` and `TangXaioSROCK2W2Ito`. The last of these is not currently used. One of the main advantages of SROCK methods is the varying number of stages which can be chosen from depending on the spectral radius of the problem. But the paper describing `TangXaioSROCK2W2Ito` only has constants for 5 stages and it is not trivial to calculate these constants so this method is not suggested. Along with these I also tried improving `RKMilCommute` GPU Compatibility and Memory utilization. I also improved the General Noise handling in `SROCK1`, adding noise rate type stability along with some memory optimisation. I added more robust tests for Commutative Noise Solvers.

I made contributions to the Docs Page by adding docs for the ODE and SDE solvers I've added.

| Solver | Description |
|:--------------:|:--------:|
| **SROCKEM(strong_order_1 = false)** | This is an explicit strong order 1/2 solver for stiff Ito type problems. This is basically the Euler-Maruyama Method with First Order ROCK stabilization. It can handle 1-D, Diagonal, Commutative and General Noise. It has strong order 1/2 and weak order 1 for all noise cases. |
| **SROCKEM(strong_order_1 = true)** | This is an explicit strong order 1 solver for stiff Ito type problems. This is basically the Euler-Maruyama Method with First Order ROCK stabilization. It can handle 1-D, Diagonal, Commutative and General Noise. It has strong order 1 and weak order 1 for all noise cases. The order 1 convergence is obtained with a few extra calculation and extra u-type arrays. |
| **SKSROCK** | This is an explicit solver with strong and weak order 1 for Ito type problems. This has a really large stability domain about 10 times that of SROCK1. |


## List of Contributions during Weeks 5 - 8

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
With the above contibutions  [Issue #73](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/issues/73) of [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl) is almost complete with only `SROCK2KomBur` and `SROCKC2` remaining. After that I want to implement a robust way of approximating Double Stochastic Integrals with order 1 accuracy.
