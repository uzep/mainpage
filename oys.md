---
layout: default
title: Öğrenme Yönetim Sistemi
author: ozmen
---

# Öğrenme Yönetim Sistemi (LMS) Modülü
Öğrenme Yönetim Sistemi (ÖYS) Sakarya Üniversiteinde tasarlanıp kodlanmıştır. Sistemde çeşitli kademelerde roller tanımlanmıştır. Örnek olarak "üst yönetici", "yönetici", "birim sorumlusu", "bölüm sorumlusu", "öğretim elemanı", "öğrenci" ve "herkes" verilebilir. Roller içinde bireyler kendilerine belirlenen kısıtlar ile kaynaklara erişebilirler. Örneğin, bir "öğretim elemanı" sadece kendisine tanımlı sanal sınıflara girebilir, öğrencilere duyuru gönderebilir ve arayüzlerinde bu sınıflara ait tanımlı detaylara erişebilir. Ders planları, öğrenci kayıtları ve öğretim elemanı bilgileri üniversitelerin kendi bilgi sistemlerinde (Sabis, Proliz, Ünipa gibi) tutulmaktadır, haftalık sanal sınıfların oluşturulabilmesi için bu bilgilerin sistemler arasında steril bir şekilde paylaşılması gerekmektedir.

### Üniversite bilgi sisteminden verilerin UZEP'e aktarılması:
UZEP üzerine üniversite bilgi sisteminden bilgi aktarımı iki şekilde yapılabilir: 1) Bilgi aktarım servisinin sağlanması (API), 2) Dosya üzerinden veri transferi. Üniversite bilgi sistemini yöneten kurum tarafından API sağlanması durumunda, UZEP'e bilgi aktarımı çok kısa sürede ve tamamıyla steril ortamda gerçekleşmektedir. Bunun olabilmesi için üniversiteye yazılım sağlayan firma ile UZEP yazılım ekibinin görüşmesi ve istenilen biçimde API hazırlanması gerekmektedir. 

İkinci yöntem ise Excel ile verilerin üniversite bilgi sisteminden alınarak UZEP ortamına yüklenmesi şeklindedir. Üniversite bilgi sistemlerinde genelde Excel formatında bilgi indirmek için arayüzler olduğundan, ikinci yöntem daima iş görür. 

Her iki yöntemde de üniversitelerimizin hassas verileri hiçbir süretle yabancı sunuculara yüklenmemektedir. Tüm veriler ülkemizde konuşlandırılmış ULAKBİM sunucularında saklanacaktır, bu verileri yükleme işlemleri üniversitelerin yetkil persoenlleri tarafından yapılacaktır. Eğitimler sırasında veri transferinin nasıl yapılacağı anlatılacak, ayrıca bu konuda kılavuz ve video yardım dokümanları bu siteye yüklenecektir.

Veri aktarım kılavuzu için [tıklayınız.](/veriAktarim.html).<br>

[![Veri aktarım yardım videosu](https://www.youtube.com/watch?v=IGX8_7mBlpY&list=PLrX4FlRljtXNG8PJSkIdddhN466QjaXRW&index=7/0.jpg)](https://www.youtube.com/watch?v=IGX8_7mBlpY&list=PLrX4FlRljtXNG8PJSkIdddhN466QjaXRW&index=7)<br>

### Haftalık sanal sınıfların oluşturulması:
Haftalık sanal sınıf programları oluşturulmadan önce, sanal derslerin tüm üniversite içinde günlere ve gün içindeki saatlere dengeli dağılmasının gözetilmesi faydalı olacaktır. Sanal sınıflar merkezden UZEM tarafından haftalık olacak şekilde tüm üniversite için hazırlanabileceği gibi her bir öğretim elemanı kendi dersi için sistem üzerinden sanal sınıf oluşturabilecektir. Sanal sınıflar, ekran paylaşımı, uygulama pencersinin paylaşımı veya beyaz tahta paylaşımı şeklinde yürütülebilmektedir. 

UZEP üzerinde **Sanal Sınıf Oluşturma** kılavuzu için [tıklayınız.](/sanalSinif.html).
<!--Şekilde sanal sınıf oluşturma arayüzü görülmektedir.-->

<!--img src="assets/images/sanalSinif.png"/><br-->

<!--img src="assets/images/sanalSiniflar.png"/-->



### Öğrencilerin sanal sınıflara aktarılması:
Üniversite bilgi sisteminden öğrenci kayıtları çekildiğinde, öğrencinin kişisel bilgileri yanında, bulunduğu yarıyıl ve seçtiği dersler de bulunmaktadır. Veri aktarımı ile bu bilgiler UZEP'e yüklendiğinde otomatik olarak öğrencilerin derslere yerleştirilmesi tamamlanmış olacaktır. Bunun dışında öğrenci ekleme veya çıkartmak için yönetici arayüzünde ilave seçenekler bulunmaktadır. Öğrenciler kendi arayüzlerinden atandıkları sınıfları görürler, herhangi bir sanal ders saati gelmişse öğrenci açılan linke tıkladığında derse giriş yapabilir. Ders saati süresince katılım canlı olarak, ders saati sonrası katılım ise kayıt üzerinden izleme şeklindedir. 

UZEP'e veri aktarım işlemleri detaylarına erişmek için [tıklayınız.](/veriAktarim.html).

### Öğretim elemanlarının sanal sınıflara tahsisi:
Öğrenci kayıtlarının çekilmesi gibi öğretim elemanlarının bilgileri de üniversite bilgi sisteminden çekilir. Çekilen veri içinde öğretim elemanınlarının dönemsel eğitim görevlendirme bilgileri de bulunmaktadır. Bu bilgiler UZEP tarafından otomatik olarak sınıflarla eşleştirilir. Dönem içi değişiklikler için sistem üzerinde atama değişikliği için arayüzler bulunmaktadır. Dersin öğretim elemanı sisteme girdiğinde, o dönem yürüteceği dersleri otomatik olarak kendi arayüzünde görür. Derslere tıkladığında, ders ile ilgili sanal sınıflara ve duyurulara erişmek için butonlar bulunmaktadır. 

Bir dersin arayüzü ile ilgili detaylara erişmek için [tıklayınız.](/dersler.html).

<!--img src="assets/images/ogrElemArayuz.png"/><br-->

<!--img src="assets/images/faaliyetler.png"/-->


### Sanal sınıf aktivitelerinin izlenmesi:
Öğretim elemanı dersi ne zaman yapmıi ne kadar kalmış, öğrencilerin canlı yayına katılımları, kaç defa sonradan izleme yapmışlar gibi istatistiki veriler sistemden rapor olarak alınabilir. Ayrıca anlık olarak sistem yükü, devam eden canlı yayınların adedi sağlanan arayüzden görülebilir.

Raporlar ile ilgili detaylı bilgilere erişmek için [tıklayınız](/rapor.html).
