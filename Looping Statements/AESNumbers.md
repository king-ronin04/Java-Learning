# AES Numbers
Varun is the founder of Event Management Company, "Sparsh Services". In the company all the financial transactions are carried out online and Varun has strictly insisted his staff to do any transactions on web browsers that supports AES encryption numbers.

A number is an AES number if it has exactly four divisors. In other words, there are exactly four numbers that divide into it evenly. For example, 10 is an AES number because it has exactly four divisors (1, 2, 5, 10). 12 is not an AES number because it has too many divisors (1, 2, 3, 4, 6, 12). 11 is not an AES number either. There is only one AES number in the range 10...12.

Given a range of numbers, write a program that counts how many numbers from that range are AES numbers. 

#### Input format :
The input consists of 2 space-separated integers, which corresponds to the lower limit and the upper limit of the number range.
<br>
You may assume that the numbers in the range are less than 1000.

#### Output format :
Output a single line that gives the count of AES numbers from the given range.

**Sample test cases :<br>
Input 1 :<br>**
1 20<br>
**Output 1 :<br>**
5

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```java
import java.io.*;
import java.util.*;
class Series1 {
	public static void main(String [] args) {
	    int n,i,j,k=2,s=0;
	    Scanner sc = new Scanner(System.in);
	    n = sc.nextInt();
	    for(i=0;i<n;i++)
	    {
	        for(j=2;j<=k/2;j++)
	        {
	            if(k%j==0) { 
	            	s=1;
	            	break;
	            	}
	        }
	        if(s==0) { 
	        	System.out.print(k+" ");
	        	}
	        else { 
	        	i--; 
	        	}
	        k++;s=0;
	    }

	}
}

```
