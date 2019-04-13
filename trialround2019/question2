## Question 2
```java
//Freya Jiang’s solution
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
      Scanner in = new Scanner(new BufferedReader(new InputStreamReader(System.in)));
      int t = in.nextInt();
      for (int i = 1; i <= t; ++i) {
        int n = in.nextInt();
        int[] wall = new int[n];

        char[] wallStrings = in.next().toCharArray();
        for (int j = 0; j < n; j++) {
          wall[j] =  wallStrings[j] - '0';
        }
        int currentSum = 0;
        int k = (n + 1) / 2;
        for (int j = 0; j < k ; j++) {
          currentSum += wall[j];
        }
        int result = currentSum;
        for (int j = k; j < n; j++) {
          currentSum -= wall[j - k];
          currentSum += wall[j];
          result = Math.max(result, currentSum);
        }
        System.out.println("Case #" + i + ": " + result);
      }
    }
}
```
