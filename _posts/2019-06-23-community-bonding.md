---
layout: post
title: Community Bonding Period
---

The Julia Community is simply amazing. Along the way I had my share of genuine but sometimes stupid and irritating doubts, everybody was really helpful. Slack is very active and very well organised. I'm really grateful to be a part of this community.

I spent the first last week of May going through literature on S-ROCK methods which I proposed to implement during my GSoC. After the first week I tried fixing bugs and getting the benchmarks for ROCK methods ready. I worked towards optimising memory usage in ROCK-methods, RKC, IRKC, and SERK-methods. Also we put in place certain step size limits to prevent the solver from going unstable. Also During this period I implemented SERK2 and ESERK4 which are similar SERK methods that I proposed but have ordrs 2 and 4 replectively.

With this IRKC and SERK-methods are almost complete and only their benchmarking remains.

Below are the list of contributions:

| S.No.       |      PR      |    Status   |
|:-----------:|:------------:|:-----------:|
| 1. |Implemented ESERK5  [#692](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/692) | Merged |
| 2. |IRKC Memory Usage  [#723](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/723) | Merged |
| 3. |ROCK2 Less Memory Usage  [#729](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/729) | Merged |
| 4. |SERK2v2  [#732](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/732) | Merged |
| 5. |IRKC adaptive fix  [#733](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/733) | Merged |
| 6. |IRKC extra allocation  [#734](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/734) | Merged |
| 7. |ESERK4  [#737](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/737) | Open |
| 8. |Fix ROCK methods  [#740](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/740) | Merged |
| 9. |CleanUp ROCK Methods and Memory Usage ROCK4  [#741](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/741) | Merged |
| 10. |Limiting Step_Size ROCK methods  [#745](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/745) | Merged |
| 11. |Step_size limitations on SERK Methods and RKC  [#752](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/752) | Merged |
| 12. |Fix RKC_utils  [#759](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/759) | Merged |
| 13. |RKC_utils bug  [#765](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/765) | Open |
