# 최대공약수와 최소공배수
## https://programmers.co.kr/learn/courses/30/lessons/12940
```
import java.util.Arrays;

public class Quiz47_YacksuAndGongbeasu {

	public static void main(String[] args) {
		Solution47 sol = new Solution47();
		sol.solution(13, 14);
	}

}
class Solution47 {
    public int[] solution(int n, int m) {
        int[] answer = new int[2];
        // 최대공약수
        for(int i=1; i<=n; i++) {
        	if(n%i==0 && m%i==0) answer[0] = i;
        }
        // 최소공배수
        if(m%n == 0) answer[1] = m;
        else{
        	int a = 2;
        	while(true) {
        		if((m*a++)%n == 0) {
        			answer[1] = m*--a;
        			break;
        		}
        		
        	}
        } 
        System.out.println(Arrays.toString(answer));
 
        return answer;
    }
}
```
