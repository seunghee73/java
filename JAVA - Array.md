- 배열

```sql
package test;

public class DefineDemo {

    public static void main(String[] args) {
        String[] Names = {"마이클", "안소니", "그린버그", "피터슨"};
        System.out.println(Names.length);
        System.out.println(Names[0]);
        System.out.println(Names[1]);
    }

}
```

```sql
4
마이클
안소니
```

```sql
package test;

public class DefineDemo {

    public static void main(String[] args) {

        String[] Plays = new String[3];
        System.out.println(Plays.length);

        Plays[0] = "엘리펀트송";
        Plays[1] = "알앤제이";
        Plays[2] = "오펀스";
        // Plays[3] = "킬미나우";
        // 배열의 크기를 벗어나기 때문에 에러가 발생

        System.out.println(Plays.length);

    }

}
```

```sql
3
3
```

- 배열과 반복문

```sql
package test;

public class ArrayLoopDemo {

    public static void main(String[] args) {
        String[] Names = {"마이클", "안소니", "그린버그", "피터슨"};

        for (int i = 0; i < Names.length; i++) {

            System.out.println("여기에 " + Names[i] + "이 있어요");

        }

    }

}
```

```sql
여기에 마이클이 있어요
여기에 안소니이 있어요
여기에 그린버그이 있어요
여기에 피터슨이 있어요
```

- for - each

```sql
package test;

public class ForeEachDemo {

    public static void main(String[] args) {

        String[] Names = {"마이클", "안소니", "그린버그", "피터슨"};
        for (String i : Names){
            System.out.println("여기에 "+ i + "이 있어요");
        }
    }

}
```

```sql
여기에 마이클이 있어요
여기에 안소니이 있어요
여기에 그린버그이 있어요
여기에 피터슨이 있어요
```


