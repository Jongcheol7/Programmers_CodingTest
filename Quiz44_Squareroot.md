# 정수 제곱근 판별
## https://programmers.co.kr/learn/courses/30/lessons/12934
```
public class Quiz44_Squareroot {

	public static void main(String[] args) {
		Solution44 sol = new Solution44();
		sol.solution(121);
	}

}
class Solution44 {
    public long solution(long n) {
        long answer = (long) Math.sqrt(n);
        if(answer*answer == n) answer = (answer+1) * (answer+1);
        else answer = -1;
        return answer;
    }
}
```
