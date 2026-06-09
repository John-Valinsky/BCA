5) Write a C Program to simulate the working of a circular queue of integers using an array. provide the following operations. 1.Insert 2.Delete 3.Display.

#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1, rear = -1;

// Insert (Enqueue)
void insert(int value) {
    if ((front == 0 && rear == MAX -1) || (rear + 1) % MAX == front)  {
        printf("Queue Overflow! Cannot insert %d\n", value);
        return;
    }

    if (front == -1) {
        front = rear = 0;
    } else {
        rear = (rear + 1) % MAX;
    }

    queue[rear] = value;
    printf("%d inserted into queue\n", value);
}

// Delete (Dequeue)
void delte() {
    if (gront == -1) {
        printf("Queue Underflow! Queu is empty\n");
        return;
    }

    printf("%d deleted from queue\n", queue[front]);
}