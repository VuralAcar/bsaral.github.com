---
layout: post
title: Ubuntuda LAMP Server Kurulumu
---

Linux ' ta yapılan web sitelerini yayınlamak amacıyla PHP+Apache+Mysql üçlüsü
gereklidir.Bunları sisteme ayrı ayrı kurmak mümkündür. Fakat Ubuntu ve diğer
birçok Linux dağıtımlarında bu iş için LAMP(Linux, Apache, Mysql, Php) paketi geliştirilmiştir.
Şimdi terminali açıp sırayla aşağıdaki kodları girelim :

		sudo apt-get install tasksel
		sudo tasksel install lamp-server
		sudo apt-get install phpmyadmin
		
		
son kod yazıldıktan sonra phpmyadmin kurulumu gerçekleşmeye başlar.ilk olarak karşınıza [E-H]
seçeneği gelir E ye basarak devam edin. Daha sonra karşınıza iki seçeneğin çıktığı bi ekran
gelir burda Apache2 yi seçerek devam edin.son olarak sizden şifre girmenizi isteyecektir.şifre girebilir
ya da boş bırakıp ENTER a basarak devam edebilirsiniz.


		sudo chmod 0777 /var/www/
		
Bu kodu da yazdıktan sonra var/www/ (yani burası localhostumuzun klasörüdür.) klasörünün içine
deneme.php adlı yeni bi belge açın ve aşağıdaki kodları girin :

		<?php
		echo 	"merhaba";
		?>
		
Yazıp kaydettikten sonra web tarayıcınız da  http://localhost/deneme.php yazın.Eğer sayfanız açılıyorsa
LAMP server başarıyla kurulmuş demektir.
