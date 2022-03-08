Apache web sunucusu loglarını cloudwatch'a gönderin
--

Bu laboratuvar çalışmasında, apache httpd loglarını cloudwatch'a göndereceğiz ve loglarımızı AWS Managemenet Konsolundan kontrol edeceğiz.

## adımlar

1. Önce bazı web trafik günlükleri oluşturmak için bir web sunucusu kurup başlatalım. Bu komut, RHEL ve Amazon Linux için çalışır.
```console
sudo yum install httpd -y
sudo service httpd start
```
2. Bulunduğunuz örneğin genel IP'sini kopyalayın ve bunu bir web tarayıcısına yapıştırın ve birkaç kez yenileyin.

3. Bu, bazı loglar oluşturmalıdır. Log dosyasının içine bakarak doğrulayabilirsiniz.
```console
sudo cat /var/log/httpd/access_log
```
4.Cloudwatch Unified Agent'ı indirin.
```console
wget https://s3.amazonaws.com/amazoncloudwatch-agent/amazon_linux/amd64/latest/amazon-cloudwatch-agent.rpm
```
5.Cloudwatch Agent'ı yükleyin
```console
sudo rpm -U ./amazon-cloudwatch-agent.rpm
```
6. Sihirbazla cloudwatch aracısını yeniden yapılandırın
```console
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard
```
Seçimlerimi buradan kontrol edin. Bazıları dışında seçeneklerin çoğu varsayılandır. Köşeli Parantezin içindeki numarayı seçtiysem, bu, varsayılan seçeneği seçtiğim anlamına gelir. 

![Ekran Görüntüsü - 2022-03-08 10-56-38](https://user-images.githubusercontent.com/68228757/157191992-01f7996d-92a1-4399-8d56-adb49af5a7de.png)

![Ekran Görüntüsü - 2022-03-08 10-57-56](https://user-images.githubusercontent.com/68228757/157192204-9e0c9095-a802-4003-852f-a9348f4b1f93.png)

![Ekran Görüntüsü - 2022-03-08 10-58-57](https://user-images.githubusercontent.com/68228757/157192366-e2d09678-5085-4b29-9d3e-d6c9d269e6aa.png)

![Ekran Görüntüsü - 2022-03-08 10-59-59](https://user-images.githubusercontent.com/68228757/157192584-ea8678d6-a424-4611-8d76-c8993e6e5e8d.png)

![Ekran Görüntüsü - 2022-03-08 11-01-16](https://user-images.githubusercontent.com/68228757/157192764-a808e7c0-d2f0-47a4-9f0c-070b893ad758.png)

![Ekran Görüntüsü - 2022-03-08 11-02-41](https://user-images.githubusercontent.com/68228757/157192962-fe75c613-7dd4-4768-afcd-a8f85c6d89ab.png)



