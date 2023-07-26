# Competitive Test
"Axcent Academy" has arranged for a competitive test for medical students from rural villages. Those successful students of the test will be awarded the scholarship for their NEET preparations at Axcent Academy. Benny, the co-coordinator and founder of the academy has given one problem for the first stage of the test. The problem goes like this:
<br>
Given an array A1, A2, ..., AN, count the number of subarrays of array A which are non-decreasing.
<br>
A subarrayA[i, j], where 1 ≤ i ≤ j ≤ N is a sequence of integers Ai, Ai+1, ..., Aj.
<br>
A subarrayA[i, j] is non-decreasing if Ai ≤ Ai+1 ≤ Ai+2 ≤ ... ≤ Aj. Count the total number of such subarrays.
<br>
Benny himself has not computed the solution of the problem. Write a program to help him find the answer for the same to evaluate the students. 

#### Input format :
The first line of input contains a single integer N denoting the size of array. Assume that the maximum value for N as 50.
<br>
The second line contains N space-separated integers A1, A2, ...,AN denoting the elements of the array.

#### Output format :
Output in a single line, the count of the total number of such subarrays.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
1 4 2 3<br>
**Output 1 :** <br>
6

**Input 2 :** <br>
3<br>
3 1 4<br>
**Output 2 :<br>**
4


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class CompetitiveTest {
	public static void main(String [] args) {
		int n,i,j=0,k=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
	    for(i=0;i<n-1;i++)
	    {
	        if(a[i]<=a[i+1]){j++;}
	        else{k=k+(j*(j+1)/2);j=0;}
	    }
	    k=k+(j*(j+1)/2);
	    System.out.println(k+n);

	}
}

```
