# 문제설명<br>
#### 두 수를 입력받고, 최대공약수 & 최소공배수 구하기<br><br>
# 제한 사항<br>
####
- 두 수는 1 이상 1000000 이하인 자연수<br><br><br>
# 입출력 예<br>
| n | m | return|
---|:---:|---:
| 3 | 12 | [3, 12] |
| 2 | 5  | [1, 10] |

```java
package Programmers;

class Solution4 {
	  public int GCM(int n, int m)
	  {
		  int temp;
		  
		  if(n<m)
		  {
			  temp = n;
			  n = m;
			  m = temp;
		  }
		  
		  // 삼항 연산자
		  return (m<=0) ? n : GCM(m, n%m);
		  //if(m<=0)
	    	        // 최대공약수
	    	        //return n;
	          //else
	    	        //return GCM(m, n%m);
	  }
	
	  public int[] solution(int n, int m) {
	      int[] answer = new int[2];
          // 최대공약수
	      answer[0] = GCM(n, m);
	      // 최소공배수
	      answer[1] = n*m/ answer[0];
	    	  
	      return answer;
	  }
	}

public class GCMLCM {
	public static void main(String[] args) {
		Solution4 sol = new Solution4();
		int []arr = sol.solution(21, 6);
		System.out.println(arr[0]);
		System.out.println(arr[1]);
	}
}
```
