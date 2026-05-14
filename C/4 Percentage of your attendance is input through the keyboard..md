4) Percentage of your attendance is input through the keyboard. Write C program to calculate and display internal mark based on percentage of attendance.

#include <stdio.h>

int main() {
    float attendance;
    int marks;

    // Input attenance percentage
    printf("Enter attendance percentage: ");
    scanf("%f", &attendance);

    // Calculate internal marks
    if (attendance >= 95) {
        marks = 5;
    }

    else if (attendance >= 90) {
        marks = 4;
    }

    else if (attendance >= 85) {
        marks = 3;
    }

    else if (attendance >= 80) {
        
    }
}