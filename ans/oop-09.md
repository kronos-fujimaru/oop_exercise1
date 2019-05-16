#### OopMain5.java
```java
public class OopMain5 {
    public static void main(String[] args) {

        Computer[] devices = {
                new Computer("CONY", "Windows 10", 500),
                new SmartPhone("Pineapple", "iOS", 64, 901234),
                new Tablet("Sumsong", "Android", 128, "takeshi")
        };

        for (int i = 0; i < devices.length; i++) {
            devices[i].showSpec();
            System.out.println();
        }
    }
}
```
