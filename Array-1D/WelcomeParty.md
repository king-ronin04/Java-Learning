# Welcome Party

New Year is shortly arriving and the students of St. Philip’s College of Business are eager to receive the freshers for the coming year. The Welcome party for the freshers is going to be organized in a week’s time and in connection to that the College Management has ordered the students to renovate their class room block. The Class room block has N rooms in it numbered from 1 to N. Each room is currently painted in one of the red, blue or green colors. Students are given configuration of colors of their class room block by an array consisting of N values. In this array, color red will be denoted by '1', green by '2' and blue by '3'.

The Management wanted the class room block to be repainted such that each class room has same color. For painting, Students have all the 3 color paints available and mixing any 2 color paints will result into 3rd color paint i.e

·    1 + 2 = 3
<br>
·    2 + 3 = 1
<br>
·    3 + 1 = 2

For example, if a room is already painted in green color, painting that room red color, will make the color of the room blue.

Also, students have many buckets of paint of each color. Simply put, you can assume that they will not run out of paint. Students are a bit lazy, so they does not want to work much and therefore, has asked you to find the minimum number of rooms they have to repaint (possibly zero) in order to have all the rooms with same color as told by the Management. Can you please help them?

#### Input format :
First line of input contains an integer N, denoting the number of class rooms in the College’s class room black. Assume that the maximum value for N as 50.
<br>
Next line of input contains N values, denoting the current color configuration of rooms.

#### Output format :
Print the minimum number of rooms that need to be painted in order to have all the rooms painted with same color i.e red, blue or green.

**Sample test cases :<br>
Input 1 :**
```
3
1 2 1
```
**Output 1 :**
```
1
```
**Input 2 :**
```
3
1 1 1
```
**Output 2 :**
```
0
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```
import java.util.*;
public class Main{
    
    public static int mR(int N, int[] colors){
        int [] colorCounts= new int[3];
        for(int color: colors){
            colorCounts[color-1]++;
        }
        int maxCount=Arrays.stream(colorCounts).max().orElse(0);
        int minR=N-maxCount;
        return minR;
    }
    
    public static void main(String [] args){
        Scanner sc=new Scanner(System.in);
        int N=sc.nextInt();
        int [] colors=new int[N];
        for(int i=0;i<N;i++){
            colors[i]=sc.nextInt();
        }
            int result=mR(N,colors);
            System.out.println(result);
        
    }
}
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
```
import java.io.*;
import java.util.*;
class Welcomepaarty {
	public static void main(String [] args) {
		int i,j=0,n,k=0,c=0;
		Scanner sc = new Scanner(System.in);
		n=sc.nextInt();
		int a[] = new int[n];
		for(i=0;i<n;i++) {
			a[i] = sc.nextInt();
		}
	    for(i=0;i<n;i++)
	    {
	        if(a[i]==1) { 
	        	k++;
	        	}
	        else if(a[i]==2) { 
	        	j++;
	        	}
	        else { 
	        	c++;
	        	}
	    }
	    if(k>j)
	    {
	        if(k>c)
	        {
	            System.out.println(n-k);
	        }
	        else {
	        	System.out.println(n-c);
	        	}
	    }
	    else if(j>c) {
	    	System.out.println(n-j);
	    	}
	    else { 
	    	System.out.println(n-c);
	    	}

	}
}

```
