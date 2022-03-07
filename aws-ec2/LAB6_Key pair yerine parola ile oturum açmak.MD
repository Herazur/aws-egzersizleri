## Key pair yerine parola ile oturum açmak


## adımlar

1. Bir SSH ile EC2 bulut sunucunuzda oturum açın. Çalışan bir EC2 Bulut Sunucunuz yoksa bir tane oluşturun.
2. Kullanıcı için bir şifre belirleyin. Aşağıdaki örnek, kullanıcı olarak ec2 kullanıcısını kullanır:
 ```console
    sudo passwd ec2-user
    Changing password for user ec2-user.
    New password:
    Retype new password:
    Şifre yenileme başarılı ise şöyle görünür:
    passwd: all authentication tokens updated successfully./ ya da / passwd: tüm kimlik doğrulama belirteçleri başarıyla güncellendi.
 ```
3. /etc/ssh/sshd_config dosyasındaki PasswordAuthentication parametresini bulup güncelleyin. Eğer görüntüleyemiyorsanız sudo su komutu ile yetki alıp deneyin:
 ```console
PasswordAuthentication yes
 ```
 4. SSH hizmetini yeniden başlatın. Amazon Linux, RHEL 5 ve SUSE Linux için şu komutu kullanın:
 ```console
   sudo service sshd restart
  ```
5. EC2 oturumundan çıkın ve ardından parola doğrulamasını test etmek için oturum açın.
```console
ssh ec2-user@instance_publicadres
```
6. Sizden bir şifre istenecektir. Parolayı girin ve ec2 kurulumunda başarıyla oturum açmış olmalısınız
