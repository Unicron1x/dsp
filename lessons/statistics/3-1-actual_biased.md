[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> resp = nsfg.ReadFemResp()

num_children = resp['numkdhh']

pmf1= thinkstats2.Pmf(num_children, label = 'numkdhh')

thinkplot.Pmf(pmf1)
thinkplot.Config(xlabel='Num of Kids', ylable='Probability')







Biased_PMF = BiasPmf(pmf1, label = 'observations')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf1, Biased_PMF])
thinkplot.Show(xlabel='class size', ylabel='PMF')

mean_actual = pmf1.Mean()
mean_biased = Biased_PMF.Mean()
print('actual mean:{}, biased mean:{}'.format(mean_actual, mean_biased))



