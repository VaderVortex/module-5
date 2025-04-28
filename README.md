# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	int main() {
	float length, width, area;
	float *ptrLength = &length, *ptrWidth = &width, *ptrArea = &area;
	printf("Enter the length of the rectangle: ");
	scanf("%f", ptrLength);
	printf("Enter the width of the rectangle: ");
	scanf("%f", ptrWidth);
	*ptrArea = (*ptrLength) * (*ptrWidth);
	printf("The area of the rectangle is: %.2f\n", *ptrArea);
	return 0;
	}



## OUTPUT
![image](https://github.com/user-attachments/assets/8fe93db3-7427-4f1b-a074-83e5dca9b2cb)
		       	
## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
	#include <stdio.h>
	#include <stdlib.h>
	int main() {
	char *str = (char*)malloc(8 * sizeof(char)); // 8 characters
	if (str == NULL) {
	printf("Memory allocation failed!\n");
	return 1;
	}
	str[0] = 'W';
	str[1] = 'E';
	str[2] = 'L';
	str[3] = 'C';
	str[4] = 'O';
	str[5] = 'M';
	str[6] = 'E';
	str[7] = '\0';
	printf("%s\n", str);
	free(str);
	return 0;
	}


## OUTPUT
![image](https://github.com/user-attachments/assets/d3614f9a-50f9-4698-b3d2-25b27245add6)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM
To write a C Program to store the student information and display it using structure.

## ALGORITHM
1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
	#include <stdio.h>
	#include <string.h>
	struct Student {
	char name[50];
	int rollNo;
	float marks;
	};
	int main() {
	struct Student student1;
	printf("Enter student's name: ");
	fgets(student1.name, sizeof(student1.name), stdin);
	student1.name[strcspn(student1.name, "\n")] = 0;
	printf("Enter roll number: ");
	scanf("%d", &student1.rollNo);
	printf("Enter marks: ");
	scanf("%f", &student1.marks);
	printf("\nStudent Information:\n");
	printf("Name: %s\n", student1.name);
	printf("Roll Number: %d\n", student1.rollNo);
	printf("Marks: %.2f\n", student1.marks);
	return 0;
	}

## OUTPUT
![image](https://github.com/user-attachments/assets/59176b4a-82d7-40e4-bf84-6b14a926f8b4)


## RESULT
Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM
To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM
1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	#include<string.h>
	struct Employee {
	char name[50];
	float basicSalary;
	float hra;
	float da;
	float grossSalary;
	};
	int main() {
	struct Employee employees[3];
	for (int i = 0; i < 3; i++) {
	printf("Enter details for Employee %d:\n", i + 1);
	printf("Enter name: ");
	fgets(employees[i].name, sizeof(employees[i].name), stdin);
	employees[i].name[strcspn(employees[i].name, "\n")] = 0;
	printf("Enter basic salary: ");
	scanf("%f", &employees[i].basicSalary);
	printf("Enter HRA (House Rent Allowance): ");
	scanf("%f", &employees[i].hra);
	printf("Enter DA (Dearness Allowance): ");
	scanf("%f", &employees[i].da);
	employees[i].grossSalary = employees[i].basicSalary + employees[i].h
	getchar();
	printf("\n");
	}
	printf("\nEmployee Details and Gross Salary:\n");
	for (int i = 0; i < 3; i++) {
	printf("\nEmployee %d:\n", i + 1);
	printf("Name: %s\n", employees[i].name);
	printf("Basic Salary: %.2f\n", employees[i].basicSalary);
	printf("HRA: %.2f\n", employees[i].hra);
	printf("DA: %.2f\n", employees[i].da);
	printf("Gross Salary: %.2f\n", employees[i].grossSalary);
	}
	return 0;
	}


## OUTPUT
![image](https://github.com/user-attachments/assets/5d29b7d7-1a05-4fdc-a4d4-5488fdaf98d0)

 

## RESULT
Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 





# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM

1. Start the program.

2. Define a struct `student` with:

    - `name`: a character array (size 10) for the student's name (not used in the logic).
    - `rollno`: an integer for the student's roll number (also unused).
    - `subject[5]`: an array to store marks of 5 subjects.
    - `total`: an integer to store total marks.

3. Declare an array `s[2]` of type `struct student` for 2 students.  
   Also declare variables `n`, `i`, and `j` for input and iteration.

4. Input Loop (`i = 0 to 1`):

    - Read an integer `n` (but it's not used later — possibly intended for roll number or as a placeholder).
    - Loop `j = 0 to 4`:

        - Read 5 subject marks into `s[i].subject[j]`.

5. Total Marks Calculation Loop (`i = 0 to 1`):

    - Initialize `s[i].total` to `0`.
    - Loop `j = 0 to 4`:

        - Add each subject mark to `s[i].total`.

6. Override Total (Hardcoded):

    - Set `s[0].total = 374`.
    - Set `s[1].total = 383`.

7. Output Loop (`i = 0 to 1`):

    - Print `s[i].total` for each student.

8. End the program.


## PROGRAM
	#include <stdio.h>
	#include<string.h>
	struct Student {
	char name[50];
	int marks[5];
	float total;
	float average;
	};
	int main() {
	struct Student student;
	printf("Enter student's name: ");
	fgets(student.name, sizeof(student.name), stdin);
	student.name[strcspn(student.name, "\n")] = 0;
	printf("Enter marks for 5 subjects:\n");
	int sum = 0;
	for (int i = 0; i < 5; i++) {
	printf("Subject %d: ", i + 1);
	scanf("%d", &student.marks[i]);
	sum += student.marks[i];
	}
	student.total = sum;
	student.average = sum / 5.0;
	printf("\nStudent Details:\n");
	printf("Name: %s\n", student.name);
	printf("Total Marks: %.2f\n", student.total);
	printf("Average Marks: %.2f\n", student.average);
	return 0;
	}

## OUTPUT
![image](https://github.com/user-attachments/assets/4be74b29-9e3b-4a7c-b979-6278f1ba78b4)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


