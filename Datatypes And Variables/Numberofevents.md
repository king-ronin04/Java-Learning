# Number of events
"Pine Tree" Company has signed up a big time Event Management deal from the Rotary Youth Club for a Trade Fair organized at Codissia Complex, wherein all startup companies in the Software industry are demonstrating their latest products and services and meet with industry partners and Customers.

Amphi Event Management System has to be modified to write a piece of code that will get the input of the number of events to be hosted for the Fair at Codissia from its users and display the same. Help the company to accomplish the requirement.

### Input format :
First line of the input is an integer that corresponds to the number of events to be hosted at Codissia.

### Output format :
Output should display the number of events to be hosted at Codissia.

#### Sample test cases :
#### Input 1 :
50
#### Output 1 :
Number of events hosted in Codissia is 50


```java
import java.util.*;
import java.io.*;
class Numberofevents {
	public static void main(String [] args) {
		int number;
		Scanner sc = new Scanner(System.in);
		number = sc.nextInt();
		System.out.println("Number of events hosted in Codissia is " +number);
	}
}

```
