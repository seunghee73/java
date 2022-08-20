```java
package test;

public class EqualDemo {

    public static void main(String[] args) {
        System.out.println(1==2);
        System.out.println(1==1);
        System.out.println("one"=="one");
        System.out.println("one"=="two");
    }

}
```

```java
false
true
true
false
```

```java
package test;

public class EqualDemo {

    public static void main(String[] args) {
        System.out.println(1!=2);
        System.out.println(1!=1);
        System.out.println("one"!="one");
        System.out.println("one"!="two");
    }

}
```

```java
true
false
false
true
```

```java
package test;

public class EqualDemo {

    public static void main(String[] args) {
        System.out.println(1>2);
        System.out.println(1<2);
        System.out.println(1<1);
    }

}
```

```java
false
true
false
```

```java
package test;

public class EqualDemo {

    public static void main(String[] args) {
        String a = "칠삼";
        String b = new String("칠삼"); 
        // new를 통해 "칠삼" 데이터의 위치를 다른 곳에 저장
        System.out.println(a == b);
        System.out.println(a.equals(b));
    }

}
```

```java
false
true
```


