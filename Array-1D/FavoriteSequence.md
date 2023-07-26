# Favorite Sequence
Lucarnos Film Festival is an annual film festival and is also known for being a prestigious platform for art house films. Lucy, being a movie lover visits the Lucarnos Film Festival. There were many films screened in the show, of which Lucy somehow choose the best movie of her choice and set off to watch it.

The movie which Lucy chose to watch has N sequences. A sequence is defined as a series of scenes in a movie that form a distinct narrative unit. Lucy likes a sequence better if the sequence contains her favorite sequence in the movie as a substring.

Given the sequence and Lucy’c favorite sequence(F) check whether her favorite sequence is contained in the sequence.

#### Input format :
The first line of the input contains an integer N, which corresponds to the length of the sequence.
<br>
The second line of the input contains N space-separated integers, which corresponds to the sequence.
<br>
The third line of the input contains an integer n, which corresponds to the length of favorite sequence F.
<br>
The last line of the input contains n space-separated integers, which corresponds to the favorite sequence.

#### Output format :
Print "Yes" (Without quotes)if the sequence contains Lucy’sfavourite sequence otherwise print "No" (Without quotes).

**Sample test cases :<br>
Input 1 :<br>**
6<br>
1 2 3 4 5 6<br>
3<br>
2 3 4<br>
**Output 1 :<br>**
Yes

**Input 2 :<br>**
6<br>
22 5 6 33 1 4<br>
2<br>
4 15<br>
**Output 2 :<br>**
No


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```java
import java.io.*;
import java.util.*;
class favouriteSequence {
	public static void main(String [] args) {
		int n,m,i,j,k=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
		m = sc.nextInt();
		int b[] = new int[m];
		for(i=0;i<m;i++) {
			b[i] = sc.nextInt();
		}
		for(j=0;j<n;j++)
	    {
	        if((b[0]==a[j])&&(j+m<=n))
	        {
	            for(i=0;i<m;i++){if(b[i]==a[j+i]){k++;}}
	        }
	    }
		if(k == m) {
			System.out.println("Yes");
		}
		else {
			System.out.println("No");
		}

	}
}

```
