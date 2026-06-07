4) Write a C Program to simulate the working of a queue of integers using an array. Provide the following operations. 1.Insert 2.Delete 3.Display.

#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1, rear = -1;

// Insert (Enqueue)
void insert(int value) {
    if (rear == MAX -1) {
        printf("Queue Overflow! Cannot insert %d\n", value);
    } else {
        if (front == -1) 
            front = 0;
        queue[++rear] = value;
        printf("%d inserted into queue\n", value);
    }
}