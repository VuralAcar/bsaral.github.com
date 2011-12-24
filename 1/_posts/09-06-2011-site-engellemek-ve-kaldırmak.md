---
layout: post
title: Site Engellemek Ve Engellemeleri Kaldırmak
---

###<a id="site-engelleme"> SİTE ENGELLEME </a> 

engellemek istediğimiz site <code>omu.edu.tr</code> olsun.

uçbirime

<code> sudo gedit /etc/hosts </code>

komutunu yazarak hosts dosyamızı açıyoruz.

açılan dosyaya sitenin IP adresini ve kendisini aşağıdaki gibi ekliyoruz.

       
       0.0.0.0 *.omu.edu.tr        



bu şekilde düzenlediğimizde omu'nun IP adresi <code>0.0.0.0 </code> olmadığından bağlantı hatası verecek yani siteye giriş engellenmiş olunacaktır.eğer sitenin engellenmesini kaldırıp tekrar eski haline döndürmek
istiyorsanız hosts dosyasında yazdığınız sitenin IP adresini ve kendisini silmeniz yeterlidir.

<img src="https://github.com/bsaral/bsaral.github.com/blob/master/images/2.png?raw=true"/>



###<a id="engel-kaldir"> ENGELLENEN SİTEYE GİRİŞ </a> 

DNS değişikliği yapılmadan yasaklanmış siteler arasından sadece seçtiğiniz sitelere girmek için bu yöntem uygulanır.

ilk önce sitenin IP adresi öğrenilir.(örn: yasaklı sitemiz <code>omu.edu.tr</code> olsun.)

uçbirimi açıp

<code> ping -c 1 www.omu.edu.tr </code>

komutunu yazdığımızda siteye 1 adet ping göndermiş oluruz.

<img src="https://github.com/bsaral/bsaral.github.com/blob/master/images/3.png?raw=true"/>

sonra hosts dosyası açılır.

<code> sudo gedit /etc/hosts </code>

ve IP adresleri eklenir.

           
           193.140.28.7 *.omu.edu.tr

kaydedip çıktıktan sonra yasaklı sitemize ulaşabilir duruma gelmiş oluruz.













