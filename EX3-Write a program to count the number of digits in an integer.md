# EX3 Write a program to count the number of digits in an integer.
## DATE: 23-11-2025
## AIM:
To write a C program to count the number of digits in an integer.

## Algorithm
Step 1: Start  
Step 2: Read an integer num from the user.  
Step 3: Define a recursive function countDigits(num) that:  
            • Checks if num is equal to 0.    
            • If yes, return 0 (base condition).    
            • Otherwise, return 1 + countDigits(num / 10).    
Step 4: In the main function, call countDigits(num) and store the result in count.  
Step 5: Display "Number of digits: " followed by the value of count.  
Step 6: Stop.  

## Program:

/*
Program to to count the number of digits in an integer
Developed by: SAADHANA L
RegisterNumber:  212224060224
*/

import java.util.*;
public class CountDigits {
	static int countDigits(int num) {
		if (num == 0)
			return 0;
		return 1 + countDigits(num / 10);
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter an integer: ");
		int num = sc.nextInt();

		int count = countDigits(num);
		System.out.println("Number of digits: " + count);
	}
}




## Output:
<img width="796" height="274" alt="image" src="https://github.com/user-attachments/assets/957a7ae3-b610-473f-93a9-989ec5f04b64" />




## Result:
Thus, the Java program to to count the number of digits in an integer is implemented successfully.
