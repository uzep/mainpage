---
layaout: default
title: Entegrasyon
author: ozmen
---
# Entegrasyon

Üniveriste Yönetim Sistemi (ÜYS) ile UZEP entegrasyonu için iki yol bulunmaktadır: 1) ÜYS ile UZEP arasında sağlanan web servislerini kullanmak, diğeri ise kayıtların ÜYS'den dosyaya (Excel) indirilip, gerekli düzenlemeleri yaptıktan sonra UZEP'e yüklemek şeklindedir. 

2020 Güz döneminde entegrasyon Excel dosya üzerinden sağlanacaktır. Sorunsuz bir veri aktarımı için Excel dosyalarındaki verilerin UZEP'in beklediği biçimde olması gerekmektedir. UZEP veri akatarımı arayüzünde (bkz. Şekil 1) örnek Excel dosyalar bulunmaktadır. Bu örnek dosyalar sistemin beklediği şekilde biçimlendirilmiştir, dolayısı ile önce bu dosyalar indirilmeli, ÜYS'den indirilen veriler buraya kopyalanarak entegrasyon yapılmalıdır.  

**Entegrasyon için aktarılması gereken veriler şunlardır:** <br> 
**1. Birimler:** Üniversite hiyerarşisi içinde Fakülte, Meslek Yüksek Okulları (MYO), Enstitüler ve bunların altındaki bölümler ve programlar birimler olarak adlandırılmıştır. <br>
**2. Dersler:** Üniversitenin tüm birimlerinde tanımlı ve bölümlerin ders planlarında yer alan dersler.<br>
**3. Kullanıcılar (yöneticiler, öğrenciler, öğretim elemanları):** Üniversitede ders veren öğretim elemanları ve kayıtlı öğrenciler. İstenirse dışarıdan davetli de derse katılabilir, bunun için bireysel olarak kullanıcı eklenmesi gerekmektedir. <br>
**4. Ders takvimi:** Üniversite bölümlerinin haftalık ders programları. Ders programlarının sanal ders programı ile aynı olması gerekmez. Sisteme örgün bir program girilebilir, sanal dersler bu programa uygun veya farklı yerlerde icra edilebilir. <br>
**5. Ders katılımcıları:** Sanal derslere tanımlanan kullanıclar, öğrenciler ve öğretim elemanları. <br>

<img style="border:1px solid black" src="assets/images/veriAktarim.png"/>  
<p style="text-align: center;">Şekil 1. Excel dosyalar ile entegrasyon arayüzü. </p>

**Entegrasyon işlem basamakları:**
1. Entegrasyonu doğru bir şekilde yapabilmek için  UZEP'in "veri akatarımı" arayüzündeki örnek dosyaları indirin.
2. Dosyalar içindeki ilk satırı (başlık satırını) koruyarak diğer verileri silin.
3. Üniveriste Yönetim Sisteminden (ÜYS) indirdiğiniz verileri başka bir Excel sayfasında hazır edin.
4. Hazır edilen verileri kontrol ettikten sonra (gerekiyorsa düzenleme yaparak) UZEP'ten indirilen sayfaya, kolonları gözeterek yapıştırın.
5. Excel dosyayı **İçeri Aktar** butonunu kullanarak UZEP'e yükleyin.
6. **Tümünü Sil** butonu kullanılarak herhangi bir bölümün verisi tamamen silinebilir. Bu buton eylemi geri alınamaz, bu nedenle kullanılmadan önce mutlaka veriler yedeklenmelidir.

Tüm veriler aktarıldığında UZEP dönem için kullanıma hazır olacaktır. Bu noktadan sonra tekil değişiklikler UZEP-Yönetici arayüzlerinden yapılabilir.

### Entegrasyon için aktarılacak veriler hakkında açıklayıcı bilgiler:

### Birimler Dosyası:

<img style="border:1px solid black" src="assets/images/birim.png"/> 
<p style="text-align: center;">Şekil 1. Birimler dosyası biçimi (Fakülteler, MYO'lar, Enstitüler ve bu birimlerin altında bulunan bölümler/programlar). </p> <br>

**Tabloya ait açıklamalar:**<br>

**DepartmentExternalId:** Üniversitedeki bir bölüm/programın numarasıdır. Buraya girilen sayı tüm üniversite içinde tekil (ayırdedici) olmalı ve Excel tabloya **sayı** olarak girilmelidir.<br>

**FacultyName:** Bölüm/programın bağlı olduğu fakülte/enstitü veya MYO adı. Excel tabloya **metin** olarak girilmelidir.<br>

**DepartmentName:** Bölüm/program adı. Excel tabloya **metin** olarak girilmelidir.<br><br>

### Dersler dosyası:

<img style="border:1px solid black" src="assets/images/dersler.png"/> 
<p style="text-align: center;">Şekil 2. Dersler dosyası biçimi (Baz dersler ve şube dersler). </p><br>

**Tabloya ait açıklamalar:**<br>

**BaseCourseDepartmentExternalId:** Baz (temel) dersin bağlı olduğu birim/bölüm/program kodudur. Buraya girilecek olan sayı, mutlaka Şekil 1'de gösterilen tabloda tanımlı olmalıdır. Örneğin, Makine Mühendisliği bölümüne bağlı Mukavemet baz dersi için buraya Makine Mühendisliği bölümünün kodu girilmelidir. Benzer şekilde, aynı fakültede bir başka Mukavemet dersi İnşaat Mühendisliği Bölümünde olabilir, bu durumda bu iki dersi birbirinden ayırmak için bölüm kodları farklı olmalıdır. Şekil 2.'deki örnekte _456_ numaralı bölüme bağlı _Sistem Yöneticiliği_ dersi görülmektedir. _456_ numaralı bölüm örneğin _Bilişim Sistemleri Mühendisliği_ bölümüdür. Bu Excel tabloda aynı bölüme ait çok sayıda baz ders olabilir, bu derslerin hepsinin bölüm kodu aynı olacaktır. Aynı tabloya tüm fakültenin veya tüm üniversitenin baz dersleri konulabilir. Her bölümün dersleri ayrı dosyalarda tutuluyorsa, bu dosyalar ayrı ayrı sisteme yüklenebilir. Benzer şekilde, tüm dersler bir dosyada toplandıysa, tüm üniversitenin dersleri bir kerede UZEP'e yüklenebilir. Excel tabloda bu kolon **sayı** veya **metin** olarak biçimlendirilebilir.<br>

**BaseCourseExternalId:** Baz dersin ayırdedici numarasıdır ve üniversitedeki baz dersler içinde tekil olmalıdır. Baz dersler Eğitim Bilgi Sisteminde (EBS) var olan ders planlarındaki derslerdir. Bazı baz dersler fakültede tekil olabilir, örneğin Matematik dersi gibi. Bazı dersler de tüm üniversitede tekil olabilir, örneğin Türkçe gibi. Dolayısıyla, sisteme işlenecek her bir baz dersin mutlaka ayırdedici bir kodu olmalıdır. Benzer şekilde baz dersten türetilen şube derslere de baz ders kodundan farklı kodlar verilmelidir. Excel tabloya **sayı** veya **metin** olarak girilebilir. <br>

**BaseCourseName:** Baz (temel) dersin adıdır. Bölüm ders planlarındaki derslerin adlarıdır. Baz ders ile şube derslerin adları genelde aynı olur (zorunlu değil).<br>

**CourseDepartmentExternalId:** Baz dersten türetilen şube dersin açılacağı bölümün kodudur. Örneğin baz ders üniversite ölçeğinde bir ders _Türkçe_ olsun. Bu ders Bilgisayar Mühendisliği bölümünde açılmak istenirse, bölümün kodu buraya girilmlidir. Şekil 2.'deki örnekte Bilişim Sistemleri Mühendisliği Bölümünün kodu _456_ dır, yani baz ders ve şube ders aynı bölüme bağlıdır. Excel tabloya **sayı** veya **metin** olarak girilebilir.<br>

**CourseExternalId:** Şube dersin ayırdedici kodudur. Şube ders kodu, baz ders kodundan farklı olmalıdır (ders tek şube açılmışsa aynı olabilir). Üniversitede açılan tüm şube derslerin kodu birbirinden farklı olmalıdır. Şekil 2.'deki örnekte Bilişim Sistemleri Mühendisliği bölümünde yürütülecek _Sistem Yöneticiliği_ dersinin şube kodu _9976_ olarak girilmiştir. Bu dersten bir B şubesi daha açılmak istenirse, yeni şubenin kodu mutlaka farklı olmalıdır. Excel tabloya **sayı** veya **metin** olarak girilebilir.<br>

**CourseCode:** Dersin EBS ders planında görünen ve bilinen kodu, örneğin _MAT101_ gibi. Excel tabloya metin biçiminde girilmelidir.<br>

**CourseName:** Şube dersin adıdır, genelde baz ders adı ile aynıdır (olmak zorunda değil). Şube dersler genelde bir dersin A şubesi, B şubesi veya sabah şubesi, gece şubesi diye bilinir. Örneğin _Matematik_ dersi için 4 şube açılsa, tüm şube derslerinin adları da yine baz dersin adı, yani _Matematik_ olur. Ancak bazen farklı durumlar da olabilir: Örneğin, yabancı dil baz dersin adı _İngilizce_ iken şube derslerinin adları _İngilizce (Başlangıç)_, _İngilizce (Orta)_ ve _İngilizce (İleri)_ olabilir. Sistem her iki durumu da tanımlamaya uygundur.<br><br>

### Kullanıcılar dosyası:

<img style="border:1px solid black" src="assets/images/kullanicilar.png"/> 
<p style="text-align: center;">Şekil 3. Kullanıcılar dosyası (Yöneticiler, öğretim elemanları ve öğrenciler). </p><br>

**Tabloya ait açıklamalar:**<br>

**Username:** Kullanıcı adıdır. Excel tabloya Üniversite Yönetim Sistemindeki (ÜYS) kullanıcı adı girilebilir (tavsiye edilir). Sistem açısından herhangi bir sorun olmamakla beraber, kullanıcı adı olarak TC numarasının seçilmesi önerilmez. Öğretim elemanı UZEP üzerinden sınıf listesi alıp bir yerlerde yayınladığında KVKK açısından sıkıntı oluşturabilir.<br>

**Name:** Kullanıcının ilk adıdır. İki ya da daha çok ismi olanlar için Excel tabloya iki veya daha fazla kelime girilebilir.<br>

**Surname:** Kullanıcının soyadı.<br>

**Email:** Kullanıcının email adresi. <br>

**SocialNumber:** Kullancıının TC numarası veya herhangi bir numara girilebilir. Tekil olmak zorunda değildir.<br> 

**Password:** Kullanıcıya verilen geçici şifredir, ilk girişte kullanıcı tarafından değişitirilmelidir (sistem değişim için uyarı mesajı verir).<br>

**Role:** Kullanıcıya verilen roldür, UZEP üzerindeki kaynaklara (verilere) erişimi denetlemek için kullanılır. UZEP'te tanımlı roller _Süper Yönetici_, _Yönetici_, _İstatistik Bilgi_, _Öğretim elemanı_ ve _Öğrenci_ şeklindedir. Excel dosya ile topluca kullanıcı tanımlamada her kullanıcının rolü tabloya girilmelidir. Yöneticiler arayüz üzerinden tekil kullanıcı tanımlandığında rolsüz oluşmaktadır. Bu durumda ayrıca kullanıcıya rol tanımlanmalıdır.<br><br>

### Takvim dosyası:

<img style="border:1px solid black" src="assets/images/hprog.png" height="400"/> 
<p style="text-align: center;">Şekil 4. Ders takvimi dosya biçimi (Haftalık ders programları). </p><br>

**Tabloya ait açıklamalar:**<br>

**CourseExternalId:** Sanal sınıf takvimi girilecek şube dersin kodudur. Şube ders ile ilgili açıklamalar yukarıda Şekil 2 nin altında verilmiştir.<br>

**Start:** Sanal dersin başlama tarihi ve zamanıdır.<br>

**End:** Sanal dersin bitiş tarihi ve zamanıdır.<br>

**Username:** Dersin öğretim elemanıdır. Eğer dersi yürüten birden fazla öğretim elemanı varsa, ders için oluşturulan _Takvim_ satırları kopyalanıp aynı Excel dosyanın altına ilave edilmelidir. Kopyalanan satırlarda tek değişen kısım _Username_ kısmı olacaktır. Buraya ikinci öğretim elemanının kullanıcı adı yazılmalıdır. Derse daha fazla öğretim elemanı ilave edilecekse işlem her bir öğretim elemanı için tekrarlanmalıdır. Örneğin misafir bir öğretim elemanı sadece bir oturuma katılacaksa, o durumda bu dosyaya sadece bir satır ilave edilmelidir.<br><br>

### Katılımcılar dosyası:

<img style="border:1px solid black" src="assets/images/dersKullanici.png"/> 
<p style="text-align: center;">Şekil 5. Ders katılımcıları dosyası biçimi (Derslere kaydolmuş öğrenciler veya öğretici olarak görevlendirilmiş öğretim elemanları). </p><br>

**Tabloya ait açıklamalar:**<br>

**Username:** Derse katılacak öğrencinin kullanıcı adıdır. <br>

**CourseExternalId:** Şube dersin kodu. Şube ders ile ilgili açıklamalar yukarıda Şekil 2.'nin altında verilmiştir.<br>

**EnumCourseUserType:** Derse katılan kişinin öğrenci veya öğretmen olduğu bilgisidir. Örneğin; 0: Öğretmen, 1: Öğrenci gibi. <br>

**MetaData:** Derse katılanlar (öğretmen, öğrenci veya misafir olabilir) ile ilgili ilave bilgi girişi için ayrılmış bir alandır. Örneğin, iki şube dersin birleştirilmesi ile yeni bir şube oluşturulabilir. Bu durumda, derse katılan öğrencilerin hangi şubeden (veya bölümden) geldiklerini ayrıştırmak için kullanılabilir, yani öğrencinin bölüm kodu burada kullanılabilir. Bu kısım tamamen serbest olarak kullanılabilir, Excel dosyada **sayı** veya **metin** biçiminde olabilir. <br><br>


## İki veya daha fazla şubenin birleştirilmesi:

İki veya daha şubede bulunan öğrenciler tek bir şubede birleştirilebilir. Bunun için şu işlemler yapılmalıdır:
1. Birleştirilecek şube dersler için aynı baz ders altında yeni bir şube ders oluşturulur. Farklı baz dersler altındaki şubeler de birleştirilebilir. Bu durumda her hangi bir baz ders altında yeni bir şube ders oluşturulur.
2. Şekil 5.'teki gibi yeni bir Excel dosyaya birleştirilmek istenen derslerdeki öğrenciler (varsa öğretim elemanları) eklenir. 
3. Excel dosyada "CourseExternalId" altına yeni oluşturulan dersin kodu girilir (tüm öğrencilerin toplancağı dersin kodu). 
4. "MetaData" kolonuna ise öğrencilerin şube kodu veya öğrenciler farklı bölümlerden geliyorsa bölüm kodu girilebilir. Bu bilgi öğrencilerin nerden geldiğini bulmak için kullanılabilir. 

