---
layout: post
title: HTML-PHP-MYSQL İle Form Tasarlamak
---

Amacımız kullanıcı kaydı tutan bir web formu ve bu formdan bilgi alıcak bir php dosyası oluşturup , Php
dosyası içerisinde ki bilgileri veri tabanına aktarımını sağlayan tasarımı oluşturmaktır.İlk önce web formumuzu yapalım :

					<html>
					<head>
					<META http-equiv=content-type content=text/html;charset=UTF-8>
					<title>   PHP-MYSQL   </title>
					</head>
					<body>
					<form action="form.php" method="post">
					İSMİNİZ 
					<input type="text" name="isim"/><br>
					PAROLANIZ 
					<input type="password" name="par"/><br>
					MAİL ADRESİNİZ
					<input type="text" name="mail"/><br>
					
					<input type="submit" value="GONDER"/>
					</form>

					</body>
					</html>
					
En basit haliyle kullanıcı için bir web formu oluşturduk. Daha sonra bu formdan bilgileri alıcak ve veri tabanına aktarımını sağlayacak
olan PHP dosyamızı oluşturalım :

					<META http-equiv=content-type content=text/html;charset=UTF-8>

					<?php
					$baglan=mysql_connect("localhost","KULLANICI ADINIZ","KULLANICI ŞİFRENİZ") or die ("veri tabanına bağlanamadı.");
					if(!$baglan){
						die ("veritabanına bağlanılmadı.".mysql_error());
					}
						
					$veri=mysql_query("create database if not exists kaydet",$baglan);
					if ($veri){
						echo "veritabanı oluşturuldu.";}
					else {
						echo "hata".mysql_error();}

					mysql_select_db("kaydet") or die ("hata2");
					mysql_query("drop table if exists form") or die ("hata3");
					mysql_query("create table form(
					isim varchar(30),
					parola char(100) primary key,
					mail text(150))") or die ("hata4");

					mysql_query("insert into form (isim,parola,mail) values ('$_POST[isim]','$_POST[par]','$_POST[mail]')") 
					or die ("hata5".mysql_error());




					mysql_close($baglan);
						
					?>

