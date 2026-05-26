16) Write a C program to demonstrations functions call by value and call by references.

#include<stdio.h>

// Call by Value
void callByValue(int x, int y) {
    int temp;
    temp = x;
    x = y;
    y = temp;

    printf("Inside callByValue: x = %d, y = %d\n",x, y);
}

// Call by Reference
void callByReference(int *x, int *y) {
    int temp;
    temp = *x;
    *x = *y;
    *y = temp;
    printf("Inside callByReference: x = %d, y = %d\n", *x, *y);
}