#### Shop.java
```java
public abstract class Shop {

	String name;
	int purchasePrice = 0;

	Shop(String name) {
		this.name = name;
	}

	abstract void open();

	abstract void close();

	void showPurchasePrice() {
		System.out.println("買取価格は" + purchasePrice + "円です。");
	}
}
```

#### ApplianceShop.java
```java
import java.util.ArrayList;
import java.util.List;

public class ApplianceShop extends Shop {

	List<Computer> devices = new ArrayList<>();

	ApplianceShop(String name) {
		super(name);
	}

	@Override
	void open() {
		System.out.println(name + "は10時に開店します。");
	}

	@Override
	void close() {
		System.out.println(name + "は21時に閉店します。");
	}

	void purchase(Computer device) {
		devices.add(device);
		purchasePrice += 10000;
	}
}
```

#### OopMain6.java
```java
public class OopMain6 {
	public static void main(String[] args) {

		ApplianceShop ashop = new ApplianceShop("Yodoyabashi Camera");

		Computer com = new Computer("CONY", "Windows 10", 500);
		Computer sp = new SmartPhone("Pineapple", "iOS", 64, 901234);
		Computer tab = new Tablet("Sumsong", "Android", 128, "takeshi");

		ashop.open();
		ashop.purchase(com);
		ashop.purchase(sp);
		ashop.purchase(tab);
		ashop.showPurchasePrice();
		ashop.close();

	}
}
```
