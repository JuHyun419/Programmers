# 문제설명<br>
#### 정수 x와 자연수 n을 입력 받아 x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴<br><br>
# 제한 조건<br>
####
- n은 1000 이하인 자연수<br><br><br>
# 입출력 예<br>
| x | n | answer |
---|:---:|---:
| 2 | 5 | [2, 4, 6, 8, 10]
| 4 | 3 | [4, 8, 12] |
| -4 | 2 | [-4, -8 ] |

```java
// <<< Java >>>
package ProgrammersLv1;

import java.util.Scanner;

// x, n을 입력받아서 x부터 시작해 x씩 증가하는 숫자를 n개 지니는 배열 리턴
class Solution14 {
	  public long[] solution(int x, int n) {
	      long[] answer = {};
	      answer = new long[n];
	      for(int i=0; i<n; i++)
	      {
	    	  // x*1, x*2, x*3, x*4, ...
	    	  answer[i] =  x * (i+1);
	      }
	      return answer;
	  }
	}

public class xlengthnNum {

	public static void main(String[] args) {
		Solution14 sol = new Solution14();
		
		Scanner scan = new Scanner(System.in);
		int x = scan.nextInt();
		int n = scan.nextInt();
		long []arr = new long[n];
		
		arr = sol.solution(x, n);
		for(int i=0; i<arr.length; i++)
		{
			System.out.print(arr[i] + " ");
		}
	}

}

