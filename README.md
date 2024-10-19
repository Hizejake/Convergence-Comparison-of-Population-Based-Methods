# Convergence-Comparison-of-Population-Based-Methods

## Introduction

This project explores the convergence properties of two popular population-based metaheuristic optimization algorithms: Particle Swarm Optimization (PSO) and Differential Evolution (DE). These algorithms are tested on several benchmark functions to compare their performance in terms of convergence to the global minimum.

## Metaheuristics

Metaheuristics are high-level procedures designed to generate or select heuristics that provide sufficiently good solutions to optimization problems, especially with incomplete or imperfect information. They are widely used for solving complex optimization problems that are otherwise difficult to solve using traditional methods.

## Population-Based Methods

Population-based methods are a subset of metaheuristics that use a population of candidate solutions to explore the search space. These methods iteratively improve the population by applying operators inspired by natural processes such as selection, crossover, and mutation.

## Particle Swarm Optimization (PSO)

PSO is a computational method used for optimizing a problem by iteratively improving a candidate solution with regard to a given measure of quality. It simulates the social behavior of birds flocking or fish schooling. Each particle in the swarm represents a potential solution and adjusts its position based on its own experience and the experience of neighboring particles.

### PSO Algorithm

1. **Initialization**: Initialize a swarm of particles with random positions and velocities.
2. **Velocity Update**: Update the velocity of each particle based on its own best position and the global best position.
3. **Position Update**: Update the position of each particle based on its velocity.
4. **Evaluation**: Evaluate the fitness of each particle.
5. **Termination**: Repeat steps 2-4 until a stopping criterion is met.

## Differential Evolution (DE)

DE is a population-based optimization algorithm that uses differential mutation and crossover to explore the search space. It is particularly effective for continuous optimization problems.

### DE Algorithm

1. **Initialization**: Initialize a population of candidate solutions randomly.
2. **Mutation**: Create mutant vectors by adding the weighted difference between two population vectors to a third vector.
3. **Crossover**: Combine the mutant vectors with the target vectors to create trial vectors.
4. **Selection**: Select the better vectors between the target and trial vectors to form the new population.
5. **Termination**: Repeat steps 2-4 until a stopping criterion is met.

## Benchmark Functions

### Rastrigin Function

The Rastrigin function is a non-convex function used as a performance test problem for optimization algorithms. It is highly multimodal, meaning it has a large number of local minima. The function is defined by:

$$f(x) = An + \sum_{i=1}^{n} \left[ x_i^2 - A \cos(2\pi x_i) \right]$$

where \(A = 10\), \(x_i \in [-5.12, 5.12]\).

### Sphere Function

The Sphere function is a simple convex function used to test optimization algorithms. It is defined by:

$$f(x) = \sum_{i=1}^{n} x_i^2$$

### Rosenbrock Function

The Rosenbrock function, also known as the Rosenbrock's valley or Rosenbrock's banana function, is a non-convex function used to test optimization algorithms. It is defined by:

$$f(x) = \sum_{i=1}^{n-1} \left[ 100 (x_{i+1} - x_i^2)^2 + (1 - x_i)^2 \right]$$

### Ackley Function

The Ackley function is a widely used multimodal test function for optimization algorithms. It is defined by:

$$f(x) = -20 \exp\left(-0.2 \sqrt{\frac{1}{n} \sum_{i=1}^{n} x_i^2}\right) - \exp\left(\frac{1}{n} \sum_{i=1}^{n} \cos(2\pi x_i)\right) + 20 + \exp(1)$$

## Results

The following table summarizes the results of the PSO and DE algorithms on the benchmark functions:

| Function   | Algorithm | Global Best Position                         | Global Best Value       |
|------------|-----------|----------------------------------------------|-------------------------|
| Rastrigin  | PSO       | [-1.344908055753581e-09, 2.376406622046473e-09] | [0.]                    |
| Rastrigin  | DE        | [9.25688223e-10, 5.08266979e-10]             | [0.]                    |
| Sphere     | PSO       | [-2.913048664423185e-12, -4.749938907398819e-12] | [3.10477721e-23]        |
| Sphere     | DE        | [ 2.23285558e-25, -1.73256573e-24]           | [3.05164045e-48]        |
| Rosenbrock | PSO       | [0.8475505669968298, 0.7175626751327775]     | [0.02330156]            |
| Rosenbrock | DE        | [1. 1.]                                      | [0.]                    |
| Ackley     | PSO       | [-3.110308272445469e-12, -3.533160664564651e-12] | [1.3316015e-11]         |
| Ackley     | DE        | [-9.31411575e-17, -2.38160702e-16]           | [4.4408921e-16]         |

## Conclusion

In general, the Differential Evolution (DE) algorithm achieved better results compared to the Particle Swarm Optimization (PSO) algorithm. While both algorithms were able to find the global best positions for the benchmark functions, DE consistently found positions closer to the global optimum with lower function values. This highlights the effectiveness of DE in exploring the search space and the importance of parameter tuning for achieving optimal results.

## References

- Kennedy, J., & Eberhart, R. (1995). Particle swarm optimization. In Proceedings of ICNN'95 - International Conference on Neural Networks (Vol. 4, pp. 1942-1948).
- Storn, R., & Price, K. (1997). Differential Evolution – A Simple and Efficient Heuristic for global Optimization over Continuous Spaces. Journal of Global Optimization, 11, 341-359.