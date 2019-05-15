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
public class Computer extends Calculator {
    Computer(String maker) {
        super(maker);
    }

    void paint() {
        System.out.println("イラストを描きます。");
    }
}
```

#### OopMain2.java
```java
public class OopMain2 {
    public static void main(String[] args) {

        Computer com = new Computer("CONY");
        System.out.println("120 + 80 = " + com.add(120, 80));
        com.paint();

    }
}
```
