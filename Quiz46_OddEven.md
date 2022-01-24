# 짝수와 홀수
## https://programmers.co.kr/learn/courses/30/lessons/12937
```
public class Quiz46_OddEven {

	public static void main(String[] args) {
		Solution46 sol = new Solution46();
		sol.solution(3);
	}

}
class Solution46 {
    public String solution(int num) {
        return (num%2==0) ? "Even" : "Odd";
    }
}
```
