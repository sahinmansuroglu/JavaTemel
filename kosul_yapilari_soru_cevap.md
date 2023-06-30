### Soru 1: Bir sayının pozitif, negatif veya sıfır olduğunu kontrol eden programı tasarlayınız.

```java
int sayi = 10;

if (sayi > 0) {
    System.out.println("Sayı pozitiftir.");
} else if (sayi < 0) {
    System.out.println("Sayı negatiftir.");
} else {
    System.out.println("Sayı sıfırdır.");
}

```

### Soru 2: Kullanıcının girdiği notun harf notuna dönüştüren programı tasarlayınız


```java

Scanner scanner = new Scanner(System.in);

System.out.print("Notunuzu girin: ");
int not = scanner.nextInt();

if (not >= 90) {
    System.out.println("A");
} else if (not >= 80) {
    System.out.println("B");
} else if (not >= 70) {
    System.out.println("C");
} else if (not >= 60) {
    System.out.println("D");
} else {
    System.out.println("F");
}
```

### Soru 3: Klavyeden girilen 2 sayı ve işlem (+, - , *, / )'e göre hesaplama yapan uygulama tasarlayınız. ( if-else if yapısı ile )

```java
import java.util.Scanner;

public class HesapMakinesi {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Birinci sayıyı girin: ");
        double sayi1 = scanner.nextDouble();

        System.out.print("İkinci sayıyı girin: ");
        double sayi2 = scanner.nextDouble();

        System.out.print("İşlemi girin (+, -, *, /): ");
        char islem = scanner.next().charAt(0);

        double sonuc = 0;

        if (islem == '+') {
            sonuc = sayi1 + sayi2;
        } else if (islem == '-') {
            sonuc = sayi1 - sayi2;
        } else if (islem == '*') {
            sonuc = sayi1 * sayi2;
        } else if (islem == '/') {
            sonuc = sayi1 / sayi2;
        } else {
            System.out.println("Geçersiz işlem girdiniz!");
            return;
        }

        System.out.println("Sonuç: " + sonuc);
    }
}

```

### Soru 4: Klavyeden girilen 2 sayı ve işlem (+, - , *, / )'e göre hesaplama yapan uygulama tasarlayınız. (switch case yapısı ile )

```java
import java.util.Scanner;

public class HesapMakinesi {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Birinci sayıyı girin: ");
        double sayi1 = scanner.nextDouble();

        System.out.print("İkinci sayıyı girin: ");
        double sayi2 = scanner.nextDouble();

        System.out.print("İşlemi girin (+, -, *, /): ");
        char islem = scanner.next().charAt(0);

        double sonuc = 0;

        switch (islem) {
            case '+':
                sonuc = sayi1 + sayi2;
                break;
            case '-':
                sonuc = sayi1 - sayi2;
                break;
            case '*':
                sonuc = sayi1 * sayi2;
                break;
            case '/':
                sonuc = sayi1 / sayi2;
                break;
            default:
                System.out.println("Geçersiz işlem girdiniz!");
                return;
        }

        System.out.println("Sonuç: " + sonuc);
    }
}

```
### Soru 5: Klavyeden girilen kullanıcı adı ve şifreye göre doğruysa giriş başarılı yanlışsa giriş başarısız yazdıran programı tasarlayınız. (kullanıcı adı: Admin şifre:sfr1357 olsun)



```java
import java.util.Scanner;

public class GirisProgrami {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Kullanıcı Adı: ");
        String kullaniciAdi = scanner.nextLine();

        System.out.print("Şifre: ");
        String sifre = scanner.nextLine();

        if (kullaniciAdi.equals("Admin") && sifre.equals("sfr1357")) {
            System.out.println("Giriş Başarılı!");
        } else {
            System.out.println("Giriş Başarısız!");
        }
    }
}

```

### Soru 6: Klavyeden girilen 3 sayıyı büyükten küçüğe sıralayan programı tasarlayınız.




```java
import java.util.Scanner;

public class SayiSiralama {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("1. Sayıyı girin: ");
        int sayi1 = scanner.nextInt();

        System.out.print("2. Sayıyı girin: ");
        int sayi2 = scanner.nextInt();

        System.out.print("3. Sayıyı girin: ");
        int sayi3 = scanner.nextInt();

        int temp;

        if (sayi1 < sayi2) {
            temp = sayi1;
            sayi1 = sayi2;
            sayi2 = temp;
        }

        if (sayi1 < sayi3) {
            temp = sayi1;
            sayi1 = sayi3;
            sayi3 = temp;
        }

        if (sayi2 < sayi3) {
            temp = sayi2;
            sayi2 = sayi3;
            sayi3 = temp;
        }

        System.out.println("Sıralama: " + sayi1 + " > " + sayi2 + " > " + sayi3);
    }
}


```

