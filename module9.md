EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>

int stack[50], top = -1,size=5;
void push(int val) {
    if (top==size- 1){
        printf("Stack Overflow\n");
        return;
    }
        stack[++top] = val;
}
void display() {
    if (top==-1) {
        printf("Stack is empty\n");
        return;
    }
    for (int i = top; i >= 0; i--){
        printf("%d ", stack[i]);
    }
}
int main() {
    push(10);
    push(20);
    push(30);
    printf("Stack elements:\n");
    display();
    return 0;
}
```
Output:

<img width="1633" height="334" alt="11" src="https://github.com/user-attachments/assets/01648a7b-fff3-4049-9ad4-d5e18fb378d9" />

Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>
float stack[50];
int top=-1,size=5;
void push(float val) {
    if (top==size- 1) {
        printf("Stack Overflow\n");
        return;
    }
    stack[++top] = val;
    printf("Pushed %.2f\n", val);
}
int main() {
    push(1.5);
    push(2.5);
    push(3.5);
    return 0;
}
```
Output:

<img width="1631" height="343" alt="12" src="https://github.com/user-attachments/assets/c5b2156a-cc33-42da-8f76-1ed9b4c05994" />

Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>
int queue[50];
int front = 0, rear = -1,size=5;

void enqueue(int val) {
    if (rear==size-1){
        printf("Queue Full\n");
        return;
    }
        queue[++rear] = val;
}
void display() {
    if (rear < front) {
        printf("Queue is empty\n");
        return;
    }
    for (int i = front; i <= rear; i++){
        printf("%d ", queue[i]);
    }
}
int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    printf("Queue elements:\n");
    display();
    return 0;
}
```
Output:

<img width="1644" height="343" alt="13" src="https://github.com/user-attachments/assets/6676aee3-843b-417b-b83e-9c80d3687cf1" />

Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
float queue[50];
int front=-1,rear=-1,size=5;
void enqueue(float val) {
    if (rear==size-1) {
        printf("Queue Full\n");
        return;
    }
    if(front==-1){
        front=0;
    }
    queue[++rear] = val;
    printf("%.2f stored sucessfully\n",val);
}

int main() {
    enqueue(1.1);
    enqueue(2.2);
    enqueue(3.3);

    return 0;
}
```
Output:

<img width="1625" height="330" alt="14" src="https://github.com/user-attachments/assets/1be851a8-7190-4287-8051-21f68d489d95" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.


EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
#include <stdio.h>
int queue[50];
int front = -1, rear = -1,size=5;
void enqueue(int val) {
    if (rear==size- 1) {
        printf("Queue Full\n");
        return;
    }
    if (front == -1){
        front = 0;
    }
    queue[++rear] = val;
}
void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty\n");
        return;
    }
    printf("Deleted element: %d\n", queue[front]);
    front++;
    if (front > rear) {
        front = rear = -1;
    }
}
int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    dequeue();
    dequeue();
    return 0;
}
```
Output:

<img width="1647" height="333" alt="15" src="https://github.com/user-attachments/assets/c7957b2d-df09-454e-8c66-ce98a6f8d8c8" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
