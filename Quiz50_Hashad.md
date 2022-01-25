# 하샤드 수
## https://programmers.co.kr/learn/courses/30/lessons/12947
```
public class Quiz50_Hashad {

	public static void main(String[] args) {
		Solution50 sol = new Solution50();
		sol.solution(11);
	}

}
class Solution50 {
    public boolean solution(int x) {          
        int sum = 0;
        int num = x;
        int length = Integer.toString(x).length();
        for(int i=0; i<length; i++) {
        	sum += num % 10;
        	num = num / 10;
        	if(num == 0 ) break;
        }     
        return (x % sum == 0) ? true : false;
    }
}
