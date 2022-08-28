- try - catch
  - try 부분의 내용을 실행하고 에러가 발생하면 catch로 넘어간다.

```java
package practice;

class Calculator{
    int left, right;

    public void setOprands(int left, int right){
        this.left = left;
        this.right = right;
    }

    public void sum(){
        System.out.println(this.left + this.right);
    }

    public void avg(){
        System.out.println((this.left + this.right) / 2);
    }

    public void divide(){
        try{
        System.out.println(this.left / this.right);
        } catch(Exception e){
            System.out.println("계산 결과 오류가 발생했습니다:" + e.getMessage());
        }
    }

}

public class CalculDemo {


    public static void main(String[] args) {
        // TODO Auto-generated method stub

        Calculator c1 = new Calculator();
        c1.setOprands(10, 0);
        c1.sum();
        c1.avg();
        c1.divide();
    }
}
```

```java
10
5
계산 결과 오류가 발생했습니다:/ by zero
```

- try - catch - finally
  - finally : 예외처리와 관계 없이 항상 실행

```java
package practice;

class Calculator{
    int left, right;

    public void setOprands(int left, int right){
        this.left = left;
        this.right = right;
    }

    public void sum(){
        System.out.println(this.left + this.right);
    }

    public void avg(){
        System.out.println((this.left + this.right) / 2);
    }

    public void divide(){
        try {
        System.out.println(this.left / this.right);
        } catch(Exception e){
            System.out.println("계산 결과 오류가 발생했습니다:" + e.getMessage());
        } finally {
            System.out.println("Always");
        }
        System.out.println("Here");
    }

}

public class CalculDemo {


    public static void main(String[] args) {
        // TODO Auto-generated method stub

        Calculator c1 = new Calculator();
        c1.setOprands(10, 0);
        c1.sum();
        c1.avg();
        c1.divide();
    }
}
```

```java
10
5
계산 결과 오류가 발생했습니다:/ by zero
Always
Here
```

- throw

```java
package practice;

class FoolException extends Exception{

}

public class ExceptDemo {

    public void CodeName(String nick){
        try{
            if ("바보".equals(nick)){
                throw new FoolException();
            }

            System.out.println("나는 하얀 코끼리");
            System.out.println("당신은 " + nick);

        } catch(FoolException e){
            System.err.println("FoolException이 발생했습니다.");
        }

    }

    public static void main(String[] args) {

        ExceptDemo n = new ExceptDemo();
        n.CodeName("바보");
        System.out.println("-------");
        n.CodeName("존재의 위기");

    }

}
```

```java
FoolException이 발생했습니다.
-------
나는 하얀 코끼리
당신은 존재의 위기
```

- throws

```java
package practice;

class FoolException extends Exception{

}

public class ExceptDemo {

    public void CodeName(String nick) throws FoolException{
        if ("바보".equals(nick)){
            throw new FoolException();
        }
        System.out.println("나는 하얀 코끼리");
        System.out.println("당신은 " + nick);

    }

    public static void main(String[] args) {

        ExceptDemo n = new ExceptDemo();
        try{
            n.CodeName("바보");
            System.out.println("-------");
            n.CodeName("존재의 위기"); // 수행되지 않음
        } catch (FoolException e) {
            System.err.println("FoolException이 발생했습니다.");
        }

    }

}
```

```java
FoolException이 발생했습니다.
```



- 트랜잭션
  - 포장, 영수증발행, 발송에서는 예외를 throw하고 상품발송에서 throw된 예외를 처리해서 모두 취소하는 것이 완벽한 트랜잭션 처리 방법이다.
  
  ```java
  상품발송() {
      try {
          포장();
          영수증발행();
          발송();
      }catch(예외) {
          모두취소();  // 하나라도 실패하면 모두 취소한다.
      }
  }
  
  포장() throws 예외 {
     ...
  }
  
  영수증발행() throws 예외 {
     ...
  }
  
  발송() throws 예외 {
     ...
  }
  ```
  
  
