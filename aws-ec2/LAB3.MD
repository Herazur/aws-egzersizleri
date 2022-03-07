IAM Rolü ile EC2 Bulut Sunucusu izinleri verin
--

adımlar
--

- **IAM** Kontrol Paneli'ne gidin
- Sol gezinme bölmesinde **Kullanıcılar**'a tıklayın
- Bir kullanıcı ekleyin ve ona **Programmatic access** verin
- İleri'ye tıklayın ve **Attach existing policies directly**'i seçin
- AmazonS3FullAccess'i arayın ve ekleyin Bu politikaları aramak için arama kutusunu kullanın ve onay kutusuna tıklayın
- Sonrasında etiketlere tıklayın ve Review'e tıklayın ve oluşturun.
- **Show**'a tıklayın ve **Access key ID** ve **Secret access key** i bir yere kaydedin. Veya isterseniz CSV dosyasını da indirebilirsiniz.
- Bir Amazon Linux EC2 Bulut Sunucusu Başlatın
- SSH erişimi olmalı
- Diyelim ki bu andan itibaren Amazon S3 ile çalışmak istiyorsunuz. Birkaç bucket yapın ve birkaç bucket listeleyin. AWS Komut Satırı arayüzünü kullanabilirsiniz. Amazon Linux AMI'de bu zaten yüklü.
- AWS CLI'yi yapılandırın
```
aws configure
```
