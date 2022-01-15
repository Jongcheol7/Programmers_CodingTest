# 신규 아이디 추천
## https://programmers.co.kr/learn/courses/30/lessons/72410

```
public class Quiz02_RecomendationNewID {

	public static void main(String[] args) {
		Solution2 sol = new Solution2();
		String newId = sol.solution("...!@BaT#*..y.abcdefghijklm");
		System.out.println(newId);
	}

}

class Solution2 {
	public String solution(String new_id) {

		new_id = new_id.toLowerCase(); //1단계 - 모든 대문자는 소문자로
		new_id = new_id.replaceAll("([^-_.0-9a-z])", ""); //2단계 - -._나 숫자, 소문자를 제외하고 모두 제거
		new_id = new_id.replaceAll("[.]{2,}", "."); //3단계 - .이 두개 연속이면 하나로 바꾸기
		new_id = new_id.replaceAll("^[.]", ""); //4단계 - .으로 시작하거나 끝나면 지우기
		new_id = new_id.replaceAll("[.]$", "");

		//5단계 - 값이 없으면 a로 채우기
		if(new_id.equals("")) {
			new_id = "a"; 
		}

		//6단계 - 16자 이상이면 15자까지 만들고, 끝 자리가 .이면 제거
		if(new_id.length() >= 16) {     
			new_id = new_id.substring(0, 15);
			for(int i=0; i<new_id.length(); i++) {
				if(new_id.substring(new_id.length()-1).equals(".")) {
					new_id = new_id.substring(0, new_id.length()-1);
				}
			}
		}

		//7단계 - 글자가 2자 이하면 마지막 글자를 계속 넣기
		while(true){
			if(new_id.length()<=2) {
				new_id = new_id.concat(new_id.substring(new_id.length()-1));
				continue;
			}
			break;
		}


		String answer = new_id;
		return answer;
	}
}
```
