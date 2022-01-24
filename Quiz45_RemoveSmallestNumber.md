# 제일 작은 수 제거하기
## https://programmers.co.kr/learn/courses/30/lessons/12935
```
import java.util.ArrayList;
import java.util.List;

public class Quiz45_RemoveSmallestNumber {

	public static void main(String[] args) {
		Solution45 sol = new Solution45();
		sol.solution(new int[] {4,3,2,1});
	}

}
class Solution45 {
    public int[] solution(int[] arr) {
        
        List<Integer> list = new ArrayList<Integer>();
        
        // 만약 길이가 1이면 배열에 -1 넣고 리턴
        if(arr.length == 1) {
        	int[] answer2 = {-1};
        	return answer2;
        }
        
        // 배열을 리스트에 복사
        for(int a : arr) {
        	list.add(a);
        }
        
        // 배열에서 최소값 찾기
        int min = arr[0];
        for(int i=0; i<arr.length; i++) {
        	min = Math.min(min, arr[i]);
        }
        
        list.remove(list.indexOf(min));	//indexof 는 인덱스를 반환해준다
        int[] answer = new int[list.size()];
        for(int i=0; i<answer.length; i++) {
        	answer[i] = list.get(i);
        }
    
        return answer;
    }
}
```
