[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

> > 
    ##Actual
    pmf = resp.numkdhh
    pmf = thinkstats2.Pmf(pmf, label='actual')
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel='Number of Children', ylabel='Probability',
                    title='Actual Distribution')
                 
    ##Both Actual and Biased plotted on same graph
    biased_pmf = BiasPmf(pmf, 'biased')
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased_pmf])
    thinkplot.Config(xlabel='Number of Children', ylabel='PMF')

    #Compute the means
    print('Actual Mean:', pmf.Mean())
    print('Biased Mean:', biased_pmf.Mean())
    Actual Mean: 1.02420515504
    Biased Mean: 2.40367910066
