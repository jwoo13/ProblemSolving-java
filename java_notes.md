# Java 정리

<details open>
  <summary><strong>&nbsp;📖&nbsp;&nbsp;목차</strong></summary>

  &nbsp;&nbsp;[기본](#기본)
  <br>
   &nbsp;&nbsp;[StringBuilder](#stringbuilder)
</details>

<br>


## 기본

### import

```java
import java.util.*;  // Scanner, ArrayList, StringTokenizer
import java.io.*;  // BufferedReader
import java.util.stream.*;  // Collectors
import java.awt.*;  // Point
```

## Stringbuilder

### 특징

String과 StringBuilder는 Java에서 문자열을 다루기 위해 사용되는 클래스들이지만, **주요 차이점은 "불변성(immutability)"과 "성능"**이다
<br>
<br>
String
불변 객체:String 객체는 한 번 생성되면 값을 변경할 수 없습니다.
문자열을 변경하는 모든 작업은 새로운 String 객체를 생성합니다.
<br>
예:
```java
String str = "Hello";
str = str + " World"; // 새로운 객체가 생성됨
```
성능:문자열 변경이 빈번하게 발생할 경우, 새로운 객체를 계속 생성하므로 메모리와 성능에 영향을 줄 수 있습니다.
<br>
사용 사례:문자열 변경이 거의 없는 경우.짧은 문자열을 다룰 때.

<br>
<br>
StringBuilder
가변 객체:StringBuilder는 기존 객체를 수정하며, 새로운 객체를 생성하지 않습니다.

예:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.append(" World"); // 기존 객체가 수정됨
```

성능:문자열 변경이 빈번한 경우, StringBuilder는 메모리를 효율적으로 사용하며 성능이 좋습니다.
<br>
사용 사례:문자열 조작이 빈번히 발생할 때.긴 문자열을 다룰 때.

### 메소드

```java
public String solution(String my_string) {
        StringBuilder sb = new StringBuilder(my_string);
        sb.reverse(); 
        return sb.toString();
    } // 문자열 뒤집기

```

<br>
