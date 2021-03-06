## Başlık Dosyaları (Header Files)
+ gereksiz yere bir başlık dosyası include edilmiş mi? _(gereksiz başlık dosyalarının include edilmesinden kaçınılmalı)_ 
  + ön bildirim _(forward declaration)_ yapmak yerine gereksiz yere başlık dosyası include edilmiş mi?
+ başlık dosyasında olmaması gereken _using bildirimi_ var mı? _(başlık dosyalarında using bildirimi olmamalı namespace üyesi isimler başlık dosyalarında nitelenerek kullanılmalı)_
+ başlık dosyasında olmaması gereken _using namespace direktifi_ var mı? _(başlık dosyalarında using namespace bildirimi olmamalı namespace üyesi isimler başlık dosyalarında nitelenerek kullanılmalı)_
+ başlık dosyasında tek tanımlama kuralını _(ODR)_ çiğneyen bir tanımlama var mı?  _(tek tanımlama kurallarına uyulmalı)_

## Önişlemci (Preprocessor)
+ Koşullu derleme komutları _(conditional compiling)_ dışında makrolar kullanılmış mı? _(makro kullanımından kaçınmak gerekiyor)_
  + sembolik sabit olarak makro kullanılmış mı? _(makro kullanımından kaçınmak gerekiyor)_
  + fonksiyonel makrolar _(functional macro)_ kullanılmış mı? _(makro kullanımından kaçınmak gerekiyor)_

## Değişken Bildirimleri
+ Aritmetik türlerden ya da pointer türlerinden ilk değer verilmeden tanımlanan değişkenler var mı? _(akis yönde bir zorunluluk olmadıkça değişkenlere ilk değer verilmeli)_
  
## Const Doğruluğu (Const Correctness)
+ değişkenler varsayılan biçimde _(default)_ _const_ olarak tanımlanmamış mı? _(default olarak parametre değişkenleri dışındaki değişkenler const olmalı)_
+ salt okuma _(read-only access)_ amaçlı kullanılacak değişkenler const yapılmamış mı?
  + arama tablosu _(lookup table)_ olarak kullanılan veri yapıları _const_ yapılmamış mı?
  + okuma amaçlı erişim sağlayan referans parametreler _const_ yapılmamış mı?
  + gösterici değişkenlerin tanımında gereken yerlerde _const_ anahtar sözcüğü kullanılmış mı?
    + low level const olması gerekenler low level const yapılmış mı?
    + top level const olması gerekenler top level const yapılmış mı?
  + aralık tabanlı for döngülerinde okuma amaçlı kullanılacak döngü değişkeni olarak kullanılan sol taraf referansları const yapılmamış mı?
  + _const_ olması gereken üye fonksiyonları _const_ yapılmamış mı?

## constexpr & consteval
+ Derleme zamanında hesaplanabilecek değerler için _constexpr_ olmayan fonksiyonlar kullanılmış mı?
+ Derleme zamanında hesaplanması gereken değerler için _consteval_ olmayan fonksiyonlar _(C++20)_ kullanılmış mı?

## Yorum satırları (Comment Lines)
+ gereksiz yorum satırı var mı? _(gereksiz yorum satırlarından kaçınmak gerekiyor)_
  + kodun açık ve net olduğu yerlerde _(selfexplanatory)_ açıklama satırları kullanılmış mı? _(gereksiz yorum satırlarından kaçınmak gerekiyor)_
+ güncellenmesi _(update)_ gereken yorum satırları güncellenmemiş mi?
+ yorum satırları gereksiz yere uzun tutulmuş mu? _(uzun açıklamalardan kaçınılmalı)_
+ değişken bildirimleri için açıklama satırı var mı? _(değişken bildirimleri için açıklama yapılmış ise muhtemelen kötü isimlendirme söz konusudur)_
+ _debug_ amaçlı _comment out_ yapılmış kodlar kaynak dosyada bırakılmış mı?
       
## İsimlendirme (Naming)
+ anlaşılmaz isimler kullanılmış mı? _(isimler anlaşılır ve betimleyici olmalı)_
+ Türkçe isim kullanılmış mı? _(isimler Türkçe olmamalı)_
+ isimlendirmede tutarlı biçimde bir konvensiyon kullanılmamış mı? 
+ birbirine çok yakın isimler seçilmiş mi? _(x1, x2, x3 gibi)_
+ görsel olarak _0_ ile karıştırılma riski olan _'o'_ karakteri kullanılmış mı?
+ fonksiyon isimleri fonksiyonun yaptığı işe betimlemiyor mu?
+ tamamı büyük harf olan _(all caps)_ isimler kullanılmış mı? _(all caps isimler kullanılmamalı)_ 
+ isimlerde gereksiz ön ekler kullanılmış mı?
+ standart kütüphane tarafından rezerve edilmiş isimler kullanılmış mı?

## Sabitler (constants)
+ _nullptr_ yerine _NULL_ makrosu kullanılmış mı? _(NULL makrosu kullanılmamalı)_
+ _nullptr_ yerine tam sayı sabiti olarak _0_ kullanılmış mı? _(nullptr sabiti kullanılmalı)_
+ tam sayı ve gerçek sayı sabitlerinin türü doğru seçilmiş mi?
+ isimlendirilmesi gereken sabitler isimsiz olarak kullanılmış mı? _(özel anlama sahip sabitler isimlendirilmeli)_
+ büyük tam sayı sabitlerinin yazımında basamak ayıracı _(digit separator)_ kullanılmamış mı? _(kodun kolay okunması için basamak ayraçları kullanılmalı)_ 
    
## Numaralandırmalar (enums)
+ kapsamlı enum türü _(enum class)_ yerine kapsamsız enum türü kullanılmış mı? _(zorunlu durumlar dışında kapsamsız enum türlerinin kullanımından kaçınılmalı)_
+ isimlendirilmemiş bir _enum_ türü kullanılmış mı? _(kodun kolay okunması için enum türleri isimlendirilmeli)_
+ gereksiz biçimde numaralandırma sabitlerinin değerleri belirlenmiş mi? _(gerekmiyorsa tüm numara sabitleri varsayılan değerlere sahip olmalı)_
+ gereksiz biçimde baz tür _(underlying type)_ belirlenmiş mi? _(gerekmedikçe baz tür belirtilmemeli)_
+ numaralandırma sabitleri tamamı büyük harf _(all caps)_ isimlendirilmiş mi? _(all caps isimlerden kaçınılmalı)_

## İfadeler ve Operatörler (Expressions & Operators)
+ karmaşık ve fazla sayıda operatör içeren ifadelerde öncelik parantez(ler)i kullanılmamış mı? _(uzun ve karmaşık ifadelerin okunmasını kolaylatırmak ve kodlama hatalarından kaçınmak için öncelik parantezleri kullanılmalı)_

## Kontrol Deyimleri (Control Statements)
+ _STL_ algoritmaları yerine ham döngü deyimleri _(raw loops)_ kullanılmış mı? _(ham döngülerden mümkün olduğunca kaçınılmalı)_
+ gereksiz _do while_ döngüsü kullanılmış mı? _(do while döngü deyimleri kod okumayı zorlaştırıyor ve hata yapma riskini arttırıyor. Gerekli durumların haricinde do while döngülerinden kaçınılmalı)_
+ aralık tabanlı for döngü deyimleri _(range-based for loop)_ yerine geleneksel _for_ döngü deyimi kullanılmış mı?
+ gereksiz _goto_ deyimi kullanılmış mı?
+ _switch_ deyimlerinde gereksiz _default_ case kullanımı var mı?

## Tür Dönüşümleri ve Tür Dönüştürme Operatörleri

## İsim Alanları (Namespaces)
+ global fonksiyonlar _namespace_ içinde değil mi? _(isim çakışmalarına karşı önlem almak için global fonksiyonlar bir namespace içinde olmalı)_
+ isim alanları isimleri tamamı küçük harf mi _(all lower case)_ ? 

## Fonksiyonlar
+ fonksiyon ismi iyi seçilmiş mi?
+ verilen isim yeterince betimleyici değil mi?
+ fonksiyonlara birden fazla görev yüklenmiş mi? _(fonksiyonların tek bir görevi olmalı, bir fonksiyona birden fazla görev yüklenmemeli)_
+ küçük birden fazla fonksiyon yerine tek bir (uzun) fonksiyon tanımlanmış mı? _(uzun fonksiyonlardan kaçınılmalı, hata yapma riski artıyor, kod değişikliği yapmak ve test etmek zorlaşıyor)_
+ kullanılmayacak parametreler (gereksiz yere) isimlendirilmiş mi? _(kullanılmayacak [dummy] parametrler isimlendirilmemeli)_
+ fonksiyon parametre sayısı fazla mı? _(parametre sayısı minimize edilmeli, fazla parametreye sahip fonksiyonlara yapılan çağrılarda hata riski artıyor)_
+ _variadic_ fonksiyon tanımlanmış mı? _(variadic fonksiyonlar yerine variadic template(ler) kullanılmalı)_
+ fonksiyon parametreleri için _strong type_ yerine doğrudan tam sayı türleri kullanılmış mı?
+ uzun kod satırlarına sahip (10 satırdan fazla) _inline_ fonksiyonlar tanımlanmış mı? _(uzun inline fonksiyonlar tipik olarak bir avantaj sağlamıyor)_
+ geri dönüş değeri adres türlerinden olan fonksiyonlar var mı? _(adres döndüren fonksiyonlar hata riskini arttırıyor)_

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
+ değişkenler ilk kullanıldıkları yerde _(yere yakın)_ tanımlanmamış mı? _(değişken isimlerinin kapsamı mümkün olduğunca daraltılmalı)_
+ yerel bir isim global bir ismi maskeliyor mu? 
+ yerel bir isim sınıf kapsamındaki bir ismi maskeliyor mu?
+ değişken isimlerinin kapsamları gereksiz yere geniş tutulmuş mu?
+ gereken yerlerde kapsam daraltılması için ilk değer vermeli if deyimi _(if with initializer)_ kullanılmamış mı?
+ gereken yerlerde "yapılandırılmış bağlama" _(structured binding)_ kullanılmamış mı?

## Tür Çıkarımı (Type Deduction)

## Taşıma Semantiği (Move Semantics) 
+ sınıfın _move member_'ları _delete_ edilmiş mi? _(move memberler delete edilmemeli)_
+ _return_ ifadesinde _std::move_ işlevi çağrılmış mı? _(copy elision ya da derleyici optimizasyonu devre dışı bırakılmış olabilir)_

## Kopyalamanın Eliminasyonu (Copy Elision)

## Sınıflar (Classes)
+ oluşturulan sınıf _cohesive_ mi?
+ veri gizleme ilkelerine uyulmuş mu?
+ tek sorumluluk _(Single Responsibility Principle)_ ilkesine uyulmuş mu?
+ üye fonksiyonlar
  + _const_ olması gereken üye fonksiyonlar _const_ yapılmış mı?
  + üye fonksiyon içinde gereksiz yere (sık tekrarlanan) _this_ kullanımı var mı?
  + üye fonksiyon içinde _if (this == nullptr)_ sınaması var mı?

## Exception Handling
+ sınıfların _move constructor_, _move assignment_, _swap_ işlevleri _noexcept_ olarak tanımlanmış mı?
+ _catch_ bloklarının sırası doğru mu? (özelden genele)
+ verilmemesi gereken _noexcept_ garantisi verilmiş mi?
+ kod tekrarı yerine _exception handling_ fonksiyonları _(lippincott functions)_ kullanılmış mı?

## Akıllı Göstericiler (Smart Pointers)
+ _new_ ve _delete_ operatörleri doğrudan kullanılmış mı?
+ dinamik ömürlü nesneler ham göstericiler _(raw pointers)_ ile kullanılmış mı?

## Attribute'lar 
+ geri dönüş değerinin kullanılması lojik açıdan zorunlu olan fonksiyonlar için _[[nodiscard]]_ attribute'ı kullanılmış mı?
+ _switch_ deyimlerinde gerekli yerlerde _[[fallthrough]]_ attribute'ı kullanılmış mı?

## Concurrency

## STL
+ C dizisi _(C array)_ kullanılan yerler var mı? _(istisnai durumlar dışında std::array kullanılmalı) _

## Kod Yerleşimi (Code Layout)
+ kod yerleşiminde tutarlı ve istikrarlı şekilde bir konvensiyon kullanılmış mı?
+ genel kabul görmüş istisnalar dışında _80_ karakterden daha uzun kod satırı var mı?

## Diğer Konular ve Araçlar (Miscellaneous)
+ _deprecated_ dil ya da standart kütüphane öğeleri kullanılmış mı?

