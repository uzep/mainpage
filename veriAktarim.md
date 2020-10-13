---
layaout: default
title: Veri Akatrımı
author: ozmen
---
# Veri aktarımı

Üniveriste Yönetim Sistemi'nden (ÜYS) veri aktarımı için iki yol bulunmaktadır. Bunlardan birisi ÜYS ile UZEP arasında yapılan protokol ile sağlanan web servislerini kullanmak, diğeri ise kayıtların ÜYS'den dosyaya (Excel) indirilip, gerekli düzenlemeleri yaptıktan sonra UZEP'e yüklemek şeklindedir. Bu dönem veri aktarımı için Excel dosya üzerinden transfer yöntemi kullanılacaktır. Sorunsuz bir veri aktarımı için Excel dosyalarındaki verilerin UZEP'in beklediği biçimde olması gerekmektedir. UZEP veri akatarımı kısmında örnek Excel dosyalar bulunmaktadır. Bu örnek dosyalar sistemin beklediği şekilde biçimlendirilmiştir, dolayısı ile önce bu dosyalar indirilmelidir. ÜYS'den başka Excel dosyalara indirilen verileri kopyalayarak ve kolonları dikkatlice gözeterek bu dosyalara yapıştırmak veri transferi için en uygun yol olacaktır.  

**Aktarılacak veriler ve açıklamaları şöyledir:** <br> 
**1. Birimler:** Üniversite hiyerarşisi içinde Fakülte, Meslek Yüksek Okulları (MYO), Enstitüler ve bunların altındaki bölümler ve programlar birimler olarak adlandırılmıştır. <br>
**2. Dersler:** Üniversitenin tüm birimlerinde tanımlı ve bölümlerin ders planlarında yer alan dersler.<br>
**3. Kullanıcılar (yöneticiler, öğrenciler, öğretim elemanları):** Üniversitede ders veren öğretim elemanları ve kayıtlı öğrenciler. İstenirse dışarıdan davetli de derse katılabilir, bunun için bireysel olarak kullanıcı eklenmesi gerekmektedir. <br>
**4. Ders takvimi:** Üniversite bölümlerinin haftalık ders programları. Ders programlarının sanal ders programı ile aynı olması gerekmez. Sisteme örgün bir program girilebilir, sanal dersler bu programa uygun veya farklı yerlerde icra edilebilir. <br>
**5. Ders katılımcıları:** Sanal derslere tanımlanan kullanıclar, öğrenciler ve öğretim elemanları. <br>

Aktarılacak verilerin biçimleri örnek olarak aşağıdaki şekillerde verilmiştir.<br>

<br><img style="border:1px solid black" src="assets/images/birim.png"/> 
<p style="text-align: center;">Şekil 1. Birimler dosyası biçimi (Fakülteler, MYO'lar, Enstitüler ve bu birimlerin altında bulunan bölümler/programlar). </p> <br>

**DepartmentExternalId:** Bir bölüm/programın numarası, bu numara tüm üniversite içinde tekil (ayırdedici) olmalıdır. Excel tabloya **sayı** olarak girilmelidir.<br>

**FacultyName:** Bölüm/programın bağlı olduğu fakülte/enstitü veya MYO adı. Excel tabloya **metin** olarak girilmelidir.<br>

**DepartmentName:** Bölüm/program adı. Excel tabloya **metin** olarak girilmelidir.<br><br>

<img style="border:1px solid black" src="assets/images/dersler.png"/> 
<p style="text-align: center;">Şekil 2. Dersler dosyası biçimi (Baz dersler ve şube dersler). </p><br>

**BaseCourseDepartmentExternalId:** Baz (temel) dersin bağlı olduğu birim/bölüm numarası. Örneğin Mukavemmet dersi Makine bölümüne bağlı ise Makine bölüm numarası buraya girilmelidir. Şeki,ldeki örnekte _456_ numaralı bölüme bağlı _Sistem Yöneticiliği_ dersi görülmektedir. _456_ numaralı bölüm _Bilişim Sistemleri Mühendisliği_ bölümüdür. Bu tabloda aynı bölüme bağlı çok sayıda ders olabilir. Excel tabloya **metin** olarak girilmelidir.<br>

**BaseCourseExternalId:** Baz dersin ayırdedici numarası, bu numara baz dersler için tekil olmalıdır. Baz dersler Eğitim Bilgi Sisteminde (EBS) var olan derslerdir. Bazı baz derler fakültede tek olabilir, örneğin Matematik gibi. Bazı tersler de tüm üniversitede tek olabilir, örneğin Türkçe gibi. Dolayısıyla baz derslerin ayırdedici bir numarası olmalı, baz dersten türetilen şubelere ise farklı numaralar verilmelidir. Excel tabloya **metin** olarak girilmelidir. <br>

**BaseCourseName:** Baz (temel) dersin adı, genellikle baz ders ile şube dersler aynı isimlidir. Örneğin _Matematik_ dersi için 4 şube açılsa, herbir şubenin de adları yine _Matematik_ olacaktır. Ancak bazen farklı durumlar da olabilir: Örneğin baz dersin adı _İngilizce_ iken şube derslerin adları _İngilizce (Başlangıç)_, _İngilizce (Orta)_ ve _İngilizce (İleri)_ olabilir. <br>

**CourseDepartmentExternalId:** Baz dersten türetilen şubenin açılacağı bölüm kodu. Örneğin baz ders üniversite ölçeğinde bir ders _Türkçe_ olsun. Bu ders Bilgisayar Mühendisliği bölümünde açılmak istenirse, bölümün kodu buraya girilmlidir. Şekil 2.'deki örnekte Bilişim Sistemleri Mühendisliği Bölümünün kodu _456_ dır, baz ders ve şube dersin her ikisi de aynı bölüme bağlıdır. Excel tabloya **metin** olarak girilmelidir.<br>

**CourseExternalId:** Bir şube dersin ayırdedici kodu. Bu kod baz ders kodundan ayrı olarak verilmelidir. Üniversitede açılan tüm şube derslerin kodu farklı olmalıdır. Şekil 2.'deki örnekte Bilişim Sistemleri Mühendisliği bölümünde yürütülecek _Sistem Yöneticiliği_ dersinin şube kodu _9976_ olarak girilmiştir. Bu dersten bir B şubesi daha oluşturulsaydı, o dersin kodu bundan farklı olmalıdır. Excel tabloya **metin** olarak girilmelidir.<br>

**CourseCode:** Dersin bilinen kodu, örneğin _MAT101_ gibi. Excel tabloya metin biçiminde konulmalıdır.<br>

**CourseName:** Dersin adı, genelde baz ders adı ile şube ders adı aynıdır. <br><br>

<img style="border:1px solid black" src="assets/images/kullanicilar.png"/> 
<p style="text-align: center;">Şekil 3. Kullanıcılar dosyası (Yöneticiler, öğretim elemanları ve öğrenciler). </p><br>

**Username:** Kullanıcı adı. Üniversite Yönetim Sistemindeki (ÜYS) kullanıcı adı kullanılabilir. Sistem açısından herhangi bir sorun olmamakla beraber, kullanıcı adı olarak TC numarasının seçilmesi önerilmez. Öğretim elemanı sınıf listesi alıp yayınladığında KVKK açısından sıkıntı oluşturabilir.<br>
**Name:** Kullanıcının ilk adı. İki isimli olanlar için iki kelime veya daha fazlası olabilir.<br>
**Surname:** Kullanıcının soyadı.<br>
**SocialNumber:** Kullancıının TC numarası veya herhangi bir numara girilebilir. Tekil olmak zorunda değildir.<br> 
**Password:** Kullanıcıya verilen şifre. İlk kullanımda değişitirilir (değişitirilmelidir).<br>
**Role:** Kullanıcıya verilen rol. Sistemde tanımlı roller _Süper Yönetici_, _Yönetici_, _İstatistik Bilgi_, _Öğretim elemanı_ ve _Öğrenci_ şeklindedir. Arayüzler üzerinden kullanıcı tanımlandığında rolsüz olarak oluşmaktadır. Arayüz üzerinden tekil olarak tanımşanmış bir kullanıcının sistemden yararlanabilmesi için ayrıca rol tanımlanması gerekir.<br><br>

<img style="border:1px solid black" src="assets/images/hprog.png" height="400"/> 
<p style="text-align: center;">Şekil 4. Ders takvimi dosya biçimi (Haftalık ders programları). </p><br>

**CourseExternalId:** Dersin şube kodu. Şube ders ile ilgili açıklamalar yukarıda Şekil 2 nin altında var.<br>
**Start:** Dersin başlama tarihi ve zamanı.<br>
**End:** Dersin bitiş tarihi ve zamanı.<br>
**Username:** Dersin öğretim elemanı. Eğer dersi yürüten birden fazla öğretim elemanı varsa, ders için oluşturulan _Takvim_ satırları kopyalanıp aynı Excel dosyanın altına ilave edilir. İlave gelen satırlarda tek değişen kısım _Username_ kısmı olacaktır. Buraya ikinci öğretim elemanının kullanıcı adı yazılacaktır. Derse daha fazla öğretim elelmanı ilave edilecekse işlem her bir öğretim elemanı için tekrarlanır. Örneğin misafir bir öğretim elemanı sadece bir oturuma katılacaksa, bu dosyaya sadece bir satır ilave edilir.<br><br>

<img style="border:1px solid black" src="assets/images/dersKullanici.png"/> 
<p style="text-align: center;">Şekil 5. Ders katılımcıları dosyası biçimi (Derslere kaydolmuş öğrenciler veya öğretici olarak görevlendirilmiş öğretim elemanları). </p><br>

**Username:** Derse katılacak öğrencinin kullanıcı adı. <br>
**CourseExternalId:** Dersin şube kodu. Şube ders ile ilgili açıklamalar yukarıda Şekil 2 nin altında var.<br>
**EnumCourseUserType:** Derse katılan kişinin öğrenci veya öğretmen olduğu bilgisidir. 0: Öğretmen, 1: Öğrenci. <br>
**MetaData:** Derse katılanlar ile ilgili ilave bilgi için kullanılmak üzere ayrılmış bir alan. Örneğin bir sanal sınıf iki şubenin birleştirilmesinden oluşturulabilir. Böyle bir durumda, derse katılan öğrencilerin nereden geldiklerini ayrıştırmak için kullanılabilir, yani öğrenci bölüm kodu burada kullanılabilir. Bu kısım tamamen serbest olarak kullanılabilir, Excel dosyada _sayı_ veya _metin_ biçiminde olabilir. <br><br>

<img style="border:1px solid black" src="assets/images/veriAktarim.png"/>  
<p style="text-align: center;">Şekil 6. UZEP'e Excel dosya kullanarak veri aktarım arayüzü. </p>


**İşlem basamakları:**
1. Veri aktarımını doğru bir şekilde yapabilmek için UZEP arayüzündeki örnek dosyayı indirin.
2. Bu dosya içindeki ilk satırı (başlık satırını) koruyarak diğer verileri silin.
3. Üniveriste Yönetim Sisteminden indirdiğiniz verileri başka bir Excel sayfasında hazır edin.
4. Hazır edilen sayfayı kontrol ettikten sonra (gerekiyorsa düzenleme yaparak) UZEP'ten indirilen sayfaya, kolonları gözeterek yapıştırın.
5. Excel dosyayı **İçeri Aktar** butonunu kullanarak UZEP'e yükleyin.
6. **Tümünü Sil** butonu kullanılarak herhangi bir bölümün verisi tamamen silinebilir. Bu buton eylemi geri alınamaz, bu nedenle kullanılmadan evvel mutlaka veriler yedeklenmelidir.

Tüm veriler aktarldığında UZEP dönem için kullanıma hazır olacaktır. Bu noktadan sonra tekil değişiklikler UZEP-Admin arayüzlerinden yapılabilir.