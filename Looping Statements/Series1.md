# Series 1

The Event Organizing Company "Buzzcraft" focuses event management in a way that creates a win-win situation for all involved stakeholders. Buzzcraft don't look at building one time associations with clients, instead, aim at creating long-lasting collaborations that will span years to come. This goal of the company has helped them evolve and gain more clients within notable time.
The number of clients of the company from the start day of their journey till now is recorded sensibly and is seemed to have followed a specific series like: 2,3,5,7,11,13,17,19, 23 ... 

Write a program which takes an integer N as the input and will output the series till the Nth term.

#### Input format :
First line of the input is an integer N.

#### Output format :
Output a single line the series till Nth term, each separated by a comma.

**Sample test cases :<br>
Input 1 :** <br>
5<br>
**Output 1 :**  <br>
2 3 5 7 11 <br>

**Input 2 :** <br>
10 <br>
**Output 2 :** <br>
2 3 5 7 11 13 17 19 23 29

------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class Series1 {
	public static void main(String [] args) {
	    int n,i,j,k=2,s=0;
	    Scanner sc = new Scanner(System.in);
	    n = sc.nextInt();
	    for(i=0;i<n;i++)
	    {
	        for(j=2;j<=k/2;j++)
	        {
	            if(k%j==0) { 
	            	s=1;
	            	break;
	            	}
	        }
	        if(s==0) { 
	        	System.out.print(k+" ");
	        	}
	        else { 
	        	i--; 
	        	}
	        k++;s=0;
	    }

	}
}
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;

public class Main{
    
    static boolean prime(int n){
        if(n==1)
            return false;
        if(n==2 || n==3) return true;
        if(n%2==0 || n%3==0) return false;
        
        for(int i=5;i*i<=n;i+=6){
            if(n%i==0 || n%(i+2)==0)    
                return false;
        }
        return true;
    }
    
    
    public static void main(String [] argss){
        int n;
        Scanner sc=new Scanner(System.in);
        n=sc.nextInt();
        int count=1;
        for(int i=2;count<=n;i++){
            if(prime(i)){
                count++;
                System.out.print(i+" ");
            }
        }
    }
}
```
