14) Write a program in C to accept lines of text and then display the number of alphabets, digits and special characters.

#include<stdio.h>

int main() {
    char str[200];
    int i = 0;
    int alphabets = 0; digits = 0; special = 0;

    // Input line of text
    printf("Enter a line of text:\n");
    fgets(str, sizeof(str), stdin);

    // Process each character
    while (str[i] != '\0') {
        if ((str[i] >= 'A' && str[i] <= 'Z')) ||
            ((str[i] >= 'a' && str[i] ))
    }
}