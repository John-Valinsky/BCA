13) Write C program to find the multiplication of two matrices using two dimensional array.

#include<stido.h>

int main() {
    int a[10][10], b[10][10], result[10][10];
    int i, j, k;
    int r1, c1, r2, c2;

    // Input dimensions
    printf("Enter rows and columns of first matrix: ");
    scanf("%d %d", &r1, &c1);

    printf("Enter rows and columns of second matrix: ");
    scanf("%d %d", &r2, &c2);

    // Check if multiplicaiton is possible
    if (c1 != r2) {
        printf("Matrix multiplicaiton not possible!\n");
    }
}