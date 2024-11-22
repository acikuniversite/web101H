**Bootstrap Nedir?**

**Bootstrap**, web geliştirmeyi hızlandıran bir **önceden yazılmış CSS ve JavaScript kütüphanesidir**. Web sayfalarınızı hızlıca güzel ve işlevsel hale getirebilmek için kullanılır. Özellikle **mobil uyumlu** (responsive) web tasarımları yapmak için çok kullanışlıdır.

**Neden Bootstrap Kullanılır?**

- **Zaman Kazandırır:** Sıfırdan yazmak yerine, Bootstrap'ın sunduğu hazır bileşenleri kullanabilirsiniz.
- **Responsive (Mobil Uyumluluğu):** Bootstrap, sayfanızın her cihazda güzel görünmesini sağlar.
- **Hazır Tasarımlar:** Butonlar, formlar, navigasyon menüleri gibi öğeler zaten stil verilmiş şekilde gelir.
- **Kolay Kullanım:** HTML, CSS ve JavaScript konusunda temel bilgiyle kolayca kullanabilirsiniz.
-----
**Bootstrap Nasıl Kullanılır?**

**1. Bootstrap'ı Projeye Dahil Etme**

Bootstrap'ı kullanmanın iki yolu vardır: **CDN (Content Delivery Network)** kullanarak veya **Bootstrap dosyalarını indirerek**.

**CDN ile Kullanım:**

HTML dosyanızın <head> kısmına şu satırları ekleyerek Bootstrap'ı projenize dahil edebilirsiniz:

```html
<!-- Bootstrap CSS -->
<link href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" rel="stylesheet">
<!-- Bootstrap JS -->
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>

```
**Dosya İndirme ile Kullanım:**
- [Bootstrap’ın resmi sitesinden](https://getbootstrap.com/) Bootstrap dosyalarını indirip projene dahil edebilirsin.
- CSS ve JavaScript dosyalarını yerel olarak da kullanabilirsin.
-----
**Temel Bootstrap Bileşenleri**

**1. Grid Sistemi (Düzen Sistemi)**

Bootstrap’ın en önemli özelliklerinden biri **grid sistemi**dir. Bu sistem, sayfanın elemanlarını düzenlemek için kullanılır ve sayfanın genişliğini **12 sütuna** böler.

- Her eleman, bu 12 sütunluk yapıya uygun şekilde yerleştirilir.
- Cihaz boyutlarına göre **responsive** (duyarlı) olmasını sağlar.

**Örnek:**

```html
<div class="container">
`  `<div class="row">
`    `<div class="col-md-4">4 Sütun</div>
`    `<div class="col-md-4">4 Sütun</div>
`    `<div class="col-md-4">4 Sütun</div>
`  `</div>
</div>

```
- container: İçeriğin merkezi bir alanda düzgün yerleşmesini sağlar.
- row: Satır oluşturur (sütunları gruplayan etiket).
- col-md-4: 4 sütun genişliğinde bir alan oluşturur. md (medium) ekran boyutu için geçerlidir.

**2. Butonlar**

Bootstrap, kullanımı kolay ve şık butonlar sağlar. Butonların renkleri ve boyutları için sınıflar kullanılır.

**Örnek:**

```html
<button class="btn btn-primary">Birincil Buton</button>
<button class="btn btn-secondary">İkincil Buton</button>
<button class="btn btn-success">Başarılı Buton</button>

```
- btn: Butonun temel sınıfıdır.
- btn-primary, btn-secondary: Butonun farklı stilleri.

**3. Navigasyon Menüsü (Navbar)**

Bootstrap ile kolayca şık bir navigasyon menüsü oluşturabilirsiniz.

**Örnek:**

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
`  `<a class="navbar-brand" href="#">Marka Adı</a>

`  `<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
`    `<span class="navbar-toggler-icon"></span>
`  `</button>

`  `<div class="collapse navbar-collapse" id="navbarNav">

`    `<ul class="navbar-nav">
`      `<li class="nav-item active">
`        `<a class="nav-link" href="#">Ana Sayfa <span class="sr-only">(geçerli)</span></a>
`      `</li>
`      `<li class="nav-item">
`        `<a class="nav-link" href="#">Hakkında</a>
`      `</li>
`      `<li class="nav-item">
`        `<a class="nav-link" href="#">İletişim</a>
`      `</li>
`    `</ul>

`  `</div>
</nav>

```
- navbar: Navigasyon menüsünü başlatır.
- navbar-expand-lg: Menü, büyük ekranlarda genişler.
- navbar-light bg-light: Menü arka planını açık yapar.

**4. Kartlar (Cards)**

Kartlar, Bootstrap'ta içerik gruplarını düzenlemek için kullanılır.

**Örnek:**

```html
<div class="card" style="width: 18rem;">
`  `<img src="image.jpg" class="card-img-top" alt="...">
`  `<div class="card-body">

`    `<h5 class="card-title">Kart Başlığı</h5>
`    `<p class="card-text">Bu, kart içeriği hakkında kısa bir açıklamadır.</p>
`    `<a href="#" class="btn btn-primary">Detaylar</a>
`  `</div>
</div>

```
- card: Kart oluşturur.
- card-img-top: Üstteki resmi yerleştirir.
- card-body: Kartın gövde kısmıdır.
-----
**Bootstrap’ın Avantajları**

- **Kolay ve hızlı kullanım:** Kapsamlı bir dokümantasyona sahiptir.
- **Responsive tasarımlar:** Web siteniz her cihazda düzgün çalışır.
- **Çok sayıda bileşen:** Butonlardan menülere, form elemanlarından kartlara kadar pek çok hazır bileşen sunar.
- **Esneklik:** Projeye uygun şekilde özelleştirme yapabilirsiniz.
-----
**Bootstrap ile Başlarken İpuçları**

- **Dökümantasyonu takip et:** Bootstrap Dökümantasyonu
- **Özelleştirmeler yap:** Bootstrap'ı kullanarak, sayfanıza özgü renkler ve stiller ekleyebilirsiniz.
- **Mobil öncelikli tasarım yap:** Bootstrap responsive olduğu için, tasarımınızın tüm cihazlarda uyumlu olmasını sağlar.

