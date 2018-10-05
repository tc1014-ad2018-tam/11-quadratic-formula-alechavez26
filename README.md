# 11-quadratic-formula-alechavez26
11-quadratic-formula-alechavez26 created by GitHub Classroom
/* This program will help the user to solve a quadratic formula.
 *
 * Alejandra Chávez Cruz
 * A01411970@itesm.mx
 * 04/oct/18
 * */

#include <stdio.h>
#include <math.h>

// I write a function for when subtracted in the general formula
(double a, double b, double c){
    double xmn = 0;
    xmn = ((0-b) - (sqrt(pow(b,2) - (4*a*c)))) / (2*a);
    return xmn;
}
//I write a function for when added in the general formula
double discmas (double a, double b, double c) {
    double xms = 0;
    xms = ((0-b) + (sqrt(pow(b,2) - (4*a*c)))) / (2*a);
    return xms;
}

int main() {
    //Declare
    double a;
    double b;
    double c;
    double xmn;
    double xms; 

    printf("Hi. Im gonna help you solve the quadratic formula.\n");
    printf("First you only have to give me values for a, b, and c, and separate them with a coma:\n"); 
    scanf("%lf, %lf, %lf", &a, &b, &c);
    while (a == 0) {        
        printf("Can't use that number! Give me another one.\n");
        scanf("%lf", &a);
    }

    // Here the functions 
    xmn = discmenos(a, b, c);
    xms = discmas(a, b, c);

    // If the problem cant be resolve i tell to the user
    if (pow(b, 2) < 4*a*c) {
        printf("I can't solve the root of a negative number!\n");
    } else {
        printf("When subtracting the root, the value of x is: %lf\n", xmn);
        printf("When adding up the root, the value of x is: %lf", xms);  
    }

    return 0;
}
