---
layout: post
title: About The Project
---

I got selected for Google Summer of Code 2019 for a project in The Julia Programming Language under the joint mentorship of [Chris Rackaukas](http://chrisrackauckas.com/), [Samuel Isaacson](http://math.bu.edu/people/isaacson/) and [Yingbo Ma](https://github.com/YingboMa).

My project is under [JuliaDiffEq](https://github.com/JuliaDiffEq), titled [Native Julia ODE, SDE, DAE, DDE, and (S)PDE Solvers](https://summerofcode.withgoogle.com/projects/#6552298552033280).

## About The Project

The main aim of this project as the title suggests revolves around adding Native Julia ODE, SDE solvers. JuliaDiffEq already boasts a rich library of solvers, my project focuses on improving it by adding Stabilized Explicit Solvers and Differential Algebraic Equations Solver.

Conventionally Stiff problems are considered to be the domain of Implicit-DiffEq solvers and Non-stiff problems are approached by explicit methods. A step of explicit method is usually cheaper than it implicit counterpart because implicit solvers as the name suggests involve solving large usually nonlinear implicit equations but they are still preferred because in case of stiff problems explicit methods suffer from serious step-size reduction because of stability issues. Here is where Stabilized methods come into play, they focus on extending the stability domains of explicit methods by the use of chebyshev polynomials. These methods have stability domains that increase quadratically with the number of stages, thus they can be used for stiff moderately-stiff and some stiff equations saving the effort required to solve large systems of implicit equations.

The second major part of my project in a DAE Solver. There are many DAE solvers available but they usually fail to compute consistent initial conditions. I plan on implementing a DAE solver based on BDF formulas that is capable of calculating consistent initial conditions for DAE of index 1.

 