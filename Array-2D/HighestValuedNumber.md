# Highest Valued Number

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:
<br>
·    All of the black cells must be connected.
<br>
·    Each numbered cell must be part of a white island of connected white cells.
<br>
·    Each island must have the same number of white cells as the number it contains (including the numbered cell).
<br>
·    Two islands may not be connected.
<br>
·    There cannot be any 2x2 blocks of black cells.
<br>
Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color.

**Problem Statement:** <br>
Write a program to find the highest valued number in the numbered cells, given a valid initial board configuration. Below figure is the sample valid initial configuration.



#### Input format :
First line of the input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a valid initial board configuration with N*N cells. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by the integer 20 in the matrix representation of the input configuration.

#### Output format :
Output should display the highest valued number in the numbered cells.

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
6
```
**Input 2 :**
```
5
20 20 20 20 4
1 20 20 20 20
20 20 20 20 20
20 2 20 20 20
20 20 20 20 20
```
**Output 2 :**
```
4
```


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;
class highestValuedNumber {
	public static void main(String [] args) {
		int i,j,n,k=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[][] = new int[n][n];
		for(i=0;i<n;i++) {
			for(j=0;j<n;j++) {
				a[i][j] = sc.nextInt();
				if(a[i][j] < 11) {
					if(a[i][j] > k) {
						k=a[i][j];
					}
				}
			}
		}
		System.out.println(k);
	}
}

```

