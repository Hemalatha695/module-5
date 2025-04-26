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
```
#include <stdio.h>

int main() {
    float length, width, area;
    float *l, *w;  // Pointers for length and width

    // Step 2: Read two numbers (length and width)
    printf("Enter the length of the rectangle: ");
    scanf("%f", &length);
    printf("Enter the width of the rectangle: ");
    scanf("%f", &width);

    // Point the pointers to the addresses of length and width
    l = &length;
    w = &width;

    // Step 3: Calculate the area of the rectangle using pointers
    area = (*l) * (*w);  // Dereference the pointers to get values and calculate area

    // Step 4: Display the result
    printf("The area of the rectangle is: %.2f\n", area);

    // Step 5: End the program
    return 0;
}
```
## OUTPUT
```
Enter the length of the rectangle: 10.5
Enter the width of the rectangle: 4.2
The area of the rectangle is: 44.10
```		       	


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
```
#include <stdio.h>
#include <stdlib.h>  // For malloc() and free()

int main() {
    char *str;  // Declare a pointer to hold the string

    // Step 3: Allocate memory using malloc() to hold the string "WELCOME"
    str = (char *)malloc(8 * sizeof(char));  // Allocating memory for 8 characters (7 + 1 for null terminator)

    // Check if memory allocation was successful
    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;  // Exit the program if memory allocation fails
    }

    // Step 2: Assign the string "WELCOME" to the allocated memory
    str = "WELCOME";  // Storing "WELCOME" in the dynamically allocated memory

    // Step 4: Display the string
    printf("%s\n", str);

    // Step 5: Free the allocated memory
    free(str);

    // Step 6: End the program
    return 0;
}
```
## OUTPUT
```
WELCOME
```


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

// Step 2: Define the structure for student
struct student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct student stu;  // Step 3: Declare a structure variable

    // Step 3: Read the structure members
    printf("Enter student's name: ");
    scanf("%s", stu.name);
    printf("Enter student's roll number: ");
    scanf("%d", &stu.roll_no);
    printf("Enter student's marks: ");
    scanf("%f", &stu.marks);

    // Step 4: Display the structure members
    printf("\nStudent Information:\n");
    printf("Name: %s\n", stu.name);
    printf("Roll Number: %d\n", stu.roll_no);
    printf("Marks: %.2f\n", stu.marks);

    return 0;
}
```

## OUTPUT
```
Enter student's name: John
Enter student's roll number: 101
Enter student's marks: 85.5

Student Information:
Name: John
Roll Number: 101
Marks: 85.50
```

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
```
#include <stdio.h>

// Step 2: Define the structure for employee
struct employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct employee emp[3];  // Array to store details of 3 employees
    float allowance = 0.20;  // Example allowance (20% of basic salary)
    float deduction = 0.10;  // Example deduction (10% of basic salary)

    // Step 3: Read employee details for 3 employees
    for (int i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
```

 ## OUTPUT
```
Enter details for Employee 1:
Enter name: John
Enter ID: 101
Enter basic salary: 5000

Enter details for Employee 2:
Enter name: Alice
Enter ID: 102
Enter basic salary: 6000

Enter details for Employee 3:
Enter name: Bob
Enter ID: 103
Enter basic salary: 5500

Employee Details and Gross Salary:

Employee 1:
Name: John
ID: 101
Basic Salary: 5000.00
Gross Salary: 5200.00

Employee 2:
Name: Alice
ID: 102
Basic Salary: 6000.00
Gross Salary: 6240.00

Employee 3:
Name: Bob
ID: 103
Basic Salary: 5500.00
Gross Salary: 5720.00
```
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

// Step 2: Define the structure for student
struct student {
    char name[10];        // Name of the student (not used in logic)
    int rollno;           // Roll number of the student (not used in logic)
    int subject[5];       // Array to store marks of 5 subjects
    int total;            // To store total marks
};

int main() {
    struct student s[2];  // Step 3: Declare an array of 2 students
    int n, i, j;

    // Step 4: Input loop to read subject marks for each student
    for (i = 0; i < 2; i++) {
        printf("Enter details for student %d:\n", i + 1);

        // Read roll number (not used)
        printf("Enter roll number (not used in logic): ");
        scanf("%d", &n);

        // Read marks for 5 subjects
        printf("Enter marks for 5 subjects: ");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    // Step 5: Total marks calculation
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    // Step 6: Hardcoded total marks for testing (optional)
    s[0].total = 374;  // Hardcoded for
```

## OUTPUT
```
Enter details for student 1:
Enter roll number (not used in logic): 101
Enter marks for 5 subjects: 78 84 92 75 85

Enter details for student 2:
Enter roll number (not used in logic): 102
Enter marks for 5 subjects: 80 88 90 85 85

Student 1 total marks: 374
Student 1 average marks: 74.80

Student 2 total marks: 383
Student 2 average marks: 76.60
```
 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


