---
layout: page
title: Projects
permalink: /projects/
---
# Projects

## Fluid membrane
When we talk about isotropic fluid membranes, the classic example that comes to mind is a soap bubble. Microscopically, it consists of a thin layer of water enclosed by two layers of surfactant molecules. Both the water and surfactant molecules are free to move tangentially, meaning the membrane behaves as a two-dimensional isotropic fluid. However, due to the lack of internal structure, the only stress it can support is tangential, known as surface tension.

A more structured example of a fluid membrane is the lipid bilayer, which forms the basis of biological cell membranes. When surrounded by water, lipid molecules orient oppositely to the surfactant molecules in a soap bubble and tend to internally crystallize. This additional structure allows for elastic responses beyond surface tension. Physicists have used liquid crystal theory to derive the elastic energy for these membranes, known as the Canham–Helfrich energy. This model has proven highly predictive—for instance, in explaining the biconcave geometry of red blood cells.

Mathematically, the Canham–Helfrich energy is particularly elegant, depending only on two geometric invariants of the surface: the mean curvature and the Gaussian curvature. Independently, this same energy arises in differential geometry under the name Willmore energy. The Willmore conjecture, concerning the minimal Willmore energy configuration for tori, remained open for decades before being resolved in the early 2010s.

However, the critical points of this energy describe only equilibrium configurations. To understand how membranes evolve toward equilibrium, one must study the associated gradient flows. These flows are also useful in surface fairing tasks in geometry processing. Yet from a computational standpoint, they are challenging: the flows are fourth-order with respect to the embedding of the surface and nonlinear, imposing strong constraints on numerical stability and timestep. Moreover, due to the reparametrization invariance of the energy, the critical condition has a large kernel, which can lead to mesh degradation over time. Various approaches have been proposed to mitigate this, including introducing alternative metrics for the gradient flow or restricting the flow to specific subspaces such as being conformal or isometric.

This brings us to a more physically grounded alternative. From the perspective of continuum mechanics, the realistic dynamics of fluid membranes arise from the viscous limit of the Navier–Stokes equations. This leads to evolving Stokes flow, a natural gradient flow governed by the viscous dissipation metric and subject to volume-preserving (i.e., incompressibility) constraints.