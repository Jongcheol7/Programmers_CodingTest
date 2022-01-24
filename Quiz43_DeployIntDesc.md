# 정수 내림차순으로 배치하기
## https://programmers.co.kr/learn/courses/30/lessons/12933
```
public class Quiz43_DeployIntDesc {

	public static void main(String[] args) {
		Solution43 sol = new Solution43();
		sol.solution(118372);
	}

}
class Solution43 {
    public long solution(long n) {      
        List<Long> list = new ArrayList<Long>(); // 컬렉션 사용
        int length = Long.toString(n).length(); // 숫자의 길이 알아내기
        for(int i=0; i<length; i++ ) {
        	list.add(n%10);    // 끝자리 하나씩 list에 
        	n = n/10;
        }
        
        Collections.sort(list);
        Collections.reverse(list);
        String num = ""	;
        for(Long a : list) {
        	num += a;
        }
          
        return Long.parseLong(num);
    }
}
```
