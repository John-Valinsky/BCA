1) Write a C Program to create a Sequential file with at least 4 records, each record having the shown below. Roll No : Non zero positive integer. Student Name : Character string of length 25 Marks 1,Marks 2, Marks 3: Positive Integer.

#include <stdio.h>
#include <stdlib.h>

struct Student {
	int rollNo;
	char name[25];
	int marks1, marks2, marks3;
};

int main() {
	FILE *fp;
	struct Student s;
	int i;

	// Open file in write mode
	fp = fopen("students.dat", "wb");

	if (fp == NULL) {
		printf("Error opening file!\n");
		exit(1);
	}

	printf("Enter details for 4 students:\n");

	for (i = 0; i < 4; i++) {
		printf("\nStudent %d\n", i + 1);

	// Input validation for roll number
	do {
		printf("Enter Roll No (positive integer): ");
		scanf("%d", &s.rollNo);
	} while (s.rollNo <= 0);

	printf("Enter Name: ");
	scanf(" %[")
}