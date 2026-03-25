EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* next;
}*head=NULL;
void insert(int data) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = head;
    head = newNode;
}
void search(int data) {
    struct Node* temp = head;
    int position=0;
    while (temp != NULL) {
        if (temp->data == data) {
            printf("Element %d found at location %d\n",data,position);
            return;
        }
        temp = temp->next;
        position++;
    }
    printf("Element %d not found\n",data);
}
int main() {
    insert(10);
    insert(20);
    insert(30);
    search(20);
    return 0;
}
```
Output:
<img width="1630" height="331" alt="16" src="https://github.com/user-attachments/assets/34956dd0-d431-4817-b667-d120085fc5df" />

Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next;
}*head=NULL;
void insert(int data){
    struct Node*newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory not Allocated\n");
        return;
    }
    newNode->data=data;
    newNode->next=head;
    head=newNode;
}
void display(){
    struct Node*temp;
    if(head==NULL){
        printf("List is Empty\n");
        return;
    }
    temp=head;
    while(temp!=NULL){
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    insert(10);
    insert(20);
    insert(30);
    display();
    return 0;
}
```
Output:
<img width="1633" height="330" alt="17" src="https://github.com/user-attachments/assets/59eff19a-1124-47fc-b3ef-57be0f6b4a09" />

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next,*prev;
};
struct Node *head=NULL;

void insert(int val){
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory Not Allocated");
        return;
    }
    newNode->data=val;
    newNode->prev=NULL;
    newNode->next=head;
    if(head!=NULL){
        head->prev=newNode;
    }
    head=newNode;
}
void display(){
    struct Node *temp=head;
    while(temp->next!=NULL){
        temp=temp->next;
    }
    while(temp!=NULL){
        printf("%d<->",temp->data);
        temp=temp->prev;
    }
    printf("NULL\n");
}
int main(){
    insert(10);
    insert(20);
    insert(30);
    display();
    return 0;
}
```
Output:
<img width="1627" height="330" alt="18" src="https://github.com/user-attachments/assets/1ebcdc67-4aef-4c2e-80c6-a2d966c02aa5" />

Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next,*prev;
};
struct Node *head=NULL;

void insert(int val){
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory Not Allocated");
        return;
    }
    newNode->data=val;
    newNode->prev=NULL;
    newNode->next=head;
    if(head!=NULL){
        head->prev=newNode;
    }
    head=newNode;
}
void display(){
    struct Node *temp=head;
    while(temp!=NULL){
        printf("%d<->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    insert(10);
    insert(20);
    insert(30);
    display();
    return 0;
}
```
Output:
<img width="1636" height="335" alt="19" src="https://github.com/user-attachments/assets/ae591ada-4fee-4641-a0a5-4a5d687beb81" />

Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:
```
#include<stdio.h>
#include<stdlib.h>
struct Node{
    int data;
    struct Node*next,*prev;
};
struct Node *head=NULL;

void insert(int val){
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    if(newNode==NULL){
        printf("Memory Not Allocated");
        return;
    }
    newNode->data=val;
    newNode->prev=NULL;
    newNode->next=head;
    if(head!=NULL){
        head->prev=newNode;
    }
    head=newNode;
}
void delete(){
    struct Node *temp=head;
    if(head==NULL){
        printf("List is Empty");
        return;
    }
    if(temp->next==NULL){
        free(temp);
        head=NULL;
        return;
    }
    if(temp->next!=NULL){
        head=head->next;
        free(temp);
    }
}
void display(){
    struct Node *temp=head;
    while(temp!=NULL){
        printf("%d<->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
int main(){
    insert(10);
    insert(20);
    insert(30);
    display();
    delete();
    display();
    return 0;
}
```
Output:
<img width="1624" height="344" alt="20" src="https://github.com/user-attachments/assets/5c616046-209d-4155-9507-a489b38fa52c" />

Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





