# 문제 설명<br>
#### 두 정수 a,b가 주어졌을떄, a와 b사이에 속한 모든 정수의 합 구하기<br><br><br>
# 제한 조건<br>
####
- a와 b가 같으면 아무수나 리턴  
- a, b는 -10,000,000 이상 10,000,000이하인 정수  
- a, b의 대소관계는 정해져 있지 않다.<br><br><br>
# 입출력 예  
| a | b | return |
---|:---:|---:
| 3 | 5 | 12 |
| 3 | 3 | 3 |
| 5 | 3 | 12 |  

```java
class Solution {
  public long solution(int a, int b) {
      long answer = 0;
      if(a>=b)
           for(int i=b; i<=a; i++)
           {
              answer += i; 
           }
      else
          for(int i=a; i<=b; i++)
          {
              answer += i;
          }
      return answer;
      }
}
```
Update
