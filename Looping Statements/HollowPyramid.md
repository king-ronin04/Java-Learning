# Hollow Pyramid

The much awaited event at the entertainment industry every year is the "Screen Awards". This year the event is going to be organized on December 25 to honour the Artists for their professional excellence in Cinema. The Organizers of the event, J&R Events, decided to design some attractive and LED Matrix panel boards for the show promotions all across the venue.
<br>
The Event organizers wanted to program the display boards with some specific pattern using alphabets and special characters. Help them write a program to design the pattern of a hollow pyramid in the matrix panel, given the number of lines of the pattern. 

#### Input format :
First line of the input is an integer that refers to the number of lines in the pattern.

#### Output format :
Output the pattern as given in the output.

**Sample test cases :<br>
Input 1 :<br>**
4<br>
**Output 1 :<br>**
![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/306f5263-35d4-4118-913a-8d8f2120e0ea)


**Input 2 :<br>**
5<br>
**Output 2 :<br>**
![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/43c5b309-3930-4486-8764-6b970c20826f)


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Hollowpyramid {
	public static void main(String [] args) {
	    int n,i,j,k;
	    Scanner sc = new Scanner(System.in);
	    n = sc.nextInt();
	    k=(2*n)-1;
	    for(i=n;i>0;i--)
	    {
	        for(j=1;j<=k;j++)
	        {
	            if((j==i)||(j==k-i+1)||(i==1)) { 
	            	System.out.print("*");
	            	}
	            else if((j<i)||(j>k-i)) { 
	            	System.out.print("b");
	            	}
	            else { 
	            	System.out.print("i");
	            	}
	        }
	        System.out.println();
	    }

	}
}

```
