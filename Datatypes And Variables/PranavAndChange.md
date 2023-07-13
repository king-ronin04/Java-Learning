# Pranav and Change 

Pranav, an enthusiastic kid visited the "Fun Fair 2017" along with his family. His father wanted him to purchase entry tickets from the counter for his family members. Being a little kid, he is just learning to understand about units of money. Pranav has paid some amount of money for the tickets but he wants your help to give him back the change of Rs. N using minimum number of rupee notes. 

Consider a currency system in which there are notes of seven denominations, namely, Rs. 1, Rs. 2, Rs. 5, Rs. 10, Rs. 50, Rs. 100. If the change given to Pranav Rs. N is input, write a program to computer smallest number of notes that will combine to give Rs. N.



**Input format :** <br>
First line of the input is an integer N, the change to be given to Pranav.

**Output format :** <br>
Output should display the the smallest number of notes that will combine to give N.

**Sample test cases :** <br>
**Input 1 :** <br>
1200<br>
**Output 1 :** <br>
12

**Input 2 :** <br>
242 <br>
**Output 2 :** <br>
7

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.Scanner;

public class PranavAndChange {

  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int x = sc.nextInt();
    sc.close();
    int[] arr = { 100, 50, 10, 5, 2, 1 };
    int count = 0;
    for (int ele : arr) {
      if (x >= ele) {
        count += x / ele;
        x %= ele;
      }
    }
    System.out.println(count);
  }
}


```
