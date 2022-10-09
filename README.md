### 2D/3V Flux-reconstructed Discontinuous Galerkin Fast Spectral (DGFS)
is an open-source software code for solving single/multi-species Boltzmann equation and related kinetic models for gas flows. It is designed for CUDA-enabled GPUs 
and applies the high-order flux-reconstructed discontinuous Galerkin schemes. The primary codebase for the DGFS has been originally developed by Dr. Shashank Jaiswall as part of his PhD dissertation research supported under the NSF award "CDS&E: DEterministic Evaluation of Kinetic Boltzmann equation with Spectral H/p/v Accuracy".  

TheBotzmann equation for gas flows describes the evolution of the gas molecular velocity distribution function $f=f(t, vec{x},\vec{v})$: 

The collision integral calculations use two methodologies: 
* the explicit fast spectral schemes for full Boltzmann **[Gamba 2017, Jaiswal 2019a, Jaiswal 2019b]**. The method applies to general collision kernels, and the results can be "directly" compared with the DSMC without need of any recalibration or parametric fitting.  
* the implicit schemes for linear kinetic models  **[Dimarco 2013, Dimarco 2017]**

The time integration is performed via: 
* 1st/2nd order explicit Strong Stability Preserving (SSP) Runge Kutta (RK) schemes
* 1st/2nd/3rd order implicit-explicit Ascher-Ruuth-Spiteri (ARS) and backward-difference (BDF) schemes  

The overall schemes are simple from mathematical and implementation perspective; highly accurate in both physical and velocity spaces as well as time; robust, i.e. applicable for general geometry and spatial mesh; exhibits nearly linear parallel scaling; and directly applies to general collision kernels needed for high fidelity flow modelling.  

### References:
* **[Gamba 2017]** Gamba, I. M., Haack, J. R., Hauck, C. D., & Hu, J. (2017). 
  *A fast spectral method for the Boltzmann collision operator with general collision kernels.* SIAM Journal on Scientific Computing, 39(4), B658-B674.
* **[Dimarco 2013]** Dimarco, G., & Pareschi, L. (2013). 
  *Asymptotic preserving implicit-explicit Runge--Kutta methods for nonlinear kinetic equations.* SIAM Journal on Numerical Analysis, 51(2), 1064-1087.
* **[Dimarco 2017]** Dimarco, G., & Pareschi, L. (2017). 
  *Implicit-explicit linear multistep methods for stiff kinetic equations.* SIAM Journal on Numerical Analysis, 55(2), 664-690.
* **[Jaiswal 2019a]** Jaiswal, S., Alexeenko, A. A., and Hu, J. (2019)
  *A discontinuous Galerkin fast spectral method for the full Boltzmann equation with general collision kernels.* Journal of Computational Physics 378: 178-208. https://doi.org/10.1016/j.jcp.2018.11.001
* **[Jaiswal 2019b]** Jaiswal, S., Alexeenko, A. A., and Hu, J. (2019)
  *A discontinuous Galerkin fast spectral method for the multi-species full Boltzmann equation.* Computer Methods in Applied Mechanics and Engineering 352: 56-84. https://doi.org/10.1016/j.cma.2019.04.015
* **[Jaiswal 2019d]** Jaiswal, S., Pikus, A., Strongrich A., Sebastiao I. B., Hu, J., and Alexeenko, A. A. (2019)
  *Quantification of thermally-driven flows in microsystems using Boltzmann equation in deterministic and stochastic context.* Physics of Fluids 31(8): 082002. https://doi.org/10.1063/1.5108665

### License:
*DGFS* is released as GNU GPLv2 open-source software. 
This code has been derived from "PyFR". Please see licenses folder for restrictions.


