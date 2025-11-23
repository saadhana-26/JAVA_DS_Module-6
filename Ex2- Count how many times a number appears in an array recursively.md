# Ex2 Count how many times a number appears in an array recursively.
## DATE:23-11-2025
## AIM:
To write a Java program to Count how many times a number appears in an array recursively.

## Algorithm
1.Start the program.  
2.Read the number of elements n from the user.  
3.Declare an array arr of size n.  
4.Read all the n elements of the array from the user.  
5.Read the number x whose occurrences need to be counted.  
6.Define a recursive function countOccurrences(arr, n, x) that:    

      a. If n == 0, return 0.    
      b. If the last element arr[n - 1] is equal to x,  return 1 + countOccurrences(arr, n - 1, x).
      c. Else, return countOccurrences(arr, n - 1, x).  
7.Call the recursive function countOccurrences(arr, n, x) and store the result in count.  
8.Display the message: "x appears count times in the array."  
9.Stop the program.  

## Program:

/*
Program Count how many times a number appears in an array recursively.
Developed by: SAADHANA L
RegisterNumber:  212224060224
*/

import java.util.*;
public class CountOccurrences {
    static int countOccurrences(int[] arr, int n, int x) {
        if (n == 0)
            return 0;
        if (arr[n - 1] == x)
            return 1 + countOccurrences(arr, n - 1, x);
        else
            return countOccurrences(arr, n - 1, x);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter array elements:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        System.out.print("Enter number to count: ");
        int x = sc.nextInt();

        int count = countOccurrences(arr, n, x);
        System.out.println(x + " appears " + count + " times in the array.");
    }
}



## Output:
<img width="509" height="395" alt="image" src="https://github.com/user-attachments/assets/0240f68d-9977-4e75-af1d-dbcc49c4e7af" />




## Result:
Thus, the Java program to Count how many times a number appears in an array recursively is implemented successfully.
