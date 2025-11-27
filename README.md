# Mean, Variance and Cross Correlation



AIM:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:

Mean:The average value of a set of data or signal
Variance:How far the data values spread out from the mean
Cross-Correlation:A measure of similarity between two signals at different time shifts

Algorithm
1. Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function. 2. Generate Sample Points: Decide on the range and the number of sample points. Generate
these sample points within the desired range. 3. Evaluate the Function: Compute the function values at each of these sample points. 4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the
mean and variance of the computed function values. 5. Display Results: Output the computed mean variance and Cross Correlation

PROGRAM
 clear;
 clc;
 clear;
 //Mean Value
 function X=f(x), z=3*(1-x)^2,//Marginal Probability Density Function X=x*z
 endfunction
 a=0;
 b=1;
 EX=intg(a,b,f);//Mean value of X
 function Y=c(y)
 z=3*(1-y)^2,//Marginal Probability Density Function Y=y*z
 endfunction
 EY=intg(a,b,c);//Mean value of Y
 disp(EX,"i)Mean of X =")
 disp(EY," Mean of Y =")
 Variance
 function X=g(x), z=3*(1-x)^2,//Marginal Probability Density Function
 X=x^2*z
 endfunction
 a=0;
 b=1;
 EX2=intg(a,b,g);
 function Y=h(y)
 z=3*(1-y)^2,//Marginal Probability Density Function
 Y=y^2*z
 endfunction
 EY2=intg(a,b,h);
 vX2=EX2-(EX)^2;//Variance of X
 vY2=EY2-(EY)^2;//Variance of Y
 disp(vX2,"ii)Variance of X");
 disp(vY2," Variance of Y");
 Cross Correlation
 x= input("type in the reference sequence=");
 y= input("type in the second sequence=");
 n1=max(size(y))-1;
 n2=max(size(x))-1;
 r=corr(x,y,n1);
 plot2d3('gnn',r);

Calculation

i)Mean of X = 0.25
Mean of Y = 0.25
ii) Variance of X 0.0375
Variance of Y 0.0375
Cross Correlation
Type in the reference sequence = [1 2 3 4 5 6 7 8]
Type in the second sequence = [2 1 3 5 6 3 5 9]

Output Waveform


<img width="756" height="647" alt="image" src="https://github.com/user-attachments/assets/e484ff43-49f5-4154-8e63-1726420adb4a" />


RESULT:
Thus, the mean, variance and cross correlation are executed in Scilab and output is verified
