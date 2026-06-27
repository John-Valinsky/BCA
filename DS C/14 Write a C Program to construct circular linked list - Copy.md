14) Write a C Program to construct circular linked list 1. insert 2. delete) 3. Display

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
    struct Node* temp = head;

    newNode->data = value;

    if (head == NULL) {
        newNode->next = newNode;
        head = newNode;
        return;
    }

    while (temp->next != head)
        temp = temp->next;

    newNode->next = head;
    temp->next = newNode;
    head = newNode;
}

// Insert at end
void insertLast(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    struct Node* temp = head;

    newNode->data = value;

    if (head == NULL) {
        newNode->next = newNode;
        head = newNode;
        return;
    }

    while (temp->next != head)
        temp = temp->next;

    temp->next = newNode;
    newNode->next = head;
}

// Insert at middle (position)
void insertMiddle(int value, int pos) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    struct Node* temp = head;
    int i;

    newNode->data = value;

    for (i = 1; i < pos - 1 && temp->next != head; i++)
        temp = temp->next;

    if (pos == 1) {
        insertFirst(value);
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
    struct Node* last = head;

    if (head->next == head) {
        free(head);
        head = NULL;
        return;
    }

    while (last->next != head)
        last = last->next;

    head = head->next;
    last->next = head;
    free(temp);
}

// Delete last node
void deleteLast() {
    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    struct Node* temp = head;
    struct Node* prev = NULL;

    if (head->next == head) {
        free(head);
        head = NULL;
        return;
    }

    while (temp->next != head) {
        prev = temp;
        temp = temp->next;
    }

    prev->next = head;
    free(temp);
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

    for (i = 1; i < pos && temp->next != head; i++) {
        prev = temp;
        temp = temp->next;
    }

    prev->next = temp->next;
    free(temp);
}

// Display list
void display() {
    if (head == NULL) {
        printf("List is empty\n");
        return;
    }

    struct Node* temp = head;

    printf("Circular Linked List: ");
    do {
        printf("%d -> ", temp->data);
        temp = temp->next;
    } while (temp != head);

    printf("(Back to Head)\n");
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