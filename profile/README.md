# Welcome to `nosnoc`
The `nosnoc` organization focuses on nonsmooth optimization, with a primary focus on optimal control of nonsmooth dynamical systems.
We also maintain several tailored solver for solving optimization with complementarity constraints.

## Packages
We currently maintain the following packages:
- `nosnoc`: The namesake project. It contains tools for modeling and solving optimal control problems whose dynamics have a discontinous right hand side:
  - Piecewise Smooth Systems: Systems whose dynamics exhibit state based switches in dynamics. We support primarily Filippov systems but also more generically systems with Heaviside step functions on the right hand side.
  - Complementarity Lagrangian Systems: Complementarity based formulations of rigid body dynamics, both in 2d and 3d.
  - Constrained Dynamical Systems: Systems whose dynamics are constrained to a (possibly time-varying) set in the full statespace. These include Projected Dynamical Systems and their variants, as well as First-order Moreau Sweeping Processes.
  
  This package is written in Matlab using `CasADi` for modeling and automatic differentiation.
  It further contains a regularization/relaxation based solver for Mathematical Programs with Complementarity Constraints (MPCC), implementing the myriad of relaxations and regularizations that have been proposed over the last decades.
- `nosnoc_py`: A partial re-implementation of the `nosnoc` package in python. 
  It contains only some of the features of the Matlab package.
  If you want to use some features which are not currently implemented feel free to reach out to the authors via github issues or via email.
- `mpecopt`: A Matlab implementation of an active set solver for MPCCs.
  It is globally convergent to B-stationary points which are "true" local minima of MPCCs.
- `LCQPow`: A sequential convex programming approach for solving Quadratic Programs with linear complementarity constraints.
- `nosbench`: A benchmark suite of MPCCs arising from nonsmooth optimal control and simulation solvers.