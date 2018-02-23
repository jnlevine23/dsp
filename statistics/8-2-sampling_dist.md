[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (sampling distribution)

>> 
```python
def Estimate3(n=10, iters=1000):
    lam = 2

    means = []
    #medians = []
    for _ in range(iters):
        xs = np.random.exponential(1.0/lam, n)
        L = 1 / np.mean(xs)  #Maximum likelihood estimator 
        #Lm = np.log(2) / thinkstats2.Median(xs)
        means.append(L)
        #medians.append(Lm)
        
    print('mean error L:', MeanError(means, lam))
    print('Standard Error L:', RMSE(means, lam))
    #print('mean error Lm:', MeanError(medians, lam))
    #print('rmse Lm:', RMSE(medians, lam))
    
    mean_cdf = thinkstats2.Cdf(means, label='L')
    thinkplot.Cdf(mean_cdf)
    thinkplot.Config(xlabel='Sample Mean', ylabel='CDF', 
                     title='Sampling Distribution of Estimate L')
    
    CI = mean_cdf.Percentile(5), mean_cdf.Percentile(95)
    print("90% Confidence Interval:", CI)
    
Estimate3() 

mean error L: 0.235484021658
Standard Error L: 0.819914907742
90 Percent Confidence Interval: (1.304205954302821, 3.7860329477312624)
```
![sampling_distribution_L](https://github.com/jnlevine23/dsp/blob/master/img/sampling_distribution_L.png?raw=true)
