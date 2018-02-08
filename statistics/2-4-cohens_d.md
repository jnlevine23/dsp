[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

> > 
    #Means of each group 
    firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
    (7.201094430437772, 7.325855614973262)

    def CohenEffectSize(group1, group2):
        """Computes Cohen's effect size for two groups.
    
        group1: Series or DataFrame
        group2: Series or DataFrame
    
        returns: float if the arguments are Series;
             Series if the arguments are DataFrames
        """
        diff = group1.mean() - group2.mean()

        var1 = group1.var()
        var2 = group2.var()
        n1, n2 = len(group1), len(group2)

        pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
        d = diff / np.sqrt(pooled_var) #the pooled standard deviation 
        return d
    
        CohenEffectSize(others.totalwgt_lb, firsts.totalwgt_lb)
        0.0886729
        
    
    
    It seems first babies are very slightly lighter than others. According to Cohen's d, the difference in means between 
    the two groups is 0.089 standard deviations. This is a small difference, however it is still a difference and shows 
    that other babies tend to be a bit heavier than first babies on average. 
    This is slightly larger than Cohen's d for the difference in pregnancy lengths. There seems to be a greater difference 
    in the weights between the first and other babies compared to the difference in pregnancy lengths. Still, Cohen's d for 
    both birth weights and pregnancy lengths is quite small and is most likely a negligible statistic unless one is observing 
    a massive amount of pregnancies. 

