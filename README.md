# linearRegression
Linear Regression
Let’s have three features: x1, x2, x3 and output y, linear regression says that: 
y = m1x1 + m2x2 + m3x3 + b
The plot of the linear regression algorithm is as follows:

Coefficient of Determination
Coefficient of determination is given as: 
Score (COD) = 1 - (ΣyiT - yip)/(ΣyiT - yimean)
Here the numerator depicts the actual error and the denominator depicts the worst error prediction if we predict all the outputs as the mean value of outputs. This score generally lies between 0 and 1, higher the value, better the prediction. The score can also go negative if the value of actual error is worse than if we predict every value as the mean value.





Cost Function
Let’s consider the following plot:


Here we can easily observe that line B would be a better fit line or better estimation than line A. But the real question is how can we find the best fit line. This can be understood by the concept of error function.

Let there be a dataset with n features and m entries. The best feature line can be written as:
1mΣ m1xi1 + m2xi2 + m3xi3 + … mnxin + c
Here, (m1xi1 + m2xi2 + m3xi3 + … mnxin + c) is for the ith entry which is summated for all the m entries.

Now the error function is written as: 
1mΣ yip - (m1xi1 + m2xi2 + m3xi3 + … mnxin + c)
But there is a fundamental issue while using the above equation for calculating the best fit line as the positive errors can reduce or negate the negative errors and we would get a faulty best fit line.



So a better cost/error function will be:
CF = 1mΣ (yip - (m1xi1 + m2xi2 + m3xi3 + … mnxin + c))2
When we square the terms then all errors are positive and also not linearly dependent, this helps us to generate the best fit line.
Calculation of best fit line
We know that cost function can be written as:
CF = 1mΣ (yip - (mxi + c))2
Now let’s calculate the partial differential of the cost function (CF) with m and with c.
∂CF/∂m = 1mΣ ∂(yip - (mxi + c))2/∂m
∂CF/∂m = 1mΣ 2(yip - (mxi + c))(-xi)
Putting ∂CF/∂m = 0 we get:
1mΣ yipxi - mxi2 + cxi = 0 
Dividing by N, we get:
1mΣ yipxi/N - 1mΣmxi2/N + 1mΣcxi/N = 0 
yx.mean() - mx.mean() + cx.mean() =0 ---> eq 1
Similarly finding ∂CF/∂c:
∂CF/∂c = 1mΣ ∂(yip - (mxi + c))2/∂c
∂CF/∂c = 1mΣ 2(yip - (mxi + c))
Putting ∂CF/∂m = 0 we get:
1mΣ yip - mxi - c = 0 


Dividing by N, we get:
1mΣ yip/N - 1mΣmxi/N - 1mΣc/N = 0 
y.mean() - mx.mean() - c =0 ---> eq 2
By solving eq 1 and 2 we get,
c = y.mean() - mx.mean() and,
m = xy.mean() - x.mean()y.mean()/x2.mean() - x.mean()2
