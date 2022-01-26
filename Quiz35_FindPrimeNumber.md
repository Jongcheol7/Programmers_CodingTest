# 소수 찾기
## https://programmers.co.kr/learn/courses/30/lessons/12921
```
public class Quiz35_FindPrimeNumber {
	public static void main(String[] args) {
		Solution35 sol = new Solution35();
		sol.solution(5);
	}

}
class Solution35 {
	public int solution(int n) {        
        int cnt = 0;     
        for(int i=2; i<=n; i++) {
        	int cnt2 = 0;
        	for(int k=1; k<=(int)Math.sqrt(i); k++) {
        		if(i%k == 0) cnt2++;
                if(cnt2 == 2) break;
        	}
        	if(cnt2 == 1) cnt++;       	
        }
        return cnt;
    }
}
```
