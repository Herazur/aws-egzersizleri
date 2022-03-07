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
- Diyelim ki bu andan itibaren Amazon S3 ile çalışmak istiyorsunuz. Birkaç bucket yapın ve birkaç bucket listeleyin. AWS Komut Satırı arayüzünü kullanabilirsiniz bilgisayarınızda kullanmak isterseniz awscli ı yüklemeniz gerekmektedir.
- AWS CLI'yi yapılandırın bunun için bilgisayarınızda awscli yüklü olması gerekir
```console
aws configure
```
- Daha önce oluşturup kaydettiğiniz kullanıcının acces key id'sini ve secret access key anahtarlarını girin.
- Bölgenizin adını girin
- AWS CLI'den rastgele bir adla bir S3 paketi oluşturun. Uygun izinleriniz varsa, hem s3 bucket oluşturabilir hem de listeleyebilirsiniz.
```console
aws s3 mb s3://mybucketnameherazur
```
S3 paketlerinizi listeleyin.
```console
aws s3 ls
```
- EC2'den S3'e bağlanmak için Erişim anahtarlarını kullandınız.
- Kimlik bilgisi dosyasını görüntüleyin. Sabit kodlanmış kimlik bilgileri, güvenlik açısından güvensizdir.
```console
cat ~/.aws/credentials
```
