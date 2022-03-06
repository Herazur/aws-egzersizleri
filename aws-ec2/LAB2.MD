Laboratuvar 3: EC2 örneğinde Apache web sunucusunu kurun ve ondan altın bir görüntü oluşturun
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
