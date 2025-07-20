# 🧩 Full-Stack Wappler Web Projesi

Bu proje, **Wappler** ile geliştirilmiş, tam işlevsel ve modüler yapıya sahip bir web uygulamasıdır. Uygulama, frontend ve backend yapılarını birleştiren, kullanıcı deneyimini ön planda tutan bir sistem sunar.

---

## 🚀 Özellikler

### 🔧 Layout Sistemi
- Tüm sayfalar **ana layout** dosyasına bağlanır.
- `navbar` ve `footer` layout dosyasına gömülüdür.
- Sayfa içerikleri `<%- await include(content, locals); %>` ifadesi ile layout'a dinamik olarak entegre edilir.

---

### 🏠 Ana Sayfa (Home)
- Gelişmiş **carousel bileşeni** kullanılarak dikkat çekici tanıtım alanı oluşturulmuştur.
- Alt bölümde:
  - Bilgilendirici içerikler
  - Görsel destekli açıklamalar
- Sayfa sonunda:
  - **Newsletter (Bülten) abonelik formu**
  - Kullanıcılar e-posta adreslerini girerek **PostgreSQL veritabanına** kaydolur.
  - Başarılı aboneliklerde **bildirim (toast)** gösterilir, form resetlenir.

---

### 🧑‍💼 Hakkımızda Sayfası (About)
- Statik içeriklerden oluşur.

---

### 🛍️ Ürün Sayfası (Products)
- API üzerinden dinamik olarak ürünler çekilir.
- Kullanıcılar:
  - Ürünleri **sepete ekleyebilir**
  - **Sepetten çıkarabilir**
- Sepet:
  - **Modal pencere** ile açılır
  - Ayrı bir **cart (sepet) sayfası** da mevcuttur
- Sepet sayfası üzerinden **ödeme sayfasına yönlendirme** yapılır.
- Not: Ödeme sistemi pasif durumdadır, test modundadır.

---

### 📬 İletişim Sayfası (Contact)
- Kullanıcıların site sahibine **e-posta göndermesi** sağlanır.
- Gelişmiş form özellikleri:
  - **Form resetleme**
  - **Başarı ve hata bildirimi (notifications)**

---

## 🛠️ Teknolojiler

| Katman | Kullanılan Teknoloji |
|--------|-----------------------|
| Frontend | HTML5, CSS3, Bootstrap 5, App Connect (Wappler) |
| Backend | Wappler Server Connect, Node.js |
| Database | PostgreSQL |
| API | Dinamik ürün verisi çekimi |
| Bildirim Sistemi | Wappler Notifications & Toast |
| Deployment | (Henüz devreye alınmadı / planlanıyor) |

---

## 🔐 Güvenlik & UX Detayları
- Tüm formlar client-side ve server-side olarak doğrulanır.
- Formlar gönderildikten sonra otomatik resetlenir.
- Kullanıcı geri bildirimi için toast & notification desteği vardır.

---

## 🧪 Durum
> Bu proje şu an için geliştirme aşamasındadır. Ödeme sistemi devre dışıdır. Ancak UI/UX ve veri akışı test edilmektedir.

---

## 📁 Kurulum

> Geliştirici ortamı için:

```bash
git clone https://github.com/kullaniciadi/projeadi.git
cd projeadi
# Wappler ile açın ve PostgreSQL bağlantısını yapılandırın
