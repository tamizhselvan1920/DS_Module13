# Ex5 Count Inversions in an Array
## DATE: 28.11.2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j

## Algorithm
1. Start.
2. Read the array elements.
3. Set inversion count to zero.
4. Use two loops to check if arr[i] > arr[j] for all i < j and increase count.
5. Display the total inversions and stop.
  

## Program:
```
/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by:TAMIL SELVAN
*/
```
```
import java.util.Scanner;

public class InversionCount {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int count = 0;

        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j]) {
                    count++;
                }
            }
        }

        System.out.println("Number of inversions = " + count);
    }
}

```
## Output:
<img width="335" height="117" alt="image" src="https://github.com/user-attachments/assets/fea612e0-7833-429d-b520-fd13995d871f" />


## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
