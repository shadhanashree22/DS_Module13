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

int getPriority(char operator) {
    switch(operator) {
        case '^': return 3;
        case '*':
        case '/': return 2;
        case '+':
        case '-': return 1;
        default: return 0;
    }
}

int main() {
    char postfix[100];
    int i;
    
    printf("Enter a Postfix Expression: ");
    scanf("%s", postfix);
    
    printf("\nOperator priorities:\n");
    for(i = 0; postfix[i] != '\0'; i++) {
        if(postfix[i] == '+' || postfix[i] == '-' ||
           postfix[i] == '*' || postfix[i] == '/' ||
           postfix[i] == '^') {
            printf("Operator %c has priority %d\n", postfix[i], getPriority(postfix[i]));
        }
    }
    
    return 0;
}

   
```

## Output:

![image](https://github.com/user-attachments/assets/a40afc24-40a1-4c19-8e89-b415f4a93c1e)


## Result:

Thus, the program successfully finds and displays the priority of each operator in the given postfix expression.

