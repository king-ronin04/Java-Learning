# Calendar Quiz

Super Quiz Bee is a famous quiz Competition that tests students on a wide variety of academic subjects. This week’s participants were kids of age 12 to 15 and the quiz questions were based on Gregorian calendar.
<br> 
In the first round of the competition, the Host of the event told the participants that it was Monday on the date 01/01/2001. Later he questioned each one of the participant what would be the day on the 1st January, giving them a particular year. Write a program to help the Host validate the answers given by the participants.

#### Input format :
The input consists of an integer that represents the year.

#### Output format :
Output prints the day on which the 1st January of that year lies.

**Sample test cases : <br>
Input 1 :**  <br>
1994 <br>
**Output 1 :** <br>
Saturday 

**Input 2 :** <br> 
2014 <br>
**Output 2 :** <br> 
Wednesday

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;
import java.io.*;
class Calendarquiz {
	public static void main(String [] args) {
		int year, d,c,f =0;
		Scanner sc = new Scanner(System.in);
		year = sc.nextInt();
	    year=year-1;
	    d=year%100;
	    c=year/100;
	    f=d/4;
	    f=f+d;
	    f=f+(c/4);
	    f=f-(2*c);
	    f=f+29;
	    f=f%7;
	    if(f<0)
	    {
	        f=f+7;
	    }
	    switch(f)
	    {
	        case 0:System.out.println("Sunday");break;
	        case 1:System.out.println("Monday");break;
	        case 2:System.out.println("Tueday");break;
	        case 3:System.out.println("Wednesday");break;
	        case 4:System.out.println("Thursday");break;
	        case 5:System.out.println("Friday");break;
	        case 6:System.out.println("Saturday");break;
	    }

	}
}

```

