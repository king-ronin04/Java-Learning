# Calculating Gain Percentage

Vikram buys an old scooter for Rs. A and spends Rs. B on its repairs. If he sells the scooter for Rs. C , what is his gain % ?
![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/f1ced22a-de03-44ac-9ed5-a9f257e4f97d)

Write a program to compute the gain %.

**Input format :** <br>
First line of the input consists of the price of the scooter.<br>
Second line of the input consists of the repair charges.<br>
Third line of the input consists of the selling price.

**Output format :**
Output prints the gain percentage. Round off the output to two decimal places.

**Sample test cases :** <br>
**Input 1 :**<br>
4700<br>
800<br>
5800<br>
**Output 1 :**<br>
5.45

---------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.text.DecimalFormat;
import java.util.*;

class Gainpercentage {

  public static void main(String[] args) {
    int price, repair, sp, cp, gain;
    double gainpercent;
    DecimalFormat d = new DecimalFormat("0.00");
    Scanner sc = new Scanner(System.in);
    price = sc.nextInt();
    repair = sc.nextInt();
    sp = sc.nextInt();
    cp = price + repair;
    gain = sp - cp;
    gainpercent = ((double) gain / (double) cp) * 100;
    System.out.println(d.format(gainpercent));
  }
}

```
