# Sum of Odd and Even Digits

Write a program to calculate the sum of odd and even digits in a number. The input consists of a single integer 'n' which corresponds to the given number.The output must display the sum of odd numbers and even numbers.

#### Input format :
Input consists of a long number.

#### Output format :
Output prints the sum of odd numbers and even numbers separated by a space.

**Sample test cases : <br>
Input 1 :** <br>
3924209420352 <br>
**Output 1 :** <br>
29 16


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```java
import java.io.*;
import java.util.*;
class Sumofoddandeven {
	public static void main(String [] args) {
		long num;
		int digit,sumeven=0,sumodd = 0;
		Scanner sc = new Scanner(System.in);
		num = sc.nextLong();
		while(num != 0) {
			digit = (int) (num%10);
			if(digit%2 == 0) {
				sumeven += digit;
			}
			else {
				sumodd += digit;
			}
			num /= 10;
		}
		System.out.println(sumodd+" "+sumeven);
	}
}


```
