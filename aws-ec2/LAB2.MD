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

Örnek'in Genel IP adresini bir Web tarayıcısına yapıştırarak Web Sunucusunun çalışıp çalışmadığını test edin. Genel IP, Örnek Açıklama sekmesi altında bulunur.

Apache Web Sunucusu Hoş Geldiniz Web Sayfasını görmelisiniz

Kök kullanıcı olun
