# x만큼 간격이 있는 n개의 숫자
## https://programmers.co.kr/learn/courses/30/lessons/12954
```
public class Quiz53_PlusXHowManyN {

	public static void main(String[] args) {
		Solution53 sol = new Solution53();
		sol.solution(-4, 2);
	}

}
class Solution53 {
    public long[] solution(int x, int n) {
        long[] answer = new long[n];
        long num = x;
        for(int i=0; i<n; i++) {
        	answer[i] = num;
        	num = num + x;
        }        
        return answer;
    }
}
```
