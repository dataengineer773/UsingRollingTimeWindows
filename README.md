Given time series data, you want to calculate some statistic for a rolling time, Rolling (also called moving) time windows are conceptually simple but can be difficult to understand at
first. Imagine we have monthly observations for a stock’s price. It is often useful to have a time window
of a certain number of months and then move over the observations calculating a statistic for all observations in the time window.
For example, if we have a time window of three months and we want a rolling mean, we would
calculate:
1. mean(January, February, March)
2. mean(February, March, April)
3. mean(March, April, May)
4. etc.
Another way to put it: our three-month time window “walks” over the observations, calculating the
window’s mean at each step.
pandas’ rolling allows us to specify the size of the window using window and then quickly calculate
some common statistics, including the max value (max()), mean value (mean()), count of values
(count()), and rolling correlation (corr()).
Rolling means are often used to smooth out time series data because using the mean of the entire time
window dampens the effect of short-term fluctuations.
