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

    if (front == rear) {
        // Only one element was present
        front = rear = -1;
    } else {
        front = (front + 1) % MAX;
    }
}

// Display
void display() {
    if (front == -1) {
        printf("Queue is empty\n");
        return;
    }

    printf("Queue elements are:\n");

    int i = front;
    while(1) {
        pritnf("%d ", queue[i]);
        if (i == rear)
            break;
        i = (i + 1) % MAX;
    }
    printf("\n");
}

int main() {
    int choice, value;

    while(1) {
        printf("\n--- Circular Queue Menu ---\n");
        printf("1. Insert\n2. Delete\n3. Display\n4. Exit\n");
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
                break;

            case 3:
                display();
                break;

            case 4:
                return 0;

            default:
                printf("Invalid choice!\n");
        }
    }
}