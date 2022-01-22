# 문자열을 정수로 바꾸기
## https://programmers.co.kr/learn/courses/30/lessons/12925
```
public class Quiz37_StringToInt {

	public static void main(String[] args) {
		Solution37 sol = new Solution37();
		sol.solution("-1234");
	}
}
class Solution37 {
    public int solution(String s) {
        return Integer.parseInt(s);
    }
}
```
