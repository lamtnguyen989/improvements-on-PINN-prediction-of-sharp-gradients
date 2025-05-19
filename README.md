# Improvements on PINN prediction of sharp gradients processes

The Physics-Informed Neural Network (PINN) is a novel framework introduced in [1] as a low to no data machine learning model that is used to predict physical processes (often encoded as PDEs) numerically. The main advantage that PINNs offered is that they are continuous solvers meaning there will not be a need for domain partitioning procedure that is required by most traditional numerical models.

Despite this, there are limitations however, mostly stem from the **Spectral Bias** problem present with neural networks in general where the network will tend to learn low-frequency (smooth) functions much faster than high-frequency (rapidly varying) functions. Therefore, the repository will be an exploratory project on implementing not only baseline models for predicting behaviors of sharp gradient processes, but also examining research literatures for ways to improve upon the performance of PINNs for such processes as well.

# Case Study

We will primarily be investigating the performance of the PINN on the 1-dimensional Burger's equation

$$ \begin{aligned} \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} - \nu  \frac{\partial^2 u}{\partial x^2} = 0 \end{aligned}$$

where the viscocity parameter $\nu  \to  0$. More specifically, as [1] points out for $\nu < 0.01$, the solution approaches the inviscid case where the shock is not diffused out therefore standard PINNs will fail to converge to the correct solution, so it is suffices to set $\nu = 0.001$ for the investigation.

In particular for benchmarking, we will compare the model's performance against the analytical solution on the spatial domain $x \in [-1,1]$ with time-evolution $t \in [0,1]$ and boundary conditions

$$u(x,0) = -\sin(\pi x) \qquad u(-1,t) = u(1,t) = 0  $$

# Models & Improvements

# Summary & Remarks

# References

[1] M.Raissi, P. Perdikaris, G.E. Karniadakis. *Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations.* https://doi.org/10.1016/j.jcp.2018.10.045