# 수박수박수박수?
## https://programmers.co.kr/learn/courses/30/lessons/12922
```
public class Quiz36_WaterMelon {

	public static void main(String[] args) {
		Solution36 sol = new Solution36();
		sol.solution(5);
	}

}
class Solution36 {
    public String solution(int n) {
        String answer = "";
        
        for(int i=1; i<=n/2; i++) {
        	answer = answer + "수박";
        }
        if(n%2 != 0) answer = answer + "수";
        
        System.out.println(answer);
        
        return answer;
    }
}
```
