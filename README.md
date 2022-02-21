# portfolio_management_with_R
An application of Rockafellar and Uryasev (2000) using real financial data, a GJR-GARCH model for margins, and copulas to model their dependence structure. 

## 1) portfolio_optimization
In the "portfolio_optimization" notebook, I illustrate the whole process followed to solve the portfolio optimization problem as suggested by Rockafellar and Uryasev (2000). This methodology requires the simulation of a large number of tomorrow return series. To do this, I use a GJR-GARCH (1,1,1) with Skewed-t errors and a C-Vine copula.

In short, the problem that I solve here is the following. We have d stocks and want to conform a portfolio of them, that is, we need to decide the proportion of our wealth that w_{i,t} that will be invested in each stock. How do we choose this allocation? We choose the portfolio strategy that minimizes market risk.

## 2) rolling_window_evaluation
In this notebook, I evaluate the portfolio performance using the approach illustrated in 1). Specifically, I compute the evolution of wealth by hypothetically investing $100 at day t=0. The evolution of wealth is given by  
```math
W_{t+1}=W_t(1 + w_{1,t}r_{1,t}+w_{2,t}r_{2,t}+...+w_{d,t}r_{d,t})
```
where 
 
```math
W_0=100
```
 
