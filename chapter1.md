# Background you will need for PGM
## Probability
__Expectation and Conditional Expectation__
> For discrete variables
$$
E(X) = \sum_{x\in X}x \cdot p(x)
$$
For continuous variables
$$
E(X) = \int_{x}x \cdot p(x) dx
$$
Conditional Expextation
$$
E(X|y) = \int_x x\cdot p(x|y)dx
$$

__Variance, Covariance, Covariance Matrix and Correlation__
> The variance of a RV X    
$$
\begin{aligned}
\delta_X^2=Var(X) &= \int_x[x-E(X)]^2\cdot p(x)dx
\\
&=E(X^2)-E^2(X)
\end{aligned}
$$
Conditional variance
$$
\begin{aligned}
\delta_{X|y}^2 = Var(X|y)&=\int_x[x-E(X|y)]^2\cdot p(x|y)dx
\\
&=E(X^2|y)-E^2(X|y)
\end{aligned}
$$
Covariance of RV X and Y
$$
\begin{aligned}
\sigma_{XY}^2&=E[(x-E(X))\cdot (y-E(Y))]\\
&=E(XY)-E(X)E(Y)
\end{aligned}
$$
Covariance Matrix for random vector $X^{N\times1}$
$$
\begin{aligned}
\Sigma_X^{N\times N}&=E[(x-E(X))(x-E(X))^T]\\&=E(XX^T)-E(X)E^T(X)
\end{aligned}
$$
The diagonal is variance and the off diagonal is covariance.    
Correlation between X and Y   
$$
\rho_{XY} = \frac{\sigma^2_{XY}}{\sigma_X\cdot\sigma_Y}\, -1\leq\rho_{XY}\leq1
$$

__Probability Rules__
> Product Rule
$$
p(X,Y)=p(X|Y)p(Y)
$$
Chain Rule
$$
p(A,B,C)=p(A)p(B|A)p(C|B,A)
$$
Conditional Chain Rule
$$
p(A,B,C|D,E)=p(A|D,E)p(B|A,D,E)p(c|A,B,D,E)
$$
This run can be used for sequential data.
Union Rule
$$
p(X\cup Y) = p(x)+p(y)-p(X,Y)
$$
if $X$ and $Y$ are mutually exclusive
$$
p(X\cup Y) = p(x)+p(y)
$$
Sum Rule
$$
p(X)=\sum_Y p(X,Y)
$$     

__Bayes' Rule__
> $$
p(X|Y) = \frac{p(X)p(Y|X)}{p(Y)}
$$
where $p(X|Y)$ is called posterior probability of $X$, $p(X)$ is called prior probability of $X$, $p(Y|X)$ is called likelihood of $X$ and $p(Y)$ is caled the probability of evidence.    
This can be further written as 
$$
p(H|E_1,E_2) = \frac{p(H|E_1)p(E_2|H,E_1)}{p(E_2|E_1)}=\frac{p(H|E_1)p(E_2|H,E_1)}{\sum_H p(E_2|H,E_1)p(H|E_1)}
$$
==if $E_1,E_2$ are conditionally independent given $H$, we have==
$$
p(H|E_1,E_2) = \frac{p(H|E_1)p(E_2|H)}{\sum_H p(E_2|H)p(H|E_1)}
$$
## Optimization