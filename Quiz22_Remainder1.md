# 나머지가 1이 되는 수 찾기
## https://programmers.co.kr/learn/courses/30/lessons/87389
```
public class Quiz22_Remainder1 {

	public static void main(String[] args) {
		Solution22 sol = new Solution22();
		sol.solution(10);
	}

}
class Solution22 {
    public int solution(int n) {
        int answer = 0;
        
        for(int i=2; i<n; i++) {
        	if(n%i == 1) {
        		answer = i;
        		break;
           	}
        }
        
        System.out.println(answer);
        
        return answer;
    }
}
```
