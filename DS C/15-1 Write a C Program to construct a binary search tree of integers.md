15) Write a C Program using dynamic variables and pointers to construct a stack of integer using linked list and to perform the following operations: 1. Push 2. Pop 3. Display The program should print appropriate messages for stack overflow, stack underflow and stack empty.

#include <stdio.h>
#include <stdlib.h>

// Define node
struct Node {
    int data;
    struct Node* next;
};

struct Node* top = NULL;

// Push operation
void push(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));

    if (newNode == NULL) {
        printf("Stack Overflow (Memory not available)\n");
        return;
    }

    newNode->data = value;
    newNode->next = top;
    top = newNode;

    printf("Inserted %d\n", value);
}

// Pop operation
void pop() {
    if (top == NULL) {
        printf("Stack Underflow (Stack is empty)\n");
        return;
    }

    struct Node* temp = top;
    printf("Deleted element: %d\n", top->data);

    top = top->next;
    free(temp);
}

// Display stack
void display() {
    struct Node* temp = top;

    if (top == NULL) {
        printf("Stack is empty\n");
        return;
    }

    printf("Stack elements:\n");
    while (temp != NULL) {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}

// Main function
int main() {
    int choice, value;

    while (1) {
        printf("\n1.Push\n2.Pop\n3.Display\n4.Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value: ");
                scanf("%d", &value);
                push(value);
                break;

            case 2:
                pop();
                break;

            case 3:
                display();
                break;

            case 4:
                exit(0);

            default:
                printf("Invalid choice\n");
        }
    }

    return 0;
}