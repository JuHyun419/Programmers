# K번째 수
https://programmers.co.kr/learn/courses/30/lessons/42748

```java
import java.util.*;

class Solution {
public int[] solution(int[] array, int[][] commands) {
		int[] answer = new int[commands.length];
		for(int i=0; i<commands.length; i++) {
			// 새로운 배열의 크기 -> commands[i][1] ~ commands[i][0]까지 자른 후 정렬하므로 두 값 빼고 +1
			int[] arr = new int[commands[i][1] - commands[i][0] + 1];
			int arrIndex = 0;
			
			// commadns의 [i][0]-1 ~ [i][1]까지 잘라서 array 배열의 요소 값을 arr에 저장하기.
			// 예제대로 2번째 ~ 5번째라면 배열의 인덱스상 1, 2, 3, 4 값이 들어가야 하므로 -1 해줌.
			for(int j=commands[i][0]-1; j<commands[i][1]; j++) 
				arr[arrIndex++] = array[j];
			
			Arrays.sort(arr);	// 배열 정렬
			answer[i] = arr[commands[i][2] - 1];
		}
		return answer;
	}
}
```
