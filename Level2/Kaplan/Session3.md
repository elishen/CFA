### SS3 R9 

# Correlation and Regression 

$$ COV = \frac {\sum_{t=1}^{n} (X_{t,1} - \bar X_1) (X_{t,2} - \bar X_2)}{n-1}
$$

$$ corr = \frac {cov_{1,2}}{s_1s_2}$$

### Limitations to Correlation Analysis

* Outliers
* Spurious correlation
* Nonlinear dependency

### Correlation Test: 2-tailed t-test

* $$H_0: correlation = 0$$

* Sample correlation
* n pairs of observations
* Test statistic: 

$$ t = \frac {r \sqrt{n-2} }{\sqrt { 1-r^2}}$$

$$t\uparrow$$, if $$r\uparrow$$ and/or $$n\uparrow$$

Reject $H_0$ if |computed t| > | critical t|

### Linear Regression 

* Assumptions: 
	* Linear relations between X and y
	* Independent variable uncorrelated with error term
	* Expected value of error term is zero
	* Variance of the error term is constant
	* Error term is independently distributed
	* Error term is normally distributed 

### Regression Coefficient t-test

* A test of statistical significance (slope $\ne$ 0) 
* 

$$ 
H_0: b_i = 0 $$ vs. $$H_a : b_i \ne 0
$$

* Use t-test with (n-k-1) DoF. 

$$ t_{b_i} = \frac {\hat {b_i} - b_i} {S_{b_i}} \\
= \frac {estimate - pypothesized} { std\ error } \\
= \frac {\hat {b_i} - 0} {s_{b_i}} \\
= \frac {slope} {std\ error} 
$$

* Standard Error: $$ \sigma / \sqrt{n}$$

* Confidence Interval of estimated $$\beta$$ : 
$$ \hat{b} \pm $$ critical t $$ \times s_{b_i}$$


* Confidence Interval of Predicted Y


$$ \hat {Y} \pm (t_c \times std\ error \ of\ forecast) \\
s_f^2 = SEE^2 \Big[ 1 + \frac{1}{n} + \frac {(X - \bar {X})^2} {(n-1)S_x^2} \Big]
$$

* Critical t is 2-tailed with n-2 DoF

* For large samples, $$s_f$$ can be approximated by SEE. 

### ANOVA (analysis of Variance)

* Total Variation = Explained + unexplained 

$$ SST = RSS + SSE $$

* Sum of squared total: 
* Residual sum of squares: $$\sum (\hat {Y_i} - \bar {Y})^2$$
* Sum of squared errors: $$\sum (Y_i - \hat{Y_i}) ^2$$

* **MSR** Mean squared regression: RSS / k

* **MSE** Mean squared error: SSE / (n-k-1)

* Degree of Freedom for SST is n-1: n-k-1 + k

### SEE 


* SEE measures accuracy of predicted values from regression equation. SEE $\downarrow$, Model Accuracy $\uparrow$. 

$$ SEE = \sqrt {SSE} {n-k-1} = \sqrt {MSE} = \sigma_{\epsilon} $$

### the coefficient of determination ($$R^2$$)

* $$R^2$$ measures percentage of total variation in dependent variable explained by independent variables. 

* from 0 to 1

* measures of the goodness of fit


$$ R^2 = RSS / SST$$

* For simple linear regression (k=1), $$ R^2 = (r_{XY})^2$$


### Limitations of Regression

* Relationships change over time (parameter instability) 
* Public knowledge of relationships eliminate usefulness 
* Assumption violations:

	
### SS3 R10

# Multiple Regression 

### Example: Hedge Fund Returns 

* Small Cap stocks (WSC)
* High-yield bonds (HYB)
* Emerging markets (IFC)

The t-test shows p-value for HYB is 0.137. Cannot reject $$H_0$$. HFR not influeced by HYB. 

### p-Values

* The probability that the computed value is greater than the critical value, $$p < \alpha$$

* the smallest significance level at which we can reject $$H_0$$










