# Valid Configuration

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:
<br>
·       All of the black cells must be connected.
<br>
·       Each numbered cell must be part of a white island of connected white cells.
<br>
·       Each island must have the same number of white cells as the number it contains (including the numbered cell).
<br>
·       Two islands may not be connected.
<br>
·       There cannot be any 2x2 blocks of black cells.
<br>
Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color. 

__Problem Statement:__
<br>
The step 1 of solving the puzzle is identifying "Full islands".
<br>
An island is full if it contains as many white cells as the number in the region. Any 1s are trivially full regions. When you encounter a full region, any cells that boarder it must be black. Here we show the cells that must be black due to a single celled white island.
<br>
Below figure is the one after identifying full islands
<br>
The step 2 of solving the puzzle is to identify the neighbors.
<br>
Since two numbers in a nurikabe puzzle cannot be part of the same island, any cell that has two numbered neighbors must be black. The two cases are when a cell is between two numbered cells, or (as in the image) when two numbered cells in the nurikabe are adjacent diagonally.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/2cb8dbc2-7294-4169-ac2b-a640f835776d)
![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/21f090aa-943e-4c3b-bc1a-97bdccb2672a)

Given a board configuration in which empty white cells are represented by -1, black cells are represented by 0 and grey cells are represented by 20. Write a program to find whether it is a valid configuration assuming it to be obtained after performing step 1 and 2.

#### Input format :
First and only line of input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a board configuration with N*N cells assuming it to be obtained after performing step 1 and step 2. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by 20, empty white cells are represented by -1 and black cells are represented by 0 in the matrix representation of the input configuration.

#### Output format :
Output should display "Yes" (without quotes) if the given configuration is a valid one obtained after performing step 1 and 2 of the nurikabe puzzle. Print "No" otherwise.
<br>
Refer sample input and output for formatting specifications.

**Sample test cases :<br>
Input 1 :**
```
5
20 0 1 0 2
20 20 0 20 -1
20 20 20 20 20
3 0 2 20 20
20 20 20 20 20
```
**Output 1 :**
```
Yes
```
**Input 2 :**
```
5
20 0 1 0 2
20 20 0 20 -1
20 20 20 20 20
3 20 2 20 20
20 20 20 20 20
```
**Output 2 :**
```
No
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class validConfiguration {
	public static void main(String [] args) {
		int i,j,n,s=1;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[][] = new int[n][n];
		for(i=0;i<n;i++) {
			for(j=0;j<n;j++) {
				a[i][j] = sc.nextInt();
			}
		}
	    for(i=0;i<n;i++)
	    {
	        for(j=0;j<n;j++)
	        {
	            if(a[i][j]==1)
	            {
	                if((i>0)&&(a[i-1][j]!=0)){s=0;break;}
	                if((i<n-1)&&(a[i+1][j]!=0)){s=0;break;}
	                if((j<n-1)&&(a[i][j+1]!=0)){s=0;break;}
	                if((j>0)&&(a[i][j-1]!=0)){s=0;break;}
	            }
	            if((a[i][j]>0)&&(a[i][j]<11))
	            {
	                if((i<n-2)&&(a[i+2][j]<11)&&(a[i+2][j]>0)){if(a[i+1][j]!=0){s=0;break;}}
	                if((j<n-2)&&(a[i][j+2]<11)&&(a[i][j+2]>0)){if(a[i][j+1]!=0){s=0;break;}}
	                if((i>0)&&(j>0)&&(a[i-1][j-1]<11)&&(a[i-1][j-1]>0)){if((a[i-1][j]!=0)||(a[i][j-1]!=0)){s=0;break;}}
	                if((i<n-1)&&(j>0)&&(a[i+1][j-1]<11)&&(a[i+1][j-1]>0)){if((a[i+1][j]!=0)||(a[i][j-1]!=0)){s=0;break;}}
	            }
	        }
	        if(s==0){break;}
	    }
	    if(s ==0) {
	    	System.out.println("No");
	    }
	    else {
	    	System.out.println("Yes");
	    }

	}
}

```
