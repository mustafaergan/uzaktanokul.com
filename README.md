# Uzaktan Okul Web Sayfası

uzaktanokul.com için başlatılmış tanıtım sitesi denemesi. Start Bootstrap "Agency" şablonu Spring Boot
ve Thymeleaf ile tek sayfa olarak sunuluyor; metinler şablondaki yer tutucu (lorem ipsum) içeriklerden
öteye geçmedi.

> **Not:** Bu depo 2017 yılında örnek amaçlı yazıldı ve artık güncellenmiyor. Bağımlılıkları eskidir ve
> bilinen güvenlik açıkları içerir; üretimde kullanmayın.

## İçerik

Proje `webpage/` klasöründedir.

| Yol | Ne yapar |
|---|---|
| `src/main/java/.../WebpageApplication.java` | Spring Boot giriş sınıfı (`ServletInitializer` ile WAR olarak da dağıtılabilir) |
| `src/main/java/.../controller/MainController.java` | `/` isteğinde `index` şablonunu döndürür |
| `src/main/resources/templates/` | Thymeleaf şablonları: `index.html`, `header.html`, `menu.html` |
| `src/main/resources/static/` | Agency şablonunun CSS/SCSS, JavaScript, görsel ve hazır kütüphane dosyaları (Bootstrap, Font Awesome, jQuery) |
| `src/main/resources/static/mail/contact_me.php` | Şablonla gelen PHP iletişim formu betiği; Spring Boot altında çalışmaz |
| `src/main/resources/application.properties` | Thymeleaf ayarları ve sunucu portu (8090) |

## Teknolojiler

- Java 8, Spring Boot 1.5.8 (Web, Thymeleaf, `LEGACYHTML5` modu için nekohtml)
- `pom.xml` içinde kullanılmayan başka başlangıç paketleri de var (Jersey, Mail, Freemarker, Spring Social,
  MySQL sürücüsü); kodda karşılıkları yok.
- Ön yüz: Start Bootstrap Agency v4.0.0-beta (MIT lisanslı), Bootstrap 4 beta
- Maven Wrapper (`mvnw`)

## Çalıştırma

```bash
cd webpage
./mvnw spring-boot:run      # Windows: mvnw.cmd spring-boot:run
```

Ardından tarayıcıda `http://localhost:8090/` adresini açın. Veritabanı gerekmez.
