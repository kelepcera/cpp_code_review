## Başlık Dosyaları (Header Files)
+ gereksiz yere bir başlık dosyası include edilmiş mi?
  + ön bildirim _(forward declaration)_ yapmak yerine gereksiz yere başlık dosyası include edilmiş mi?
+ başlık dosyasında _using bildirimi_ var mı?
+ başlık dosyasında _using namespace direktifi_ var mı?
  
## Const Doğruluğu (Const Correctness)
  + salt okuma _(read-only access)_ amaçlı kullanılacak değişkenler const yapılmış mı?
    + lookup table olarak kullanılan veri yapıları const yapılmış mı?
    + okuma amaçlı erişim sağlayan referans parametreler const yapılmış mı?
    + gösterici değişkenler
      + low level const
      + top level const
    + aralık tabanlı for döngülerinde döngü değişkeni olarak kullanılan sol taraf referansları
    + const olması gereken üye fonksiyonları

## Yorum satırları (Comment Lines)
+ gereksiz yorum satırı var mı?
+ güncellenmesi _(update)_ gereken yorum satırı var mı?
  
     
## İsimlendirme (Naming)
  + Türkçe isim kullanılmış mı?
  + isimlendirmede tutarlı bir konvensiyon kullanılmış mı?
  + birbirine çok yakın isimler seçilmiş mi? (x1, x2, x3)
  + görsel olarak 0 ile karıştırılma riski olan o karakteri
  + fonksiyon isimleri iyi seçilmiş mi?

## Sabitler (constants)
  + nullptr
    + nullptr yerine NULL makrosu kullanılmış mı?
    + nullptr yerine tam sayı sabiti olarak 0 kullanılmış mı?
    
## Numaralandırmalar (enums)

## Fonksiyonlar
+ fonksiyon ismi iyi seçilmiş mi?
  + verilen ismi  yeterince betimleyici mi?
+ fonksiyonlara birden fazla görev yüklenmiş mi?
  + küçük birden fazla fonksiyon yerine tek bir (uzun) fonksiyon tanımlanmış mı? 
+ kullanılmayacak parametreler (gereksiz yere) isimlendirilmiş mi?
+ fonksiyon parametre sayısı fazla mı?

## Lambda İfadeleri (Lambda Expressions)
  
## Kapsam Sızıntısı (Scope Leakage)
## Taşıma Semantiği (Move Semantics) 
  + Sınıfın move member'ları delete edilmiş mi?

## Kopyalamanın Eliminasyonu (Copy Elision)

# Sınıflar (Classes)

