

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max_of_four(int ,int ,int ,int);
int main(){
    int a,b,c,d;
    printf("Enter four numbers : ");
    scanf("%d %d %d %d",&a,&b,&c,&d);
    int max=max_of_four(a,b,c,d);
    printf("Maximum is : %d",max);
    return 0;
}
int max_of_four(int a,int b,int c, int d){
    int max1=(a>b)? a:b;
    int max2=(c>d)? c:d;
    return (max1>max2)? max1:max2;
}
```
Output:
<img width="1628" height="333" alt="21" src="https://github.com/user-attachments/assets/fccf8275-5175-45a0-bf2d-0490fe60ce97" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void max(int ,int);
int main(){
    int a,b;
    printf("Enter m and k : ");
    scanf("%d %d",&a,&b);
    max(a,b);
    return 0;
}
void max(int n ,int k){
    int max_and=0,max_or=0,max_xor=0;
    int mand,mor,mxor;
    for(int i=1;i<=n;i++){
        for(int j=i+1;j<=n;j++){
            mand=i&j;
            mor=i|j;
            mxor=i^j;
            if(mand<k&&mand>max_and){
                max_and=mand;
            }
            if(mor<k&&mor>max_or){
                max_or=mor;
            }
            if(mxor<k&&mxor>max_xor){
                max_xor=mxor;
            }
        }
    }
    printf("%d\n%d\n%d",max_and,max_or,max_xor);
}
```
Output:
<img width="1634" height="340" alt="22" src="https://github.com/user-attachments/assets/a123fad6-db77-4d1f-85a6-d2fc0026ef5a" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
int main(){
    int total_shelves;
    printf("Enter number of shelves : ");
    scanf("%d",&total_shelves);
    int total_quaries;
    printf("Enter number of queries : ");
    scanf("%d",&total_quaries);
    int *total_books=(int*)calloc(total_shelves,sizeof(int));
    int **total_pages=(int**)malloc(total_shelves*sizeof(int*));
    for(int i=0;i<total_shelves;i++){
        total_pages[i]=NULL;
    }
    for(int i=0;i<total_quaries;i++){
        int type;
        scanf("%d",&type);
        if(type==1){
            int x,y;
            scanf("%d %d",&x,&y);
            total_books[x]++; 
            total_pages[x]=(int*)realloc(total_pages[x],total_books[x]*sizeof(int));
            total_pages[x][total_books[x]-1]=y;
        }
        else if(type==2){
            int x,y;
            scanf("%d %d",&x,&y);
            printf("%d\n",total_pages[x][y]);
        }
        else if(type==3){
            int x;
            scanf("%d",&x);
            printf("%d\n",total_books[x]);
        }

    }
    return 0;
}
```
Output:
<img width="1643" height="335" alt="23" src="https://github.com/user-attachments/assets/90c5f0dd-5ba3-4fe8-8b4b-9ef2cfdaf93e" />

Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
int main() {
    int n, sum = 0;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    int a[n];
    printf("Enter elements:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }
    printf("Sum = %d\n", sum);
    return 0;
}
```
Output:
<img width="1632" height="348" alt="24" src="https://github.com/user-attachments/assets/75d81142-e4fc-45b7-a30c-bbf0bf0fbf68" />

Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.


Program:
```
#include <stdio.h>
int main() {
    char str[100];
    int i = 0, count = 0;
    printf("Enter a sentence:\n");
    scanf("%[^\n]",str);
    while (str[i] != '\0') {
        if((i == 0 && str[i] != ' ' && str[i] != '\n')||(str[i] != ' ' && str[i-1] == ' ')){
            count++;
        }
        i++;
    }
    printf("Number of words = %d\n", count);
    return 0;
}
```
Output:
<img width="1635" height="336" alt="25" src="https://github.com/user-attachments/assets/e5741379-842a-4b8e-968e-e08cf9238d06" />

Result:
Thus, the program is verified successfully.
Thus, the program that counts the number of words in a given sentence is verified 
successfully.
