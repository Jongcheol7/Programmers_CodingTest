# 자연수 뒤집어 배열로 만들기
## https://programmers.co.kr/learn/courses/30/lessons/12932
```
public class Quiz42_IntToStringReverse {

	public static void main(String[] args) {
		Solution42 sol = new Solution42();
		sol.solution(12345);
	}

}
class Solution42 {
    public int[] solution(long n) {
        
    	int[] answer = new int[Long.toString(n).length()];
    	for(int i=0; i<answer.length; i++) {
    		answer[i] = (int) (n % 10);
    		n = n / 10;
    	}
        return answer;
    }
}
```
