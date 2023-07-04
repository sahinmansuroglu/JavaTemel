### Soru 1: Uzun ve kısa kenar uzunluğu verilen dikdörtgenin çevresini ve alanını hesaplayıp ekrana yazan programı tasarlayınız.





```java

public class Program {
    public static void main(String[] args) {
        // Dikdörtgenin uzun ve kısa kenar uzunluklarını belirleyin
        double uzunKenar = 5.5;
        double kisaKenar = 4;

        // Çevre ve alanı hesaplayın
        double cevre = 2 * (uzunKenar + kisaKenar);
        double alan = uzunKenar * kisaKenar;

        // Sonuçları ekrana yazdırın
        System.out.println("Dikdörtgenin çevresi: " + cevre);
        System.out.println("Dikdörtgenin alanı: " + alan);
    }
}
```


### Soru 2: Yarı çap uzunluğu verilen dairenin alanine hesaplatıp ekrana yazdıran programı tasarlayınız



```java
public class DaireAlanHesaplama {
    public static void main(String[] args) {
        // Yarı çap uzunluğunu sabit bir değer olarak belirleyin
        double yariCap = 5.0;

        // Alanı hesaplayın
        double alan = Math.PI * yariCap * yariCap;

        // Sonucu ekrana yazdırın
        System.out.println("Dairenin alanı: " + alan);
    }
}

```

### Soru 3: Verilen 4 puanın ortalamasını bulup ekrana yazdıran programı tasarlayınız



```java
public class Program {
    public static void main(String[] args) {
        // Verilen puanları sabit bir şekilde belirleyin
        int puan1 = 80;
        int puan2 = 90;
        int puan3 = 85;
        int puan4 = 95;

        // Puanların toplamını hesaplayın
        int toplam = puan1 + puan2 + puan3 + puan4;

        // Ortalamayı hesaplayın
        double ortalama = (double) toplam / 4;

        // Sonucu ekrana yazdırın
        System.out.println("Puanların ortalaması: " + ortalama);
    }
}

```

### Soru 4: String tipinde adları metin1, metin2 ve metin3 olan üç tane değişken tanımlayınız. Değerleri sırasıyla “Yazılım”, “Test”  ve “Otomasyonu” olsun. Bu üç metini dördüncü bir değişkende aralarında boşluk olacak şekilde birleştirerek ekrana yazdırınız.





```java
public class Program {
    public static void main(String[] args) {
        String metin1 = "Yazılım";
        String metin2 = "Test";
        String metin3 = "Otomasyonu";

        String birlesikMetin = metin1 + " " + metin2 + " " + metin3;

        System.out.println(birlesikMetin);
    }
}

```

### Soru 5: Bir öğrencinin girdiği sınavlarda yıl sonu puanı hesaplanırken ilk 2 sınavının % 25'i son sınavının ise % 50'si toplanarak bulunmaktadır. Buna göre 3 sınav verilen bir öğrencinin yıl sonu puanını hesaplayınız.





```java
public class Program {
    public static void main(String[] args) {
        int sinav1 = 80;
        int sinav2 = 90;
        int sinav3 = 70;

        double yilSonuPuani = (sinav1 + sinav2) * 0.25 + sinav3 * 0.5;

        System.out.println("Yıl sonu puanı: " + yilSonuPuani);
    }
}

```

### Soru 6: Verilen 3 basamaklı sayının rakamlarını alt alta yazdırınız.





```java
public class Program {
    public static void main(String[] args) {
        int sayi = 123;

        int birlerBasamagi = sayi % 10;
        int onlarBasamagi = (sayi / 10) % 10;
        int yuzlerBasamagi = sayi / 100;

        System.out.println(yuzlerBasamagi);
        System.out.println(onlarBasamagi);
        System.out.println(birlerBasamagi);
    }
}

```


