# Full Islands

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:

·    All of the black cells must be connected.
<br>
·    Each numbered cell must be part of a white island of connected white cells.
<br>
·    Each island must have the same number of white cells as the number it contains (including the numbered cell).
<br>
·    Two islands may not be connected.
<br>
·    There cannot be any 2x2 blocks of black cells.

Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color.

**Problem Statement:**
<br>
The step 1 of solving the puzzle is identifying "Full islands".
<br>
An island is full if it contains as many white cells as the number in the region. Any 1s are trivially full regions. When you encounter a full region, any cells that boarder it must be black. Here we show the cells that must be black due to a single celled white island.

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/af0822c0-766f-4f2c-91c9-c431f1e374db)


#### Input format :
First line of the input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a valid initial board configuration with N*N cells. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by the integer 20 in the matrix representation of the input configuration.

#### Output format :
Output should display the board configuration with N*N cells after applying step 1. Grey colored cells are represented by the integer 20, numbered cells are represented by the same number given in the input and black cells are represented by 0.
<br>
Refer sample input and output for formatting specifications.

**Sample test cases :<br>
Input 1 :**
```
5
20 20 1 20 3
20 20 20 20 20
20 20 20 20 20
20 20 20 20 20
6 20 3 20 20
```
**Output 1 :**
```
20 0 1 0 3 
20 20 0 20 20 
20 20 20 20 20 
20 20 20 20 20 
6 20 3 20 20 
```
**Input 2 :**
```
5
20 20 20 20 20
3 20 20 6 20
20 20 20 20 20
20 2 20 20 1
20 20 20 20 20
```
**Output 2 :**
```
20 20 20 20 20 
3 20 20 6 20 
20 20 20 20 0 
20 2 20 0 1 
20 20 20 20 0
```


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class fullIslands {
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
	        	if((i>0) && (a[i-1][j] ==1)) { a[i][j]=0;}
	        	if((i<n-1)&& (a[i+1][j] == 1)) {a[i][j] =0;}
	            if((j>0) && (a[i][j-1] ==1)) { a[i][j] =0;}
	            if((j<n-1) && (a[i][j+1] ==1)) {a[i][j] =0;}
	        }
	    }
	    for(i=0;i<n;i++)
	    {
	        for(j=0;j<n;j++)
	        {
	            System.out.print(a[i][j]+" ");
	        }
	        System.out.println();
	    }

	}
}

```
