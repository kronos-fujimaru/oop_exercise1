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

#### SmartPhone.java
```java
public class SmartPhone extends Computer {

    int phoneNum;
    int charge = 0;

    SmartPhone(String maker, String os, int storageSize, int phoneNum) {
        super(maker, os, storageSize);
        this.phoneNum = phoneNum;
    }

    @Override
    void showSpec() {
        System.out.println("メーカー：" + maker);
        System.out.println("OS：" + os);
        System.out.println("ストレージサイズ：" + storageSize);
        System.out.println("電話番号：" + phoneNum);
    }

    void call(int toPhoneNum) {
        if (this.phoneNum == toPhoneNum) {
            System.out.println("電話できません。");
        } else {
            System.out.println(toPhoneNum + "に電話しています。");
            charge += 30;
        }
    }

    void showCharge() {
        System.out.println("今月の電話代：" + charge + "円");
    }
}
```

#### OopMain5.java
```java
public class OopMain5 {
    public static void main(String[] args) {

        SmartPhone sp = new SmartPhone("Pineapple", "iOS", 64, 901234);
        sp.call(901235);
        sp.call(901236);
        sp.call(901234);
        sp.call(901237);
        sp.showCharge();

    }
}
```
