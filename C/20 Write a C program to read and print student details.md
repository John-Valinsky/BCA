20) Write a C program to read and print student details such as roll number as integer, name as character and percentage as float using structure pointer.

#include<stdio.h>

// Define structure
struct student {
    int rollNo;
    char name[50];
    float percentage;
};

int main() {
    struct student s1;
    struct student *ptr;

    // Assign pointer to structure
    ptr = &s1;

    // Input 
}