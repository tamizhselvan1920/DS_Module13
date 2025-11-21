# EX3 Implementation of Tower of Hanoi
## DATE: 
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm

1. If n is 0, do nothing and return.

2. Move the top n-1 disks from peg x to peg z using peg y as temporary storage.

3. Move the largest disk from peg x to peg y and print this move.

4. Move the n-1 disks from peg z to peg y using peg x as temporary storage.

5. Repeat the above steps recursively until all disks are moved from peg x to peg y.

## Program:
```C
/*
Program to implement Tower of Hanoi
Developed by: THAMIZH SELVAN R
RegisterNumber: 212222230158
*/

#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
    if(n>0)
    {
        TOH(n-1,x,z,y);
        printf("%c to %c\n",x,y);
        TOH(n-1,z,y,x);
    }
}

int main()
{
    int a;
    scanf("%d",&a);
    TOH(a,'A','B','C');
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/a0eabf58-7041-47cd-83b1-0579565db275)

## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
