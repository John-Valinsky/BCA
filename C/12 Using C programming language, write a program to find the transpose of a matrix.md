12) Using C programming language, write a program to find the transpose of a matrix.

#include<stdio.h>

int main() {
    int a[10][10], transpose[10][10];
    int i, j, rows, cols;

    // Input size of matrix
    printf("Enter number of rows and columns: ");
    scanf("%d %d", &rows, &cols);

    // Input matrix elements
    pritnf("Enter elements of the matrix:\n");
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            scanf("%d", &a[i][j]);
        }
    }

    // Compute transpose
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            transpose[j][i] = a[i][j];
        }
    }

    // Display original matrix
    printf("\nOriginal Matrix:\n");
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            printf("%d ", a[i][j]);
        }
        printf("\n");
    }

}