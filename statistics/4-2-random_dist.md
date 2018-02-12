[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 
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

