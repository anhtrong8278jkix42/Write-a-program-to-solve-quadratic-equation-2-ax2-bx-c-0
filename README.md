# Write-a-program-to-solve-quadratic-equation-2-ax2-bx-c-0
Write a program to solve quadratic equation 2: ax2 + bx + c = 0
import math
 
"""
# Solve quadratic equation 2: ax2 + bx + c = 0
# @param a: coefficient of order 2
# @param b: coefficient of order 1
# @param c: free term
"""
def giaPTBac2(a, b, c):
    # check the coefficients
    if (a == 0):
        if (b == 0):
            print("Equation has no solution!");
        else:
            print("Equation has one solution: x = ", + (-c / b));
        return;
 
    # calculate delta
    delta = b * b - 4 * a * c;
    # calculation
    if (delta > 0):
        x1 = (float)((-b + math.sqrt(delta)) / (2 * a));
        x2 = (float)((-b - math.sqrt(delta)) / (2 * a));
        print ("Equation has 2 solutions: x1 = ", x1, " and x2 = ", x2));
    elif (delta == 0):
        x1 = (-b / (2 * a));
        print("Equation with double solutions: x1 = x2 = ", x1);
    else:
        print("Equation has no solution!");
 
# Enter coefficients
a = float(input("Enter the quadratic factor, a = "));
b = float(input("Enter the coefficient of order 1, b = "));
c = float(input("Enter a free constant, Python = "));
# Call the function to solve the quadratic equation
stagePTBac2(a, b, c)
