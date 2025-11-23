# Ex5 Count Inversions in an Array
## DATE:23-11-2025
## AIM:
To write a Java program  to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j.

## Algorithm
1.Start the program.   
2.Read the number of elements n from the user.  
3.Declare an array arr of size n.  
4.Read all the n elements of the array from the user.  
5.Define a function countInversions(arr) that:    
- a. Initialize count = 0.  
- b. Repeat for i = 0 to n - 2:  
--> i. For each j = i + 1 to n - 1:  
--> ii. If arr[i] > arr[j], increment count by 1.  
- c. Return the value of count.
  
6.Call the function countInversions(arr) and store the result in a variable.  
7.Display the total number of inversions.  
8.Stop the program.    

## Program:

/*
Program toto Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < j
Developed by: SAADHANA L
RegisterNumber:  212224060224
*/
~~~
import java.util.Scanner;

public class CountInversions {
    public static int mergeSortAndCount(int[] arr, int left, int right) {
        int count = 0;
        if (left < right) {
            int mid = (left + right) / 2;
            count += mergeSortAndCount(arr, left, mid);
            count += mergeSortAndCount(arr, mid + 1, right);
            count += mergeAndCount(arr, left, mid, right);
        }
        return count;
    }

    private static int mergeAndCount(int[] arr, int left, int mid, int right) {
        int[] leftArr = new int[mid - left + 1];
        int[] rightArr = new int[right - mid];

        for (int i = 0; i < leftArr.length; i++) leftArr[i] = arr[left + i];
        for (int i = 0; i < rightArr.length; i++) rightArr[i] = arr[mid + 1 + i];

        int i = 0, j = 0, k = left, swaps = 0;

        while (i < leftArr.length && j < rightArr.length) {
            if (leftArr[i] <= rightArr[j]) {
                arr[k++] = leftArr[i++];
            } else {
                arr[k++] = rightArr[j++];
                swaps += (leftArr.length - i); // Count inversions
                
            }
       
        }

        while (i < leftArr.length) arr[k++] = leftArr[i++];
        while (j < rightArr.length) arr[k++] = rightArr[j++];

        return swaps;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) arr[i] = sc.nextInt();
        System.out.println(mergeSortAndCount(arr, 0, n - 1));
    }
}

~~~

## Output:
<img width="377" height="256" alt="image" src="https://github.com/user-attachments/assets/e4dd96ae-4f71-4d62-897b-cbc7f236dec0" />



## Result:
Thus the Java program to to Count the number of inversions in an array where inversion is defined as: arr[i] > arr[j] and i < jis implemented successfully.
