İlk Basit bir Lambda fonksiyonunu oluştur
--

1. Lambda Servisine geçiş yapalım.
2. **Create function** > **Author from scratch** fonksiyonu ile devam edin.
3. **Runtime** Python seçip fonksiyonu oluşturalım.
4. Aşağıdaki kodu girelim. 

```
import json

def lambda_handler(event, context):
    # TODO implement
    print('This is my AWS Lambda function')
    if event ['planet'] == 'Earth':
    	return 'Moon'
    elif event['planet'] == 'Sun':
    	return 'This is not the planet'
    else:
    	return 'We do not recognize your argument!'
```

5. **Deploy** ve sonrasında **Test** edelim.
6. **Event template** "Hello-world" olarak kalabilir.
```
{
  "planet": "Earth"
}
```
7. Test eventi girdikten sonra test edin ve sonucu **response**'da görün
8. Test event'te **Earth** yerine **Sun** veya olmayan bir gezegen girip sonuçları tekrar gözlemleyebilirsin.
