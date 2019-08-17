# 문제설명<br>
#### 정수를 담고 있는 배열 arr의 평균값을 return하는 함수, solution을 완성<br><br><br>
# 제한사항<br>
####
- arr은 길이 1 이상, 100 이하인 배열
- arr의 원소는 -10,000 이상 10,000 이하인 정수<br><br><br>
# 입출력 예<br>
| arr | return |
---|:---:
| [1,2,3,4] | 2, 5|
| [5, 5] | 5
```java
// <<< Java >>>
package Programmers;

class Solution2{
	public double solution(int[] arr)
	{
		double answer = 0;
		for(int i=0; i<arr.length; i++)
		{
			answer += arr[i];
		}
		return answer / arr.length;
	}
}

public class ArrAvg {

	public static void main(String[] args) {
		Solution2 sol = new Solution2();
		int[] arr = {1, 2, 3, 4};
		int[] arr2 = {5, 5};
		
		System.out.println(sol.solution(arr));
		System.out.println((int)sol.solution(arr2));
	}
}
```
---
```c
// <<< C >>>
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>

// arr_len은 배열 arr의 길이입니다.
double solution(int arr[], size_t arr_len) {
    double answer = 0;
    int i;
    double sum = 0;
    for(i=0; i<arr_len; i++)
    {
        sum = sum + arr[i];
    }
    answer = sum / arr_len;
    return answer;
}

int main(void)
{
	int arr[4] = {1, 2, 3, 4};
	printf("%.1f\n", solution(arr, 4));
	
	int arr1[2] = {5, 5};
	printf("%.ff\n", solution(arr1, 2));
}
```
---
```python3
## Python
def solution(arr):
    answer = 0
    for i in range(len(arr)):
        answer = answer + arr[i]
    answer = answer / len(arr)
    return answer
```
