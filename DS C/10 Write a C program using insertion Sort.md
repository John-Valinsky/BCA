10) Write a C program using insertion Sort.

#include <stdio.h>

int main() {
    int arr[100], n, j, key;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Insertion Sort
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;
    }

    arr[j + 1] = key;
}

printf("Sorted array:\n");
for(i = 0; i < n; i++)