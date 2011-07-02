---
layout: post
title: Kullanıcı Şifresinin Unutulması
---

Kullanıcı şifresi unutulduysa,ilk yapmanız gereken sisteminizi kurtarma modunda (Recovery Mode) yani GRUB menüsünün 2.seçeneğinden başlatmak olacaktır.sistem açıldığında karşınıza bir pencere çıkar.bu pencerenin en sonunda bulunan "root kullanıcısı olarak uçbirimi aç" seçeneğini tercih edin.altta uçbirim açılır.uçbirime ilk olarak

<code> passwd KULLANICI_ADINIZ </code>

yazıp ENTER a basın.bu kodu yazdıktan sonra sizden yeni şifrenizi girmenizi isteyecektir.şifreyi girdikten sonra

<code> reboot </code>

yazıp ENTER a bastığınızda işleminiz tamamlanmış olur.
