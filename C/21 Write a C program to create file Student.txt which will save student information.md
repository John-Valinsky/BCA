21) Write a C program to create file "Student.txt" which will save student information such as student roll number, name and total marks for n students and display lists of students on screen by reading from the same file.

#include <stdio.h>
#include <stdlib.h>

// Structure definition
struct student {
    int rollNo;
    char name[50];
    float marks;
};

int main() {
    FILE *fp;
    struct student s;
    int n, i;

    // Open file in write mode
    fp = fopen ("Student.txt", "w");

    if (fp == NULL) {
        printf("Error opening file!\n");
        exit(1);
    }

    // Input number of students
    printf("Enter number of students: ");
    scanf("%d", &n);

    // Write data to file 
    for (i = 0; i < n; i++) {
        printf("\nEnter details of student %d\n". i + 1);

        printf("Rool No: ");
        scanf("%d", &s.rollNo);

        printf("Name: ");
        scanf("")
    }
}