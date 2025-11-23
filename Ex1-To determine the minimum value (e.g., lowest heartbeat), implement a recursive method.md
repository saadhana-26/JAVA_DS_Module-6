# EX 1 You’re creating a health monitoring device which stores several sensor readings in an array. To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
## DATE:23-11-2025
## AIM:
To write a JAVA program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.

## Algorithm
1.Start the program.  
2.Read the array elements.  
3.Define a recursive function findMin(arr, n):  
4.Base case: If array size is 1, return the element.  
5.Recursive case: Return the smaller value between arr[n-1] and findMin(arr, n-1).  
6.Display the result.  
7.Stop the program.  

## Program:

/*
Program To determine the minimum value (e.g., lowest heartbeat), implement a recursive method.
Developed by: K L RAVEENDRANATH
RegisterNumber:  212224060212
*/

import java.util.*;

public class MinValueRecursion {
    static int findMin(int[] arr, int n) {
        if (n == 1)
            return arr[0];
        return Math.min(arr[n - 1], findMin(arr, n - 1));
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of readings: ");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter the readings:");
        for (int i = 0; i < n; i++)
            arr[i] = sc.nextInt();

        int minValue = findMin(arr, n);
        System.out.println("Lowest heartbeat (Minimum Value): " + minValue);
    }
}



## Output:

<img width="579" height="259" alt="image" src="https://github.com/user-attachments/assets/cb1a3036-22be-4362-be09-196de1cd9a9e" />




## Result:
Thus the JAVA program to find the minimum value (e.g., lowest heartbeat), implement a recursive method has implemented successfully.
