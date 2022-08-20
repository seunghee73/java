# JAVA - 형변환

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
    
    ```java
    package test;
    
    public class DivisionDemo {
    
        public static void main(String[] args) {
            int a = 7;
            int b = 3;
    
            float c = 7.0F;
            float d = 3.0F;
    
            System.out.println(a/b); // int
            System.out.println(c/d); // float
            System.out.println(a/d); // float
    
        }
    
    }
    ```
    
    ```java
    2
    2.3333333
    2.3333333
    ```
  
  - 명시적 형 변환
    
    - 자동 형 변환이 적용되지 않는 경우에는 수동으로 형 변환
    - 괄호 안에 데이터 타입을 지정해서 값 앞에 위치
