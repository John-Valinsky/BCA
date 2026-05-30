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

    // Input using pointer
    printf("Enter Roll Number: ");
    scanf("%d", &ptr->rollNo);

    printf("Enter Name: ");
    scanf(" %[^\n]", ptr->name);

    printf("Enter Percentage: ");
    scanf("%f", &ptr->percentage);

    // Output using pointer
    printf("\n--- Student Details ---\n");
    printf("Roll Number: %d\n", ptr->rollNo);
}