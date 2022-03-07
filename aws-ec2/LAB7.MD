Cloudwatch birleşik aracısını EC2 bulut sunucusuna kurun. Amazon Linux AMI kullanarak Özel Metrikler Toplayın
--

1. Her şeyden önce, EC2 bulut sunucularının ölçümleri cloudwatch'a gönderebilmesi için gerekli IAM rollerini oluşturun
2. EC2 Eşgörünümü için IAM Rolü oluştururken ilkeler(policy) listesinde, CloudWatchAgentServerPolicy yanındaki onay kutusunu seçip attach edin .
3. Güvenlik grubunda 80 ve 22 numaralı bağlantı noktaları açık olan bir EC2 bulut sunucusu başlatın.
4. Örneğe ssh ile bağlanın
5. 
