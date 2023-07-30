During the Independence Day celebration, the Department of Mathematics had arranged for a challenge where college students participated in large number. Many interesting games were conducted, one such game that attracted most students was the tile game where the students were given 'N' square tiles of the same size and were asked to form the largest possible square using those tiles.

Help the students by writing a program to find the area of the largest possible square that can be formed, given the side of a square tile (in cms) and the number of square tiles available.

#### Input format :
First line of the input is an integer that corresponds to the side of a square tile (in cms).
<br>
Second line of the input is an integer that corresponds to the number of square tiles available.

#### Output format :
Output should display the area of the largest possible square that can be formed (in square cms) with the available tiles.

**Sample test cases :<br>
Input 1 :<br>**
5<br>
8<br>
**Output 1 :<br>**
100.0

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.util.*;
class SquareTile {
    public static void main(String[] args) {
        Scanner sc =new Scanner(System.in);
        double l= sc.nextDouble();
        double n= sc.nextDouble();
        int i;
        int m;
        i=1;
        m=0;
        while(i*i <= n)
    {
        m=i*i;
        i++;
    }
   double a=m*(l*l);
    System.out.println(a);
    }
    
}

```
