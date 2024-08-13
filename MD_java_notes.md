# [알고리즘 Java 정리 노트 / ps(problem solving) 필기]
**- PS process:&nbsp;&nbsp;프로그래머스 입문 100문제 -**
```
**(별)이게 있다는 건 좀 중요하다는 뜻


삼항연산자
int answer = (num1 == num2) ? 1 : -1;
        return answer;

형변환 
 double result = (double) num1 / (double) num2;        
        return (int)(result*1000);


짝수홀수 가릴때 많이 쓸듯
 answer[num_list[i] % 2]++;

약수 개수 구하는 법
for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                answer++;
            }
        }


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

??.equals(문자열)
문자열 맞는지 틀린지 비교할때 위의 코드 잊지 말기
예)direction.equals("left")
st[i].equals("Z")
꼭 문자열에 문자열 비교할때 써야함

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
글고 반환할땐
        Arrays.sort(answer);
        return answer;
이런식으로 나눠서 코딩해야함 
        ***return Arrays.sort(answer);***
이렇게는 못함
Arrays.sort(arr, Collections.reverseOrder());
안에 인자를 이런식으로 넣으면 내림차순 정렬이라함

my_string.toLowerCase()
my_string.toUpperCase()
Lower은 대문자를 소문자로
Upper은 소문자를 대문자로
        String answer = "";
        answer = my_string.toLowerCase();



Arrays.copyOf(배열,길이)
배열의 길이만큼 복사함
int[] tmp = Arrays.copyOf(array, array.length); 
Arrays.sort(tmp); 


indexOf(int i)
indexOf(String s)
특정 문자나 문자열에서 해당하는  문자의 인덱스 값을 반환하고
찾지 못했을 경우 '-1' 을 반환하는 메소드
int index = numstr.indexOf(kstr);
        
        
split()
문자열을 자르는 메소드 split()
문자열 String 을 특정 문자로 자를때 사용할 수 있는 메소드
공백으로 문자열을 자를때, split(" ") 으로 자르면 되지만,
 문자열이 끝나고 마지막에 붙는 공백은 얻어지지 않는다.
String[] word = letter.split(" ");

"[0-9]"이거는 숫자로 쪼개라
"[^0-9]"이거는 숫자를 제외한 걸로 쪼개라
"[^0-9+]"는 하나 이상의 연속된 문자를 의미.
＊＊＊중요 포인트＊＊＊
aAb1B2cC34oOp 이런 문자열이 주어지고 자른다면
첫글자랑 마지막글자가 숫자가 아닌 문자이므로 처음 과 끝에 앞뒤로
０인덱스 마지막인덱스에 빈 문자열이 생김
그래서 예외처리 꼭 해줘야함
１ａｂｃｅ 이런식이면 ０인덱스에는 빈문자열 안생기고
마지막에 생김 



Integer.parseInt(s[i]);
이거는 기본적으로 문자열을 정수형으로 바꿔주는 코드
또 다른 코드로
Integer.parseInt()
10진수를 2진수로 바꿔주는 역할을 함
2자리에 8을 넣으면 8진수, 16을 넣으면 16진수로 바꿀 수 있음
String s = "110";
int n = Integer.parseInt(s, 2);
System.out.print(n);
// output: 6



***valueOf()***
valueOf 메소드는 괄호 안의 해당 객체를 String 객체로 변환시키는
 역활을 한다. String의 객체로 형변환이다.
int a = 5;
String b = String.valueOf(a);


!s[i].isEmpty())
 빈 문자열 체크인지 아닌지 확인할때 쓰는데
주로예외처리  때문에 많이 씀


charAt(i)
String 타입의 데이터(문자열)에서 특정 문자를 char 타입으로 
변환할 때 사용하는 함수이다.
String sample = "abc";
char target = sample.charAt(0);
i 자리에는 int 형 변수를 넣어서 원하는 위치의 문자를 가져올 수 있다.


length 와 length() 차이 
length는 배열의 크기
length()는 문자열의 크기


String.toCharArray()***
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
        
        
**StringBuilder**(유용하게 쓰일듯)
StringBuilder는 String과 다르게 값이 변할 수 있다.
StringBuilder는 문자열과 문자열을 더할 때 새로운 객체를 생성
하는 것이 아니라 기존의 데이터에 더하는 방식을 사용
문자열이 수정이 가능하다 정도로 이해
       StringBuilder sb = new StringBuilder();
        for(char c : my_string.toCharArray()){
            sb.append((c + "").repeat(n));
        }
        return sb.toString();
       
repeat()
String 문자열을 파라미터의 주어진 횟수만큼 반복

toString()
메서드는 객체가 가지고 있는 정보나 값들을 문자열로 
만들어 리턴하는 메소드 입니다.
StringBuilder쓸때 주의할점은 꼭 반환형으로 변환해야함
sb.toString();이런식으로

append()
문자열 뒤에 추가해주는 메소드이다
   sb.append((c + "").repeat(n));
 여기서 c + ""는 문자열로 반환해주고
 만약 ""가 없으면 char형이 반환됨 그래서 repeat도 이 코드에선 못씀


insert()
문자열을 인수에 전달한 후 문자열의 지정된 인덱스에 추가
 System.out.println(strr.insert(4, "Script"));
************************************
주의할점 만약 예를 들어 0 인덱스에 반복문을 통해 계속 추가하면 원래 있던 
값들은 오른쪽으로 즉 인덱스 값들이 증가하면서 옮겨짐
        while(age>0){
            sb.insert(0,(char)((age % 10)+(int)'a'));
            
        }
여기서 sb 빈 문자열에 0인덱스에 계속 넣으면 원래 있던 값들은 오른쪽으로
옮겨짐
***************************************


Integer.toBinaryString()
10진수를 2진수로 바꿔주는 역할
int n = 23
String s = Integer.toBinaryString(n);
System.out.print(s);
// output: 10111



--------------------------------------------------------------------
신박한 풀이
    public long solution(int balls, int share) {
       long answer = 0;

        int d = (balls - share) > share ? share : balls - share;
        if (d == 0) return 1;

        return solution(balls - 1, d - 1) * balls / d;
    }
서로 다른 n개 중 m개를 뽑는 경우의 수 공식