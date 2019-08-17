# 문제설명
#### 두개의 정수 n과 m이 주어진다.  
#### 별(*) 문자를 이용해 가로:n, 세로:m인 직사각형 출력  
<br>  

# 제한조건
####
 - n, m은 1000이하인 자연수
 
# 예시
## 입력 : 5 3  
## 출력 

`*****`  
`*****`  
`*****`   
<br>


```java
import java.util.Scanner;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        for(int i=0; i<b; i++)
        {
        	for(int j=0; j<a; j++)
        	{
        		System.out.print("*");
        	}
        	System.out.println();
        }
    }
}
```
