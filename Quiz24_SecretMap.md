# 비밀지도
## https://programmers.co.kr/learn/courses/30/lessons/17681
```
public class Quiz24_SecretMap {

	public static void main(String[] args) {
		Solution24 sol = new Solution24();
		int[] arr1 = {9,20,28,18,11};
		int[] arr2 = {30,1,21,17,28};
		sol.solution(5, arr1, arr2);
	}

}
class Solution24 {
    public String[] solution(int n, int[] arr1, int[] arr2) {
        String[] answer = new String[n];
        int arr11[][] = new int[n][n];
        int arr22[][] = new int[n][n];
        
        // 첫번째 배열 2차함수로 지도찍기
        for(int i=0; i<n; i++) {
        	int x = arr1[i];       	
        	for(int k=n-1; k>=0; k--) {        		
        		arr11[i][k] = x % 2;
        		x = x / 2;        		
        	}
        }
        
        // 두번째 배열 2차함수로 지도찍기
        for(int i=0; i<n; i++) {
        	int x = arr2[i];       	
        	for(int k=n-1; k>=0; k--) {        		
        		arr22[i][k] = x % 2;
        		x = x / 2;        		
        	}
        }
        
        // 두개의 2차배열을 각각 비교하여 한개라도 값이 1일시 #으로 치환       
        for(int c=0; c<n; c++) {
        	answer[c] = "";
        	for(int d=0; d<n; d++) {
        		if(arr11[c][d] == 1 || arr22[c][d] == 1) {
        			answer[c] = answer[c] + "#";
        		}else {
        			answer[c] = answer[c] + " ";
        		}
        	}
        }    
        
        return answer;
    }
}
```
