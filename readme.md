## Nedir bu Richard.db ?
Json tabanlı çalışan bir veritabanıdır, sadeliği ve türkçe komutları ile hızlı ve güvenli çalışmaktadır.
 
## Nasıl json tanımlarım?
```js
/// Önce Tanımlama yapalım
const Veritabani = require("richard.db");
const rdb = new Veritabani("./richard.json");
```

## Peki nasıl kullanabilirim?
```js
/// Veri değerini sabitlemek (set)

rdb.ayarla("Verimiz", "Richard Watterson"); // Verimiz verisini "Richard Watterson" olarak sabiledik.

// Veri değerini çekmek
rdb.cek("Verimiz"); // Çıktı olarak "Richard Watterson" çıktısını alacaksınız.
rdb.bul("Verimiz"); // Çıktı olarak "Richard Watterson" çıktısını alacaksınız.

// Veri silme
rdb.sil("Verimiz"); // Verimiz verisini sildik.

// Veri kontrolü
rdb.kontrol("Verimiz"); // Eğer ki veri bulunuyor ise "true" çıktısı alırsınız, eğer ki veri bulunmuyorsa "false" çıktısını alırsınız. 

// Veri ekleme - Veri azaltma
rdb.ekle("Sayı", 5); // Sayı verimize 5 eklendi

rdb.eksilt("Sayı", 4); // Sayı verimizden 4 eksiltildi

// Verimize değer ekleme
rdb.degerekle("Kimlik", { Isim: "Richard", Soyisim: "Watterson"}); // Kimlik verisine isim ve soyisim değerlerini ekledik.

// Jsondaki verileri silme 
rdb.temizle(); // rdb ile tanımlı olan Json dosyasını tamamen temizledik.
```
