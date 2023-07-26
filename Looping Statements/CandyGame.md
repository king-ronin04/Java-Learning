# Candy Game 
Mona set off with great zeal to the "Fun Fair 2017". There were numerous activities in the fair, though Mona liked the Candy game. Delicious candies were wrapped in colourful foiled sheets with some random numbers on each of the candies. The game coordinators then formed many groups of few candies together, such that each candy group makes an integer and hid them all around the room. The objective of the game is that the players should look for the occurrences of number four anywhere in the integers (candy groups) placed in the room.

Mona started off with the game where there are many such integers, for each of them she should calculate the number of occurrences of the digit 4 in the decimal representation. Can you please help her in succeeding the game?

#### Input format :
The only line of input contains a single integer from the candy group.

#### Output format :
Output should contain the number of occurrences of the digit 4 in the respective integer from the candy groups that Mona gets.

**Sample test cases : <br>
Input 1 :** <br>
447474 <br>
**Output 1 :** <br>
4 

**Input 2 :** <br>
12<br>
**Output 2 :** <br>
0


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;
import java.io.*;
class Candygame {
	public static void main(String [] args) {
		int n,i,count = 0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		for(i=0;n>0;i++) {
			if(n%10 == 4) {
				count++;
			}
			n= n/10;
		}
		System.out.println(count);
	}
}

```
