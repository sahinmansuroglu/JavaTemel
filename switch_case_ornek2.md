>Kullanıcının girdiği bir ay numarasına göre o ayın kaç gün içerdiğini ekrana yazdıran  programı Switch-Case yapısını kullanarak tasarlayınız. 


```java
import java.util.Scanner;

public class AyGunSayisiProgrami {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Bir ay numarası girin (1-12): ");
        int ay = scanner.nextInt();

        int gunSayisi;

        switch (ay) {
            case 1:
            case 3:
            case 5:
            case 7:
            case 8:
            case 10:
            case 12:
                gunSayisi = 31;
                break;
            case 4:
            case 6:
            case 9:
            case 11:
                gunSayisi = 30;
                break;
            case 2:
                gunSayisi = 28;
                break;
            default:
                System.out.println("Geçersiz bir ay numarası girdiniz.");
                return;
        }

        System.out.println("Bu ay " + gunSayisi + " gün içerir.");
    }
}

```
