13) Write a C Program to construct doubly linked list and perform the following operations: 1. insert(first, middle, last position) 2. delete(first, middle, last position) 3. Display

#include <stdio.h>
#include <stdlib.h>

// Define node
struct Node {
    int data;
    struct Node* prev;
    struct Node* next;
};

struct Node* head = NULL;

// Insert at beginning
void insertFirst(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->prev = NULL;
    neNode->next = head;
}