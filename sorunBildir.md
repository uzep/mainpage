---
layaout: default
title: Sorun-bildir
author: ozmen
---

# Sorun-bildir nasıl kullanılır? (Yöneticiler için)

Sorun bildir sistemi (issue-tracker) github üzerinde yapılandırılmıştır. Tanımlı **yöneticiler** [https://github.com/uzep/takip](https://github.com/uzep/takip) adresine kullanıcı adı ve şifreleri ile girerek sorun bildirebilirler, süreci interaktif olarak izleyebilirler. 

**Sorun bildirmek için aşağıdaki adımlar takip edilmelidir:**

1. Herhangi bir web tarayıcısı ile "https://github.com/uzep/takip" adresine kullanıcı adı ve şifre ile giriş yapılır.
2. Açılan sayfada menüden **issues** sekmesi tıklanır.
3. Sağ üst tarafta **New issue** (yeşil bir buton) tıklanır (Bkz. Şekil 2)
4. Açılan pencerede iki kısım vardır. **Title** kısmına sorunun adı veya kısaca tanımı yazılır. **Write** sekmesi altındaki pencereye de sorunun detaylı tarifi yazılır. Metin yazdığınız kutu üzerine dosya sürükleyerek ekleme yapabilirsiniz. Bu dosya resim dosyası olabileceği gibi başka türden dosyalar da olabilir. 
5. **Preview** sekmesi ile yazdığınız metnin (ve resim dosyası yüklediyseniz) nasıl görüneceğine bakabilirsiniz.
6. **Submit new issue** (metin yazılan yerin altında yeşil bir buton) butonu ile sorun bildirme tamamlanmış olur (Bkz. Şekil 1).
7. Girilen sorunu UZEP geliştiricileri görürler. Sorun UZEP ekibinden kimin alanına giriyorsa, **hata** veya **iyileştirme önerisi** gibi türünü de etiketleyerek kendi üzerine alır. Sorun bildiren kişi, kimin çözüm için çalıştığını sistem üzerinden görebilir, diyalog oluşturabilir.
8. Sorun çözüldüğünde geliştirici tarafından süreç kapatılır. Kapatılmış sorun-çözüm süreçleri (ve diyaloglar) ana panelden kaldırılır. 
9. Kapatılmış süreçleri görmek için panelde "Closed" etiketi tıklanmalıdır. Aşağıdaki pencerede daha önce çözülmüş problemler ve detayları görülebilir (Bkz. Şekil 2).  

<br><img style="border:1px solid black" src="assets/images/issueTracker2.png"/>
<p style="text-align: center;">Şekil 1. Sorun bildirim arayüzü. Orta yerdeki mavi çerçeveli kısma mesaj girilebilir veya sürkleme yoluyla resim, dosya yüklenebilir. "Submit new issue" butonu (yeşil buton) tıklandığında sorun bildirimi yapılmış olur.</p>

<br><img style="border:1px solid black" src="assets/images/issueTracker3.png"/>
<p style="text-align: center;">Şekil 2. Tamamlanmış sorun-bildir süreçleri listesi. Bu arayüzden "New issue" butonu ile sorun bildirilebilir veya devam eden (Open), tamamlanmış bildirimler (Closed) görülebilir. Bildirimler listesinde kalın yazı (bold) ile sorunun kısa tanımı ile beraber etiketi, ikinci satırda ise bildirim anından şimdiye kadar geçen süre ve bildirenin kullanıcı adı görülür. "Assignee" kısmında ise sorunun kim tarafından ele alındığı görülür. </p>
