# EX 1 Display operator precedence in the infix expression.
## DATE: 24.02.2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Start the program and take the Postfix expression as input.
2. Traverse each character of the expression.
3. If the character is an operator (+, -, *, /, ^), find its priority:
   ^ → 3
   *, / → 2
   +, - → 1
4. Display the operator and its priority.
5. End the program.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: S V SHADHANASHREE
RegisterNumber:  212223230202
*/

#include <stdio.h>
#include<string.h>
int main()
{
   int i,j;
   char ch[100]="+7*45%20";
   
   //write your code here
   int length=strlen(ch);
   for(i=0;i<=length;i++)
   {
       if(ch[i]=='+'||ch[i]=='-'||ch[i]=='*'||ch[i]=='/'||ch[i]=='&'||ch[i]=='|'||ch[i]=='%'||ch[i]=='^')
       {
       j=priority(ch[i]);
       switch(j)
       {
           case 1:
           printf("%c  ----> Lowest Priority\n",ch[i]);
           break;
           case 2:
           printf("%c  ----> Second Lowest Priority\n",ch[i]);
           break;
           case 3:
           printf("%c  ----> Second Highest Priority\n",ch[i]);
           break;
           case 4:
           printf("%c  ----> Highest Priority\n",ch[i]);
           break;
       }
       }
   
   }
   
}
   
```

## Output:

![image](https://github.com/user-attachments/assets/2452b768-042d-4843-bc9f-5a05453ad0ff)

## Result:

Thus, the program successfully finds and displays the priority of each operator in the given postfix expression.



## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
