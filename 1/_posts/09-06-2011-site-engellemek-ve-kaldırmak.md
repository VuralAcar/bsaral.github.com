---
layout: post
title: Site engellemek ve engellemeleri kaldırmak
---

1- SİTE ENGELLEME 

engellemek istediğimiz site <code>omu.edu.tr</code> olsun.

uçbirime

<code> sudo gedit /etc/hosts </code>

komutunu yazarak hosts dosyamızı açıyoruz.

açılan dosyaya sitenin ip adresini ve kendisini aşağıdaki gibi ekliyoruz.

<code> 0.0.0.0 http://www.omu.edu.tr 
       0.0.0.0 omu.edu.tr        
       0.0.0.0 www.omu.edu.tr      
       0.0.0.0 *.omu.edu.tr        
</code>


bu şekilde düzenlediğimizde omu'nun ip adresi <code>0.0.0.0 </code> olmadığından bağlantı hatası verecek yani siteye giriş engellenmiş olunacaktır.





