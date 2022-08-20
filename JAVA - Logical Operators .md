- && ( AND )
  
  - 좌항과 우항의 값이 모두 참(true)일 때 참
  
  ```sql
  package test;
  
  public class AndDemo {
  
      public static void main(String[] args) {
  
          if (true && true) {
              System.out.println("A");
          } // true
          if (true && false) {
              System.out.println("B");
          } // false
          if (false && true) {
              System.out.println("C");
          } // false
          if (false && false) {
              System.out.println("D");
          } // false
      }
  
  }
  ```
  
  ```sql
  A
  ```

- || ( OR )
  
  - 좌항과 우항 중에 하나라도 참이라면 전체가 참
  
  ```sql
  package test;
  
  public class OrDemo {
  
      public static void main(String[] args) {
  
          if (true || true) {
              System.out.println("A");
          } // true
          if (true || false) {
              System.out.println("B");
          } // true
          if (false || true) {
              System.out.println("C");
          } // true
          if (false || false) {
              System.out.println("D");
          } // false
      }
  
  }
  ```
  
  ```sql
  A
  B
  C
  ```

- ! ( NOT )
  
  - !는 부정의 의미로 boolean의 값을 역전시키는 역할
  
  ```sql
  package test;
  
  public class NotDemo {
  
      public static void main(String[] args) {
  
          if (!true) {
              System.out.println("A");
          }
  
          if (!false) {
              System.out.println("B");
          }
  
      }
  
  }
  ```
  
  ```sql
  B
  ```
