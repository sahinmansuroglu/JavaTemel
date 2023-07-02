###  Soru 1: Klavyeden 2 tane string(metin) girdiriniz. İkinci  metinin 1. metinin içinde olup olmadığını bulan programı tasarlayınız.



```java
import java.util.Scanner;

public class MetinKontrol {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Birinci metini giriniz: ");
        String metin1 = scanner.nextLine();

        System.out.print("Ikinci metini giriniz: ");
        String metin2 = scanner.nextLine();

        if (metin1.contains(metin2)) {
            System.out.println("Ikinci metin birinci metinin içinde bulunuyor.");
        } else {
            System.out.println("Ikinci metin birinci metinin içinde bulunmuyor.");
        }
    }
}


```

###  Soru 2: Klavyeden girilen cümlede kaç kelime olduğunu hesaplayıp ekrana yazdıran programı tasarlayınız.



```java
import java.util.Scanner;

public class Program {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Bir cumle giriniz: ");
        String cumle = scanner.nextLine();
        String[] kelimeler = cumle.split(" ");
        int kelimeSayisi = kelimeler.length;
        System.out.println("Girilen cumlede " + kelimeSayisi + " kelime bulunuyor.");
    }


}


```

###  Soru 3:  : Klavyeden girilen kelimenin harflerini alt alta ekrana yazdıran programı tasarlayınız.



```java
import java.util.Scanner;

public class Program {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Bir kelime giriniz: ");
        String kelime = scanner.nextLine();

        for (int i = 0; i < kelime.length(); i++) {
            char harf = kelime.charAt(i);
            System.out.println(harf);
        }
    }

   
}


```

###  Soru 4:  Klavyeden girilen harflerini kelimenin alfabetik sıraya göre alt alta ekrana yazdıran programı tasarlayınız.



```java
import java.util.Arrays;
import java.util.Scanner;

public class Program {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Bir kelime giriniz: ");
        String kelime = scanner.nextLine();

        char[] harfler = kelime.toCharArray();
        Arrays.sort(harfler);

        for (char harf : harfler) {
            System.out.println(harf);
        }
    }
}


```

###  Soru 5: Aşağıdaki metin içerisindeki sayıların toplamını bulup ekrana yazdıran programı tasarlayınız.
```java
String metin = "10-12-52-75-66-77";
```

```java
public class Program {
    public static void main(String[] args) {
        String metin = "10-12-52-75-66-77";
        String[] sayilar = metin.split("-");
        int toplam = 0;

        for (String sayi : sayilar) {
            int sayiInt = Integer.parseInt(sayi);
            toplam += sayiInt;
        }

        System.out.println("Sayıların Toplamı: " + toplam);
    }
}


```

###  Soru 6:  Aşağıdaki ürün listesinde her bir ürünün adedi ve birim fiyatı verilmektedir. Buna göre ürün adlarını ve her bir ürünün toplam tutarını alt alta ekrana yazdıran programı tasarlayınız

```java
String urunListesi = "ram,2,45;cpu,3,50;klavye,4,15;mouse,2,10";
```


```java
public class Program {
    public static void main(String[] args) {
        String urunListesi = "ram,2,45;cpu,3,50;klavye,4,15;mouse,2,10";

        // Ürünleri virgül ve noktalı virgül karakterlerine göre parçalara ayırma
        String[] urunler = urunListesi.split(";");

        // Her bir ürün için işlemleri gerçekleştirme
        for (String urun : urunler) {
            String[] urunBilgileri = urun.split(",");
            String urunAdi = urunBilgileri[0];
            int adet = Integer.parseInt(urunBilgileri[1]);
            double birimFiyat = Double.parseDouble(urunBilgileri[2]);
            double toplamTutar = adet * birimFiyat;

            // Ürün adını ve toplam tutarını ekrana yazdırma
            System.out.println("Ürün Adı: " + urunAdi);
            System.out.println("Toplam Tutar: " + toplamTutar);
            System.out.println();
        }
    }
}


```


