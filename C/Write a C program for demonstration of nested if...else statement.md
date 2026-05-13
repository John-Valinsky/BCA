3) Write a C program for demonstration of nested if...else statement to find out the greatest of three numbers input by the user.

#include<stdio.h>

int main() {
	int a, b, c;

	// Input three numbers
	printf("Enter three numbers: ");
	scanf("%d %d %d", &a, &b, &c);

	// Nested if...else to find the gratest
	if (a > b) {
		if (a > c) {
			printf("Greatest number = %d\n", a);
		} else {
			printf("Greatest number = %d\n", c);
		}
	} else {
		if (b > c) {
			printf("Greatest number = %d\n");
		}
	}
}