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

#### Computer.java
```java
public class Computer extends Calculator {

    String os;
    int storageSize;

    Computer(String maker) {
        super(maker);
    }

    Computer(String maker, String os, int storageSize) {
        this(maker);
        this.os = os;
        this.storageSize = storageSize;
    }

    void paint() {
        System.out.println("イラストを描きます。");
    }

    void showSpec() {
        System.out.println("メーカー：" + maker);
        System.out.println("OS：" + os);
        System.out.println("ストレージサイズ：" + storageSize);
    }
}
```

#### OopMain3.java
```java
public class OopMain3 {
    public static void main(String[] args) {

        Computer com1 = new Computer("CONY");
        com1.os = "Windows 8";
        com1.storageSize = 250;

        Computer com2 = new Computer("TOOSHIBA", "Windows 10", 500);

        com1.showSpec();
        System.out.println();
        com2.showSpec();

    }
}
```
