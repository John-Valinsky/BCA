2) Write a C Program to convert and print a given valid parenthesized infix arithmetic expression to postfix expression. The expression consist of single character operands and the binary operator +,-,* and /.

#include <stdio.h>
#include <ctype.h>

#define MAX 100

char stack[MAX];
int top = -1;

// Push function
void push(char x) {
    stack[++top] = x;
}

// Pop function
char pop() {
    return stack[top--];
}

// Check precedence
int precedence(char x) {
    if (x == '+')
}