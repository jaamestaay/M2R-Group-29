# M2R Group 29: Scientific Machine Learning

This is the GitHub repository for the MATH50002 Group Research Project (M2R) on Scientific Machine Learning by Group 29 (James Tay, Jiaru Li, Xinyan Wang, Tianshi Liu, Jiankuan Liu).

## Report Outline

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

## Current Work

James Tay:

- Extension of automatic differentiation material (dual numbers) covered in the MATH50003 Numerical Analysis course to cover automatic differentiation in higher dimensions.
- Examining the implementations of commonly used Julia modules (Autodiff, Zygote, etc) which make use of (reverse-mode) automatic differentiation based on Labs 2 and 3 of SciMLSANUM2024.
- Working on basic ideas of gradient descent and extending them to more sophisticated methods used in practice (including but not limited to SGD) to locate various minima.
- Currently working on how to apply these methods in solving neural ODEs/CDEs (where applicable) to make them more efficient. Largely working in Julia.

Jiaru Li:

- Description and explanation of neural network (NN) and how it works, based on Lab 5 of SciMLSANUM2024.
- Some simple applications to further illustrate the concepts.
  (1) Regression. Polynomial regression was introduced in the numerical analysis course, and I am going to take the ideas further and discuss nonlinear regression based on NN. Comparison of least squares and NN methods will also be discussed, in order to explore the ways in which NN becomes powerful.
  (2) Number recognition using MNIST. Being a standard example from machine learning, it helps us to discover how NN works in terms of real-world applications.
- Julia code to accompany the ideas. Where appropriate, Python will also be used.

Xinyan Wang:

- Explain backpropagation for neural network and the adjoint method for neural ODEs.
- Provide an explanation of the idea behind neural ODEs.
- Use Julia to construct and apply a neural ODE model.
- Show the limitations and strengths of neural ODEs, and introduce some ways to optimize a simple neural ODE.

Tianshi Liu:

- Extend the proof of the adjoint method for neural ODEs to neural CDEs.
- State the definitions for tensor product, signature, log signature, and introduce log ODE method. (Statement maybe omitted in the presentation, and the lengthy proof omitted in the report)
- Use Julia to construct and apply a neural CDE model based on previous neural ODE model.
- Perform a modelling of time series data combining the work of Xinyan and me, and analyze the results of the experiment.
- Show the limitations and strengths of neural CDEs.

Jiankuan Liu:

- Example of a neural network: Continuous dynamics of financial time series data, such as stock prices and market indices. This is an application of Recurrunt Neural Network. Neural ODEs naturally capture the continuous evolution of market data by embedding neural network architectures within the differential equation solving process. The details would be studied by Tianshi.
- Implementation in Julia.
