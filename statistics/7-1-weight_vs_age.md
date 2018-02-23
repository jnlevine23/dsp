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

