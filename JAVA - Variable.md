- 변수의 선언과 할당
  
  - 숫자
  
  ```java
  `package test;
  
  public class Integer {
  
      public static void main(String[] args) {
          int a;
          a = 7;
          System.out.println(a);
  
          a = 3;
          System.out.println(a);
  
          int b = 7;
  
          System.out.println(a+7);
          System.out.println(a+b);
  
      }
  
  }
  ```
  
  ```java
  7
  3
  10
  10
  ```
  
  - 문자
  
  ```java
  package test;
  
  public class StringDemo {
  
      public static void main(String[] args) {
          String a = "칠삼";
          System.out.println(a);
  
          String b, c;
          b = "칠"; c = "삼";
          System.out.println(b+c);
      }
  
  }
  ```
  
  ```java
  칠삼
  칠삼
  ```

- 데이터타입
  
  - 자료형을 잘못 선언하게 되면 아예 컴파일이 불가능
    
    | 정수  | byte    |
    | --- | ------- |
    | 정수  | short   |
    | 정수  | int     |
    | 정수  | long    |
    | 실수  | float   |
    | 실수  | double  |
    | 문자  | char    |
    | 문자열 | String  |
    | 논리  | boolean |

- 데이터타입

```java
package test;

public class ConstantDemo {

    public static void main(String[] args){
        double a = 7.3;
        System.out.println(a);
        // float b = 2.2;
        // 2.2는 double 타입이기 때문에 위와 같은 코드는 에러가 발생한다.
        float b = 7.3F;
        System.out.println(b);
    }

}
```

```java
7.3
7.3
```
