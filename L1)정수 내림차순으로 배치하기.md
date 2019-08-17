# 문제설명  
#### 정수 n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수 리턴  
#### n이 118372 => 873211을 리턴<br><br><br>
# 제한 조건  
####
 - n은 1이상 8000000000 이하인 자연수<br><br><br>  
# 입출력 예  
| n | return |
---|:---:  
| 118372 | 873211|  
```java
package Programmers;

import java.util.*;

class Solution8{
	public long solution(long n) {
		long answer = 0;
		StringBuilder sb = new StringBuilder();
		StringBuilder sb2 = new StringBuilder();
		
		// sb => "118372"
		sb.append(n);
		
		List<Integer> list = new ArrayList<>();
		for(int i=0; i<sb.length(); i++)
		{
			// list에 문자열 sb를 i, i+1까지 짤라서 int형으로 넣는다.
			list.add(Integer.parseInt(sb.substring(i, i+1)));
		}
		
		// list 정렬(sort)
		Collections.sort(list);
		
		// list 역순(reverse)
		Collections.reverse(list);
		
		for(int i=0; i<list.size(); i++) {
			sb2.append(list.get(i));
		}
		return Long.valueOf(String.valueOf(sb2));
	}
}

public class IntegerDESC {

	public static void main(String[] args) {
		Solution8 sol = new Solution8();
		System.out.println(sol.solution(118372));
	}
}

```
