# Age - 2

The Pan Am 73 flight from Bombay to New York en route Karachi and Frankfurt was hijacked by a few Palestinian terrorists at the Karachi International Airport. The senior flight purser Neerja Banhot withered her fear and helped evacuating the passengers on board.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/a5b382a6-9d44-4ab0-91ea-43e2992585d9)


Neerja planned to evacuated the passengers in rows that have an average age greater than x. Given r the number of rows, c the number of columns, a list of integers representing the ages of passengers, can you find the number of rows with an average age greater than x?

#### Input format :
The first line of input consists of an integer r, corresponding to the number of rows of seats in the aircraft.
<br>
The second line of input consists of an integer c, corresponding to the number of seats in a row.
<br>
The next r lines of input consist of c integers that correspond to the ages of passengers.
<br>
The next line of input is an integer x corresponding to the cut-off age.

#### Output format :
The output consists of an integer corresponding to t the number of rows with an average age greater than x.

**Sample test cases :<br>
Input 1 :**
```
4
5
23 34 45 56 67
98 78 65 78 90
85 76 98 1 2
5 6 7 8 9
25
```
**Output 1 :**
```
3
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Age2 {
	public static void main(String [] args) {
		int r,c,i,j,age,sum=0,count=0,avg=0;
		Scanner sc = new Scanner(System.in);
		r = sc.nextInt();
		c = sc.nextInt();
		int a[][] = new int[r][c];
		for(i=0;i<r;i++) {
			for(j=0;j<c;j++) {
				a[i][j] = sc.nextInt();
			}
		}
		age = sc.nextInt();
		for(i=0;i<r;i++) {
			for(j=0;j<c;j++) {
				sum += a[i][j];
			}
			avg = sum/c;
			if(avg > age) {
				count++;
			}
			sum =0;
			avg =0;
		}
		System.out.println(count);
	}
}

```
