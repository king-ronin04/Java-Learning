# Salary Computation
Danny has recently got his job offer as an Event Concept Creator at Sparsh Event Services. The Company has sent him a detailed salary structure with details of his basic salary, HRA and DA. The Company has promised to pay him as under:

If his basic salary is less than Rs. 15000, then HRA = 15% of basic salary and DA = 90% of basic salary.
<br>
If his basic salary is either equal to or above Rs. 15000, then HRA = Rs. 5000 and DA = 98% of basic salary.
<br>
If the Danny’s salary is given as input, write a program to find his gross salary.
<br>
Note : Gross Salary = Basic Salary+HRA+DA

#### Input format :
First line of the input is an integer that corresponds to the basic salary of Danny.

#### Output format :
Output should display the double value that refers to the gross salary of Danny. Display the output correct to 2 decimal places.

**Sample test cases : <br>
Input 1 :** <br>
12000<br>
**Output 1 :** <br>
24600.00 <br>

**Input 2 :** <br>
30000 <br>
**Output 2 :** <br>
64400.00

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
import java.io.*;
import java.util.*;
import java.text.*;
class Salarycomputation {
	public static void main(String [] args) {
		int salary;
		double amount,hra,da;
		DecimalFormat d = new DecimalFormat("0.00");
		Scanner sc = new Scanner(System.in);
		salary = sc.nextInt();
		if(salary < 15000) {
			hra = 0.15*salary;
			da = 0.90*salary;
			amount = salary+hra+da;
		}
		else {
			da = 0.98*salary;
			amount = salary+5000+da;
		}
		System.out.println(d.format(amount));
	}
}

```
