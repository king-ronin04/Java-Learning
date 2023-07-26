# Series 2
The Event Organizing Company "Buzzcraft" focuses event management in a way that creates a win-win situation for all involved stakeholders. Buzzcraft don't look at building one time associations with clients, instead, aim at creating long-lasting collaborations that will span years to come. This goal of the company has helped them evolve and expand big with more workforces within notable time.

The number of employees of the company from the start day of their journey till now is recorded sensibly and is seemed to have followed a specific series like: 20, 60, 104, 152, 204,…….

Write a program which takes an integer N as the input and will output the series till the Nth term.

#### Input format :
First line of the input is an integer N.

#### Output format :
Output a single line the series till Nth term, each separated by a comma.

**Sample test cases : <br>
Input 1 :<br>**
5<br>
**Output 1 :<br>**
20 60 104 152 204 <br>

**Input 2 :<br>**
10<br>
**Output 2 :<br>**
20 60 104 152 204 260 320 384 452 524 


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Series2 {
	public static void main(String [] args) {
		int n,i,m=20;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
	    for(i=0;i<n;i++)
	    {
	        System.out.print(m+ " ");
	        m=m+40+(i*4);
	    }

	}
}

```
