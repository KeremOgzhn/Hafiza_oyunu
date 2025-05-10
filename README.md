Collecting workspace informationProjeniz, `Kart` ve `Main` olmak üzere iki Java sınıfından oluşan bir hafıza kartı oyunudur.

## Hafıza Oyunu

Bu proje, konsol tabanlı bir hafıza kartı oyunudur. Oyuncular, 4x4'lük bir tahtada gizlenmiş kart çiftlerini bulmaya çalışır.

### Nasıl Oynanır?

1.  Oyun başladığında, 4x4'lük bir kart tahtası görüntülenir. Tüm kartlar başlangıçta kapalıdır.
2.  Oyuncudan ilk tahmin için bir satır (i) ve sütun (j) değeri girmesi istenir.
3.  Seçilen kart açılır ve değeri gösterilir.
4.  Oyuncudan ikinci tahmin için bir satır (i) ve sütun (j) değeri girmesi istenir.
5.  İkinci kart açılır:
    *   Eğer ikinci kartın değeri ilk kartın değeriyle eşleşirse, her iki kart da açık kalır. "Tebrikler! Doğru tahmin ettiniz." mesajı gösterilir.
    *   Eğer kartlar eşleşmezse, "Yanlış tahmin. Tekrar deneyin." mesajı gösterilir ve ilk açılan kart tekrar kapatılır.
6.  Tüm kart çiftleri doğru bir şekilde eşleştirilene kadar oyun devam eder.
7.  Tüm kartlar açıldığında oyun biter.

### Dosyalar

*   **Kart.java:**
    *   Bir oyun kartını temsil eden sınıftır.
    *   Her kartın bir `deger` (char) ve bir `tahmin` (boolean) durumu vardır. `tahmin` durumu, kartın açık (true) mı yoksa kapalı (false) mı olduğunu belirtir.
    *   `getDeger()`, `setDeger()`, `isTahmin()`, ve `setTahmin()` gibi getter ve setter metotlarını içerir.

*   **Main.java:**
    *   Oyunun ana mantığını içerir.
    *   `kartlar` adında 4x4'lük bir `Kart` dizisi oluşturur ve başlangıç değerlerini atar.
    *   `main` metodu, oyun döngüsünü yönetir. `oyunBittiMi()` metodu false döndürdüğü sürece `oyunTahtasi()` ve `tahminEt()` metotlarını çağırır.
    *   `tahminEt()`: Kullanıcıdan iki kart seçmesini ister, kartları karşılaştırır ve `tahmin` durumlarını günceller.
    *   `oyunBittiMi()`: Tahtadaki tüm kartların `tahmin` durumunun true olup olmadığını kontrol eder.
    *   `oyunTahtasi()`: Oyun tahtasının güncel durumunu konsola yazdırır. Açık kartların değerini, kapalı kartları ise boş olarak gösterir.
