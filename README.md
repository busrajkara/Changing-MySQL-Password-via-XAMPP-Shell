# Changing-MySQL-Password-via-XAMPP-Shell
# XAMPP Shell Üzerinden MySQL Şifre Değiştirme

## Giriş
Bu doküman, XAMPP Shell kullanarak MySQL root şifresini nasıl değiştireceğinizi adım adım açıklamaktadır.

## Gereksinimler
- XAMPP kontrol paneli
- MySQL veritabanı

## Adım 1: XAMPP Kontrol Panelini Açma
- XAMPP kontrol panelini başlatın.
- MySQL servisinin çalıştığından emin olun.
- "Shell" butonuna tıklayarak komut satırını (CLI) açın.

## Adım 2: MySQL'e Root Olarak Bağlanma
Aşağıdaki komutla MySQL veritabanına root kullanıcı olarak bağlanın:


mysql -u root -p
Komut çalıştırıldığında mevcut root şifresi istenecektir. Eğer şifre yoksa direkt Enter'a basabilirsiniz.
Adım 3: MySQL Şifresini Değiştirme
Root kullanıcısının şifresini değiştirmek için aşağıdaki komutu kullanın:


ALTER USER 'root'@'localhost' IDENTIFIED BY 'YeniŞifre';
YeniŞifre kısmını kendi belirlediğiniz güçlü bir şifre ile değiştirin.
Adım 4: Değişiklikleri Uygulama
Yapılan değişikliklerin aktif olması için aşağıdaki komutu çalıştırın:


FLUSH PRIVILEGES;
Adım 5: MySQL'den Çıkış Yapma
Şifrenin başarıyla değiştiğinden emin olduktan sonra MySQL'den çıkmak için aşağıdaki komutu kullanın:


exit;
Sonuç
Artık XAMPP Shell üzerinden MySQL şifreniz başarıyla değiştirilmiştir. Herhangi bir sorunla karşılaşırsanız, XAMPP belgelerine başvurabilirsiniz.
