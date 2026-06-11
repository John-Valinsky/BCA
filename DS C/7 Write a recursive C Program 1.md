7) Write a recursive C Program for Searching an element on a given list of integers using the Binary Search method.

#include <stdio.h>

int binarySearch(int arr[], int low, int high, int key) {
    if (low > high) 
        return -1;

    int mid = (low + high) / 2;

    if (arr[mid] == key) 
        return mid;
    else if (key < arr[mid])
        return binarySearch(arr, low, mid -1, key);
    else
        return binarySearch(arr, mid + 1, high, key);
}

int main() {
    int arr[100], n, i, key, result;

    printf("Enter number of elements: ");
    scamf("%d", &m);

    printf("Enter elements in sorted order:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to search: ");
    scanf("%d", &key);

    result = binarySearch(arr, 0, n - 1, key);
}