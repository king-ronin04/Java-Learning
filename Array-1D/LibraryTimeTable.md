# Library Time table
With the initiative of the Students Council of Sherland State University, the College Management has inaugurated a mini library in the hostel premises.There are N students living in the hostel. Any student can use the library but on a condition that only one student should avail it at a time. Based on this condition, the Hostel Warden came up with a timetable for library's usage in order to avoid the conflicts:
<br>
• The first student starts to use the library at the time O and should finish the reading not later than at the time A1.
<br>
• The second student starts to use the library at the time A1 and should finish the reading not later than at the time A2.
<br>
• And so on.
<br>
• The N-th student starts to use the library at the time AN-1 and should finish the reading not later than at the time AN

The holidays in Sherland are approaching, so today each of these N students wants to read some new edition of "Heart of Darkness". The i-th student needs Bi units of time to read the book.

The students have understood that probably not all of them will be able to read everything they want from the book. How many students will be able to read the book without violating the schedule?

#### Input format :
The first line of input contains a single integer N denoting the number of students. Assume that the maximum value for N as 50.
<br>
The second line contains N space-separated integers A1, A2, ...,AN denoting the moments of time by when the corresponding student should finish reading.
<br>
The third line contains N space-separated integers B1, B2, ...,BN denoting the time required for each of the students to read.

#### Output format :
Output a single line containing the number of students that will be able to finish reading.

**Sample test cases :<br>
Input 1 :<br>**
3<br>
1 10 15<br>
1 10 3<br>
**Output 1 :** <br>
2

**Input 2 :** <br>
3<br>
10 20 30<br>
15 5 20<br>
**Output 2 :** <br>
1


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class libraryTimeTable {
	public static void main(String [] args) {
		int i,n,j=0,k=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[] = new int[n];
		int b[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
		for(i=0;i<n;i++) {
			b[i] = sc.nextInt();
		}
		for(i=0;i<n;i++)
	    {
	        if((a[i]-j)>=b[i]){k++;}
	        j=a[i];
	    }
	    System.out.println(k);

	}
}

```
