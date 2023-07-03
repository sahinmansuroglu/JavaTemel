### Soru :  Klavyeden girilen 2 sayı üzerinde method kullanılarak 4 işlem hesaplama örneği.



```java
import java.util.Scanner;

public class Program {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Birinci sayıyı girin: ");
        double sayi1 = scanner.nextDouble();

        System.out.print("İkinci sayıyı girin: ");
        double sayi2 = scanner.nextDouble();

        double toplam = toplama(sayi1, sayi2);
        double fark = cikarma(sayi1, sayi2);
        double carpim = carpma(sayi1, sayi2);
        double bolum = bolme(sayi1, sayi2);

        System.out.println("Toplam: " + toplam);
        System.out.println("Fark: " + fark);
        System.out.println("Çarpım: " + carpim);
        System.out.println("Bölüm: " + bolum);
    }

    public static double toplama(double sayi1, double sayi2) {
        return sayi1 + sayi2;
    }

    public static double cikarma(double sayi1, double sayi2) {
        return sayi1 - sayi2;
    }

    public static double carpma(double sayi1, double sayi2) {
        return sayi1 * sayi2;
    }

    public static double bolme(double sayi1, double sayi2) {
        return sayi1 / sayi2;
    }
}



```
