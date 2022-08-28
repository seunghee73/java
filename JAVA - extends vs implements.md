- 상속
  
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

- **abstract** : extends + interface, extends를 하되 몇 개는 추상 메소드로 구현되어 있다.
