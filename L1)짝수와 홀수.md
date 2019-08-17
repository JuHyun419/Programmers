# 문제설명 
#### 정수 num이 짝수일 경우 "Even"을 반환, 홀수일 경우 "Odd"를 반환<br><br>
# 제한조건
#### 
- num은 int 범위의 정수
#### 
- 0은 짝수<br><br><br>

# 입출력 예
| num | return |
---|:---:|
| `3` | "Odd" |
| `4` | "Even" |

<br>

```java
class Solution {
  public String solution(int num) {
      String answer = "";
      if ( num % 2 == 0) {
          answer = "Even";          
      } else {
          answer = "Odd";
      }
      return answer;
  }
}
```

