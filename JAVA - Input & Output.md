- Scanner

```java
package test;

import java.util.Scanner;

public class ScannerDemo {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int i = sc.nextInt(); // int가 아닌 값이 들어오면 에러 발생
        System.out.println(i / 73);
        System.out.println(i % 73);
        sc.close();

    }

}
```

```java
> 12341234
169058
0
```

```java
package test;

import java.util.Scanner;

public class ScannerDemo {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        while(sc.hasNextInt()){

            int i = sc.nextInt();
            System.out.println("입력받은 값:" + i);
            System.out.println("몫: " + i/73);
            System.out.println("나머지: " + i%73);
            System.out.println("----------");

        }

        sc.close();

    }

}
```

```java
> 12341234
입력받은 값:12341234
몫: 169058
나머지: 0
----------
> 55555555
입력받은 값:55555555
몫: 761035
나머지: 0
----------
> 73737373
입력받은 값:73737373
몫: 1010101
나머지: 0
----------
```

- BufferedReader

```java
package test;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class BufferDemo {

    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        String str;
        while ((str = reader.readLine()) != null){
            int i = Integer.parseInt(str);
            System.out.println("입력받은 값:" + i);
            System.out.println("몫: " + i/73);
            System.out.println("나머지: " + i%73);
            System.out.println("----------");

        }

    }

}
```

```java
> 12341234
입력받은 값:12341234
몫: 169058
나머지: 0
----------
> 55555555
입력받은 값:55555555
몫: 761035
나머지: 0
----------
> 73737373
입력받은 값:73737373
몫: 1010101
나머지: 0
----------
```
