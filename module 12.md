

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
};
struct Node*top=NULL;
void push(int data){
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allocated");
        return;
    }
    newNode->data=data;
    newNode->next=top;
    top=newNode;
}
void display(){
    struct Node *temp;
    if(top==NULL){
        printf("List is Empty");
        return;
    }
    temp=top;
    while(temp!=NULL){
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    push(10);
    push(20);
    push(30);
    display();
}
```
Output:
<img width="1633" height="332" alt="26" src="https://github.com/user-attachments/assets/f01cae86-0b4c-423b-bf6b-44cb066b105c" />

Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
};
struct Node*top=NULL;
void push(int data){
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allocated");
        return;
    }
    newNode->data=data;
    newNode->next=top;
    top=newNode;
}
void pop(){
    if (top==NULL) {
        printf("Stack is empty\n");
        return;
    }
    struct Node*temp=top;
    printf("Popped: %d\n", temp->data);
    top=top->next;
    free(temp);
}
void display(){
    struct Node *temp;
    if(top==NULL){
        printf("List is Empty");
        return;
    }
    temp=top;
    while(temp!=NULL){
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    push(10);
    push(20);
    push(30);
    display();
    pop();
    display();
}
```
Output:
<img width="1629" height="331" alt="27" src="https://github.com/user-attachments/assets/b3c555bc-f30d-45e0-971c-ded8839a5b1d" />

Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
}*front=NULL,*rear=NULL;
void enqueue(int data){
    struct Node*newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allcoated\n");
        return;
    }
    newNode->data=data;
    newNode->next=NULL;
    if(front==NULL){
        front=rear=newNode;
        return;
    }
    rear->next=newNode;
    rear=newNode;
}
void display(){
    struct Node*temp;
    if(front==NULL){
        printf("Queue is Empty\n");
        return;
    }
    temp=front;
    printf("Display Function:\n");
    while(temp!=NULL){
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    return 0;
}
```
Output:
<img width="1647" height="328" alt="28" src="https://github.com/user-attachments/assets/bb80bf53-d810-4f68-8e76-e8536dfcc156" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.



EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
}*front=NULL,*rear=NULL;
void enqueue(int data){
    struct Node*newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allcoated\n");
        return;
    }
    newNode->data=data;
    newNode->next=NULL;
    if(front==NULL){
        front=rear=newNode;
        printf("%d Inserted\n",data);
        return;
    }
    rear->next=newNode;
    rear=newNode;
    printf("%d Inserted\n",data);
}
int main(){
    enqueue(10);
    enqueue(20);
    enqueue(30);
    return 0;
}
```
Output:
<img width="1629" height="332" alt="29" src="https://github.com/user-attachments/assets/721d0b12-eb4e-432e-87cb-6babcdb4dcd0" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
}*front=NULL,*rear=NULL;
void enqueue(int data){
    struct Node*newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allcoated\n");
        return;
    }
    newNode->data=data;
    newNode->next=NULL;
    if(front==NULL){
        front=rear=newNode;
        return;
    }
    rear->next=newNode;
    rear=newNode;
}
void peek(){
    if(front==NULL){
        printf("Queue is empty\n");
        return;
    }
    printf("peek:%d\n",front->data);
}
int main(){
    enqueue(10);
    enqueue(20);
    enqueue(30);
    peek();
    return 0;
}
```
Output:
<img width="1638" height="338" alt="30" src="https://github.com/user-attachments/assets/fa8abcdd-e789-482a-b365-3b72b604e099" />

Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


