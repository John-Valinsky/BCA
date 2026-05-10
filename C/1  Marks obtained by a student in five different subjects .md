1) Marks obtained by a student in five different subjects are input through the keyboard. Calculate the percentage and display on the screen. Assume that the maximum marks in each subject is 100. 

#include<studio.h>
#include<stdlib.h>
#include<ctype.h>

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

	printf("Enter text (Press Ctrl+Z + Enter to stop in Windows):\n");

	// Wrtie input to file
	while ((ch = getchar()) != EOF) {
		fputc(ch, fp);
	}

	fclose(fp);

	// Open file in read mode
	fp = fopen("text.txt", "r");
	exit(1);
}