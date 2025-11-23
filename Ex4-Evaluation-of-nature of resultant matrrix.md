# Ex4 You are given a Java program that performs matrix addition. If Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension, what will be the nature (even/odd/mixed) of the resulting matrix?
## DATE:23-11-2025
## AIM:
To write a java function to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix.

## Algorithm
1.Start the program.  
2.Read the number of rows r and columns c from the user.  
3.Declare three matrices A, B, and C of size r × c.  
4.Read the elements of Matrix A from the user.  
5.Read the elements of Matrix B from the user.  
6.Initialize two Boolean variables:  
a. allEven = true  
b. allOdd = true  
7.For each element position (i, j) in the matrices:  
a. Compute the sum → C[i][j] = A[i][j] + B[i][j].  
b. Display the element C[i][j].  
c. If C[i][j] is even, set allOdd = false.  
d. Else, set allEven = false.  
8.After processing all elements:  
a. If allEven is true → Display "Resultant Matrix is EVEN."  
b. Else if allOdd is true → Display "Resultant Matrix is ODD."  
c. Else → Display "Resultant Matrix is MIXED."  
9.Stop the program.    

## Program:

/*
Program to ind the nature of resultant matrrix.
Developed by: SAADHANA L
RegisterNumber:  212224060224
*/
~~~
import java.util.*;

public class MatrixAddShort {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int r = sc.nextInt(), c = sc.nextInt();
        int[][] A = new int[r][c], B = new int[r][c];

        for (int i = 0; i < r; i++)  
            for (int j = 0; j < c; j++)
                A[i][j] = sc.nextInt();

        for (int i = 0; i < r; i++)  
            for (int j = 0; j < c; j++)
                B[i][j] = sc.nextInt();

       
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++)
                System.out.print((A[i][j] + B[i][j]) + " ");
            System.out.println();
        }
    }
}


~~~

## Output:
<img width="425" height="624" alt="image" src="https://github.com/user-attachments/assets/3ff3e0d4-23fa-4484-9c9d-067bb6f20eb4" />



## Result:
Thus, the java program to evaluate weather the given Matrix A has all odd numbers and Matrix B has all even numbers of the same dimension and find the nature of resultant matrrix is implemented successfully.
