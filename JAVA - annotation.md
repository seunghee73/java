- @Override
  
  - 선언한 메소드가 오버라이드 되었다는 것을 의미
  - 만약 상위 클래스에서 해당 메소드를 찾을 수 없으면 컴파일 에러

- @Deprecated
  
  - 해당 메소드가 더이상 사용되지 않음을 의미
  - 사용하는 경우 컴파일 경고 메시지

- @SuppressWarnings
  
  - 선언한 곳의 컴파일 경고 무시

- @SafeVarargs
  
  - 가변인자의 매개변수를 사용할 때의 경고 무시

- @Functionallnterface
  
  - 함수형 인터페이스를 지정
  - 만약 메소드가 존재하지 않거나, 1개 이상의 메소드가 존재하는 경우 컴파일 오류

- 부모 클래스의 메소드 또는 변수를 그대로 사용할 수 있는지, 혹은 무조건 재정의를 해야하는지에 따라서 상속의 형태가 다르다.

- **extends** : 부모 클래스에서 선언과 정의를 하면, 자식 클래스는 오버라이딩 할 필요 없이 이를 상속받아 사용할 수 있다.

```java
class Vehicle {
    protected int speed = 3;

    public int getSpeed() {
        return speed;
    }
    public void setSpeed(int speed) {
        this.speed = speed;
    }
}

class Car extends Vehicle {
    public void printspd() {
        System.out.println(speed);
    }
}

public class ExtendsDemo {
    public static main (String[] args) {
        Car A = new Car();
        System.out.println(A.getSpeed());
        A.printspd();
    }
}
```

- **implements(interface)** : 부모 클래스는 선언만 하고 자식 클래스가 반드시 오버라이딩(재정의) 해서 사용한다.
  
  ```java
  interface TestInterface {
    public static int num = 0;
    public void func1();
    public void func2();
  }
  
  class InterfaceExam implements TestInterface {
    @Override
    public void func1() {
  
        System.out.println(num);
  
    }
  
    @Override
    public void func2() {
  
        System.out.println(num + 1);
  
    }
  }
  
  public class ImplementsDemo {
    public static void main(String[] args) {
  
        InterfaceExam exam = new InterfaceExam();
        exam.func1();
        exam.func2();
  
    }
  }
  ```
