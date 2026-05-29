19) Define a structure called student with data members RollNo, Name and Percentage. Also write two functions getdata() to input data and printdata() to display the data.

#include<stdio.h>

// Define structure
struct student {
    int RollNo;
    char Name[50];
    float Percentage;
};

// Function to input data
void getdata(struct student *s) {
    printf("Enter Roll Number: ");
    scanf("%d", &s->RollNo);

    printf("Enter Name: ");
    scanf(" %[^\n]", s->Name);

    printf("Enter Percentage: ");
    scanf("%f", &s->)
}