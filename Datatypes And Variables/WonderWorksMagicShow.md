# WonderWorks Magic Show

The Magic Castle, the home of the Academy of Magical Arts at California has organized the great ‘WonderWorks Magic Show’. 3 renowned magicians were invited to mystify and thrill the crowd with their world’s spectacular magic tricks. At the end of each of the 3 magicians’ shows, the audience were requested to give their feedback in a scale of 1 to 10. Number of people who watched each show and the average feedback rating of each show is known. Write a program to find the average feedback rating of the WonderWorks Magic show.

**Input format :** <br>
First line of the input is an integer value that corresponds to the number of people who watched show 1.<br>
Second line of the input is a float value that corresponds to the average rating of show 1.<br>
Third line of the input is an integer value that corresponds to the number of people who watched show 2.<br>
Fourth line of the input is a float value that corresponds to the average rating of show 2.<br>
Fifth line of the input is an integer value that corresponds to the number of people who watched show 3.<br>
Sixth line of the input is a float value that corresponds to the average rating of show 3.<br>

**Output format :** <br>
Output should display the overall average rating for the show. Display the rating correct to 2 decimal places.

**Sample test cases :** <br>
**Input 1 :** <br>
400<br>
9.8<br>
500<br>
9.6<br>
100<br>
5<br>
**Output 1 :** <br>
9.22

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.text.DecimalFormat;
import java.util.*;

class Magicshow {

  public static void main(String[] args) {
    int num1, num2, num3;
    float rate1, rate2, rate3, result = (float) 0.0;
    DecimalFormat d = new DecimalFormat("0.00");
    Scanner sc = new Scanner(System.in);
    num1 = sc.nextInt();
    rate1 = sc.nextFloat();
    num2 = sc.nextInt();
    rate2 = sc.nextFloat();
    num3 = sc.nextInt();
    rate3 = sc.nextFloat();
    result = ((num1 * rate1) + (num2 * rate2) + (num3 * rate3)) / (num1 + num2 + num3);
    System.out.println(d.format(result));
  }
}


```
