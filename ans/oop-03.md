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

    double add(int num1, double num2) {
        return num1 + num2;
    }

    int add(int[] numbers) {
        int total = 0;
        for (int i = 0; i < numbers.length; i++) {
            total = add(total, numbers[i]);
        }
        return total;
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

        double result2 = calc.add(5, 3.5);
        System.out.println("5 + 3.5 = " + result2);

        int[] numbers = {10, 20, 30, 45, 25};
        int result3 = calc.add(numbers);
        System.out.println("合計は" + result3);

    }
}
```
