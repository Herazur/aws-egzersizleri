Laboratuvar 3: EC2 örneğinde Apache web sunucusunu kurun ve ondan image oluşturun
--

- Lab 1'de yaptığımız gibi bir Amazon Linux EC2 Bulut Sunucusuna SSH ile bağlanın.
- Apache web sunucusunu kurun
```console
sudo yum -y install httpd
```
- HTTPD hizmetini başlatın.
```console
sudo service httpd start  
```
- Başlangıçta HTTPD sunucusunu etkinleştir
```console
sudo chkconfig httpd on
```
- EC2 Dashboard'a gidin ve instance ı seçin.

- İnstance açıklaması altında ve Güvenlik Grubunun adına tıklayın.

- **İnbound Rules** ekleyin ve **Port range** 80 ve **Source** IP'si 0.0.0.0/0 olan bir gelen kuralı ekleyin

- İnstance'ın Public IP adresini bir Web tarayıcısına yapıştırarak Web Sunucusunun çalışıp çalışmadığını test edin. Public IP, İnstance Details sekmesi altında bulunur.

- Apache Web Sunucusu Test Page Web Sayfasını görmelisiniz

- Kök kullanıcı olun
```console
sudo su
```
- Basit bir özel index.html sayfası oluşturun ve /var/www/html üzerine koyun. Bu dizin, Apache web sunucusunun index.html dosyasını arayacağı varsayılan dizindir.
```console
echo "Merhaba. Bu sayfa benim AWS EC2 Linux Bulut Sunucumda barındırılıyor.">/var/www/html/index.html
```
- index.html dosyasına genel erişim vermek için html klasörünün iznini değiştirin
```console
chmod -R 755 /var/www/html
```
- Şimdi bir web sunucusundaki instance IP'sine tekrar göz atın. Bu mesajınızı görmelisiniz. 
'Merhaba. Bu sayfa benim AWS EC2 Linux Bulut Sunucumda barındırılıyor'
