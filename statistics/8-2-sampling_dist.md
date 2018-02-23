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
90% Confidence Interval: (1.304205954302821, 3.7860329477312624)
```
![sampling_distribution_L](https://github.com/jnlevine23/dsp/blob/master/img/sampling_distribution_L.png?raw=true)

```python
Estimate3(50), Estimate3(100), Estimate3(1000)

Standard Error L: 0.302013183816
90% Confidence Interval: (1.6218188396653599, 2.5734541100244526)
Standard Error L: 0.197657315116
90% Confidence Interval: (1.7285799078056903, 2.3604593983632123)
Standard Error L: 0.0640668024407
90% Confidence Interval: (1.8986241627970966, 2.110300289823059)
```
>>As the sample size increases, the standard error approaches 0. Standard error should decrease as the sample size grows larger and the 90& confidence interval should narrow.  
