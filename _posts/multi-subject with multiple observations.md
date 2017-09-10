# multi-subject with multiple observations
I have N subjects and I observed each of them once, resulting two variables: x and y.
I can do a correlation analysis on these N (x,y) values and obtain a r(N) value.
This has no problem.
Now I observe these N subjects b(>1) times, and I have N*b (x,y) values.
I have two choices:
- for each of the N subjects, I get a mean value of x and y from the b times of observations, and calculate the correlation: r(N).
- or I calculate the correlation of N*b (x,y) values, and have r(N*b).
It is easy to argue that the second choice incorrectly increased the power. However the first choice will lose some of the information and I don't like it either.
Now how should I correct the second choice, and make it statistically acceptable?
