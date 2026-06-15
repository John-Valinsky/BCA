11) Write a C program using quick Sort.

#include <stdio.h>

// Function of partition the array
int partition (int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low -1;
    int j, temp;

    for (j = low, j < high; j++) {
        if (arr[j] < pivot) {
            i++;

            // Swap arr[i] and arr[j]
            temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }

    // Place pivot in correct position
    temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;

    return i + 1;
}