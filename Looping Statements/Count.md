# Count
Mars Spell Bee is the largest self-motivated spelling competition held for school children. The children from different schools who are participating in the competition will be given a registration code. The registration is on a first come first serve basis to a maximum of N entries.
<br>
The competition is conducted in two different galleries of the venue. Just for the ease of their management, the Event organizers have announced to divide the children into two groups, to attend the competition in the two chosen galleries. By that note, all those children who have their registration code as an even number will be put in one gallery and those with odd number will be in another gallery.
<br>
Help the organizers to find count of number of even registration codes and odd registration codes from the total N. 

#### Input format :
The first line of the input consists of the value of n.
<br>
Next line consists of the array elements separated by a space.

#### Output format :
Output prints the count of even and odd numbers separated by a space.

**Sample test cases :<br>**
**Input 1 :<br>**
3<br>
1 4 10<br>
**Output 1 :<br>**
2 1


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class count {
	public static void main(String [] args) {
		int n,i,even =0,odd=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int [] a = new int[n];
		for(i =0;i<n;i++) {
			a[i] = sc.nextInt();
		}
		for(i =0;i<n;i++) {
			if(a[i] %2 ==0) {
				even++;
			}
			else {
				odd++;
			}
		}
		System.out.println(even+" "+odd);
		
	}
}

```
