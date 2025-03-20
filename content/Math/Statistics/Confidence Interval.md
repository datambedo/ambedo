1. Take a sample from a population
2. Calculate the *sample mean*
3. Construct $100(1-\alpha)\%$ confidence interval
    1. For a sufficiently large sample, the sample mean follows normal distribution, see ([[5) Limit Theorems#5.4 Central Limit Theorem (CLT)]])
    2. Use standard normal variable transformation $$\frac{\bar X - \mu}{\sigma / \sqrt n} \approx N(0,1)$$
    3. CI: $\bar x \pm z_{\alpha/2} \frac{\sigma}{\sqrt n}$ 
**Interpretation**
> If we take *many* independent random samples from a population, and construct many 90% confidence intervals, then we expect 90% of the intervals to contain the *true* population mean.

![[Pasted image 20250311160708.png]]