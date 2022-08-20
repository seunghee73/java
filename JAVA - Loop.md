- while

```sql
package test;

public class WhileDemo {

    public static void main(String[] args) {

        int i = 0;

        while (true) {

            if (i == 10) {
                break;
            }

            System.out.printf("%d Hi\\n", i);
            i++;
        }

    }

}
```

```sql
0 Hi
1 Hi
2 Hi
3 Hi
4 Hi
5 Hi
6 Hi
7 Hi
8 Hi
9 Hi
```

- for

```sql
for(초기화; 종료조건; 반복실행){
        구문
}
```

```sql
package test;

public class ForDemo {

    public static void main(String[] args) {
        for (int i = 0; i < 10; i++){
            System.out.println(i + " Hi");
        }

    }

}
```

```sql
0 Hi
1 Hi
2 Hi
3 Hi
4 Hi
5 Hi
6 Hi
7 Hi
8 Hi
9 Hi
```
