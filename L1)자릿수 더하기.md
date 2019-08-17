# 문제설명  
#### 자연수 N이 주어지면, N의 각 자릿수의 합을 구해서 return<br><br><br>
# 제한사항  
####  
- N의 범위 : 100,000,000 이하인 자연수<br><br><br>
# 입출력 예  
| N | answer |
---|---
| 123 | 6 |
| 987 | 24 |  
```java
package Programmers;

import java.util.*;

class Solution7 {
    public int solution(int n) {
        int answer = 0;
        int sum = 0;
        while(n!=0)
        {
        	answer = answer + (n%10);
        	n /= 10;
        }
        
        return answer;
    }
}

public class PlusSumofCount {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Solution7 sol = new Solution7();
		System.out.println(sol.solution(123));
		System.out.println(sol.solution(1234));
		System.out.println(sol.solution(12345));
		System.out.println(sol.solution(987));
	}

}

```
