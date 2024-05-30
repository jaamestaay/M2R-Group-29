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

2.2 Back-propagation (Xinyan)

- Discretise-then-optimise
- Optimise-then-discretise: Adjoint Equation

2.3 log ODE Method (Xinyan, Tianshi) (*do we really need to do this? honestly not sure how useful this is*)

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
