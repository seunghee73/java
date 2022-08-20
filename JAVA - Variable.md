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

- 형 변환 (type conversion)
  
  - 자동 형 변환
    
    - byte > short / char > int > long > float > double
    - float에서 double로는 형 변환이 가능하지만 역은 불가능하다.
    - 즉, `double a = 7.3F`는 가능한 표현이지만 `float a = 7.3`은 불가능하다.
    
    ```java
    int a = 7; // int 타입
    float b = 3.0F; // float 타입
    double c = a + b; // double 타입
    
    // 두 번의 형 변환이 일어난다.
    // a + b의 과정에서 a 가 float로 형 변환이 일어나고 c 타입이 double이기 때문에 최종적으로 double로 형 변환이 일어난다.
    ```
  
  - 명시적 형 변환
    
    - 자동 형 변환이 적용되지 않는 경우에는 수동으로 형 변환
    - 괄호 안에 데이터 타입을 지정해서 값 앞에 위치
    
    ```java
    float a = (float) 73.0;
    int b = (int) 73.1F; // 73
    ```


