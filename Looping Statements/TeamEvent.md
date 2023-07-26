# Team Event
Super Quiz Bee is a famous quiz Competition that tests students on a wide variety of academic subjects. This week’s competition was a Team event and students who register for the event will be given a unique registration code N. The participants are teamed into 10 teams and the team to which a participant is assigned to depends on the absolute difference between the first and last digit in the registration code.

The event organizers wanted your help in writing an automated program that will ease their job of assigning teams to the participants. If the registration number given is less than 10, then the program should display "Invalid Input".

#### Input format :
The only line of input contains an integer N.

#### Output format :
Output the absolute difference between the first and last digit of N.

**Sample test cases :<br>
Input 1 :** <br>
345<br>
**Output 1 :** <br>
2<br>

**Input 2 :** <br>
9 <br>
**Output 2 :** <br>
Invalid Input


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Teamevent {
	public static void main(String [] args) {
		int num,n,i,l;
		Scanner sc = new Scanner(System.in);
		num = sc.nextInt();
	    if(num>=10)
	    {
	    n=num%10;
	    l=num;
	    for(i=0;num>0;i++)
	    {
	        num=num/10;
	        if(num>0){l=num;}
	    }
	    if(l>=n) {
	    	System.out.println(l-n);
	    }
	    else {
	    	System.out.println(n-l);
	    }
	    }
	    else
	    {
	        System.out.println("Invalid Input");
	    }

	}
}
```


-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```java
import java.util.*;

public class Main{
    
    static int first(int n){
        int digit=(int)(Math.log10(n));
        n=(int)(n/(int)(Math.pow(10,digit)));
        return n;
    }
    
    static int last(int n){
        return (n%10);
    }
    
    
    public static void main(String [] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        if(n<10){
            System.out.println("Invalid Input");
        }
        else if(n==10){
            System.out.println(first(n)-last(n));
        }
        else{
            if(first(n)>last(n))
                System.out.println(first(n)-last(n));
            else
                System.out.println(last(n)-first(n));
        }
        
        
    }
}
```
