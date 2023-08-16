# Differential-Equation
Solving Partial Differential Equation Using Artificial Neural Network

# Objective
- To implement paper by lagarest et al on how to use artificial neural network for solving differential equation.
- Implemented using Tensorflow
- Learned about how to create custom loss
- Learned how to work with tf.GradientTape()
# Learning

- Consider the first order ODE: dΨ(x)/dx = f(x, Ψ) (1)
- with x ∈ [0, 1] and with the Initial Condition Ψ(0) = A.
- A trial solution is written as: Ψtrial(x) = A + xN(x, p)
- where N(x, p) is the output of a ANN with one input unit for x and weights p.
- Now all we need is a loss function, Ψtrial(x) is the solution of the differential equation 
```
d Ψtrial(x) /dx ≈ f(x, Ψtrial) 
d Ψtrial(x) /dx - f(x, Ψtrial) ≈ 0 (2)
```

- we are trying to do is get (2) close to zero, then our trial solution approximates the analytical solution to a great accuracy.

- So we define the loss function as:

```
LOSS = ∑{ (d Ψtrial(x) /dx) - f(x, Ψtrial) }2    for all x ∈ [0, 1]
```

# Results :

- Comparision between Acutal and Predicted

  ![download](https://github.com/deep-gtm/Differential-Equation/assets/70434931/b0235e49-644f-4fc2-a651-17503fd6a7d5)

# Loss :

![download (1)](https://github.com/deep-gtm/Differential-Equation/assets/70434931/7b7002d7-a43e-44f1-9b8d-8e699a83060d)
