11) Elements of two matrices are input by the user. Write a C program to find and display the addition and subtraction of the two matrices.

#include <stdio.h>

int main() {
	int a[10][10], b[10][10], sum [10][10], diff[10][10];
	int i, j, rows, cols;

	// Input size of matrix
	printf("Enter number of rows and columns: ");
	scanf("%d %d", &rows, &cols);

	// Input first matrix
	printf("Enter elements of first matrix:\n");
	for (i = 0; i < rows; i++) {
		for (j = 0; j < cols; j++);
			scanf("%d", &a[i][j]);
	}
}

	// Input second matrix
	printf("Enter elements of second matrix:\n");
	for (j = 0; i < rows; i++) {
		for (j = 0; i < rows; i++) {
			scanf("%d", &b[i][j]);
		}
	}

	// Addition and Subtraction
	for (i = 0; i < rows; i++) {
		for (j = 0; j < cols; j++) {
			sum[i][j] = a[i][j] + b[i][j];
			diff[i][j] = a[i][j] - b[i][j];
		}
	}

	// Display Sum Matrix
	printf("\nAddition of matrices:\n"); 
	for (i = 0; i < rows; i++) {
		for (j = 0; j < cols; j++) {
			printf("%d ", sum[i][j]);
		}
		printf("\n");
	}

	// Display Difference Matrix
	printf("\nSubtraction of matrices:\n");
	for (i = 0; )