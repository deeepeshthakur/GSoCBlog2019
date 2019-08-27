---
layout: post
title: Final Report
---

## Basic Info

**Name:** Deepesh Singh Thakur ([deeepeshthakur](https://github.com/deeepeshthakur))

**Proposal:** Native Julia ODE, SDE, DAE, DDE, and (S)PDE Solvers ([link](https://storage.googleapis.com/summerofcode-prod.appspot.com/gsoc/core_project/doc/5078821303222272_1554719641_Proposal-GSoC-19-Deepesh-Singh-Thakur.pdf?Expires=1566949285&GoogleAccessId=summerofcode-prod%40appspot.gserviceaccount.com&Signature=NuuOSbtU6EpED7Etuq%2BphEtmkLzVfpxGRw%2BBfln7ddVlL74laEIdc%2B%2BLIjjEVRvq2YWfPyIgBe72WnnoMN0C9p2Vp3HFigJfhKs7R1dhwJYbEUmIn%2BvaQP2rB0BxJdiNhyQLDe5SWUB5fFxiHKCMRsvshs2YAo0i1exn45Vt4KcK6McJoYfU3jKAQVT%2BQjPXzFUuEHzAcS4KD8SNdVGlILxkMZi9m32Tz5IlCkWva4Md8sUYkDhmTk%2Bqcl4LiV4FX39zMJBTpN7sZXMJWmUhJ3AZgeEBF%2FmMTcv87%2B3ALlrntXEUnb5vufHV%2B5oPHptn4p2Y12x%2F7KWmLHdxkiC8ig%3D%3D))

**Mentors:** [Dr. Christopher Rackauckas](https://github.com/ChrisRackauckas), [Yingbo Ma](https://github.com/YingboMa), [Prof. Samuel Isaacson](https://github.com/isaacsas)

**Organization:** The Julia Language (JuliaDiffEq)

**Repositories:** [StochasticDiffEq.jl](https://github.com/JuliaDiffEq/StochasticDiffEq.jl), [OrdinaryDiffEq.jl](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl), [DiffEqDevTools.jl](https://github.com/JuliaDiffEq/DiffEqDevTools.jl), [DiffEqDocs.jl](https://github.com/JuliaDiffEq/DiffEqDocs.jl), [DiffEqBenchmarks.jl](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl), [juliadiffeq.github.io](https://github.com/JuliaDiffEq/juliadiffeq.github.io).

## Pull Requests

### StochasticDiffEq.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Implemented Three Stage Split-Step Milstein Methods | [#150](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/150) | Merged |
| Implemented SROCK Method for Stratonovich-type Problems | [#153](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/153) | Merged |
| Optimised Stage-selection for SROCK1 method | [#159](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/159) | Merged |
| Implemented SROCK Method for Ito-type Problems | [#161](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/161) | Merged |
| Bug Fix in RKMilCommute | [#164](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/164) | Merged |
| Implemented SROCK2 Method for Ito-type Problems | [#166](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/166) | Merged |
| Implemented SROCKEM | [#168](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/168) | Merged |
| RKMilCommute GPU Compatibility | [#169](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/169) | Merged |
| SROCK1 General Noise and Optimisation | [#170](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/170) | Merged |
| RKMilCommute Memory Optimisation | [#173](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/173) | Merged |
| Implemented SKSROCK | [#174](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/174) | Merged |
| Fix Commutative Tests | [#175](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/175) | Merged |
| Implemented Tang Xaio SROCK2W2Ito | [#177](https://github.com/JuliaDiffEq/StochasticDiffEq.jl/pull/177) | Merged |
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
| Implemented LDDRK46 | [#607](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/607) | Merged |
| Fix Nomenclature | [#610](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/610) | Merged |
| Implemented NDBLSRK124 | [#611](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/611) | Merged |
| Implemented NDBLSRK134 | [#614](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/614) | Merged |
| Implemented NDBLSRK144 | [#616](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/616) | Merged |
| Implemented ROCK4 | [#628](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/628) | Merged |
| Implemented RKC | [#634](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/634) | Merged |
| Implemented TSLDDRK74 | [#637](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/637) | Merged |
| Implemented DGLDDRK73_C | [#641](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/641) | Merged |
| Implemented DGLDDRK84_C | [#642](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/642) | Merged |
| Implemented DGLDDRK84_F | [#644](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/644) | Merged |
| LDDRK64 to HSLDDRK64 | [#653](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/653) | Merged |
| Implemented IRKC | [#659](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/659) | Merged |
| Implemented 2R+ schemes | [#663](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/663) | Merged |
| Implemented 3R+ schemes | [#675](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/675) | Merged |
| Implemented 4R+ and 5R+ schemes | [#686](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/686) | Merged |
| IRKC Cleanup | [#687](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/687) | Merged |
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
| Implemented ESERK4 | [#737](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/737) | Merged |
| RKC_utils GPU Compatibility | [#765](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/765) | Merged |
| SERK Cleanup | [#808](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/808) | Merged |
| Bug Fix ROCK Methods | [#848](https://github.com/JuliaDiffEq/OrdinaryDiffEq.jl/pull/848) | Merged |

### DiffEqDevTools.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Fix Noise Type in Analyticless Convergence Test | [#46](https://github.com/JuliaDiffEq/DiffEqDevTools.jl/pull/46) | Merged |

### DiffEqDocs.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Fix Typo in Docs | [#193](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/193) | Merged |
| Added Docs for new ODE solvers | [#195](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/195) | Merged |
| Fix Formatting in Docs | [#216](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/216) | Merged |
| Added Docs for ODE and SDE Solvers | [#233](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/233) | Merged |

### DiffEqBenchmarks.jl

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Added Benchmark files for ROCK2 and ROCK4 | [#39](https://github.com/JuliaDiffEq/DiffEqBenchmarks.jl/pull/39) | Merged |

### juliadiffeq.github.io

| Description | Pull Requests | Current Status |
|:--------------:|:--------:|:----------:|
| Added Citings | [#20](https://github.com/JuliaDiffEq/juliadiffeq.github.io/pull/20) | Merged |
| Added Citings | [#21](https://github.com/JuliaDiffEq/juliadiffeq.github.io/pull/21) | Merged |
| Added Citings | [#22](https://github.com/JuliaDiffEq/juliadiffeq.github.io/pull/22) | Merged |


## Blog Posts

The following blogs describe the work during the entire period:
   1. [About The Project](https://deeepeshthakur.github.io/gsocblog/about-the-project/)
   2. [Community Bonding Period](https://deeepeshthakur.github.io/gsocblog/community-bonding/)
   3. [First Evaluation Report](https://deeepeshthakur.github.io/gsocblog/first-eval-report/)
   4. [Second Evaluation Report](https://deeepeshthakur.github.io/gsocblog/second-eval-report/)
   5. [Third Evaluation Report](https://deeepeshthakur.github.io/gsocblog/third-eval-report/)

## Acknowledgements
I would like to thank Dr. Christopher Rackauckas, Yingbo Ma, David Widmann, and Prof. Samuel Isaacson for their support and guidance throughout the project. Shoutout to the entire Julia community for being awesome and amazingly helpful!
