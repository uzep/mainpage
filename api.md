---
layaout: default
title: API ile Entegrasyon
author: ozmen
---

#API kullanarak entegrasyon:

Uygulama Programı Arayüzü (API) kullanarak UZEP içine veri yüklemek veya veri çekmek, yedekleme yapmak mümkündür. Bu işlemleri yapmak için istemci yazılımlar veya skriptler geliştirilebilir. Bu tür yazılımların veya skriplerin geliştirilmesi kullanıcı üniversitelere bırakılmıştır. UZEP token (jeton) bazlı yetkilendirme (authorization) yapısı kullanmaktadır. UZEP API'lerini kullanmak istediğiniz istemci yazılımlarının öncelikle UZEP'e tanımlanması (yetkilendirilmesi) gerekmektedir. Yetkilendirme sadece **Süper Yönetici** rolündeki bir kullanıcı tarafından yapılabilir.

**API kullanım işlem basamakları:**
1. İstemci tanımlama (yetkilendirme) işlemleri.
2. Mevcut API'lerin görülmesi, işlevleri ve tanımlarının incelenmesi.
3. API'lerin kullanımı.

##1. İstemci yetkilendirme (client authorization) için aşağıdaki işlemler yapılır:
1. Süper yönetici rolündeki kişiler, UZEP ana menüsünde yer alan "Ayarlar" sekmesini tıkladığında, açılan sayfada API işlemleri kısmında **Client Tanımlama** ve **Swagger** butonları bulunmaktadır (Bkz. Şekil 1). Buradaki **Client Tanımlama** butonu tıklanır. 
- İstemci tanımlamak için arayüze girilmesi gereken bilgiler:
..* **İstemci ID:** Harflerden oluşan ayırdedici bir kelime. Kendi alanınızda aynı ID ile iki istemci olamaz. Türkçe karakter kullanılmamalıdır. 
..* **İstemci adı:** Geliştirdiğiniz uygulamanın adı veya kullanım amacınıza uygun bir ad olabilir. Birkaç kelimeden oluşabilir, Türkçe karakter barındırabilir.
..* **Secret:** Gizli kelime, bilgilerin belirli bir algoritma ile şifrelenmesi için kullanılıyor. UZEP bunu otomatik üretiyor, isterseniz değiştirebilirisiniz.
..* **Token son geçerlilik tarihi:** Boş bırakılırsa sonsuz süreli token verilmiş olur. Güvenlik için kısa süreli tercih edilmelidir.  
2. **Ekle** butonu tıklanarak yeni API istemcisi UZEP'e tanıtılmış olur (Bkz. Şekil 2). 
3. API istemci tanımlama sayfasından, mevcut istemciler güncellenebilir, silinebilir  veya yeniden tanımlanabilir.

<br><img style="border:1px solid black" src="assets/images/api.png"/> 
<p style="text-align: center;">Şekil 1. API işlemleri seçimi: Sayfanın alt tarafındaki butonlardan "İstemci Tanımlama" ve "API tanımlama" (Swagger) arayüzlerine geçiş yapılabilir. </p> <br>

<br><img style="border:1px solid black" src="assets/images/token.png"/> 
<p style="text-align: center;">Şekil 2. Yeni API istemcisi tanımlama arayüzü. </p> <br>

##2. UZEP'te var olan API'ler ve tanımları: 
1. Süper yönetici rolündeki kişiler, UZEP ana menüsünde yer alan "Ayarlar" sekmesini tıkladığında, açılan sayfada API işlemleri kısmında **Client Tanımlama** ve **Swagger** butonları bulunmaktadır (Bkz. Şekil 1). Buradaki **Swagger** butonu tıklanır. 
2. Açılan sayfada ilk anda tüm API'ler, veri transfer metotları (GET veya POST) ve erişim URL'leri görülmektedir. API'ler "Baz Dersler: BaseCourse", "Dersler: Course", "Ders Kullanıcıları: CourseUser", "Takvim: Schedule", "Kullanıcılar: User", "Video" ve "Web bağlantısı: WebHookReceiver" şeklinde sınıflandırılmıştır (Bkz. Şekil 3).
3. Herhangi bir API üzerine tıklandığında parametre isimleri ve tipleri görülebilir. API'nin aktif olup olmadığı "Try it out" butonu tıklanarak görülebilir (bu buton sadece test içindir, veri getir/götür yapmaz).
4. Sayfanın alt tarafında şemalar kısmı bulunmaktadır. Buradan UZEP'te saklanacak veya getirilecek verilerin veritabanındaki tiplerini incelemek mümkündür.

<br><img style="border:1px solid black" src="assets/images/swagger.png"/> 
<p style="text-align: center;">Şekil 3. UZEP API'lerinin detayları. </p> <br>

##2. UZEP'te var olan API'lerin örnek kullanımı: 
1. Örnek kullanım için Postman uygulama arayüzü kullanılmıştır ([Bakınız](https://www.postman.com/)).