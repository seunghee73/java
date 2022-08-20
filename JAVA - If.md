- if문

```java
package test;

public class ConditionDemo {

    public static void main(String[] args) {

        int a = 1;

        if (a < 1) {
            System.out.println("Hello,");
        } else if (a == 1) {
            System.out.println("Hi,");
        } else {
            System.out.println("Oh,");
        }
        System.out.println("There");
    }

}
```

```java
Hi,
There
```

- switch문
  - 일치하는 case 이하는 모두 실행이 된다. 이를 방지하기 위해서는 break;를 사용한다.

```java
package test;

public class SwitchDemo {

    public static void main(String[] args) {

        switch(2){
        case 1:
            System.out.println("one");
        case 2:
            System.out.println("two");
        case 3:
            System.out.println("three");
        default:
            System.out.println("here");
        }

    }

}
```

```java
two
three
here
```

```java
package test;

public class SwitchDemo {

    public static void main(String[] args) {

        switch(2){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        default:
            System.out.println("here");
        }

    }

}
```

```java
two
```
