- final
  - 자료형에 값을 한 번만 설정할 수 있게 강제하는 키워드
  - 값을 한 번 설정하면 그 값을 다시 수정할 수 없음
  - 프로그램 수행 도중 그 값이 변경되면 안 되는 상황에 사용

```java
package practice;

public class FinalDemo {

    public static void main(String[] args) {
        final int n = 123;
        n = 456;
    }

}
```

```java
> 컴파일 에러 발생
```
