17) Write a C program to reverse the accepted number using function.

#include<stdio.h>

// Function to reverse number
int reverseNumber(int n) {
    int rev = 0;

    while (n != 0) {
        rev = rev * 10 + (n % 10);
        n = n / 10;
    }

    return rev;
}