[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 

```python
import numpy as np
import scipy.stats as stats

mu = 178
sigma = 7.7
distribution = stats.norm(loc=mu, scale=sigma)

low = distribution.cdf(177.8)
high = distribution.cdf(185.42)
print(high - low)
0.342746837631
```
~34% of men are between 5'10" and 6'1".
