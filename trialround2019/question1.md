## Question 1
```java
//Freya Jiang’s Solution
import java.util.*;
import java.io.*;

public class Solution {

  public static void main(String[] args) {
    Scanner in = new Scanner(new BufferedReader(new InputStreamReader(System.in)));
    
    // T is test case number
    int t = in.nextInt(); // Scanner has functions to read ints, longs, strings, chars, etc.
    for (int i = 1; i <= t; ++i) {
      int a = in.nextInt() + 1;
      int b = in.nextInt();
      
      int n = in.nextInt();
      for (int j = 0; j < n; ++j) {
        int guess = (a + b) / 2;
        System.out.println(guess);
        String result = in.next();
        if (result.equals("CORRECT")) {
            break;
        } else if (result.equals("TOO_SMALL")) {
            a = guess + 1;
        } else if (result.equals("TOO_BIG")) {
            b = guess - 1;
        } else { // WRONG_ANSWER
            return;
        }
      }
    }
  }
}
```
