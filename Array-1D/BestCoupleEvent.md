# Best Couple Event

"Shades" Television Channel organizes a fun-filled event named "Best Couple 2017", where in married couples would be invited and given many tasks and activities. Based on some criteria decided by the jury, a best couple will be chosen.

N couples registered for the event and each couple was given a registration number(it may repeat). One specific couple's registration Id got missed. The event coordinators wanted your help in finding the missing Id.

Write a program which takes an array of registration numbers as input and outputs the missing registration Id.

#### Input format :
First line of the input contains the number of couples N who registered for the event. Assume that the maximum value for N as 50.
<br>
Second line of input contains N registration Id of each of the couple, separated by a space.

#### Output format :
Output in a single line the missing registration Id.

**Sample test cases :<br>
Input 1 :<br>**
3<br>
1 2 1<br>
**Output 1 :<br>**
2

**Input 2 :<br>**
5<br>
1 1 2 2 3<br>
**Output 2 :<br>**
3


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class bestCouple {
	public static void main(String [] args) {
		int n,i,j,k=0;
		Scanner sc = new Scanner(System.in);
		n=sc.nextInt();
		int a[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
	    for(i=0;i<n;i++)
	    {
	        if(a[i]>0){k=a[i];
	        for(j=i+1;j<n;j++)
	        {
	            if(k==a[j]){a[j]=0;break;}
	            if(j==n-1){n=0;break;}
	        }}
	        if(n==0){break;}
	    }
	    System.out.println(k);

	}
}

```
