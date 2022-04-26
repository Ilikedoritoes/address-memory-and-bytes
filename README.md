#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>

void swap(int num1, int num2)
{
	int temp;
	temp = num1;
	num1 = num2;
	num2 = temp;
}

void main()
{
	int num1 = 1, num2 = 2;
	swap(num1, num2);
	printf("%d %d", num1, num2);


	//prints the numbers above, and not the swapped ones!
	// to fix this, u use pointers/addresses
	//this is a variable that has the address of the memory of the numbers.
	// like 0x30
	//      0x70 etc.
	//int*  <---- is used for this variable.

	int* P1; // <----- this is a pointer

	P1 = &num1; 
	//P1 keeps the address memory of num1.

	*P1 = 10;
	//and
	num1 = 10;
	//do the same thing


}

// bit is the smallest memory unit, which includes 1 or 0.
// █
//byte has 8 bits, which means it has 2 options in each bit, which is 256 - 1 because you start from 0. (2^8 - 1)
// █ █ █ █ █ █ █ █ █ 
// there is also a 16 option one, which is (2^16 - 1)
// █ █ █ █ █ █ █ █ █ █ █ █ █ █ █ █ █ █ 

=====================================================================================================================================================================


#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>


void main()
{
	int num1=6;
	int* P1;
	P1 = &num1;  //P1 takes the address memory from num1;
	*P1 = 10;
	printf("%d \n", *P1);
	printf("%d", num1);

}



