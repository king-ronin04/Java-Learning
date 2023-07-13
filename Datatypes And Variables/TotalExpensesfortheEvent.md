# Total Expenses for the Event

The prime functionality of an Event Management System is budgeting. An Event Management System should estimate the total expenses incurred by an event and the percentage rate of each of the expenses involved in planning and executing an event. Nikhil, the founder of "Pine Tree" wanted to include this functionality in his company’s Amphi Event Management System and requested your help in writing a program for the same.
The program should get the branding expenses, travel expenses, food expenses and logistics expenses as input from the user and calculate the total expenses for an event and the percentage rate of each of these expenses.

**Input format :** <br>
First input is a double value that corresponds to the branding expenses.
Second input is a double value that corresponds to the travel expenses.
Third input is a double value that corresponds to the food expenses.
Fourth input is a double value that corresponds to the logistics expenses.

**Output format :** <br>
First line of the output should display the double value that corresponds to the total expenses for the Event.
Next four lines should display the percentage rate of each of the expenses.
Round off the output to two decimal digits.

**Sample test cases :**<br>
**Input 1 :**<br>
20000<br>
40000<br>
15000<br>
25000<br>
**Output 1 :**<br>
Total expenses : Rs.100000.00<br>
Branding expenses percentage : 20.00%<br>
Travel expenses percentage : 40.00%<br>
Food expenses percentage : 15.00%<br>
Logistics expenses percentage : 25.00%

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```java
import java.io.*;
import java.math.*;
import java.text.*;
import java.util.*;

class Totalexpenses {
  public static void main(String[] args) {
    double branding, travel, food, logistics, sum = 0.00;
    DecimalFormat d = new DecimalFormat("0.00");
    Scanner sc = new Scanner(System.in);
    branding = sc.nextDouble();
    travel = sc.nextDouble();
    food = sc.nextDouble();
    logistics = sc.nextDouble();
    sum = branding + travel + food + logistics;
    System.out.println("Total expenses : Rs." + d.format(sum));
    System.out.println("Branding expenses percentage : " + d.format((branding / sum) * 100) + "%");
    System.out.println("Travel expenses percentage : " + d.format((travel / sum) * 100) + "%");
    System.out.println("Food expenses percentage : " + d.format((food / sum) * 100) + "%");
    System.out.println("Logistics expenses percentage : " +d.format((logistics / sum) * 100) +"%");
  }
}

```
