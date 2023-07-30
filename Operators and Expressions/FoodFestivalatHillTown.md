# Food Festival at HillTown

HillTown Inn is planning to organize a Food Festival bringing together at one place, a wide variety of cuisines from across the world on account of Christmas. The Hotel Management has rented out a square hall of an indoor Auditorium for this extravaganza. The side of the square hall is y inches in which a large square table is placed for the display of the most popular and celebrated food items. The side of the square table is x inches, such that x<y.

The Management wanted to fill the remaining floor area with a decorative carpet. To get this done, they needed to know the floor area to be filled with the carpet. Write a program to help the Management find the area of the region located outside the square table, but inside the square hall. 

#### Input format :
First line of the input is an integer y, the side of the square hall.
<br>
Second line of the input is an integer x, the side of the square table placed for display.
#### Output format :
Output should display the area of the floor that is to be decorated with the carpet.

**Sample test cases :<br>
Input 1 :<br>**
7<br>
3<br>
**Output 1 :<br>**
40

**Input 2 :<br>**
5<br>
2

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Foodfestival {
	public static void main(String [] args) {
		int hall,table;
		Scanner sc = new Scanner(System.in);
		hall = sc.nextInt();
		table = sc.nextInt();
		System.out.println((hall*hall)-(table*table));
	}
}
```
