# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE: 28.11.2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1. Start.
2. Read Matrix A and Matrix B of the same dimension.
3. Check if all elements in Matrix A are odd.
4. Check if all elements in Matrix B are even.
5. Display whether the matrices satisfy the condition and determine the nature of the resultant matrix, then stop.
## Program:
```
/*
Program to ind the nature of resultant matrrix.
Developed by: TAMIL SELVAN 
*/
```
```
import java.util.Scanner;
public class MatrixCheck {
    public static boolean allOdd(int[][] A, int rows, int cols) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (A[i][j] % 2 == 0) {  
                    return false;
                }
            }
        }
        return true;
    }
    public static boolean allEven(int[][] B, int rows, int cols) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                if (B[i][j] % 2 != 0) {  
                    return false;
                }
            }
        }
        return true;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        int rows = sc.nextInt();
        System.out.print("Enter number of columns: ");
        int cols = sc.nextInt();

        int[][] A = new int[rows][cols];
        int[][] B = new int[rows][cols];

        System.out.println("Enter Matrix A:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter Matrix B:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                B[i][j] = sc.nextInt();
            }
        }

        boolean isAodd = allOdd(A, rows, cols);
        boolean isBeven = allEven(B, rows, cols);

        System.out.println("\n--- Result ---");

        if (isAodd && isBeven) {
            System.out.println("Matrix A has all odd numbers.");
            System.out.println("Matrix B has all even numbers.");
            System.out.println("Resultant Matrix Nature: VALID (Odd + Even combination).");
        } else {
            System.out.println("Matrices do NOT satisfy the required conditions.");
            System.out.println("Resultant Matrix Nature: INVALID.");
        }
    }
}

```

## Output:
<img width="395" height="277" alt="image" src="https://github.com/user-attachments/assets/54ed1857-3b03-45c6-8116-2e4bf948d72d" />


## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
