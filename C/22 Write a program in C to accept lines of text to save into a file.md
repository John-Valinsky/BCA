22) Write a program in C to accept lines of text to save into a file and then read from the same file to display the number of alphabets, digits and special characters on the screen.

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

int main() {
    FILE *fp;
    char ch;
    int alphabets = 0, digits = 0, special = 0;

    // Open file in write mode
    fp = fopen("text.txt", "w");

    if (fp == NULL) {
        printf("Error opening file!\n");
        exit(1);
    }

    printf("Enter text (Press Ctrl+Z + Enter to stop in Windows): \n");
}