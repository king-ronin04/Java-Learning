# Ticket type
"FantasyKingdom" is a brand new Amusement park that is going to be inaugurated shortly in the City and is promoted as the place for breath-taking charm. The theme park has more than 30 exhilarating and craziest rides and as a special feature of the park, the park Authorities has placed many Ticketing Kiosks at the entrance which would facilitate the public to purchase their entrance tickets and ride tickets.
 
The Entrance Tickets are to be issued typically based on age, as there are different fare for different age groups. There are 2 types of tickets – Child ticket and Adult ticket. If the age given is less than 15, then Child ticket is issued whereas for age greater than equal to 15, Adult ticket is issued. Write a piece of code to program this requirement in the ticketing kiosks.

#### Input format :
First line of the input is an integer that corresponds to the age of the person.

#### Output format :
Output should display "Child Ticket" or "Adult Ticket" based on the conditions given.

**Sample test cases : <br>
Input 1 :**   <br>
20 <br>
**Output 1 :** <br>
Adult Ticket <br>

**Input 2 :** <br>
12<br>
**Output 2 :** <br>
Child Ticket<br>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```cpp
import java.util.*;
import java.io.*;
class Tickettype {
	public static void main(String [] args) {
		int age;
		Scanner sc = new Scanner(System.in);
		age = sc.nextInt();
		if(age < 15) {
			System.out.println("Child Ticket");
		}
		else {
			System.out.println("Adult Ticket");
		}
	}
}


```
