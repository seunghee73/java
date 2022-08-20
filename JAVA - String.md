- 문자와 문자열
  - 자바는 문자(Character)와 문자열(String)을 구분한다.
  - 자바에서 문자는 작은 따옴표로 감싸야 한다.
  - 문자열은 큰 따옴표로 감싸야 한다. 하지만 하나의 문자도 문자열이 될 수 있기 때문에 이를 큰 따옴표로 감쌌을 때 에러가 발생하지는 않는다.

```java
package test;

public class String {

    public static void main(java.lang.String[] args) {
        System.out.println('칠');
        //System.out.println('칠삼');
        // 문자열 길이가 2 이상인 경우 작은 따옴표를 사용하면 에러가 발생한다.
        System.out.println("칠");
        System.out.println("칠삼");
    }

}
```

```java
칠
칠
칠삼
```

- 이스케이프(escape)
  - \를 앞에 위치시키면 단순히 문자로 해석하도록 강제할 수 있다.
  - \n 을 사용하면 문장을 바꿀 수 있다.

```java
package test;

public class String {

    public static void main(java.lang.String[] args) {
        System.out.println("\\"칠삼\\"");

        System.out.println("안녕,\\n나는 칠삼이야!");
    }

}
```

```java
"칠삼"
안녕,
나는 칠삼이야!
```

- 문자의 연산
  - 문자와 문자를 연결할 때에는 큰 따옴표에 덧셈 연산을 사용한다.
  - 작은 따옴표를 사용하는 경우에는 문자를 아스키코드값으로 변환하고 그 값을 더한다.
