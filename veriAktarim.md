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


**DepartmentExternalId:** Bir bölüm/programın numarası, bu numara tüm üniversite içinde tekil (ayırdedici) olmalıdır. Excel tabloya **sayı** olarak girilmelidir.
**FacultyName:** Bölüm/programın bağlı olduğu fakülte/enstitü veya MYO adı. Excel tabloya **metin** olarak girilmelidir.
**DepartmentName:** Bölüm/program adı. Excel tabloya **metin** olarak girilmelidir.

<img style="border:1px solid black" src="assets/images/dersler.png"/> 
<p style="text-align: center;">Şekil 2. Dersler dosyası biçimi (Baz dersler ve şube dersler). </p><br>


<img style="border:1px solid black" src="assets/images/kullanicilar.png"/> 
<p style="text-align: center;">Şekil 3. Kullanıcılar dosyası (Yöneticiler, öğretim elemanları ve öğrenciler). </p><br>
<img style="border:1px solid black" src="assets/images/hprog.png" height="400"/> 
<p style="text-align: center;">Şekil 4. Ders takvimi dosya biçimi (Haftalık ders programları). </p><br>
<img style="border:1px solid black" src="assets/images/dersKullanici.png"/> 
<p style="text-align: center;">Şekil 5. Ders katılımcıları dosyası biçimi (Derslere kaydolmuş öğrenciler veya öğretici olarak görevlendirilmiş öğretim elemanları). </p><br>
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