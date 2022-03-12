S3 kovasına dosya yüklemesiyle tetiklenen bir Lambda işlevi
--

1. S3 bucket'a isim verip default ayarlarıyla yaratın.
2. **Lambda** servisine geçin 
3. **Author from scratch** **Runtime**'ı Python olan fonksiyon yaratmadan önce **Change default execution role** kısmında **Create a new role from AWS policy templates**'i işaretleyin. 
4. **Policy templates** > **Amazon S3 object read-only permissions** verin.
5. Fonksiyonu artık yaratabilirsiniz.
6. Aşağıdaki kodu yapıştırın.
```
import json
import urllib.parse
import boto3

print('Loading function')

s3 = boto3.client('s3')


def lambda_handler(event, context):
    #print("Received event: " + json.dumps(event, indent=2))

    # Get the object from the event and show its content type
    bucket = event['Records'][0]['s3']['bucket']['name']
    key = urllib.parse.unquote_plus(event['Records'][0]['s3']['object']['key'], encoding='utf-8')
    try:
        response = s3.get_object(Bucket=bucket, Key=key)
        print("CONTENT TYPE: " + response['ContentType'])
        return response['ContentType']
    except Exception as e:
        print(e)
        print('Error getting object {} from bucket {}. Make sure they exist and your bucket is in the same region as this function.'.format(key, bucket))
        raise e
```
7. **Deploy** edin
8. S3 trigger ekleyin
9. **Recursive invocation**'u işaretleyin ve add diyin.

![Ekran Görüntüsü - 2022-03-12 13-02-01](https://user-images.githubusercontent.com/68228757/158013578-cf5fcc20-7abf-44d5-b73b-a017d427f335.png)
yelim

10. Yarattığınız S3'e png file yükleyin.
11. Biraz zaman geçtikten sonra Lambda Monitor'de CloudWatch metriklerini görebilirsiniz.
