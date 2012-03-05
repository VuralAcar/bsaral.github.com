---
layout: post
title: Debian Testing Grafik Arayüzü Oluşturma
---

Temel kurulumu başarılı bir şekilde tamamlamış olduğunuzu ve sistemi başlattığınızda aşağıdaki gibi bir görüntü elde ettiğinizi varsayıyorum.

<img src="/images/debian.gif"/>

Grafik arayüzüne geçilmesi için 3 komutun kullanılır.

1-)
	<code>apt-get install x-window-system </code>  

2-)
	<code> apt-get install gdm </code>

Bu komut ile Gnome Desktop Manager kurulacak. Gdm bizim oturum açmamız için kullanıcı adı ve şifre gireceğimiz güzel bir grafik karşılayıcıdır.

3-) 
<code> apt-get install gnome </code>

Bu komut ile Gnome grafik ortamı ve beraberindeki uygulamaları kuracağız.

Eğer grafik ortamını KDE olmasını;

<code> apt-get install kde </code>

yada XFCE olmasını istiyorsanız :

<code> apt-get install xfce4 </code>

komutlarını kullanabilirsiniz.

Kurulum işlemleri bittikten sonra <b> gdm </b> yazarak grafik ortamına geçebiliriz.

<b>UYARI:</b> 
eğer komutları yazdığınızda "Debian E:unable to locate package sorunu" şeklinde hatalar alıyorsanız çözüme
<a href = "http://mogutcan.github.com/902/Debian-E:-unable-to-locate-package-sorunu/"> buradan </a> ulaşabilirsiniz.

<b>UYARI2:</b> 
sistemde gedit,vim şeklinde editörleriniz bulunmuyorsa nano editörünü kullanarak işlerinizi halledebilirsiniz.

<b> NOT : </b>
Eğer yapılan değişikleri geri almak,kaldırmak istiyorsanız (örn:gnome grafik ortamını kaldıralım) ;
<code> apt-get remove gnome </code> kodu ile halledebilirsiniz.

 

