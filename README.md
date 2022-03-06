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

1. **Period**, bütçenin gerçek ve tahmini harcamayı ne sıklıkta sıfırlamasını istediğinizi seçin. Her gün için **Daily**, Her ay için **Monthly**, **Quarterly** Üç ayda bir veya Yıllık için **Annually** seçin .

2. **Budget effective date (Bütçe geçerlilik tarihi)**, Bütçe döneminden sonra sıfırlanan bir bütçe için **Recurring budget (Yinelenen Bütçe)** seçin . Veya, bütçe döneminden sonra sıfırlanmayan tek seferlik bir bütçe için **Expiring budget (Süresi dolan bütçe)** seçin.

3. **Budgeting method (Bütçeleme yöntemi)**, bütçe tutarınızın her bütçe döneminde nasıl belirlenmesini istediğinizi seçin:

  -   **Fixed :** Sabit bütçe ile her bütçe döneminde aynı tutarı izleyebilirsiniz. Örneğin, maliyetlerinizi her bütçe döneminde 100$'a karşı izlemek için sabit yöntemle bir maliyet bütçesi kullanabilirsiniz.

  -   **Planned :** Planlı bütçeleme yöntemi yalnızca aylık veya üç aylık bütçeler için kullanılabilir. Planlı bir bütçeyle, her bir bütçe dönemini izlemek için farklı bir tutar belirleyebilirsiniz. Örneğin, maliyetlerinizi ilk aydaki 100 ABD Doları, ikinci ayda 110 ABD Doları ve kalan aylardaki diğer tutarlara karşı izlemek için planlanan yöntemle aylık bir maliyet bütçesi kullanabilirsiniz.

  -   **Auto-adjusting :** Otomatik olarak ayarlanan bir bütçe, belirlediğiniz bir zaman aralığında harcamanıza veya kullanımınıza göre bütçe tutarınızı dinamik olarak ayarlar. Seçtiğiniz geçmiş veya tahmin zaman aralığı, bütçeniz için otomatik ayarlama temelidir.

AWS Bütçeleri, her yeni dönemin başında, temel zaman aralığında maliyet veya kullanım verilerinizden bütçe tutarınızı hesaplar. Hesabınızın AWS maliyetleri veya kullanımı için beklentilerinize en uygun zaman aralığını seçtiğinizden emin olun. Normalde beklediğinizden daha düşük kullanıma sahip bir zaman aralığı seçerseniz, ihtiyacınız olandan daha fazla bütçe uyarısı alabilirsiniz. Normalde beklediğinizden daha yüksek kullanıma sahip bir zaman aralığı seçerseniz, ihtiyaç duyduğunuz kadar çok bütçe uyarısı alamayabilirsiniz.

Örneğin, son altı aylık temel zaman aralığıyla otomatik olarak ayarlanan bir maliyet bütçesi oluşturabilirsiniz. Bu senaryoda, son altı ayda her bütçe döneminde ortalama harcamanız 100 TL ise, yeni dönemde otomatik olarak ayarlanan bütçe tutarınız 100 TL olur.

Configure alerts (Uyarıları yapılandır)
--

Neden bütçe uyarıları oluşturmalısınız?

Bütçenizin durumundan haberdar olmak için, bütçelenen tutarınıza göre en fazla 5 farklı uyarı oluşturabilirsiniz. Örneğin, bütçelenmiş tutarınızın %75'ine ulaştığınızda sizi bilgilendirmek için bir uyarı oluşturun.

**Set alert threshold**

Uyarı eşiğini ayarla altında ,Threshold için, size bildirilmesi için ulaşılması gereken tutarı girin. Bu, absolute (mutlak) bir değer veya % (yüzde) bir değer olabilir. 

Tutarın yanında, maliyetleriniz eşik tutarını aştığında bildirilmesini istiyorsanız **Absolute value**. Veya maliyetleriniz eşik yüzdesini aştığında bildirilmesini istiyorsanız 

