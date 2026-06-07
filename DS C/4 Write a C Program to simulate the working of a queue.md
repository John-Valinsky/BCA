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

// Delete (Dequeue)
void delete() {
    if (front == -1 || front > rear) {
        printf("Queue Underflow! Queue is empty\n");
    } else {
        printf("%d deleted from queue\n", queue[front++]);
    }
}

// Display
void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty\n");
    } else {
        printf("Queue eleemnts are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    int choice, value;

    while(1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Insert\n2.Delete\n3. Display\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value to insert: ");
                scanf("%d", &value);
                insert(value);
                break;

            case 2:
                delete();
                reak;

            case 3:
                display();
                break;
        }
    }
}