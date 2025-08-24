# Microservice Mimarisi Örnek Projesi

Bu proje, Next.js ile multi-zone microfrontend mimarisi kullanılarak oluşturulmuş bir alışveriş uygulamasıdır. Ana uygulama (home) ve sepet uygulaması (cart) olmak üzere iki bağımsız mikro frontend'den oluşmaktadır.

---

## Projeye Genel Bakış

Proje, `https://fakestoreapi.com` apisini kullanarak basit bir alışveriş sistemini simüle etmektedir. `home` micro-frontend'i anaysafa(homepage), ürün listesi(products) ve ürün detayı(products/:id) sayfalarından oluşmaktadır. ürün detayı sayfaları için Next.js'in ISR teknolojisi kullanılmıştır. `cart` micro-frontend'i sepet(main) sayfasından oluşmaktadır. Proje **bun.sh** ile **typescript** kullanılarak geliştirilmiştir. Dockerfile'de bun.sh kullanılmaktadır. State yönetimleri **Redux Toolkit** ile yapılmaktadır.

---

### Kullanılan ek paketler
* **Redux Toolkit:** Toast mesajlarını ve cookie'deki cart bilgilerini taşımak için kullanılmaktadır.
* **Lucide Reacts:** Nispeten diğer kütüphanelerden daha küçük boyutlu `icon` kütüphanesidir.
* **Axios:** Fakestoreapi'ye bağlanmak için fetch'e alternatif HTTP client library olarak eklenmiştir.

**Not:** `Toast` işlemleri için herhangi bir paket kurulumu yapılmamıştır. Tarafımdan kodlanmıştır.

---

## Kurulum ve Başlangıç

### Projeleri Başlatma
Her bir micro-frontend'i ayrı ayrı başlatmanız gerekmektedir.

1.  Projeleri pull ettiğiniz klasörlerin olduğu ana klasöre girin ve bu repository'de bulunan `compose.yml` dosyasını ekleyin.
2.  Terminalde aşağıdaki komutu çalıştırın:
    ```bash
    docker compose up -d
    ```
Bu komut, her proje için Docker imajını üretecek ve gerekli ortam değişkenleriyle birlikte uygulamayı başlatacaktır.
