## Başlık Dosyaları (Header Files)
+ gereksiz yere bir başlık dosyası include edilmiş mi?
  + ön bildirim _(forward declaration)_ yapmak yerine gereksiz yere başlık dosyası include edilmiş mi?
+ başlık dosyasında _using bildirimi_ var mı?
+ başlık dosyasında _using namespace direktifi_ var mı?
+ başlık dosyasında tek tanımlama kuralını _(ODR)_ çiğneyen bir tanımlama var mı?  

## Önişlemci (Preprocessor)
+ Koşullu derleme komutları _(conditional compiling)_ dışında makrolar kullanılmış mı?
  + sembolik sabit olarak makro kullanılmış mı?
  + fonksiyonel makrolar _(functional macro)_ kullanılmış mı?

## Değişken Bildirimleri
+ Aritmetik türlerden ya da pointer türlerinden İlk değer verilmeden tanımlanan değişkenler var mı?
  
## Const Doğruluğu (Const Correctness)
+ değişkenler varsayılan biçimde _(default)_ const olarak tanımlanmış mı?
+ salt okuma _(read-only access)_ amaçlı kullanılacak değişkenler const yapılmış mı?
  + lookup table olarak kullanılan veri yapıları const yapılmış mı?
  + okuma amaçlı erişim sağlayan referans parametreler const yapılmış mı?
  + gösterici değişkenler
    + low level const olması gerekenler
    + top level const olması gerekenler
  + aralık tabanlı for döngülerinde döngü değişkeni olarak kullanılan sol taraf referansları const yapılmış mı?
  + const olması gereken üye fonksiyonları const yapılmış mı?

## constexpr & consteval
+ Derleme zamanında hesaplanabilecek değerler için _constexpr_ fonksiyonlar kullanılmış mı?
+ Derleme zamanında hesaplanması gereken değerler için _consteval_ fonksiyonlar _(C++20)_ kullanılmış mı?

## Yorum satırları (Comment Lines)
+ gereksiz yorum satırı var mı?
+ güncellenmesi _(update)_ gereken yorum satırı var mı?
+ yorum satırları gereksiz yere uzun tutulmuş mu?
       
## İsimlendirme (Naming)
+ isimler anlaşılır mı?
+ Türkçe isim kullanılmış mı?
+ isimlendirmede tutarlı bir konvensiyon kullanılmış mı?
+ birbirine çok yakın isimler seçilmiş mi? (x1, x2, x3)
+ görsel olarak 0 ile karıştırılma riski olan o karakteri kullanılmış mı?
+ fonksiyon isimleri iyi seçilmiş mi?
+ tamamı büyük harf olan _(all caps)_ isimler kullanılmış mı?
+ isimlerde gereksiz ön ekler kullanılmış mı?

## Sabitler (constants)
 + nullptr yerine NULL makrosu kullanılmış mı?
 + nullptr yerine tam sayı sabiti olarak '0' kullanılmış mı?
 + tam sayı ve gerçek sayı sabitlerinin türü doğru seçilmiş mi?
 + isimlendirilmesi gereken sabitler isimsiz olarak kullanılmış mı?
    
## Numaralandırmalar (enums)
+ kapsamlı enum türü _(enum class)_ yerine kapsamsız enum türü kullanılmış mı?
+ isimlendirilmemiş _enum_ türü kullanılmış mı?
+ gereksiz biçimde numaralandırma sabitlerinin değerleri belirlenmiş mi?
+ gereksiz biçimde baz tür _(underlying type)_ belirlenmiş mi?
+ numaralandırma sabitleri tamamı büyük harf _(all caps)_ isimlendirilmiş mi?

## Operatörler (Operators)

## Kontrol Deyimleri (Control Statements)
+ STL algoritmaları yerine ham döngü deyimleri _(raw loops)_ kullanılmış mı? 
+ gereksiz _do while_ döngüsü kullanılmış mı?
+ aralık tabanlı for döngü deyimleri _(range-based for loop)_ yerine geleneksel _for_ döngü deyimi kullanılmış mı?
+ gereksiz _goto_ deyimi kullanılmış mı?
+ _switch_ deyimlerinde gereksiz _default_ case kullanımı var mı?

## Tür Dönüşümleri ve Tür Dönüştürme Operatörleri

## İsim Alanları (Namespaces)
+ global fonksiyonlar namespace içinde mi?

## Fonksiyonlar
+ fonksiyon ismi iyi seçilmiş mi?
+ verilen ismi  yeterince betimleyici mi?
+ fonksiyonlara birden fazla görev yüklenmiş mi?
+ küçük birden fazla fonksiyon yerine tek bir (uzun) fonksiyon tanımlanmış mı? 
+ kullanılmayacak parametreler (gereksiz yere) isimlendirilmiş mi?
+ fonksiyon parametre sayısı fazla mı?
+ variadic fonksiyon tanımlanmış mı?
+ fonksiyon parametreleri için _strong type_ yerine doğrudan tam sayı türleri kullanılmış mı?
+ uzun kod satırlarına sahip (10 satırdan fazla) _inline_ fonksiyonlar tanımlanmış mı?

## Fonksiyon Yüklemesi (Function Overloading)

## Argüman Gönderimi (Parameter Passing)

## Operatör Yüklemesi (Operator Overloading)
+ operatör yüklemeleri anlaşılır ve kolay kullanılabilir mi _(intuitive)_?
+ aritmetik operatörler yüklenmiş ancak işlemli atama operatörleri yüklenmemiş mi?
+ karşılaştırma operatörleri için _three way comparison (C++20)_ kullanılmış mı?
+ programcı türleri(user defined types)_ için önek ++ operatör fonksiyonu yerine sonek ++ operatörü kullanılmış mı?

## Lambda İfadeleri (Lambda Expressions)
+ lambda ifadesinin kullanılması gereken (daha iyi olan) yerlerde global fonksiyon tanımlanmış mı?
  
## Kapsam ve Kapsam Sızıntısı (Scope & Scope Leakage)
+ Değişkenler ilk kullanıldıkları yerde tanımlanmış mı?
+ yerel bir isim global bir ismi maskeliyor mu?
+ yerel bir isim sınıf kapsamındaki bir ismi maskeliyor mu?
+ değişken isimlerinin kapsamları gereksiz yere geniş tutulmuş mu?
+ gereken yerlerde kapsam daraltılması için ilk değer vermeli if deyimi _(if with initializer)_ kullanılmış mı?
+ gereken yerlerde "yapılandırılmış bağlama" _(structured binding)_ kullanılmış mı?

## Tür Çıkarımı (Type Deduction)

## Taşıma Semantiği (Move Semantics) 
+ sınıfın move member'ları delete edilmiş mi?
+ return ifadesinde std::move işlevi çağrılmış mı?

## Kopyalamanın Eliminasyonu (Copy Elision)

## Sınıflar (Classes)
+ oluşturulan sınıf cohesive mi?
+ veri gizleme ilkelerine uyulmuş mu?
+ tek sorumluluk _(Single Responsibility Principle)_ ilkesine uyulmuş mu?
+ üye fonksiyonlar
  + const olması gereken üye fonksiyonlar const yapılmış mı?
  + üye fonksiyon içinde gereksiz yere (sık tekrarlanan) _this_ kullanımı var mı?
  + üye fonksiyon içinde _if (this == nullptr)_ sınaması var mı?

## Exception Handling
+ sınıfların move constructor, move assignment, swap işlevleri _noexcept_ olarak tanımlanmış mı?
+ _catch_ bloklarının sırası doğru mu? (özelden genele)
+ verilmemesi gereken _noexcept_ garantisi verilmiş mi?
+ kod tekrarı yerine exception handling fonksiyonları _(lippincott functions)_ kullanılmış mı?

## Akıllı Göstericiler (Smart Pointers)
+ new ve delete operatörleri doğrudan kullanılmış mı?
+ dinamik ömürlü nesneler ham göstericiler _(raw pointers)_ ile kullanılmış mı?

## Attribute'lar 
+ geri dönüş değerinin kullanılması lojik açıdan zorunlu olan fonksiyonlar için _[[nodiscard]]_ attribute'ı kullanılmış mı?
+ switch deyimlerinde gerekli yerlerde _[[fallthrough]]_ attribute'ı kullanılmış mı?

## Concurrency

## Diğer Konular ve Araçlar (Miscellaneous)

