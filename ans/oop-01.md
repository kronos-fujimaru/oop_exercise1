#### Calculator.java
```java
public class Calculator {

    String maker;

    Calculator(String maker) {
        this.maker = maker;
    }

    int add(int num1, int num2) {
        return num1 + num2;
    }
}
```

#### OopMain1.java
```java
public class OopMain1 {
    public static void main(String[] args) {

        Calculator calc = new Calculator("CASSIO");
        System.out.println(calc.maker + "の電卓を買いました。");

        int result = calc.add(10, 5);
        System.out.println("10 + 5 = " + result);

    }
}
```
