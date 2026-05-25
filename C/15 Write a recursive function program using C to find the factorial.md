15) Write a recursive function program using C to find the factorial value of any number entered through the keyboard.

#include<stdio.h>

// Recursive function
int factorial (int n) {
    if (n == 0 || n == 1)
        return 1;
    else
        return n * factorial (n -1); //Recursive call
}

int main() {
    int num, result;

    // Input number
    printf("Enter a number: ");
    scanf("%d", &num);

    // Check for negative number
    if (num < 0) {
        printf("Factorial not defined for negative number.\n");
    } else {
        
    }
}