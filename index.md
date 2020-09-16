---
layout: default
title: Uzaktan Eğitim Platformu (UZEP)
author: ozmen
---
# Uzaktan Eğitim Platformu

Tübitak tarafından desteklenen proje ile ülke çapında tüm yükseköğretim kurumlarının istifade edeceği bir uzaktan eğitim platformu geliştirilmesi planlanmıştır (Proje no: 120K200). Sistemin donanım alt yapısı ULAKBİM tarafından sağlanırken, yazılım komponentleri Sakarya Üniversitesi tarafından geliştirilmektedir. Geliştirilen sistem üniversitelerin bilişim kaynaklarına ihtiyaç duymadığından, herhangi bir yükseköğretim kurumu için çok kısa sürede hizmete alınabilmektedir. <br>

### Projenin temel hedefleri:<br> 
1. Yüksek performans ve Internet band genişliği isteyen servisler için bilişim kaynaklarının yükseköğretim kurumları arasında paylaşımı yoluyla maliyetlerin azaltılması. <br>
2. Kişisel Verilerin Korunması Kanunu (KVKK) ile uyumlu olması. <br>
3. Salgın veya doğal afet durumlarında yükseköğretim kurumlarında eğitimin sürekliliğinin sağlanması.<br>

Geliştirilen sistemin modeli **"Servis olarak Eğitim"** _(Education as a Service: EaaS)_ şeklinde bir bulut hizmeti olarak tanımlanabilir.

## Sistemin bileşenleri:
**1. [Öğrenme Yönetim Sistemi (ÖYS) Modülü](/oys.html):** Haftalık sanal ders programlarının oluşturulmasını, uzaktan yürütülen eğitim faaliyetlerinin organize edilmesini ve yürütülmesini sağlayan modül.<br>
**2. [Sanal Sınıf Modülü](/sanal.html):** Sanal sınıfların video dağıtımını sağlayan ve açık kaynak yazılımlardan yararlanılarak oluşturulmuş modül.<br>
**3. [Duyuru Modülü](/duyuru.html):** Öğrencilere çeşitli düzeylerde duyuru yapılabilmesini sağlayan modül.<br>
**4. [Çevrimiçi Sınav Modülü](/esinav.html):** Çoktan seçmeli, ucu açık, doğru yanlış tarzda soruların hazırlanabileceği ve sınavların yürütülebileceği modül.<br>
**5. [Raporlama Modülü](/rapor.html):** Öğrenci devamı, akademisyen/sanal ders yürütülme sayıları gibi raporların sistem üzerinden alınabildiği modül.<br>

<img src="assets/images/uzep.png" border="2"/>

<!-- Yakın zamanda sisteme **Ödev Modülü** de ilave edilecektir. --> 

## Proje çalışanları:
<table style="width:100%">
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/91ec7cc107fcd02a0e6e0afb6dc8a454"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://ozmen.sakarya.edu.tr/">Ahmet Özmen</a> (Proje yürütücüsü):</b><br><br>Sistemin tasarımı ve proje yönetim faaliyetlerinden sorumlu.<br><br>Mail: <a href="mailto:ozmen@sakarya.edu.tr">ozmen@sakarya.edu.tr</a><br>Tel: (264) 295 7350</td>
  </tr>
   <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/238b0472bfe4b8703b63415eb7926ce3"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://mhorzum.sakarya.edu.tr/">Mehmet Barış Horzum</a> (Araştırmacı):</b><br><br>Sistemin eğitim süreçleri ile uyumu ve geliştirme çalışmalarından sorumlu.<br><br>Mail: <a href="mailto:mhorzum@sakarya.edu.tr">mhorzum@sakarya.edu.tr</a><br>Tel: (264) 295 5141</td>
  </tr>
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/edc1b6099551f8f1deb8947aa77e1175"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://kaynak.sakarya.edu.tr/">Baran Kaynak</a> (Bursiyer - DevOps uzmanı):</b><br><br>ÖYS ve sınav modülleri ile sistemin tasarımı, kodlanması ve test süreçlerinden sorumlu.</td>
  </tr>
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/6da30b0ed9b5a3b5b2c5e415e90b2a86"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://uozbek.sakarya.edu.tr/">Uğur Özbek</a> (Bursiyer - Video streaming uzmanı):</b><br><br>Sanal sınıfların oluşturulması, video dağıtımı ve yük dengeleme süreçlerinden sorumlu.</td>
  </tr>
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/fb87e2218d31fd76fa61f3855c775f36"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://osmantuna.sakarya.edu.tr/">Osman Tuna</a> (Bursiyer - Full-stack uzmanı):</b><br><br>Tüm modüllerin entegrasyonu ve kullanıcı arayüzlerinden sorumlu.</td>
  </tr>
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/256e739d6cc48bdbe22988354c7efa7b"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://aliaksoy.sakarya.edu.tr/">Ali Aksoy</a> (Bursiyer - Full-stack uzmanı):</b><br><br>Sanal sınıf entegrasyonu ve ÖYS arayüzlerinden sorumlu.</td>
  </tr>
  <tr>
    <td><img src="//fotograf.sabis.sakarya.edu.tr/Fotograf/9930e971cee6ad63541b794662488558"></td>
    <td style="text-align:left; vertical-align:top"><b><a href="http://bgol.sakarya.edu.tr/">Burak Göl</a> (Bursiyer - Dokümantasyon):</b><br><br>Kullanım kılavuzu ve yardım dokümanlarının hazırlanmasından sorumlu.</td>
  </tr>
 </table>
