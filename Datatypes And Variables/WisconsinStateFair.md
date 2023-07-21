# Wisconsin State Fair

Wisconsin State Fair is one of the largest midsummer celebrations in the Midwest Allis, showcasing the agriculture skills and prowess of the state. The Event organizers hired few part-time employees to work at the fair and the agreed salary paid to them are as given below:

 Weekdays --- 80 / hour

 Weekends --- 50 / hour

Justin is a part-time employee working at the fair. Number of hours Justin has worked in the weekdays is 10 more than the number of hours he had worked during weekends. If the total salary paid to him in this month is known, write a program to estimate the number of hours he had worked during weekdays and the number of hours he had worked during weekends.

 

#### Input format :
First line of the input is a double value that corresponds to the total salary paid to Justin.
#### Output format :
First line of the output should display the number of hours Justin has worked during the weekdays.
<br>
Second line of the output should display the number of hours Justin has worked during the weekends.

#### Sample test cases :
#### Input 1 :
2750
#### Output 1 :
25
<br>
15


```java
import java.util.*;
import java.io.*;
class Statefair {
	public static void main(String [] args) {
		double salary;
		Scanner sc = new Scanner(System.in);
		salary = sc.nextDouble();
		int weekdays,weekends;
		weekends = (int) ((salary-800)/130);
		weekdays  = weekends+10;
		System.out.println(weekdays);
		System.out.println(weekends);
		
		
	}
}

```
