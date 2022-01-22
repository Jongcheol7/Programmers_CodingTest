# 문자열 내림차순으로 배치하기
## https://programmers.co.kr/learn/courses/30/lessons/12917
```
import java.util.Arrays;
import java.util.Collections;

public class Quiz32_StringDesc {

	public static void main(String[] args) {
		Solution32 sol = new Solution32();
		sol.solution("Zbcdefg");
	}

}
class Solution32 {
    public String solution(String s) {
        String answer = "";
        // 문자열을 각각의 문자로 배열에 저장
    	String[] StringToArray = s.split("");    	
    	Arrays.sort(StringToArray, Collections.reverseOrder());
    	for(String a : StringToArray) {
    		answer = answer + a;
    	}
    	System.out.println(answer);
    	
        return answer;
    }
}
```
