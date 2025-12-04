# MEAN-VARIANCE-AND-CROSS-CORRELATION
 Simulation of Mean and Variance Using Scilab
 # Aim
To write a program for mean, variance, and cross-correlation in Scilab and verify the output.

# Equipment Needed
Computer with i3 Processor
Scilab Software
# Algorithm
Define the Function: Specify the function you want to simulate.
Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance, and Cross-Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results: Output the computed mean, variance, and cross-correlation.
# Procedure
Refer to the algorithm and write code for the experiment.
Open Scilab on your system.
Type your code in a new editor.
Save the file.
Execute the code.
If any errors occur, correct the code and execute again.
Verify the generated results.

Program
```
clear; clc;
function X = f(x)
    z = 2*(2 - x).^2;
    X = x .* z;
endfunction
a = 0; b = 1;
EX = intg(a, b, f);
function Y = c(y)
    z = (3 - y).^2;
    Y = y .* z;
endfunction
EY = intg(a, b, c);
function X2 = g(x)
    z = 2*(2 - x).^2;
    X2 = (x.^2) .* z;
endfunction
EX2 = intg(a, b, g);
function Y2 = h(y)
    z = (5 - y).^2;
    Y2 = (y.^2) .* z;
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
disp(EX, "i) Mean of X =");
disp(EY, "   Mean of Y =");
disp(vX2, "ii) Variance of X =");
disp(vY2, "   Variance of Y =");
x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```
OUTPUT

<img width="500" height="300" alt="Screenshot 2025-11-23 103140" src="https://github.com/user-attachments/assets/b2300ab6-696a-4519-bed4-8370fe052957" />

MANUAL CALCULATION:

<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/422c53a3-59e4-44aa-b0fe-fc63568f06cb" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/449413e9-1e8d-483e-b68f-299705fb15b6" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/681c4da9-ac34-48fb-b6a8-c1c53445c599" />



RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
