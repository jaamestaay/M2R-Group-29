# M2R Group 29: Scientific Machine Learning

This is the GitHub repository for the MATH50002 Group Research Project (M2R) on Scientific Machine Learning by Group 29 (James Tay, Jiaru Li, Xinyan Wang, Tianshi Liu, Jiankuan Liu).

## Report Outline

### 1. Introduction

### 2. Basic Neural Network Theory

2.1 Definition and Implementation of Basic Neural Networks (Jiaru)

- History
- Basic Concepts
- Basic Applications (Regression, Classification)

### 3. Introduction to Neural ODEs/CDEs

3.1 Definition of Neural ODEs (Xinyan)

- Construction of Neural ODEs
- Why Neural ODEs may be advantageous compared to other formulations

### 4. Solving Neural ODEs

4.1 An elaboration of the steps taken to train and solve a Neural ODE (James)

- Loss Functions and Minima
- Automatic Differentiation
- Gradient Descent and its Applications in Neural ODEs

4.2 Back-propagation

- Discretise-then-optimise (James)
- Optimise-then-discretise: Adjoint Equation (Xinyan)

4.3 Numerical Solvers (James)

- Implicit Solvers (and why we don't use them)
- Euler's Method and Runge-Kutta Methods
- Heun's Method
- Other methods if time permits

### 5. An Application: Time Series Analysis

### 6. Extension: Neural CDEs (Tianshi)

6.1 Definition and Formulation

- Motivation for Neural CDEs
- Neural ODEs vs CDEs: Advantages and Disadvantages
- Why Neural CDEs may be advantageous compared to other formulations for problems
- Natural cubic splines for continuous path $X_t$

6.2 Solving Neural CDEs

- Optimise-then-discretise: Adjoint Equation for CDE (proof)
- log ODE Method (no proof, just statement)
- State it for completeness
- Mention that it can be cleverly avoided provided that we choose a continuously differentiable control path

6.3 Applications

- Time Series (Part of it might be a rough sketch of pseudocode/algorithm)

### 7. Conclusion
