# Count of Numbered Cells

Nurikabe logical game (sometimes called Islands in the Stream) is a binary determination puzzle. The puzzle is played on a typically rectangular grid of cells, some of which contain numbers. You must decide for each cell if it is white or black (by clicking on them) according to the following rules:

·       All of the black cells must be connected.
<br>
·       Each numbered cell must be part of a white island of connected white cells.
<br>
·       Each island must have the same number of white cells as the number it contains (including the numbered cell).
<br>
·       Two islands may not be connected.
<br>
·       There cannot be any 2x2 blocks of black cells.

Unnumbered cells start out grey and cycle through white and black when clicked. Initially numbered cells are white in color. 

**Problem Statement:** <br>
Write a program to find the count of numbered cells, given a valid initial board configuration. Below figure is the sample valid initial configuration.

﻿![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/08026930-d7ee-4475-8650-e6a6a49ca829)


#### Input format :
First line of the input is an integer N that gives the number of rows and columns of the grid.
<br>
Next N lines will have a valid initial board configuration with N*N cells. Assume that the maximum number in a cell can be 10. Grey colored cells are represented by the integer 20 in the matrix representation of the input configuration.

#### Output format :
Output should display an integer that gives the count of numbered cells, given a valid initial board configuration.

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
4
```
**Input 2 :**
```
9
20 5 20 20 3 20 20 20 20
20 20 8 20 20 20 20 5 20
20 20 20 20 20 20 2 20 20
20 20 20 20 20 20 20 20 20
20 20 20 20 20 20 20 20 20
20 20 20 20 20 20 20 20 20
20 20 3 20 20 20 20 20 20
20 3 20 20 20 20 3 20 20
20 20 20 20 1 20 20 6 20
```
**Output 2 :**
```
10
```


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
import java.io.*;
import java.util.*;
class countOfNumberedCells {
	public static void main(String [] args) {
		int i,j,n,count=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		int a[][] = new int[n][n];
		for(i=0;i<n;i++) {
			for(j=0;j<n;j++) {
				a[i][j] = sc.nextInt();
				if(a[i][j] < 11) {
					count++;
				}
			}
		}
		System.out.println(count);
	}
}

```
