# Refreshment
The Pan Am 73 flight from Bombay to New York en route Karachi and Frankfurt was hijacked by a few Palestinian terrorists at the Karachi International Airport.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/420709d9-6531-499c-b1d1-5371a5ec1bac)


Despite the alarming situation prevailing inside the flight, the senior flight purser Neerja Banhot had to wither her fear and rise to the occasion to take extra care of her passengers on board.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/57f63767-2c72-4f0b-b6a0-63348fb097fa)


Firstly, she and her crew decided to provide food and drinks to the passengers. Given n the number of rows of seats in the aircraft and the total number of people in each row, can you determine the total number of passengers in the flight.

#### Input format :
The first line of input consists of an integer n, corresponding to the number of rows in the aircraft.
<br>
Next line consists of the number of people in each row separated by a space.

#### Output format :
The first line of output consists of n integers corresponding to the number of people in each row.
<br>
The second line of output consists of an integer corresponding to the total number of people in the aircraft.
<br>
Print Invalid Input and terminate the process of getting inputs if any of the inputs is not a positive number.
<br>
Refer sample input and output for further specifications.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
12 28 30 20 45<br>
**Output 1 :** <br>
12 28 30 20 45 <br>
135

**Input 2 :** <br>
-6<br>
**Output 2 :<br>**
Invalid Input

**Input 3 :<br>**
5<br>
1 2 -3<br>
**Output 3 :<br>**
Invalid Input


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Refreshment {
	public static void main(String [] args) {
		int i,n,sum=0,count=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		if(n<0) {
			System.out.println("Invalid Input");
		}
		else {
			int a[] = new int[n];
			for(i=0;i<n;i++) {
				a[i] = sc.nextInt();
				if(a[i] <0) {
					System.out.println("Invalid Input");
					break;
				}
				else {
					count++;
					sum = sum+a[i];
				}
			}
			if(count == n) {
			for(i=0;i<n;i++) {
				System.out.print(a[i]+" ");
			}
			System.out.println();
			System.out.println(sum);
			}
		}
	}
}


```
