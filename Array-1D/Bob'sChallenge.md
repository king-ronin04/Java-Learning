# Bob's Challenge 
Stella and friends have set out on a vacation to Manali. They have booked accommodation in a resort and the resort authorities headed by Bob, organize Camp fires every night as a part of their daily activities. Stella volunteered herself for an activity called the "Stick Game".
<br>
Stella was given a total of N sticks. Length of i-th stick is Ai. Bob insists Stella to choose any four sticks and to make a rectangle with those sticks as its sides. Bob warns Stella not to break any of the sticks, she has to use sticks as a whole. 
<br>
Also, Bob wants that the rectangle formed should have the maximum possible area among all the rectangles that Stella can make. Stella takes this challenge up and overcomes it. You have to help her know whether it is even possible to create a rectangle. If yes, then tell the maximum possible area of rectangle.

#### Input format :
The first line of the input contains a single integer N denoting the number of sticks.
<br>
The second line of each test case contains N space-separated integers A1, A2, ...,AN denoting the lengths of sticks.

#### Output format :
Output a single line containing an integer representing the maximum possible area for rectangle or output -1, if it's impossible to form any rectangle using the available sticks.

**Sample test cases :<br>
Input 1 :**<br>
5<br>
1 2 3 1 2<br>
**Output 1 :<br>**
2

**Input 2 :<br>**
4<br>
1 2 2 3<br>
**Output 2 :<br>**
-1


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class BobsChallenge {
	public static int zerofun(int a[],int n)
	{
	    int i,j,k=2;
	    for(i=0;i<n;i++)
	    {
	        for(j=0;j<n;j++)
	        {
	            if(a[i]==a[j]){k--;}
	            if(k==0){break;}
	            if(j==n-1){a[i]=0;}
	        }
	        k=2;
	    }
	    k=a[0];
	    for(i=0;i<n;i++){if(a[i]>k){k=a[i];}}
	    j=0;
	    for(i=0;j<2;i++){if(k==a[i]){a[i]=0;j++;}}
	    return k;
	}

	public static void main(String [] args) {
	    int n,i,k=2,l=0;
	    Scanner sc = new Scanner(System.in);
	    n = sc.nextInt();
	    int a[] = new int[n];
	    for(i=0;i<n;i++)
	    {
	        a[i] = sc.nextInt();
	    }
	    k=zerofun(a,n);
	    l=zerofun(a,n);
	    if(l*k == 0) {
	    	System.out.println("-1");
	    }
	    else {
	    	System.out.println(l*k);
	    }

	}
}

```
