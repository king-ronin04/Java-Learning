# Grades of Rides 
“AquaticaCarnival” is the most successful event dedicated to children and families. The Event has more than 20 rides for children and adults and the organizers always ensure not to compromise on the safety of the visitors.
To ensure the safety of the rides, the organizers have graded the rides in the fair according to the following conditions:

Hurl Factor must be greater than 50.
<br>
Spin Factor must be greater than 60.
<br>
Speed factor must be greater than 100.

The grades are as follows:
<br>
Grade is 10 if all three conditions are met.
<br>
Grade is 9 if conditions (i) and (ii) are met.
<br>
Grade is 8 if conditions (ii) and (iii) are met.
<br>
Grade is 7 if conditions (i) and (iii) are met.
<br>
Garde is 6 if only one condition is met.
<br>
Grade is 5 if none of three conditions are met.
<br>
Write a program display the grade of the rides, given the values of hurl factor, spin factor and speed factor of the ride under consideration.

#### Input format :
First line of the input consists of 3 integers that gives the Hurl Factor, Spin Factor and Speed Factor of the ride, each separated by a space.

#### Output format :
Output should display the grade of the ride depending on Conditions.

**Sample test cases :<br>
Input 1 :** <br>
51 89 150 <br>
**Output 1 :** <br>
10 <br>

**Input 2 :** <br>
45 69 102 <br>
**Output 2 :** <br>
8 <br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------
```cpp
import java.io.*;
import java.util.*;
class Gradesofrides {
	public static void main(String [] args) {
		int hurl,spin,speed;
		Scanner sc = new Scanner(System.in);
		hurl = sc.nextInt();
		spin = sc.nextInt();
		speed = sc.nextInt();
		if(hurl > 50 && spin>60 && speed>100) {
			System.out.println("10");
		}
		else if(hurl>50 && spin>60) {
			System.out.println("9");
		}
		else if(spin>60 && speed>100) {
			System.out.println("8");
		}
		else if(hurl>50 && speed>100) {
			System.out.println("7");
		}
		else if(hurl>50 || spin>60 || speed>100) {
			System.out.println("6");
		}
		else {
			System.out.println("5");
		}
	}
}


```

