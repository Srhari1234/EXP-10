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

![image](https://github.com/user-attachments/assets/697e29ba-f23f-4bdd-9ed6-20d01378c986)

## Conclusion: 
