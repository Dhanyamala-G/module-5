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
int main() 
{
    int len,wid;
    printf("Enter length of rectangle:");
    scanf("%d",&len);
    printf("Enter width of rectangle:");
    scanf("%d",&wid);
    int *l=&len;
    int *w=&wid;
    float area=(*l)*(*w);
    printf("Area of rectangle is %f",area);
    
    return 0;
}
```
## OUTPUT
<img width="1657" height="473" alt="image" src="https://github.com/user-attachments/assets/bf31c22a-d0c9-4f13-8577-e531bc310b3c" />
		       	


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
#include <stdlib.h>
#include <string.h>
int main() 
{
    char *str;
    str = (char *)malloc(8 * sizeof(char));
    if(str == NULL) 
    {
        printf("Memory allocation failed.\n");
        return 1;
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}
```
## OUTPUT
<img width="1621" height="535" alt="image" src="https://github.com/user-attachments/assets/3d4e40ef-47e6-419a-afdd-104de2019beb" />



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
struct Student 
{
    char name[50];
    int roll;
    float marks;
};
int main() {
    struct Student out;
    printf("Enter name: ");
    scanf("%[^\n]", out.name);
    printf("Enter roll number: ");
    scanf("%d", &out.roll);
    printf("Enter marks: ");
    scanf("%f", &out.marks);
    printf("%s\n", out.name);
    printf("%d\n", out.roll);
    printf("%.2f\n", out.marks);
    return 0;
}
```

## OUTPUT
<img width="1456" height="612" alt="image" src="https://github.com/user-attachments/assets/fd73017a-a328-4b0b-95f2-c0b12af8a6d8" />


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
struct Employee 
{char name[50];
    int id;
    float basic_sal,allowances,bonus,gross_sal;
    //Gross Salary = Basic Salary + Allowances + Bonuse};
int main() {
    struct Employee emp[3];
    for(int i=0;i<3;i++){
        printf("Enter name: ");
        scanf("%[^\n]",emp[i].name);
        printf("Enter id: ");
        scanf("%d",&emp[i].id);
        printf("Enter basic salary: ");
        scanf("%f",&emp[i].basic_sal);
        printf("Enter allowances: ");
        scanf("%f",&emp[i].allowances);
        printf("Enter bonus: ");
        scanf("%f",&emp[i].bonus);
        getchar();
        emp[i].gross_sal=emp[i].basic_sal+emp[i].allowances+emp[i].bonus;}
    for(int j=0;j<3;j++){
        printf("Name: %s\n",emp[j].name);
        printf("ID: %d\n",emp[j].id);
        printf("Gross salary: %f\n",emp[j].gross_sal);}
    return 0;}
```
 ## OUTPUT
<img width="1365" height="776" alt="image" src="https://github.com/user-attachments/assets/86e083ee-7183-4f1a-9b1d-92ad5e69a0c9" />

 

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
#include<stdio.h>
struct Student
{
    char name[50];
    int rollno;
    int subjects[5];
    int total;
    float average;
};
int main()
{ struct Student s[2];
    for(int i=0;i<2;i++)
    {for(int j=0;j<5;j++)
        {            scanf("%d",&s[i].subjects[j]);}
    }
    
    for(int i = 0; i < 2; i++) {
        s[i].total = 0;
        for(int j = 0; j < 5; j++) {
            s[i].total += s[i].subjects[j];}
        s[i].average = s[i].total / 5.0;}
        
    for(int i = 0; i < 2; i++) {
        printf("%d %.2f\n", s[i].total, s[i].average);}
    return 0;
}
```

## OUTPUT

 <img width="1389" height="781" alt="image" src="https://github.com/user-attachments/assets/123642da-6cf4-4587-a2a9-7401e832182f" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


