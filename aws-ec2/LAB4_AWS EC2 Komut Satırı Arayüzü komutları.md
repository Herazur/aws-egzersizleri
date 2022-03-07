Lab 04 : AWS EC2 Komut Satırı Arayüzü komutları
--

* 22 numaralı bağlantı noktası açıkken bir EC2 bulut sunucusu başlatmak için Amazon Linux AMI'yi kullanın Bölgenizdeki AMI Kimliğini not edin Yap

1. CLI ile bir EC2 örneği oluşturun:
```console
aws ec2 run-instances --image-id ami-8c1be5f6 --instance-type t2.micro 
```
2. Windows AMI ile başka bir örnek başlatalım
```console
aws ec2 run-instances --image-id ami-07a29e78aeb420471 --instance-type t2.micro 
```
3. Tüm örneği ve ayrıntılarını listeleyin.
```console
aws ec2 describe-instances
```
4. Belirli şeyleri tanımlayın ve sorgulayın (Belirli nitelikleri listeleyin). Tüm örneklerin IP'sini sorgulayalım.
```console
aws ec2 describe-instances --query 'Reservations[].Instances[].PublicIpAddress'
```
5. Yalnızca Windows Örneği'ni göstermek için tanımlayın ve filtreleyin
```console
aws ec2 describe-instances --query 'Reservations[].Instances[].PublicIpAddress' --filters "Name=platform,Values=windows"
```
6. EC2 instance durdur
```console
aws ec2 stop-instances --instance-ids i-0b20d7680fa0e6ba0
```
7. EC2'yu sonlandır
```console
aws ec2 terminate-instances --instance-ids i-0b20d7680fa0e6ba0
```
Tebrikler! Artık temel AWS EC2 CLI Komutlarını biliyorsunuz.

## Referans
https://docs.aws.amazon.com/cli/latest/userguide/cli-services-ec2.html
