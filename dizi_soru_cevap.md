## int[] dizi=new int[]{85,33,54,75,96,33,21,22,69,66,33,14,22,33,99,66,55,21};

## Aşağıdaki 5 Soruyu yukarıdaki diziyi kullanarak tasarlayınız.


###  Soru 1: Dizide kaç adet 33 sayısı bulunmaktadır? Hesaplatarak ekrana yazdırınız.


```java
int count = 0;
for (int i = 0; i < dizi.length; i++) {
    if (dizi[i] == 33) {
        count++;
    }
}
System.out.println(count); // 4

```

###  Soru 2: Dizide sayıların toplamını hesaplatarak ekrana yazdırınız.


```java
int toplam = 0;
for (int i = 0; i < dizi.length; i++) {
    toplam += dizi[i];
}
System.out.println("Dizi elemanlarının toplamı: " + toplam);


```

###  Soru 3 : Dizideki çift sayıları ekrana yazdırınız.


```java
System.out.print("Çift sayılar: ");
for (int i = 0; i < dizi.length; i++) {
    if (dizi[i] % 2 == 0) {
        System.out.print(dizi[i] + " ");
    }
}
System.out.println();


```

###  Soru 4: Dizide kaç adet çift sayı, kaç adet tek sayı bulunduğunu hesaplatıp ekrana yazdırınız?



```java
int tekSayiAdedi = 0;
int ciftSayiAdedi = 0;
for (int i = 0; i < dizi.length; i++) {
    if (dizi[i] % 2 == 0) {
        ciftSayiAdedi++;
    } else {
        tekSayiAdedi++;
    }
}
System.out.println("Çift sayı adedi: " + ciftSayiAdedi);
System.out.println("Tek sayı adedi: " + tekSayiAdedi);


```

###  Soru 5 : Dizi elemanları küçükten büyüğe sıralı olarak ekrana yazdırınız.

```java
import java.util.Arrays;

// Diziyi küçükten büyüğe sırala
Arrays.sort(dizi);

// Sıralanmış diziyi ekrana yazdır
System.out.println("Dizi elemanları (küçükten büyüğe sıralı):");
for (int i = 0; i < dizi.length; i++) {
    System.out.print(dizi[i] + " ");
}
System.out.println();


```

###  Soru 1:  int tipinde 20 elemanlı bir dizi oluşturarak aşağıda istenilenleri bu diziyi kullanarak tasarlayınız.

>Dizinini elemanlarını Random sınıfını kullanarak 0 ile 100 arasında rastgele değer ile doldurunuz.

>Dizinini elemanlarını ekrana yan yana yazdırınız.

>Dizi içerisindeki sayıların toplamını ve ortalamasını hesaplatınız.

>Dizi içerisindeki tek sayıları ve çift sayıları ayrı ayrı yan yana yazdırınız.

>Dizi içerisinde kaç adet tek sayı kaç adet çift sayı bulunmaktadır hesaplatıp ekrana yazdırınız.



```java



import java.util.Random;

public class Program {
    public static void main(String[] args) {
        int[] dizi = new int[20];
        Random random = new Random();

        // Diziyi rastgele değerlerle doldurma
        for (int i = 0; i < dizi.length; i++) {
            dizi[i] = random.nextInt(101); // 0 ile 100 arasında rastgele değerler
        }

        // Diziyi ekrana yan yana yazdırma
        System.out.println("Dizi elemanları: ");
        for (int eleman : dizi) {
            System.out.print(eleman + " ");
        }
        System.out.println();

        // Dizideki elemanların toplamını ve ortalamasını hesaplama
        int toplam = 0;
        for (int eleman : dizi) {
            toplam += eleman;
        }
        double ortalama = (double) toplam / dizi.length;

        System.out.println("Dizideki elemanların toplamı: " + toplam);
        System.out.println("Dizideki elemanların ortalaması: " + ortalama);

        // Dizi içerisindeki tek ve çift sayıları ayrı ayrı yazdırma
        System.out.println("Tek sayılar: ");
        for (int eleman : dizi) {
            if (eleman % 2 == 1) {
                System.out.print(eleman + " ");
            }
        }
        System.out.println();

        System.out.println("Çift sayılar: ");
        for (int eleman : dizi) {
            if (eleman % 2 == 0) {
                System.out.print(eleman + " ");
            }
        }
        System.out.println();

        // Dizide kaç adet tek sayı ve çift sayı olduğunu hesaplama
        int tekSayiAdeti = 0;
        int ciftSayiAdeti = 0;
        for (int eleman : dizi) {
            if (eleman % 2 == 1) {
                tekSayiAdeti++;
            } else {
                ciftSayiAdeti++;
            }
        }

        System.out.println("Dizideki tek sayı adeti: " + tekSayiAdeti);
        System.out.println("Dizideki çift sayı adeti: " + ciftSayiAdeti);
    }
}
```


