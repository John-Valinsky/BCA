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
    
}