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
