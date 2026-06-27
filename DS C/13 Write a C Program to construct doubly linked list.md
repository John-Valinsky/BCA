12. Write a C Program to construct singly linked list and perform the following operations: 1.insert(first, middle, last position) 2.delete(first, middle, last position) 3.Display

#include <stdio.h>
#include <stdlib.h>

// Define node
struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

// Insert at beginning
void insertFirst(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = head;
    head = newNode;
}

// Insert at end
void insertLast(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    struct Node* temp = head;

    newNode->data = value;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
        return;
    }

    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
}

// Insert at middle (position)
void insertMiddle(int value, int pos) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    struct Node* temp = head;
    int i;

    newNode->data = value;

    for (i = 1; i < pos - 1 && temp != NULL; i++) {
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Invalid position\n");
        return;
    }

    newNode->next = temp->next;
    temp->next = newNode;
}

// Delete first node
void deleteFirst() {
    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    struct Node* temp = head;
    head = head->next;
    free(temp);
}

// Delete last node
void deleteLast() {
    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    struct Node* temp = head;

    if (temp->next == NULL) {
        free(temp);
        head = NULL;
        return;
    }

    while (temp->next->next != NULL) {
        temp = temp->next;
    }

    free(temp->next);
    temp->next = NULL;
}

// Delete from middle (position)
void deleteMiddle(int pos) {
    struct Node* temp = head;
    struct Node* prev = NULL;
    int i;

    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    if (pos == 1) {
        deleteFirst();
        return;
    }

    for (i = 1; i < pos && temp != NULL; i++) {
        prev = temp;
        temp = temp->next;
    }

    if (temp == NULL) {
        printf("Invalid position\n");
        return;
    }

    prev->next = temp->next;
    free(temp);
}

// Display list
void display() {
    struct Node* temp = head;

    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    printf("Linked List: ");
    while (temp != NULL) {
        printf("%d -> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

// Main function
int main() {
    int choice, value, pos;

    while (1) {
        printf("\n1.Insert First\n2.Insert Middle\n3.Insert Last\n");
        printf("4.Delete First\n5.Delete Middle\n6.Delete Last\n");
        printf("7.Display\n8.Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value: ");
                scanf("%d", &value);
                insertFirst(value);
                break;

            case 2:
                printf("Enter value and position: ");
                scanf("%d %d", &value, &pos);
                insertMiddle(value, pos);
                break;

            case 3:
                printf("Enter value: ");
                scanf("%d", &value);
                insertLast(value);
                break;

            case 4:
                deleteFirst();
                break;

            case 5:
                printf("Enter position: ");
                scanf("%d", &pos);
                deleteMiddle(pos);
                break;

            case 6:
                deleteLast();
                break;

            case 7:
                display();
                break;

            case 8:
                exit(0);

            default:
                printf("Invalid choice\n");
        }
    }

    return 0;
}