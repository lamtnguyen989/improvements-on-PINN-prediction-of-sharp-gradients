# Improvements on PINN prediction of sharp gradients processes

The Physics-Informed Neural Network (PINN) is a novel framework introduced in [1] as a low to no data machine learning model that is used to predict physical processes (often encoded as PDEs) numerically. The main advantage that PINNs offered is that they are continuous solvers meaning there will not be a need for domain partitioning procedure that is required by most traditional numerical models.

Despite this, there are limitations however, mostly stem from the **Spectral Bias** problem present with neural networks in general where the network will tend to learn low-frequency (smooth) functions much faster than high-frequency (rapidly varying) functions. Therefore, the repository will be an exploratory project on implementing not only baseline models for predicting behaviors of sharp gradient processes, but also examining research literatures for ways to improve upon the performance of PINNs for such processes as well.

# Case Study

# Models & Improvements

# Summary

# References

[1] M.Raissi, P. Perdikaris, G.E. Karniadakis *Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations.* https://doi.org/10.1016/j.jcp.2018.10.045