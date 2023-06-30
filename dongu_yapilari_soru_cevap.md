### Soru 1: 7 sayısının faktöriyelini hesaplatınız. (for ve while döngüsü ile 2 ayrı program yazılacak).


```java
int sayi = 7;
int faktoriyel = 1;

for (int i = 1; i <= sayi; i++) {
    faktoriyel *= i;
}

System.out.println(sayi + " sayısının faktöriyeli: " + faktoriyel);

```

```java
int sayi = 7;
int faktoriyel = 1;
int i = 1;

while (i <= sayi) {
    faktoriyel *= i;
    i++;
}

System.out.println(sayi + " sayısının faktöriyeli: " + faktoriyel);

```

### Soru 2: Aşağıdaki çıktıyı veren programı tasarlayınız. (for ve while döngüsü ile 2 ayrı program yazılacak).
              1 2 3 4 5 8 9 10 11 12


```java
for (int i = 1; i <= 12; i++) {
    if (i == 6 || i == 7)
        continue;
    System.out.print(i + " ");
}

```

```java
int i = 1;

while (i <= 12) {
    if (i == 6 || i == 7) {
        i++;
        continue;
    }
    System.out.print(i + " ");
    i++;
}

```

### Soru 3: Aşağıdaki çıktıyı veren programı tasarlayınız. (for ve while döngüsü ile 2 ayrı program yazılacak).
              12 11 10 9 6 5 4 3 2 1


```java
for (int i = 12; i >= 1; i--) {
    if (i == 7 || i == 8)
        continue;
    System.out.print(i + " ");
}

```

```java
int i = 12;

while (i >= 1) {
    if (i == 7 || i == 8) {
        i--;
        continue;
    }
    System.out.print(i + " ");
    i--;
}

```

### Soru 4: Aşağıdaki çıktıyı veren programı tasarlayınız. (for ve while döngüsü ile 2 ayrı program yazılacak).
             3 6 9 12 15 18 21 24 27 30


```java
for (int i = 3; i <= 30; i += 3) {
    System.out.print(i + " ");
}

```

```java
int i = 3;

while (i <= 30) {
    System.out.print(i + " ");
    i += 3;
}

```

### Soru 5: Aşağıdaki çıktıyı veren programı tasarlayınız. (for ve while döngüsü ile 2 ayrı program yazılacak).
              12 10 8 6 4 2 0


```java
for (int i = 12; i >= 0; i -= 2) {
    System.out.print(i + " ");
}

```

```java
int i = 12;

while (i >= 0) {
    System.out.print(i + " ");
    i -= 2;
}

```

### Soru 6:  Döngü yardımıyla kullanıcının sürekli sayı girmesini sağlayınız. Ne zaman 0 sayısını girerse döngüyü sonlandırıp girdiği sayıların ortalamasını hesaplatınız


#### Çözüm 1
```java
import java.util.Scanner;

public class SayiOrtalamasi {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int toplam = 0;
        int sayiAdedi = 0;

        while (true) {
            System.out.print("Bir sayi girin (0 to exit): ");
            int sayi = input.nextInt();

            if (sayi == 0) {
                break;
            }

            toplam += sayi;
            sayiAdedi++;
        }

        if (sayiAdedi > 0) {
            double ortalama = (double) toplam / sayiAdedi;
            System.out.println("Girilen sayilarin ortalamasi: " + ortalama);
        } else {
            System.out.println("Hiç sayı girilmedi.");
        }
    }
}

```
#### Çözüm 2
```java
import java.util.Scanner;

public class SayiOrtalamasi {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int toplam = 0;
        int sayiAdedi = -1; // Başlangıçta -1 olarak tanımlanır, çünkü 0 girişi dikkate alınmayacak.

        int sayi;

        do {
            System.out.print("Bir sayi girin (0 to exit): ");
            sayi = input.nextInt();
            toplam += sayi;
            sayiAdedi++;
        } while (sayi != 0);

        if (sayiAdedi > 0) {
            double ortalama = (double) toplam / sayiAdedi;
            System.out.println("Girilen sayilarin ortalamasi: " + ortalama);
        } else {
            System.out.println("Hiç sayı girilmedi.");
        }
    }
}

```

