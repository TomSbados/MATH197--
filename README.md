Geodesic distances are notoriously difficult to compute analytically, because of this, we aimed to apply Varadhan's formula which relates distances on manifolds to the diffusion of heat on the manifold's surface. 

To do this, we must first create an approximation of the heat kernel using Monte Carlo methods. There is a well understood theorem known as the Invariance principle which relates random walks to Brownian motion, which matches the fundamental solution to the heat equation. By approximating Brownian motion using random walks, and using the distribution of those random walks to find the heat kernel, we can plug in our approximated heat kernel into Varadhan's formula to find geodesic distances on any manifold.

In this project, I applied these theories to find geodesic distances that would be otherwise impossible to compute analytically.
