# 문제설명<br>
#### 대문자와 소문자가 섞여있는 문자열 s에서, 'p'의 개수와 'y'의 개수를 비교해서 같으면 True, 다르면 False를 리턴  
#### 'p', 'y'가 하나도 없는경우 항상 True 리턴. 단, 대문자와 소문자는 구별하지 않는다.<br><br>
# 제한 조건<br>
####
- 문자열 s의 길이 : 50 이하의 자연수  
- 문자열 s는 알파벳으로만 이루어져 있음.<br><br>
# 입출력 예<br>
| s | answer |
---|:---:
| "pPoooyY" | True 
| "Pyy" | false 

```java
package ProgrammersLv1;

class Solution29 {
    boolean solution(String s) {
        boolean answer = true;
        
        // 문자열에 p,P,  y,Y의 개수
        int p_num = 0;
        int y_num = 0;
        
        for(int i=0; i<s.length(); i++) {
        	if(s.charAt(i) == 'p' || s.charAt(i) == 'P')	
        		p_num += 1;
        	else if(s.charAt(i) == 'y' || s.charAt(i) == 'Y')
        		y_num += 1;
        	
        	// 'p', 'y'가 하나도 없는 경우
        	if(p_num == 0 && y_num == 0)
        		answer = true;
        	
        	// 'p', 'y'의 개수가 같으면 true, 다르면 false
        	answer = (p_num == y_num) ? true : false;
        }
        return answer;
    }
}

public class 문자열내p와y의개수 {

	public static void main(String[] args) {
		Solution29 sol = new Solution29();
		boolean answer1 = true;
		boolean answer2 = true;
		answer1 = sol.solution("pPoooyY");
		answer2 = sol.solution("Pyy");
		
		System.out.print(answer1 + " " + answer2);
	}

}

```
