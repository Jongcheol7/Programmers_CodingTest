# 로또의 최고순위와 최저순위
## https://programmers.co.kr/learn/courses/30/lessons/77484

<pre>
<code>
public class Quiz1_Lotto {
	
	public static void main(String[] args) {
		
		Solution sol = new Solution();
		int[] lottos = {45,4,35,20,3,9};
		int[] win_nums = {20,9,3,45,4,35};
		int[] result = sol.solution(lottos, win_nums);
		System.out.println(Arrays.toString(result));
	}
	
}

class Solution {
    public int[] solution(int[] lottos, int[] win_nums) {
    	int sameNumber = 0; // 내 번호와 담첨 번호와 몇개가 같은지
    	int count_0 = 0;    // 내 번호에서 0이 몇개가 있는지
    	int max_num = 0;    // 내 번호 0이 전부 당첨번호일 경우 총 맞은 갯수 
    	int min_num = 0;    // 내 번호 0이 전부 당첨번호와 다를 경우 총 맞은 갯수
    	int best;			// 최고 예상 등수
    	int worst;			// 최저 예상 등수
    	
    	// 내가 로또 번호에서 0이 몇개가 있는지 확인하는 메서드
    	for(int i=0; i<6; i++) {
    		if(lottos[i] == 0) {
    			count_0++;
    		}
    	}

    	// 0의 갯수에 따따 당첨번호와 몇개가 맞는지 최대 최소값 예측
    	switch(count_0) {
    		case 0:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber;
    			min_num = sameNumber;
    			break;
    		case 1:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber + 1;
    			min_num = sameNumber + 0;
    			break;
    		case 2:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber + 2;
    			min_num = sameNumber + 0;
    			break;
    		case 3:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber + 3;
    			min_num = sameNumber + 0;
    			break;
    		case 4:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber + 4;
    			min_num = sameNumber + 0;
    			break;
    		case 5:
    			sameNumber = compare(lottos, win_nums);
    			max_num = sameNumber + 5;
    			min_num = sameNumber + 0;
    			break;
    		case 6:
    			max_num = 6;
    			min_num = 0;
    			break;
    		default:
    			break;
    	}
    	    
    	// 등수는 7에서 몇개가 같은지 뺴면 나온다. 예를들어 6개가 전부 맞아버리면 7-6으로 1등이 된다.
    	best = 7 - max_num;
    	worst = 7 - min_num;
    	if(max_num == 0){
            best = 6;
        }
        if(min_num == 0){
            worst = 6;
        }
            	    	
    	
        int[] answer = {best, worst};
        return answer;
    }
    
    // 내 번호에 0이 있는지 상관없이 당첨번호와 몇개가 맞는지 확인하는 메서드
    public int compare(int[] lottos, int[] win_nums) {
    	int count = 0;
		for(int i=0; i<6; i++) {
    		for(int j=0; j<6; j++) {
    			if(lottos[i] == win_nums[j]) {
    				count++;
    			}
    		}
    	}
		return count;
	}
}
</code>
</pre>
