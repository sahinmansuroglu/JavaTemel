### Soru :  3 sayının ortalamasını hesaplayan bir method tanımlayarak bu method’u ana programda çağırınız  



```java
public class Program {
    public static void main(String[] args) {
        int sayi1 = 10;
        int sayi2 = 20;
        int sayi3 = 30;

        double ortalama = ortalamaBul(sayi1, sayi2, sayi3);
        System.out.println("Sayıların ortalaması: " + ortalama);
    }

    public static double ortalamaBul(int sayi1, int sayi2, int sayi3) {
        double toplam = sayi1 + sayi2 + sayi3;
        double ortalama = toplam / 3;
        return ortalama;
    }
}


```
