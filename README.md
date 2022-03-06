AWS Management Console'u tanıyın
--

Hedefler
--

- Bir AWS Bütçesi Oluşturun

- Servis panolarına bakın

- Bölgeleri değiştir

Bütçe türleri
--

- **Cost budget (Maliyet bütçesi)**


  Maliyetlerinizi belirli bir dolar tutarına göre izleyin ve kullanıcı tanımlı eşikleriniz karşılandığında uyarılar alın. Maliyet bütçelerini kullanarak,         belirlediğiniz bütçelenmiş tutar, beklenen bulut harcamanızı temsil eder. Örneğin, bir iş birimi için bir maliyet bütçesi ayarlayabilir ve ardından ilişkili üye  hesapları gibi ek parametreler ekleyebilirsiniz.

- **Usage budget (Kullanım bütçesi)**

  Bir veya daha fazla belirtilen kullanım türü veya kullanım türü grubu kullanımınızı izleyin ve kullanıcı tanımlı eşikleriniz karşılandığında uyarılar alın. Kullanım bütçelerini kullanarak, bütçelenen tutar, beklenen kullanımınızı temsil eder. Örneğin, Amazon EC2 ve Amazon S3 gibi belirli hizmetlerin kullanımını izlemek için bir kullanım bütçesi kullanabilirsiniz.

- **Savings Plans budget (Tasarruf Planları bütçesi)**

  Tasarruf Planlarınızla ilişkili kullanımı veya kapsamı takip edin ve yüzdeniz tanımladığınız eşiğin altına düştüğünde uyarılar alın. Bir kapsam hedefi belirlemek, örnek kullanımınızın ne kadarının Tasarruf Planları tarafından kapsandığını görmenizi sağlarken bir kullanım hedefi belirlemek, Tasarruf Planlarınızın kullanılmadığını veya yeterince kullanılmadığını görmenizi sağlar.

- **Reservation budget (Rezervasyon bütçesi)**

  Rezervasyonlarınızla ilişkili kullanımı veya kapsamı takip edin ve yüzdeniz tanımladığınız eşiğin altına düştüğünde uyarı alın. Bir kapsam hedefi belirlemek, bulut sunucusu kullanımınızın ne kadarının rezervasyonlar tarafından kapsandığını görmenizi sağlarken bir kullanım hedefi belirlemek, rezervasyonlarınızın kullanılmadığını veya yeterince kullanılmadığını görmenizi sağlar. Amazon EC2, Amazon RDS, Amazon Redshift, Amazon ElastiCache ve Amazon Elasticsearch rezervasyonları için rezervasyon uyarıları desteklenir.

Maliyet bütçesi oluşturma
--

- **Period**, bütçenin gerçek ve tahmini harcamayı ne sıklıkta sıfırlamasını istediğinizi seçin. Her gün için **Daily**, Her ay için **Monthly**, **Quarterly** Üç ayda bir veya Yıllık için **Annually** seçin .

- **Budget effective date (Bütçe geçerlilik tarihi)**, bütçe döneminden sonra sıfırlanan bir bütçe için **Recurring budget (Yinelenen Bütçe)** seçin . Veya, bütçe döneminden sonra sıfırlanmayan tek seferlik bir bütçe için **Expiring budget (Süresi dolan bütçe)** seçin.

**Budgeting method (Bütçeleme yöntemi)**, bütçe tutarınızın her bütçe döneminde nasıl belirlenmesini istediğinizi seçin:

**Fixed** : Her bütçe dönemini izlemek için bir tutar belirleyin.

**Planned :** Her bütçe dönemini izlemek için farklı tutarlar belirleyin.

**Auto-adjusting :** Bütçe tutarınızı, belirlediğiniz bir zaman aralığında harcama şeklinize göre otomatik olarak ayarlanacak şekilde ayarlayın.
