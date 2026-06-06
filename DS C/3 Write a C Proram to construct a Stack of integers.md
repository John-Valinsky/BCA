3) Write a C Proram to construct a Stack of integers and to perform the following operations on it. 1. Push 2. Pop 3. Display The program should print appropriate messages for stack overflow, stack underflow and stack empty.

#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

// Push operation
void push(int value) {
    if (top == MAX - 1) {
        printf("Stack Overflow! Cannot push %d\n", value);
    } else {
        stack[++top] = value;
        printf("%d pushed into stack\n", value);
    }
}

// Pop operation
void pop() {
    if (top == -1) {
        printf("Stack Underflow! Stick is empty\n");
    } else {
        printf("%d popped from stack\n", stack[top--]);
    }
}