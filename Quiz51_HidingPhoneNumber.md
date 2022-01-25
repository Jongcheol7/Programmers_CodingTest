# 핸드폰 번호 가리기
## https://programmers.co.kr/learn/courses/30/lessons/12948
```
public class Quiz51_HidingPhoneNumber {

	public static void main(String[] args) {
		Solution51 sol = new Solution51();
		sol.solution("01033334444");
	}

}
class Solution51 {
    public String solution(String phone_number) {
        String[] arr = phone_number.split("");
        for(int i=0; i<arr.length-4; i++) {
        	arr[i] = "*";
        }
        String answer = "";
        for(String s : arr) {
        	answer += s;
        }
        return answer;
    }
}
```
