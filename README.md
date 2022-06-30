# 1. Linear Regression from Scratch
Here, I have built a program for linear regression

There is a single feature input array x, formed by 100 random integers ranging from 0 to 100.The output y array is defined as: y = (x/2)**2 + 5*(x/3) + 7

m = x*y.mean() - x.mean()*y.mean()/x*x.mean() - x.mean()*x.mean()

c = y.mean() - m*x.mean()

Then I have calculated the score for the predicted values of y as:

Score = Score (COD) = 1 - (Σytrue - ypredicted)/(Σytrue - ymean)

The result of my findings is: 

m = 26.25812363672978

c = -353.083439176678

Test score = 0.9198879743215916

# 2. Linear Regression on diabetes dataset

10 input features, such as age, sex, bmi, s1-->6

Output value: quantitative measure of disease progression one year after baseline

Test score: 0.5335396935584695 (Not so great)
