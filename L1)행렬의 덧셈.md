# 문제설명<br>
#### 2개의 행렬 arr1, arr2를 입력받아 행렬 덧셈 결과를 반환<br><br>
# 제한 조건<br>
####
- 행렬 arr1, arr2의 행과 열의 길이는 500을 넘지 않는다.<br><br><br>
# 입출력 예<br>
| arr1 | arr2 | return|
---|:---:|---:
| [[1,2],[2,3]] | [[3,4],[5,6]]| [[4,6],[7,9]]|
| [[1],[2]] | [[3],[4]] | [[4],[6]]|

```java
// <<< Java >>>
package Programmers;

class Solution{
	public int[][] solution(int[][] arr1, int[][] arr2){
		int[][] answer = new int[arr1.length][arr1[0].length];
		for(int i=0; i<arr1.length; i++)
		{
			for(int j=0; j<arr2.length; j++)
			{
				answer[i][j] = arr1[i][j] + arr2[i][j];
			}
		}
		return answer;
	}
}

public class MatrixPlus {

	public static void main(String[] args) {
		
		Solution sol = new Solution();
		
		int [][]arr1 = {{1, 2}, {2, 3}};
		int [][]arr2 = {{3, 4}, {5, 6}};
		int [][]answer = sol.solution(arr1, arr2);
    
		for(int i=0; i<arr1.length; i++)
		{
			for(int j=0; j<arr2.length; j++)
			{
				System.out.print(answer[i][j] + " ");
			}
			System.out.println();
		}
	}
}
```
---
```python3
## <<< Python >>>
def solution(arr1, arr2):
    answer = []
    for i in range(len(arr1)):
        tmp = []
        for j in range(len(arr1[i])):
            tmp.append(arr1[i][j] + arr2[i][j])
        answer.append(tmp)
    return answer
```
