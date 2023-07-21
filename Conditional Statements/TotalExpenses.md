# Total Expenses

The much awaited event at the entertainment industry every year is the "Screen Awards". This year the event is going to be organized on December 25 to honour the Artists for their professional excellence in Cinema. The Organizers has this time decided to launch an online portal to facilitate easy booking of the Award show’s tickets.

They specifically wanted to provide an option for bulk booking in the portal, wherein there are many discounts announced. Write a program to help the Organizers to create the portal as per the requirement given below.

Given the ticket cost as 'X'.
<br>
If the number of tickets purchased is less than 50, there is no discount.
<br>
If the number of tickets purchased is between 50 and 100 (both inclusive), then 10% discount is offered.
<br>
If the number of tickets purchased is between 101 and 200(both inclusive), 20% discount is offered.
<br>
If the number of tickets purchased is between 201 and 400(both inclusive), 30% discount is offered.
<br>
If the number of tickets purchased is between 401 and 500(both inclusive), 40% discount is offered.
<br>
If the number of tickets purchased is greater than 500, then 50% discount is offered.

#### Input format :
First line of the input is an integer that corresponds to the cost of the ticket ‘X’.
<br>
Second line of the input is an integer that corresponds to the number of tickets purchased.

#### Output format :
Output should display a double value, which gives the total expenses in purchasing the tickets after discounts. Display the output correct to 2 decimal places.

#### Sample test cases :
#### Input 1 :
100<br>
5
#### Output 1 :
500.00
#### Input 2 :
100<br>
300
#### Output 2 :
21000.00

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
import java.lang.*;
import java.text.DecimalFormat;
class Totalexpenses {
	public static void main(String [] args) {
		int cost,number;
		double total = 0, discount, amount =0.00;
		DecimalFormat d = new DecimalFormat("0.00");
		Scanner sc= new Scanner(System.in);
		cost = sc.nextInt();
		number = sc.nextInt();
		total = cost*number;
		if(number < 50) {
			System.out.println(d.format(total));
		}
		else if(number >=50 && number <=100) {
			discount = total*(0.1);
			amount = total-discount;
			System.out.println(d.format(amount));
		}
		else if(number >=101 && number <=200) {
			discount = total*(0.2);
			amount = total-discount;
			System.out.println(d.format(amount));
		}
		else if(number >= 201 && number <= 400) {
			discount = total*(0.3);
			amount = total - discount;
			System.out.println(d.format(amount));
		}
		else if(number >= 401 && number <=500) {
			discount = total*(0.4);
			amount = total - discount;
			System.out.println(d.format(amount));
		}
		else if(number > 500) {
			discount = total*(0.5);
			amount= total - discount;
			System.out.println(d.format(amount));
		}
	}
}


```
