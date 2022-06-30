# linearRegression
Here, I have built a program for linear regression
There is a single feature input array y, formed by 100 random integers ranging from 0 to 100.


The output Y array is defined as: y = (x/2)**2 + 5*(x/3) + 7


m = x*y.mean() - x.mean()*y.mean()/x*x.mean() - x.mean()*x.mean()


c = y.mean() - mx.mean()


Then I have calculated the score for the predicted values of y as:


Score = Score (COD) = 1 - (Σyitrue - yipredicted)/(Σyitrue - yimean)


The result of my findings is: 


m = 26.25812363672978


c = -353.083439176678


Test score = 0.9198879743215916
