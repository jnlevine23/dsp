[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> 
```python
#Mean and Median
cdf.Mean(), cdf.Percentile(50)
(74278.707531187552, 51226.454478940461)
#mean is much greater than median indicating a positive skew 

#Skewness and Pearson's Skewness
Skewness(sample), PearsonMedianSkewness(sample) 
(4.9499202444295829, 0.7361258019141782)  #Distribution is positively skewed 

#What fraction of households report a taxable income below the mean?
cdf.PercentileRank(74278.707531187552)
66.000587956687198  #~66% report a taxable income less than the mean 

#What happens to skew if the upper bound is 10 million?
cdf = thinkstats2.Cdf(sample)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Household income ($)',
                 ylabel='CDF', 
                 title='Household Income Log10 Scale, Upper Bound = 7.0')
```
![](download.png)
