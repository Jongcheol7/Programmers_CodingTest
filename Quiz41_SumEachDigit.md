# 자릿수 더하기
## https://programmers.co.kr/learn/courses/30/lessons/12931
```
public class Quiz41_SumEachDigit {

	public static void main(String[] args) {
		Solution41 sol = new Solution41();
		sol.solution(123);
	}

}
class Solution41 {
    public int solution(int n) {
        int sum = 0;
        String num = Integer.toString(n);
        for(int i=1; i<=num.length(); i++) {
        	sum += Integer.parseInt(num.substring(i-1, i));
        }
        System.out.println(sum);

        return sum;
    }
}
```
