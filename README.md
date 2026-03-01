# 🩺 Diyabet Takip Sistemi (Diabetes Monitoring System)

JavaFX ve PostgreSQL kullanılarak geliştirilmiş masaüstü tabanlı bir diyabet hasta takip ve yönetim sistemidir.  
Bu proje, doktor ve hasta rollerine göre veri yönetimi sağlayan güvenli ve modüler bir yazılım mimarisi ile geliştirilmiştir.

---

## 🚀 Özellikler

- 👨‍⚕️ Doktor paneli
- 👤 Hasta paneli
- 📊 Kan şekeri verisi kaydı
- 🔐 Güvenli veritabanı bağlantısı (Environment Variables ile)
- ✉️ Opsiyonel e-posta gönderme özelliği
- 🗂 PostgreSQL tabanlı veritabanı
- 🖥 JavaFX masaüstü arayüz

---

## 🛠 Kullanılan Teknolojiler

- Java 21
- JavaFX
- PostgreSQL
- Maven
- Jakarta Mail

---

## ⚙️ Kurulum

### 1️⃣ Veritabanı Oluşturma

Öncelikle PostgreSQL üzerinde bir veritabanı oluşturun:

sql
CREATE DATABASE diyabet_db;
Ardından src/main/resources/database/init.sql dosyasını çalıştırarak tabloları oluşturun.

2️⃣ Environment Variables Ayarlama

Uygulama güvenlik amacıyla veritabanı bilgilerini kod içerisinde barındırmaz.
Aşağıdaki environment variable'ların ayarlanması gerekmektedir:

Windows (PowerShell)
setx DB_URL "jdbc:postgresql://localhost:5432/diyabet_db"
setx DB_USER "postgres"
setx DB_PASSWORD "your_password"

IntelliJ veya terminal yeniden başlatılmalıdır.

✉️ Opsiyonel: Email Özelliğini Aktif Etme

E-posta gönderme özelliğini kullanmak için:

setx EMAIL_FROM "your_email@gmail.com"
setx EMAIL_PASSWORD "your_gmail_app_password"

Gmail App Password kullanmak için Google hesabınızda 2FA aktif olmalıdır.
Bu değişkenler ayarlanmazsa email özelliği devre dışı kalır.

🔐 Güvenlik Notları

Veritabanı bağlantı bilgileri environment variable üzerinden alınmaktadır.

Kod içerisinde şifre veya gizli anahtar bulunmamaktadır.

Localhost kullanıldığı için veritabanı dış erişime açık değildir.

📌 Çalıştırma
mvn clean javafx:run

veya IDE üzerinden DiyabetTakipApp sınıfı çalıştırılabilir.

👨‍💻 Geliştirici
-SEFA ÖZDEMİR

Bu proje eğitim ve portföy amaçlı geliştirilmiştir.



