import java.text.NumberFormat;
import java.util.ArrayList;
import java.util.Locale;

public class Order {
    private String name;
    private int price, quantity;

    public Order(){}

    public void setItemName(String name) {
        this.name = name;
    }

    public void setItemPrice(int price) {
        this.price = price;
    }

    public void setItemQuantity(int quantity){
        this.quantity = quantity;
    }

    public String name(){
        return this.name;
    }

    public int price() {
        return this.price;
    }

    public int quantity(){
        return this.quantity;
    }

    public String printInvoiceOrder(ArrayList<Order> items){
        Locale country = new Locale.Builder().setLanguage("id").setRegion("ID").build();
        NumberFormat currencyIdr = NumberFormat.getCurrencyInstance(country);
        int total = 0;
        for (Order item : items) {
            System.out.println(item.name());
            System.out.println(item.quantity() + " * " + item.price());
            total += (item.price() * item.quantity());
        }
        return currencyIdr.format(total);
    }
}
