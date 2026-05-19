9) Write a program to perform Linear Search of any value in an array and display the position of the value if found.

#include <stdio.h>

int main() {
	int arr[100], n, i, key, position = -1;

	// Input number of elements
	printf("Enter number of elements: ");
	scanf("%d", &n);

	// Input array elements
	printf("Enter %d elements:\n", n);
	for (i = 0; i < n; i++) {
		scanf("%d", &arr[i]);
	}

	// Input value to search
	printf("Enter value to search: ");
	scanf("%d", &key);

	// Linear Search
	for (i = 0; i < n; i++) {
		
	}
}