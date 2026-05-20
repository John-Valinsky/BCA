10) Write a program using C to perform binary search for any item in an ordered array and display the position of the item if found.

#include <stdio.h>

int main() {
	int arr[100], n, i, key;
	int low = 0, high, mid;
	int position = -1;

	// Input number of elements 
	printf("Enter number of elements: ");
	scanf("%d", &n);

	// Input sorted array elements
	printf("Enter %d elements in sorted order:\n", n);
	for (i = 0; i < n; i++) {
		scanf("%d", &arr[i]);
	}

	// Input value to search
	printf("Enter value to search: ");
	scanf("%d",&key);

	high = n - 1;

	//Binary Search
	while (low <= high) {
		mid = (low + high) / 2;

		if (arr[mid] == key) {
			position = mid + 1;
		}
	}
}