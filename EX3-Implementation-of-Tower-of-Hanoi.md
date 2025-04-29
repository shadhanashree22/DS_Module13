# EX3 Implementation of Tower of Hanoi
# DATE: 24.2.25

## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm

1.Start with three rods: source (A), auxiliary (C), and destination (B).

2.If there is only one disk, move it directly from the source to the destination.

3.For more than one disk, move the top (n-1) disks from the source to the auxiliary rod using the destination as a helper.

4.Move the nth (largest) disk from the source to the destination rod.

5.Move the (n-1) disks from the auxiliary rod to the destination rod using the source as a helper.

6.Repeat the above steps recursively until all disks are moved to the destination rod.

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: HARITHA RAMESH
RegisterNumber:  212223100011
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
    int n=2;
    TOH(n,'A','B','C');
}
```
## Output:

![WhatsApp Image 2025-04-29 at 11 24 58_6ae6886e](https://github.com/user-attachments/assets/cbf99282-958c-48c0-9245-0121b5289ecc)


## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
