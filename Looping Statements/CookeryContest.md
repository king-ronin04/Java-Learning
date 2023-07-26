# Cookery Contest
 
Suzanne is participating in the Cookery Contest to be held at her Company. Suzanne is just a beginner in cooking but is more creative. She wanted to give a good show though she is going to cook for the first time. So she decided to cook only a small portion of her recipe, which has the same ratios of ingredients, but makes less food.

Suzanne however, does not like fractions. The original recipe contains only whole numbers of ingredients, and Suzanne wants the reduced recipe to only contain whole numbers of ingredients as well. Help her determine how much of each ingredient to use in order to make as little food as possible.
#### Input format :
The first line of the input consists of a positive integer N, which corresponds to the number of ingredients.
Next line contains N space-separated integers, each indicating the quantity of a particular ingredient that is used.
#### Output format :
Output exactly N space-separated integers on a line that gives the quantity of each ingredient that Suzanne should use in order to make as little food as possible.

**Sample test cases : <br>
Input 1 :** <br>
3 <br>
3 6 9 <br>
**Output 1 :**  <br>
1 2 3 


-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```java
import java.io.*;
import java.util.*;
class Cookerycontest {
	public static void main(String [] args) {
		int i,j,k,n;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
	    j=a[0];
	    for(i=0;i<n;i++)
	    {
	        if(j>a[i]){j=a[i];}
	    }
	    i=2;
	    for(k=0;i<=j;k++)
	    {
	        if((a[k]%i)!=0){i++;k=-1;}
	        else if(k==n-1)
	        {
	            for(k=0;k<n;k++)
	            {
	                a[k]=a[k]/i;
	            }
	            i=2;
	            k=-1;
	        }
	    }
	    for(i=0;i<n;i++)
	    {
	        System.out.print(a[i]+" ");
	    }

	}
}


```
