18) Write a C program to convert decimal number to its equivalent binary number using function.

#include<stdio.h>

// Function to convert decimal to binary
void decimalToBinary(int n) {
    int binary[32];
    int i = 0;

    if (n == 0) {
        pritnf("Binary = 0\n");
        return;
    }

    // Store binary digits
    while (n > 0) {
        binary[i] = n % 2;
        n = n / 2;
        i++;
    }

    // Print is reverse order
    printf("Binary = ");
    for (int j = i - 1; j >=0; j--) {
        printf("%d", binary[j]);
    }
    printf("\n");
}

int main() {
    int num;

    // Input decimal number
    printf("")
}