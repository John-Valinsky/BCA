8) Write a C program using Merge Sort.

#include <stdio.h>

void merge(int arr[], int low, int mid, int high) {
    int i = low, j = mid + 1, k = low;
    int temp[100];

    // Merge two sorted subarrays
    while (i <= mid && j <= high) {
        if (arr[i] <= arr[j])
            temp[k++] = arr[i++];
        else
            temp[k++] = arr[j++];    }
}

    // Copy remaining elements
    while (i <= mid)
        temp[k++] = arr[i++];

    while (j <= high)
        temp[k++] = arr[j++];

    // Copy remaining elements
    while (i <= mid)
        temp[k++] = arr[i++];

    while (j <= high)
        temp[k++] = arr[j++];

    // Copy back to original array
    for (i = low; i <= high; i++)
        arr[i] = temp[i];
}

void 