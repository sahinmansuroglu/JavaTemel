### Soru : Parametre olarak aldığı sayı dizisindeki sayıların ortalamasını hesaplatarak sonucu döndüren bir method tanımlayarak ana programda çağırınız.


```java
public class Program {
    public static void main(String[] args) {
        int[] sayilar = {5, 10, 15, 20, 25};

        double ortalama = ortalamaHesapla(sayilar);

        System.out.println("Sayıların ortalaması: " + ortalama);
    }

     static double ortalamaHesapla(int[] sayilar) {
        int toplam = toplamHesapla(sayilar);
        double ortalama = (double) toplam / sayilar.length;

        return ortalama;
    }

     static int toplamHesapla(int[] sayilar) {
        int toplam = 0;

        for (int sayi : sayilar) {
            toplam += sayi;
        }

        return toplam;
    }
}


```
