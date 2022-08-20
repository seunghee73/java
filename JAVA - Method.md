- 메소드

```java
package test;

public class MethodDemo {
    public static void PrintText(){
        String[] Names = {"마이클", "안소니", "그린버그", "피터슨"};
        for (String i : Names){

            System.out.println(i + " 안녕~");

        }
    }
    public static void main(String[] args) {

        PrintText();

    }

}
```

```java
마이클 안녕~
안소니 안녕~
그린버그 안녕~
피터슨 안녕~
```

- 메소드 입력값

```java
package test;

public class MethodDemo {
    public static void PrintNumber(int StartVal, int EndVal){

        for (int i = StartVal; i < EndVal+1; i++){

            System.out.println(i + "를 출력했습니다.");

        }
    }
    public static void main(String[] args) {

        PrintNumber(3, 7);

    }

}
```

```java
3를 출력했습니다.
4를 출력했습니다.
5를 출력했습니다.
6를 출력했습니다.
7를 출력했습니다.
```

- 메소드 출력값

```java
package test;

public class MethodDemo {
    public static int SumNumber(int StartVal, int EndVal){

        int output = 0;

        for (int i = StartVal; i < EndVal+1; i++){

            output += i;

        }

        return output;
    }

    public static void main(String[] args) {

        int result = SumNumber(3, 7); // 3 + 5 + 6 + 7 = 25
        System.out.println(result);

    }

}
```

```java
25
```

```sql

```


