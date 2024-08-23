# Experiment 10

# Aim:
To study and implement Pointer Operations (Call by value and Call by reference)

# Theory:
Call by Reference: In Call by Reference, instead of passing a copy of the variable, the address (or reference) of the variable is passed to the function. The function can then modify the actual value of the argument used to call the function.
Call by Value is safer when you want to ensure that the original data isn’t modified.

Call by Reference: In Call by Reference, instead of passing a copy of the variable, the address (or reference) of the variable is passed to the function. The function can then modify the actual value of the argument used to call the function.
Call by Reference is more efficient for large data structures and when you need to modify the original data.

# Codes 
## 1. Call By Value 1:
~~~
//Name: Srihari Nair
//Prn: 23070123131
//Class: EnTC B-2
#include<iostream> 
using namespace std; 
void swap(int x, int y) 
{
    int swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4, b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
~~~

## Output:

![image](https://github.com/user-attachments/assets/0483aeeb-6d7f-4087-a1ce-1f23ce8f427b)

## 2. Call By Value 2:
~~~
//Name: Srihari Nair
//Prn: 23070123131
//Class: EnTC B-2
#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int *swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
~~~

## Output:

![image](https://github.com/user-attachments/assets/fe79dbef-e8a3-455a-b37f-480cae95a1e0)

## 3. Call By Reference:
~~~
//Name: Srihari Nair
//Prn: 23070123131
//Class: EnTC B-2
#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int swap;
    swap=*x;
    *x=*y;
    *y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(&a,&b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
~~~

## Output:

![image](https://github.com/user-attachments/assets/697e29ba-f23f-4bdd-9ed6-20d01378c986)

## Conclusion: 
In C++, the concepts of call by value and call by reference, particularly when using pointers, play crucial roles in how functions interact with data. When a function is called by value, a copy of the actual argument is passed, meaning any changes made within the function do not affect the original argument. This is useful when you want to ensure the original data remains unchanged. However, even when pointers are used in a call by value, altering the pointer inside the function does not affect the original pointer in the caller function.

On the other hand, call by reference allows the function to receive a reference to the actual argument, meaning any modifications directly impact the original data. By passing a pointer as an argument, the function can directly manipulate the data at that memory location, making this approach efficient for modifying large data structures or arrays without the overhead of copying. This method is particularly advantageous when the goal is to alter the original data or handle large datasets where copying would be inefficient.
