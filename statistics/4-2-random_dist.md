[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

> > 
```python
random = np.random.random(1000)

# PMF Plot
random = np.random.random(1000)
random_pmf = thinkstats2.Pmf(random) 
thinkplot.Pmf(random_pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random Variable', ylabel='PMF')

# CDF Plot
random_cdf = thinkstats2.Cdf(random)
thinkplot.Cdf(random_cdf, label='Random Sample')
thinkplot.Config(xlabel='Random Variable', ylabel='CDF')
```

The CDF is a straight line, meaning the distribution is uniform. 
Regarding the PMF, the distribution becomes hard to analyze when there
are a large amount of values. There is a ton of random noise because the 
probability of each value is small. In this case, a CDF is easier to work 
with and interpret. 
