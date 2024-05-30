This is the GitHub repository for the MATH50002 Group Research Project (M2R) project on Scientific Machine Learning by Group 29 (James Tay, Jiaru Li, Xinyan Wang, Tianshi Liu, Jiankuan Liu).

## Report Outline
### 1. Introduction to Neural CDE Theory
1.1 Definition of Neural ODEs, Neural CDEs (Xinyan, Tianshi)  
  1.1.1 Construction of Neural ODEs and CDEs (???)  
    1.1.1.1 Neural ODEs vs Neural CDEs: Advantages and Disadvantages  
  1.2.1 Why a Neural ODE/CDE may be advantageous compared to other formulations for problems (and thus using least squares) (Jiaru)  
1.2 Construction of Feedforward Neural Networks/Recurrent Neural Networks (Jiaru)  
  1.2.2 Natural Cubic Splines, for continuous path $X_t$ (???)  
  1.2.3 Other methods (???)  
### 2. Solving Neural ODEs/CDEs
2.1 An elaboration of the steps taken to solve a Neural ODE/CDE - Training the neural differential equation (James)  
  2.1.1 Loss functions and minima  
  2.1.2 Automatic Differentiation  
  2.1.3 Gradient Descent and its applications in Neural ODes and CDEs  
2.1 Back-propagation  
  2.1.1 Discretise-then-optimise  
  2.1.2 Optimise-then-discretise: Adjoint Equation  
2.2 log ODE Method (Xinyan, Tianshi) (do we really need to do this? honestly not sure how useful this is)  
2.3 Numerical Solvers  
### 3. An application: (TBC)




Jiaru Li:
- Description and explanation of neural network (NN) and how it works, based on Lab 5 of SciMLSANUM2024.
- Some simple applications to further illustrate the concepts.
  (1) Regression. Polynomial regression was introduced in the numerical analysis course, and I am going to take the ideas further and discuss nonlinear regression based on NN. Comparison of least squares and NN methods will also be discussed, in order to explore the ways in which NN becomes powerful.
  (2) Number recognition using MNIST. Being a standard example from machine learning, it helps us to discover how NN works in terms of real-world applications.
- Julia code to accompany the ideas. Where appropriate, Python will also be used.

James Tay:
- Extension of automatic differentiation material (dual numbers) covered in the MATH50003 Numerical Analysis course to cover automatic differentiation in higher dimensions.
- Examining the implementations of commonly used Julia modules (Autodiff, Zygote, etc) which make use of (reverse-mode) automatic differentiation based on Labs 2 and 3 of SciMLSANUM2024.
- Working on basic ideas of gradient descent and extending them to more sophisticated methods used in practice (including but not limited to SGD) to locate various minima.
- Currently working on how to apply these methods in solving neural ODEs/CDEs (where applicable) to make them more efficient. Largely working in Julia.
