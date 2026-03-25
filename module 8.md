<img width="1627" height="336" alt="9" src="https://github.com/user-attachments/assets/27439902-3587-433d-9f9d-a5bf31b542e0" />EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-at	Case 13: Print "seventy nine"
-	Default: Print "Greer than 13"
4.	Exit the program.
 
Program:
```
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number (5-13): ");
    scanf("%d", &n);
    switch(n) {
        case 5: 
            printf("seventy one"); 
            break;
        case 6: 
            printf("seventy two"); 
            break;
        case 7: 
            printf("seventy three"); 
            break;
        case 8: 
            printf("seventy four"); 
            break;
        case 9:
            printf("seventy five"); 
            break;
        case 10: 
            printf("seventy six"); 
            break;
        case 11: 
            printf("seventy seven"); 
            break;
        case 12: 
            printf("seventy eight"); 
            break;
        case 13: 
            printf("seventy nine"); 
            break;
        default: 
            printf("Greater than 13");
    }
    return 0;
}
```
Output:
<img width="1630" height="342" alt="6" src="https://github.com/user-attachments/assets/69885916-783f-4711-b501-0097f92ed08e" />

Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>
int main() {
    char a[50];
    int i,j,count;
    printf("Enter a number: ");
    scanf("%s",a);
    for (i = 0;i<= 3;i++) {
        count = 0;
        for (j = 0; a[j]!='\0'; j++) {
            if (a[j]==i+'0'){
                count++;
            }
        }
        printf("%d ",count);
    }
    return 0;
}
```
Output:
<img width="1647" height="289" alt="7" src="https://github.com/user-attachments/assets/73b2fb9f-9f7d-44d6-b416-ca44e42d98d4" />

Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <string.h>
void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}
int main() {
    char s[20];
    int i, j;
    printf("Enter string: ");
    scanf("%s", s);
    int n = strlen(s);
    for (i = 0; i < n-1; i++) {
        for (j = i+1; j < n; j++) {
            if (s[i] > s[j]){
                swap(&s[i], &s[j]);
            }
        }
    }
    do{
        printf("%s\n", s);
        int k = n - 2;
        while (k >= 0 && s[k] >= s[k+1]) k--;
        if (k< 0){
            break;
        }
        int l = n - 1;
        while (s[l] <= s[k]) l--;
        swap(&s[k], &s[l]);
        for (i = k+1, j = n-1; i < j; i++, j--)
            swap(&s[i], &s[j]);
    }while (1);
    return 0;
}
```
Output:
<img width="1631" height="320" alt="8" src="https://github.com/user-attachments/assets/d0d9f1ca-7d90-4507-99a0-c573bb9a5322" />

Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include<stdio.h>
int main()
{
    int i, j, n;
    printf("Enter n:");
    scanf("%d",&n);
    for(i=n; i>1; i--)
    {
        for(j=n;j>=1;j--)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        for(j=2;j<=n;j++)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        printf("\n");
    }    
    for(i=1; i<=n; i++)
    {
        for(j=n;j>=1;j--)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        for(j=2;j<=n;j++)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        printf("\n");
    }
    
    return 0;
}

```
Output:
<img width="1627" height="336" alt="9" src="https://github.com/user-attachments/assets/033ad094-f408-47af-beaa-d0ab344b4db1" />

Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:
```
#include <stdio.h>
int square() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    return n * n;
}
int main() {
    int result = square();
    printf("Square = %d\n", result);
    return 0;
}
```
Output:
<img width="1633" height="334" alt="10" src="https://github.com/user-attachments/assets/83fde01e-2a33-49c1-aae5-5f1e6c9149e3" />

Result:
Thus, the program is verified successfully



