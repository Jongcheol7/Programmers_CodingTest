# 완주하지 못한 선수
## https://programmers.co.kr/learn/courses/30/lessons/42576?language=java

```
import java.util.HashMap;

public class Quiz10_Marathon {
	public static void main(String[] args) {
		String[] paricipant = {"marina", "josipa", "nikola", "vinko", "filipa"};
		String[] completion = {"josipa", "filipa", "marina", "nikola"};
		Solution10 sol = new Solution10();
		sol.solution(paricipant, completion);
	}
}
class Solution10 {
    public String solution(String[] participant, String[] completion) {
    	String answer = "";
    	HashMap<String, Integer> map = new HashMap<>();
    	for(int i=0; i<participant.length; i++) {
    		map.put(participant[i], map.getOrDefault(participant[i], 0)+1);
    	}
    	for(int j=0; j<completion.length; j++) {
    		map.put(completion[j], map.get(completion[j])-1);
    	}
    	for(String key : map.keySet()) {
    		if(map.get(key) != 0) {
    			answer = key;
    		}
    	}
    	    	
    	System.out.println(answer);
    	return answer;
    }
}
```
