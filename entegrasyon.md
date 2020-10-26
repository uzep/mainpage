---
layaout: default
title: Entegrasyon
author: ozmen
---
# Diğer sistemlerle entegrasyon

Üniveriste Yönetim Sistemi (ÜYS) ile UZEP entegrasyonu için iki yol bulunmaktadır:<br> 
1. ÜYS ile UZEP arasında sağlanan web servislerini (API) kullanmak, 
2. ÜYS'den verileri dosyaya (Excel) indirip, gerekli düzenlemeleri yaptıktan sonra UZEP'e yüklemek şeklindedir. 

**Entegrasyon için aktarılması gereken veriler şunlardır:** <br> 
**1. Birimler:** Üniversite hiyerarşisi içinde Fakülte, Meslek Yüksek Okulları (MYO), Enstitüler ve bunların altındaki bölümler ve programlar birimler olarak adlandırılmıştır. <br>
**2. Dersler:** Üniversitenin tüm birimlerinde tanımlı ve bölümlerin ders planlarında yer alan dersler.<br>
**3. Kullanıcılar (yöneticiler, öğrenciler, öğretim elemanları):** Üniversitede ders veren öğretim elemanları ve kayıtlı öğrenciler. İstenirse dışarıdan davetli de derse katılabilir, bunun için bireysel olarak kullanıcı eklenmesi gerekmektedir. <br>
**4. Ders takvimi:** Üniversite bölümlerinin haftalık ders programları. Ders programlarının sanal ders programı ile aynı olması gerekmez. Sisteme örgün bir program girilebilir, sanal dersler bu programa uygun veya farklı yerlerde icra edilebilir. <br>
**5. Ders katılımcıları:** Sanal derslere tanımlanan kullanıclar, öğrenciler ve öğretim elemanları. <br>

## 1. API kullanarak entegrasyon:

Sisteme veri yüklenmesi veya yüklü verilerin çekilmesi için sağlanan API'lerden yararlanılabilir. API'leri kullanarak otomatik entegrasyon veya yedekleme yazılım araçları geliştirmek mümkündür. Bu tür yazılım araçlarının geliştirilmesi UZEP'i kullanan üniversitelere bırakılmıştır. 

API ile veri transferi işlemlerinde ihtiyaç duyacağınız detaylı bilgilere erişmek için [tıklayınız](/api.html "API ile Entegrasyon").

## 2. Excel dosyaları yardımıyla entegrasyon:

Veri aktarımı için Excel dosyalarına UZEP’in beklediği biçimde verilerin yüklenmesi gerekmektedir. Excel dosyaları manuel doldurulabilir, ancak bu zor ve zahmetli ve hat ihtimali yüksek bir iş olacaktır. Bunun yerine ÜYS'den elde edilmesi hem işlemleri hızlandıracak ve yüksek doğruluykta bie entegrasyon yapılmış olacaktır. UZEP veri akatarımı arayüzünde (bkz. Şekil 1) örnek Excel dosyalar bulunmaktadır. Bu örnek dosyalar sistemin beklediği şekilde biçimlendirilmiştir, dolayısı ile önce bu dosyalar indirilmeli, ÜYS’den indirilen veriler buraya kopyalanarak entegrasyon yapılmalıdır.

Excel dosyaları ile veri transferi işlemlerinde ihtiyaç duyacağınız detaylı bilgilere erişmek için [tıklayınız](/fileEnt.html "Excel ile Entegrasyon").