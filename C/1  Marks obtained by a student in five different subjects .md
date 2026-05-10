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
}