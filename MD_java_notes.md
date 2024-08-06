# [알고리즘 Java 정리 노트 / ps(problem solving) 필기]
**- PS process:&nbsp;&nbsp;프로그래머스 입문 100문제 -**
```

삼항연산자
int answer = (num1 == num2) ? 1 : -1;
        return answer;

형변환 
 double result = (double) num1 / (double) num2;        
        return (int)(result*1000);


짝수홀수 가릴때 많이 쓸듯
 answer[num_list[i] % 2]++;


배열 중간 인덱스
 int midIndex = array.length / 2;  
    
문자열 메소드

문자열 길이(length( ))
length( ) 메소드는 문자열의 길이(문자의 수)를 리턴합니다.
String subject = "자바 프로그래밍";
int length = subject.length();


contains()
-boolean contains(CharSequence s)
-contains()함수는 대상 문자열에 특정 문자열이 포함되어 있는지 확인하는 함수이다.
- 대/소문자를 구분한다.
str1.contains(str2) ? 1: 2);


replace()
Replace 함수는 자신이 바꾸고싶은 문자로 문자열을 치환시켜주는 기능을 합니다.
String a = "무궁화 삼천리 화려강산 대한사람 대한으로 길이 보전하세 ";	
//replaceAll([정규식],[바꿀문자])
a= a.replaceAll("대한", "민국");


Arrays.sort()
배열 오름차순 정렬
import java.util.*;
   public int solution(int[] numbers) {
        Arrays.sort(numbers);
        }
반환할때 void라
int[] tmp = Arrays.copyOf(array, array.length); // array 복사본 생성
Arrays.sort(tmp); // 복사본 정렬
이거 같이 써주면 좋음


Arrays.copyOf(배열,길이)
배열의 길이만큼 복사함
int[] tmp = Arrays.copyOf(array, array.length); 
Arrays.sort(tmp); 

        
length 와 length() 차이 
length는 배열의 크기
length()는 문자열의 크기


String.toCharArray()
문자열을 한 글자씩 쪼개서 char타입의 배열에 집어넣어주는 메소드이다.
  String s1 = "Hello World";
  char[] charArr = s1.toCharArray();
  
  
Character.getNumericValue() 
메소드는 Unicode의 값을 int value로 반환한다.  
        for(char ch : str.toCharArray()) {
            answer += Character.getNumericValue(ch);
        }
        

String substring(int index)
문자열을 자르는 함수
for (int i = code; i <= cipher.length(); i = i + code) {
        answer += cipher.substring(i - 1, i);
}
*빈 문자열에 그냥 더해서 넣어도 문자열 됨*


*char형의 변수에서 정수를 더하거나 빼면 결과는 int형으로 반환됩니다.* 
        
--------------------------------------------------------------------