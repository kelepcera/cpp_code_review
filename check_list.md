## Başlık Dosyaları (Header Files)
+ gereksiz yere bir başlık dosyası include edilmiş mi?
  + ön bildirim _(forward declaration)_ yapmak yerine gereksiz yere başlık dosyası include edilmiş mi?
+ başlık dosyasında _using bildirimi_ var mı?
+ başlık dosyasında _using namespace direktifi_ var mı?
+ başlık dosyasında tek tanımlama kuralını _(ODR)_ çiğneyen bir tanımlama var mı?  
  
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
  + görsel olarak 0 ile karıştırılma riski olan o karakteri kullanılmış mı?
  + fonksiyon isimleri iyi seçilmiş mi?

## Sabitler (constants)
  + nullptr
    + nullptr yerine NULL makrosu kullanılmış mı?
    + nullptr yerine tam sayı sabiti olarak 0 kullanılmış mı?
    
## Numaralandırmalar (enums)
+ kapsamlı enum türü _(enum class)_ yerine kapsamsız enum türü kullanılmış mı?
+ isimlendirilmemiş enum türü kullanılmış mı?
+ gereksiz yere numaralandırma sabitlerinin değerleri belirlenmiş mi?

## Fonksiyonlar
+ fonksiyon ismi iyi seçilmiş mi?
  + verilen ismi  yeterince betimleyici mi?
+ fonksiyonlara birden fazla görev yüklenmiş mi?
  + küçük birden fazla fonksiyon yerine tek bir (uzun) fonksiyon tanımlanmış mı? 
+ kullanılmayacak parametreler (gereksiz yere) isimlendirilmiş mi?
+ fonksiyon parametre sayısı fazla mı?

## Argüman Gönderimi (Parameter Passing)

## Lambda İfadeleri (Lambda Expressions)
+ lambda ifadesinin kullanılması gereken (daha iyi olan) yerlerde global fonksiyon tanımlanmış mı?

  
## Kapsam ve Kapsam Sızıntısı (Scope & Scope Leakage)
+ yerel bir isim global bir ismi maskeliyor mu?
+ yerel bir isim sınıf kapsamındaki bir ismi maskeliyor mu?
+ değişken isimlerinin kapsamları gereksiz yere geniş tutulmuş mu?
+ gereken yerlerde kapsam daraltılması için ilk değer vermeli if deyimi _(if with initializer)_ kullanılmış mı?
+ gereken yerlerde "yapılandırılmış bağlama" _(structured binding)_ kullanılmış mı?

## Taşıma Semantiği (Move Semantics) 
  + Sınıfın move member'ları delete edilmiş mi?

## Kopyalamanın Eliminasyonu (Copy Elision)

## Sınıflar (Classes)
+ Oluşturulan sınıf cohesive mi?
+ Tek sorumluluk _(Single Responsibility Principle)_ ilkesine uyulmuş mu?

## Exception Handling
+ sınıfların move constructor, move assignment, swap işlevleri _noexcept_ olarak tanımlanmış mı?

## Akıllı Göstericiler (Smart Pointers)

## Attribute'lar 
+ geri dönüş değerinin kullanılması lojik açıdan zorunlu olan fonksiyonlar için _[[nodiscard]]_ attribute'ı kullanılmış mı?
+ switch deyimlerinde gerekli yerlerde _[[fallthrough]]_ attribute'ı kullanılmış mı?

