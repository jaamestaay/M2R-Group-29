# M2R Group 29: Scientific Machine Learning

This is the GitHub repository for the MATH50002 Group Research Project (M2R) on Scientific Machine Learning by Group 29 (James Tay, Jiaru Li, Xinyan Wang, Tianshi Liu, Jiankuan Liu)

## Report Outline

### 0. Basic Neural Network Theory

0.1 Definition and Implementation of Basic Neural Networks (Jiaru)

- Feedforward Neural Networks vs Recurrent Neural Networks
- Construction and Basic Applications (Regression, Classification)

### 1. Introduction to Neural ODEs/CDEs

1.1 Definition of Neural ODEs and CDEs (Xinyan, Tianshi)

- Construction of Neural ODEs and CDEs
- Neural ODEs vs CDEs: Advantages and Disadvantages
- Why Neural ODEs/CDEs may be advantageous compared to other formulations for problems
- Natural cubic splines for continuous path $X_t$

### 2. Solving Neural ODEs/CDEs

2.1 An elaboration of the steps taken to train and solve a Neural ODE/CDE (James)

- Loss Functions and Minima
- Automatic Differentiation
- Gradient Descent and its Applications in Neural ODEs and CDEs

2.2 Back-propagation (Xinyan for ODE, Tianshi for CDE (briefly extend the proof of adjoint method to the CDE case))

- Discretise-then-optimise
- Optimise-then-discretise: Adjoint Equation

2.3 log ODE Method (Xinyan, Tianshi)

- State it for completeness
- Mention that it can be cleverly avoided provided that we choose a continuously differentiable control path

2.4 Numerical Solvers

### 3. An Application (TBC)

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

- Hand-written numbers identification. This is an application of feedforward Neural Network, with n*n pixels input and 10 outputs (numbers 0-9). In gradient descent, finding the optimal minimum efficiently is crucial. If the step size is too large, the algorithm might overshoot the minimum and land at another point, while a step size that is too small can be inefficient and energy-consuming. Therefore, research focuses on finding the appropriate step size to balance efficiency and accuracy.
- Continuous dynamics of financial time series data, such as stock prices and market indices. This is an application of Recurrunt Neural Network. Neural ODEs naturally capture the continuous evolution of market data by embedding neural network architectures within the differential equation solving process. The details would be studied by Tianshi.
