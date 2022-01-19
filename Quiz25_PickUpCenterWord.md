# 가운데 글자 가져오기
## https://programmers.co.kr/learn/courses/30/lessons/12903
```
public class Quiz25_PickUpCenterWord {

	public static void main(String[] args) {
		Solution25 sol = new Solution25();
		sol.solution("qwer");
	}

}
class Solution25 {
    public String solution(String s) {
        String answer = "";
        if(s.length()%2 == 0) {
        	answer = s.substring(s.length()/2-1,s.length()/2+1);
        }else {
        	answer = s.substring(s.length()/2, s.length()/2+1);
        }
        System.out.println(answer);
        return answer;
    }
}
```
