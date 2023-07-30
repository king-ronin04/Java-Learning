# Change Position

The room that Patrick and Johnny were staying was very big. They felt lazy to walk inside the room from the bed's location to another location. So they wanted to change the position of the bed. The shape of the room is a Square. They decided to place the bed at the exact center of the room so that their walking distance would be minimised. Can you please help them in placing the bed at the exact centre?

![image](https://github.com/king-ronin04/Java-Learning/assets/103017387/cf4f30ae-b5ef-4455-9d62-4d80a2ef088f)

Given the coordinates of the left bottom vertex of the square room and the length of the side, you need to write a program to determine the coordinates of the centre of the room.

### [Assumption --- Length of the side is always even]

**Input format :** <br>
Input consists of 3 integers. The first integer corresponds to the x-coordinate of the left bottom vertex. The second integer corresponds to the y-coordinate of the left bottom vertex. The third integer corresponds to the length of the square.

**Output format :** <br>
The output prints the x and y coordinates of the center separated by a space.

**Sample test cases :** <br>
**Input 1 :** <br>
10<br>
30<br>
16<br>
**Output 1 :** <br>
18 38

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

```java
import java.io.*;
import java.util.*;

class Changeposition {

  public static void main(String[] args) {
    int x, y, length, cx, cy;
    Scanner sc = new Scanner(System.in);
    x = sc.nextInt();
    y = sc.nextInt();
    length = sc.nextInt();
    cx = x + (length / 2);
    cy = y + (length / 2);
    System.out.println(cx + " " + cy);
  }
}

```
