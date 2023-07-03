###  Soru 1 : Parametre olarak aldığı 3 sayıdan en büyüğünün  döndüren bir method tanımlayınız ve kullanınız.




```java
public class Program {

    public static void main(String[] args) {
        int sayi1 = 10;
        int sayi2 = 25;
        int sayi3 = 15;

        int enBuyukSayi = enBuyuguBul(sayi1, sayi2, sayi3);
        System.out.println("En büyük sayı: " + enBuyukSayi);
    }

    public static int enBuyuguBul(int sayi1, int sayi2, int sayi3) {
        int enBuyuk = sayi1;

        if (sayi2 > enBuyuk) {
            enBuyuk = sayi2;
        }

        if (sayi3 > enBuyuk) {
            enBuyuk = sayi3;
        }

        return enBuyuk;
    }
}


```

### Soru 2: Parametre olarak aldığı 3 adet String’I aralarına “-” işareti koyarak tek bir metin olarak döndüren metodu tanımlayınız ve kullanınız.




```java
public class Program {

    public static void main(String[] args) {
        String kelime1 = "Java";
        String kelime2 = "programlama";
        String kelime3 = "dili";

        String birlesikMetin = metinBirlestir(kelime1, kelime2, kelime3);
        System.out.println("Birleştirilmiş Metin: " + birlesikMetin);
    }

    public static String metinBirlestir(String kelime1, String kelime2, String kelime3) {
        String birlesikMetin = kelime1 + "-" + kelime2 + "-" + kelime3;
        return birlesikMetin;
    }
}


```

### Soru 3 : Parametre olarak aldığı sayının tek mi çift mi olduğunu döndüren bir method tanımlayınız ve kullanınız. 




```java
public class Program {

    public static void main(String[] args) {
        int sayi = 7;

        String sonuc = tekMiCiftMi(sayi);
        System.out.println(sayi + " sayısı " + sonuc);
    }

    public static String tekMiCiftMi(int sayi) {
        if (sayi % 2 == 0) {
            return "çift";
        } else {
            return "tek";
        }
    }
}


```

### Soru 4: Parametre olarak aldığı iki sayı arasındaki sayıların toplamını hesaplayıp döndüren  bir method tanımlayınız ve kullanınız. 




```java

public class Program {

    public static void main(String[] args) {
        int sayi1 = 5;
        int sayi2 = 10;

        int toplam = sayilarinToplami(sayi1, sayi2);
        System.out.println(sayi1 + " ile " + sayi2 + " arasindaki sayilarin toplami: " + toplam);
    }

    public static int sayilarinToplami(int sayi1, int sayi2) {
        int toplam = 0;
        for (int i = sayi1 + 1; i < sayi2; i++) {
            toplam += i;
        }
        return toplam;
    }
}

```

### Soru 5 : Parametre olarak aldığı  sayının faktöriyelini hesaplayıp sonucu döndüren bir method tanımlayınız ve kullanınız




```java
public class Main {

    public static void main(String[] args) {
        int sayi = 5;
        int faktoriyel = faktoriyelHesapla(sayi);
        System.out.println(sayi + " sayisinin faktoriyeli: " + faktoriyel);
    }

    public static int faktoriyelHesapla(int sayi) {
        int faktoriyel = 1;
        for (int i = 1; i <= sayi; i++) {
            faktoriyel *= i;
        }
        return faktoriyel;
    }
}


```

### Soru 6: Aşağıda verilen ana program’da 2 adet tanımlanmamış method vardır. Bunlar;
- “adeteGoreUrunGirisi”: Adete göre kullanıcıdan ürün girişi yaptırmakta ve girilen bu ürünleri dizi olarak döndürmektedir . 
- “urunleriListele”: Parameter olarak aldığı String dizisini ekrna yazdırmaktadır.
  
Programın doğru çalışabilmesi için bu methodları tanımlayınız.  




```java
import java.util.Scanner;

public class Program {

    public static void main(String[] args) {
        String[] urunDizi = adeteGoreUrunGirisi(5);
        urunleriListele(urunDizi);
    }

    public static String[] adeteGoreUrunGirisi(int adet) {
        Scanner scanner = new Scanner(System.in);
        String[] urunler = new String[adet];
        for (int i = 0; i < adet; i++) {
            System.out.print("Ürün girin: ");
            String urun = scanner.nextLine();
            urunler[i] = urun;
        }
        return urunler;
    }

    public static void urunleriListele(String[] urunler) {
        for (String urun : urunler) {
            System.out.println(urun);
        }
    }
}


```
