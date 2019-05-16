#### Tablet.java
```java
public class Tablet extends Computer {

    String acountName;

    Tablet(String maker, String os, int storageSize, String acountName) {
        super(maker, os, storageSize);
        this.acountName = acountName;
    }

    @Override
    void showSpec() {
        System.out.println("メーカー：" + maker);
        System.out.println("OS：" + os);
        System.out.println("ストレージサイズ：" + storageSize + "GB");
        System.out.println("アカウント名：" + acountName);
    }

    void videocall(String toAcountName) {
        if (this.acountName.equals(acountName)) {
            System.out.println("ビデオ電話できません。");
        } else {
            System.out.println(toAcountName + "にビデオ電話します。");
        }
    }
}
```

#### OopMain5.java
```java
public class OopMain5 {
    public static void main(String[] args) {

        Computer com = new Computer("CONY", "Windows 10", 500);
        Computer sp = new SmartPhone("Pineapple", "iOS", 64, 901234);
        Computer tab = new Tablet("Sumsong", "Android", 128, "takeshi");

        com.showSpec();
        System.out.println();
        sp.showSpec();
        System.out.println();
        tab.showSpec();

        // ビデオコールは実行できない
        //tab.videocall();

    }
}
```
