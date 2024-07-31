### Quick Tour of the files:

1. MATH197.ipynb
   Notebook that was used to create the findings, beginning with exploration of effective values of $t$, in addition final distance measurements.
2. StartingPointMath197-2.ipynb
   Notebook used to explain fundamentals of the project to my team.
3. Math_197_Project.pdf
   Final project presentation, explaining all fundamental topics as well as final statement, meant to be understood by all undergraduate levels. 





# Application of Varadhan's Formula for Geodesic Distance Computation

Geodesic distances are notoriously difficult to compute analytically due to the complexity of the underlying manifold structures. In this project, we aimed to apply Varadhan's formula, which relates distances on manifolds to the diffusion of heat on the manifold's surface, to compute these distances more effectively.

## Background

### Geodesic Distance
The geodesic distance between two points on a manifold is the length of the shortest path connecting them that lies entirely on the manifold. This is analogous to the concept of the "straight line" distance in Euclidean space but generalized to curved spaces.

### Varadhan's Formula
Varadhan's formula provides a connection between the heat kernel and the geodesic distance. It states that for a small time \(t\), the heat kernel \(K_t(x, y)\) on a manifold approximates the geodesic distance $d(x, y)$ as:

$$d(x, y) \approx \sqrt{-4t \log K_t(x, y)}$$

### Heat Kernel
The heat kernel \(K_t(x, y)\) is the fundamental solution to the heat equation on the manifold. It describes how heat diffuses over time from one point to another.

### Monte Carlo Methods
Monte Carlo methods are used to approximate the heat kernel through simulation. By leveraging the Invariance Principle, which relates random walks to Brownian motion, we can approximate the behavior of the heat equation.

## Methodology

### Approximating the Heat Kernel
We approximate the heat kernel using Monte Carlo methods. This involves simulating numerous random walks on the manifold and using their distribution to estimate the heat diffusion.

1. **Random Walks and Brownian Motion**: We approximate Brownian motion by simulating random walks. According to the Invariance Principle, the distribution of these random walks will converge to the distribution of Brownian motion.

2. **Estimating Heat Kernel**: From the distribution of these random walks, we estimate the heat kernel $K_t(x, y)$.

### Varadhan's Formula Application
Using the approximated heat kernel, we apply Varadhan's formula to compute the geodesic distance:

$$d(x, y) \approx \sqrt{-4t \log \hat{K}_t(x, y)}$$

where $\hat{K}_t(x, y)$ is the approximated heat kernel obtained from our simulations.

### Implementation
We implemented this approach using Python, leveraging libraries such as NumPy and SciPy for numerical computations and matplotlib for visualization.

## Results

Our approach successfully approximated geodesic distances on various manifolds, which would be otherwise difficult to compute analytically. The results demonstrate the efficacy of combining Monte Carlo methods with Varadhan's formula for practical applications in computational geometry and related fields.

## Relevant Formulas

1. **Heat Equation**:
   $$\frac{\partial u}{\partial t} = \Delta u$$
   where $u(t, x)$ is the temperature at time $t$ and point $x$, and $\Delta$ is the Laplace-Beltrami operator.

2. **Varadhan's Formula**:
   $$d(x, y) \approx \sqrt{-4t \log K_t(x, y)}$$

3. **Approximation of Heat Kernel using Monte Carlo**:
   $$\hat{K}_t(x, y) \approx \frac{1}{N} \sum_{i=1}^{N} \delta_{X_i}(y)$$
   where $X_i$ are the end points of the random walks starting from $x$, $N$ is the number of random walks, and $\delta_{X_i}(y)$ is the Dirac delta function centered at $y$.

## Conclusion

By utilizing Varadhan's formula and Monte Carlo methods, we have developed an effective technique for approximating geodesic distances on manifolds. This approach opens up new possibilities for applications in fields requiring distance computations on complex surfaces.

## Future Work

Future work could involve improving the efficiency of the Monte Carlo simulations, exploring alternative methods for approximating the heat kernel, and applying this approach to higher-dimensional manifolds.
