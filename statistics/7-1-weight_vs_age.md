[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> 
```python
import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])

#Scatter Plot 
age = live.agepreg
weights = live.totalwgt_lb
thinkplot.Scatter(weights, age, alpha=0.1, s=10)
thinkplot.Config(xlabel='Birth Weight (lbs)', ylabel="Mother's Age",
                legend=False, title='Birth Weight vs Age of Mother')
```
![scatter_plot](https://github.com/jnlevine23/dsp/blob/master/img/scatter.png?raw=true)
```python
#Pearson Correlation 
Corr(weights, age)
0.06883397035410907

#Spearman Correlation 
SpearmanCorr(weights, age)
0.0020914571012349815
```
>> There is virtually no correlation between these two variables. This makes sense, the age of the mother giving birth should have no effect on the weight of her child. 
