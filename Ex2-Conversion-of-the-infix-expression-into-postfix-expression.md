# Ex2 Conversion of the infix expression into postfix expression
## DATE: 
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Initialize an empty stack to hold operators.

2. Read the infix expression character by character from left to right.

3. If the current character is an operand (alphanumeric), print it directly.

4. If the current character is an opening parenthesis '(', push it onto the stack.

5. If the current character is a closing parenthesis ')', pop and print all operators from the stack until an opening parenthesis '(' is encountered; then discard the '('.

6. If the current character is an operator, pop and print all operators from the stack that have greater than or equal precedence compared to the current operator, then push the current operator onto the stack.

7. After processing all characters, pop and print all remaining operators from the stack.


## Program:
```C
/*
Program to convert the infix expression into postfix expression
Developed by: THAMIZH SELVAN R
RegisterNumber: 212222230158
*/

#include<stdio.h>
#include<ctype.h>

char stack[100];
int top = -1;

void push(char x) {
    stack[++top] = x;
}

char pop() {
    if (top == -1)
        return -1;
    else
        return stack[top--];
}

int priority(char x) {
    if (x == '|') return 1;
    if (x == '&') return 2;
    if (x == '+' || x == '-') return 3;
    if (x == '*' || x == '/' || x == '%') return 4;
    if (x == '^') return 5;
    return 0;
}

void IntoPost(char *exp) {
    char *e, x;
    e = exp;
    while (*e != '\0') {
        if (isalnum(*e)) {
            printf("%c ", *e);
        } else if (*e == '(') {
            push(*e);
        } else if (*e == ')') {
            while ((x = pop()) != '(') {
                printf("%c ", x);
            }
        } else {
            while (top != -1 && priority(stack[top]) >= priority(*e)) {
                printf("%c ", pop());
            }
            push(*e);
        }
        e++;
    }
    while (top != -1) {
        printf("%c ", pop());
    }
}

int main() {
    char exp[100] = "3%2+4*(A&B)";
    IntoPost(exp);
    return 0;
}

```

## Output:
![image](https://github.com/user-attachments/assets/6819b466-2b06-4ca0-bf6f-e995c1806b18)


## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
