# Daily Routine
Brendon is a little techno-whiz whose IQ is out of the charts. He has set up a laboratory at home for his research and development and was once approached by an Event Management firm to design them a Robot that would log all the activities carried out in an event at various instants during the day. This would help them keep a track and in smooth functioning of events.
<br>
Brendon, after long days of hard work designed one such Robot but wanted to test it on his own daily routines. His daily routine is very simple, he starts his day working in a computer, then he eats food and finally proceeds for sleeping thus ending his day. He has programmed his Robot to log the activities of him at various instants during the day.

Today it recorded activities that Brendon was doing at N different instants. These instances are recorded in chronological order (in increasing order of time). This log is provided to you in form of a string s of length N, consisting of characters 'C', 'E' and 'S'. If s[i] = 'C', then it means that at the i-th instant Brendon was working in Computer, 'E' denoting he was eating and 'S' means he was sleeping.

Write a program to tell whether the record log made by the robot could possibly be correct or not. 

#### Input format :
The only line of input contains the string s.
#### Output format :
Output a single line containing "yes" or "no" (without quotes) accordingly.

**Sample test cases : <br>
Input 1 :** <br>
CES<br>
**Output 1 :** <br>
Yes

**Input 2 :** <br>
SCCC <br>
**Output 2 :** <br>
No

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;
import java.lang.*;
import java.io.*;
class Main{
    public static void main(String [] args){
        Scanner sc=new Scanner(System.in);
        String s=sc.next();
        int temp=0;
        for(int i=1;i<s.length();i++)
        {
            if(s.charAt(i)<s.charAt(i-1)){
                temp=1;
            }
        }
        if(temp==1)
            System.out.println("No");
        else 
            System.out.println("Yes");
        
    }
}
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;
import java.io.*;
class Dailyroutine {
	public static void main(String [] args) {
		int i,len,count =0;
		String s;
		Scanner sc = new Scanner(System.in);
		s = sc.nextLine();
		len = s.length();
		for(i=0; i<len;i++) {
			if(s.charAt(i) == 'C') {
				count = 1;
				break;
			}
			else if((s.charAt(i) == 'S') || (s.charAt(i) == 'E')) {
				break;
			}
		}
		for(;i<len;i++) {
			if(s.charAt(i) == 'E') {
				count++;
				break;
			}
			else if((s.charAt(i)=='S')&&(count==1)) {
				count=-100;
				break;
				}
	        else if(s.charAt(i)=='S') { 
	        	break;
	        	}

		}
		for(;i<len;i++)
	    {
	        if(s.charAt(i)=='S')
	        {
	            count++;
	        }
	        else if(s.charAt(i)=='C') {
	        	count=-100;
	        	break;
	        	}
	    }

		if(count>0) {
			System.out.println("Yes");
		}
		else {
			System.out.println("No");
		}
	}
}
```
