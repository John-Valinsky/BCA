2) Temperature of your city in Fahrenheit degrees is input through the keyboard. Write a program to convert this temperature into Centigrade degrees.

#include <stdio.h>

int main() {
	float fahrenheit, celsius;

	// Input temperature in Fahrenheit
	printf("Enter temperature in Fahrenheit: ");
	scanf("%f", &fahrenheit);

	// Convert to Celsius
	celsius = (fahrenheit - 32) * 5 / 9;

	// Display result
	printf("Temperature in Celsius = %.2f\n", celsius);

	return 0;
}