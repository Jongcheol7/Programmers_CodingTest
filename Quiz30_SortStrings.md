# 문자열 내 마음대로 정렬하기
## https://programmers.co.kr/learn/courses/30/lessons/12915
```
import java.util.Arrays;

public class Quiz30_SortStrings {

	public static void main(String[] args) {
		Solution30 sol = new Solution30();
		sol.solution(new String[]{"sun", "bed", "car"}, 1);
	}

}
class Solution30 {
	public String[] solution(String[] strings, int n) {
        String[] answer = new String[strings.length];
        
        // 각 문자열에서 1번째 인덱스를 맨 앞으로 뺀다.
        for(int i=0; i<strings.length; i++) {
        	answer[i] = strings[i].charAt(n)+ strings[i];
        }
        // 배열 정렬
        Arrays.sort(answer);
        // 맨앞으로 뺀 문자 제거
        for(int i=0; i<answer.length; i++) {
        	answer[i] = answer[i].substring(1, answer[i].length());
        }
        System.out.println(Arrays.toString(answer));
        
        return answer;
    }
}
```
