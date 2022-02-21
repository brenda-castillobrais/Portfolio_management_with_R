# portfolio_management_with_R
An application of Rockafellar and Uryasev (2000) using real financial data, a GJR-GARCH model for margins, and copulas to model their dependence structure. 

## 1) portfolio_optimization
In the "portfolio_optimization" notebook, I illustrate the whole process followed to solve the portfolio optimization problem as suggested by Rockafellar and Uryasev (2000). This methodology requires the simulation of a large number of tomorrow return series. To do this, I use a GJR-GARCH (1,1,1) with Skewed-t errors and a C-Vine copula.

## 2) rolling_window_evaluation
In this notebook, I evaluate the portfolio performance using the approach illustrated in 1). Specifically, I compute the evolution of wealth by hypothetically investing \$100 at day $t_0$. The evolution of wealth is given by  
```math
W_{t+1}=W_t(1 + w_{1,t}r_{1,t}+w_{2,t}r_{2,t}+...+w_{d,t}r_{d,t})
```
where 
 
```math
W_0=100
```
 
