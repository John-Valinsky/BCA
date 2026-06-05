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
    if (x == '+' || x == '-') return 1;
    if (x == '*'  || x == '/') return 2;
    return 0;
}

int main() {
    char infix[MAX], postfix[MAX];
    int i = 0, j = 0;

    printf("Enter a valid parenthesized infix expression: ");
    scanf("%s", infix);

    while (infix[i] != '\0') {
        // If operand, and to postfix
        if (isalnum(infix[i])) {
            postfix[j++] = infix[i];
        }

        // If '(', push to stack
        else if (infix[i] == '(') {
            push(infix[i]);
        }

        // If ')' pop until '('
        else if (infix[i] == ')') {
            
        }
    }
}