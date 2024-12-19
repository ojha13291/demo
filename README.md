# demo
This is my first git repos .
<br>
Author - Ayush Kumar 

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main()
{
    float a, b, c, disc;
    float root1, root2, real, imag;

    printf("Enter a, b, c values\n");
    scanf("%f%f%f", &a, &b, &c);

    if ((a == 0) && (b == 0))
    {
        printf("Invalid coefficients\n");
        printf("Try again with valid inputs!!!!\n");
    }
    else if (a == 0)
    {
        printf("Linear equation\n");
        root1 = -c / b;
        printf("Root = %3f\n", root1);
    }
    else
    {
        disc = b * b - 4 * a * c;
        if (disc == 0)
        {
            printf("The roots are real and equal\n");
            root1 = root2 = -b / (2 * a);
            printf("Root1 = %3f\nRoot2 = %3f\n", root1, root2);
        }
        else if (disc > 0)
        {
            printf("The roots are real and distinct\n");
            root1 = (-b + sqrt(disc)) / (2 * a);
            root2 = (-b - sqrt(disc)) / (2 * a);
            printf("Root1 = %3f\nRoot2 = %3f\n", root1, root2);
        }
        else
        {
            printf("The roots are imaginary\n");
            real = -b / (2 * a);
            imag = sqrt(fabs(disc)) / (2 * a);
            printf("Root1 = %3f + %3fi\n", real, imag);
            printf("Root2 = %3f - %3fi\n", real, imag);
        }
    }
    return 0;
}
