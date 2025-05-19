# Improvements on PINN prediction of sharp gradients processes

The Physics-Informed Neural Network (PINN) is a novel framework introduced in [1] as a low to no data machine learning model that is used to predict physical processes (often encoded as PDEs) numerically by incorporated the physics of the process into the training. The main advantage that PINNs offered is that they are continuous solvers meaning there will not be a need for domain partitioning procedure that is required by most traditional numerical models.

Despite this, there are limitations however, mostly stem from the **Spectral Bias problem** present with neural networks in general where the network will tend to learn low-frequency (smooth) functions much faster than high-frequency (rapidly varying) functions. Therefore, the repository will be an exploratory project on implementing not only baseline models for predicting behaviors of sharp gradient processes, but also examining research literatures for ways to improve upon the performance of PINNs for such processes as well.

# Results

Investigating the 1-dimensional Burger's equation

$$ \begin{aligned} \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} - \nu  \frac{\partial^2 u}{\partial x^2} = 0 \end{aligned}$$

where the viscocity parameter $\nu = 0.001$ on the spatial domain $x \in [-1,1]$ with time-evolution $t \in [0,1]$ and boundary conditions

$$u(x,0) = -\sin(\pi x) \qquad \qquad u(-1,t) = u(1,t) = 0  $$

we were able to implement an improvement on the vanilla PINN model that reduce the Mean Absolute Error from 0.1995 to 0.0757 and the maximum  pointwise absolute error decreased from 0.8565 to 0.5531 which is about 62% and 35% improvements, respectively.

For more in-depth explainations and methodologies, see `findings.pdf` in the respectives equations and of course, check out the codes!