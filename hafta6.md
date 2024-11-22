# 6.Hafta - CSS Özellikleri (width-height, margin-padding, text-font)

**CSS width ve height Nedir?**

- **width (genişlik)** ve **height (yükseklik)**, HTML öğelerinin boyutlarını ayarlamak için kullanılır.
- Bu özellikler, bir kutunun (örneğin bir div, img, veya başka bir HTML öğesi) ne kadar yer kaplayacağını belirler.
-----
**Temel Kullanım**

1. **width (genişlik):** Bir öğenin yatayda ne kadar geniş olacağını belirler.
   1. Örnek: width: 200px;
1. **height (yükseklik):** Bir öğenin dikeyde ne kadar yüksek olacağını belirler.
   1. Örnek: height: 100px;
-----
**Değer Türleri**

1. **Pixel (px):** Kesin bir uzunluk belirtir.
   Örnek: width: 300px;
1. **Yüzde (%):** Bulunduğu öğeye göre orantılı boyut belirler.
   Örnek: width: 50%; (Öğe, kapsayıcısının genişliğinin %50’si kadar olur.)
1. **Auto:** Tarayıcı öğenin boyutunu otomatik olarak belirler.
   Örnek: width: auto;
1. **Viewport Ölçüleri (vw, vh):**
   1. **vw:** Tarayıcı penceresinin genişliğinin yüzdesi.
      Örnek: width: 50vw; (Ekran genişliğinin %50’si kadar.)
   1. **vh:** Tarayıcı penceresinin yüksekliğinin yüzdesi.
      Örnek: height: 100vh; (Ekran yüksekliğinin tamamı.)
-----
**Örnekler**

**1. Sabit Boyut Ayarlamak**

```css
div {
`    `width: 200px;
`    `height: 100px;
`    `background-color: lightblue;
}
```

**Sonuç:** Genişliği 200px, yüksekliği 100px olan bir kutu.

-----
**2. Yüzde Kullanımı**

```css
div {
`    `width: 50%;
`    `height: 50%;
`    `background-color: lightgreen;
}
```

**Sonuç:** Kutu, kapsayıcısının genişliğinin ve yüksekliğinin %50’si kadar olur.

-----
**3. Ekran Boyutuna Göre Ayarlama**

```css
div {
`    `width: 80vw;
`    `height: 50vh;
`    `background-color: lightcoral;
}

```
**Sonuç:** Kutu, ekranın genişliğinin %80’i, yüksekliğinin %50’si kadar olur.

-----
**HTML ve CSS Örneği**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
.kutu1 {
`            `width: 300px;
`            `height: 150px;
`            `background-color: lightblue;
`        `}
.kutu2 {
`            `width: 50%;
`            `height: 200px;
`            `background-color: lightgreen;
`        `}
.kutu3 {
`            `width: 100vw;
`            `height: 100vh;
`            `background-color: lightcoral;
`        `}
`    `</style>
</head>
<body>
`    `<h1>CSS Width ve Height Örnekleri</h1>
`    `<div class="kutu1">Sabit Boyut (300px x 150px)</div>
`    `<div class="kutu2">Yüzde ile Boyut (%50 genişlik)</div>
`    `<div class="kutu3">Ekran Boyutuna Göre (100vw x 100vh)</div>
</body>
</html>

```
-----
**Bu Örnekte Neler Var?**

1. **Sabit Boyut:** İlk kutu 300px genişlikte ve 150px yükseklikte.
1. **Yüzdelik Boyut:** İkinci kutu, tarayıcı penceresinin genişliğinin %50’sini kaplıyor.
1. **Ekran Boyutuna Göre:** Üçüncü kutu, ekranın tamamını kaplıyor.
-----
**İpuçları**

1. **Responsive Tasarımlar için:**
   Yüzde (**%**) ve viewport (**vw, vh**) kullanarak cihaz boyutuna duyarlı tasarımlar yapabilirsiniz.
1. **Otomatik Boyutlandırma:**
   Eğer içeriğe göre bir boyut istiyorsanız **auto** değerini kullanabilirsiniz.
1. **Kapsayıcıya Göre Oran Ayarlayın:**
   Eğer bir öğeyi içinde bulunduğu alanın boyutuna göre ayarlamak istiyorsanız yüzdelik değerler çok kullanışlıdır.

**CSS Margin ve Padding Nedir?**

- **Margin (Kenar Boşluğu):** Bir öğenin dışı ile başka bir öğe arasındaki boşluğu belirler.
- **Padding (İç Boşluk):** Bir öğenin içindeki içerik ile kenarları arasındaki boşluğu belirler.

Bu özellikler, öğeleri düzenlemek ve aralarındaki mesafeyi kontrol etmek için kullanılır.

-----
**Farkı Anlamak İçin Basit Bir Benzetme:**

Diyelim ki bir kutuya hediye koyuyorsunuz:

1. **Hediye (İçerik):** Öğenin içindeki metin, resim vb.
1. **Kutunun İç Boşluğu (Padding):** Hediye ile kutunun kenarları arasındaki boşluk.
1. **Kutunun Dışındaki Boşluk (Margin):** Kutunun diğer kutular veya duvarlar arasındaki mesafesi.
-----
**Nasıl Kullanılır?**

1. **Margin:**

```css
margin: değer;
Örnek: margin: 10px;

```
1. **Padding:**

```css
padding: değer;
Örnek: padding: 15px;

```
-----
**Değer Türleri**

- **Pixel (px):** Sabit bir uzunluk belirler.
  Örnek: margin: 20px;
- **Yüzde (%):** İçerik veya kapsayıcı öğeye göre orantılı boşluk belirler.
  Örnek: padding: 5%;
-----
**Margin ve Padding'in Farklı Kenarlara Uygulanması**

Hem **margin** hem de **padding** dört kenar için ayrı ayrı ayarlanabilir:

1. **Tüm Kenarlar Aynı:**

```css
margin: 20px; /\* Tüm kenarlara 20px boşluk \*/
padding: 10px; /\* Tüm kenarlara 10px iç boşluk \*/

```
1. **Farklı Kenarlar İçin:**

```css
margin: 10px 20px 30px 40px;
/\* Sırasıyla üst, sağ, alt, sol \*/
padding: 10px 15px; 
/\* Üst-alt: 10px, sağ-sol: 15px \*/
1. **Tek Tek Tanımlamak:**

```
```css
margin-top: 10px;
margin-right: 20px;
margin-bottom: 30px;
margin-left: 40px;
padding-top: 5px;
padding-right: 10px;
padding-bottom: 15px;
padding-left: 20px;

```
-----
**Örnekler**

**1. Margin ile Dış Boşluk Ayarlama**

```css
div {
`    `margin: 20px;
`    `background-color: lightblue;
}

```
**Sonuç:** Div öğesi diğer öğelerden 20px uzaklıkta.

-----
**2. Padding ile İç Boşluk Ayarlama**

```css
div {
`    `padding: 15px;
`    `background-color: lightgreen;
}

```
**Sonuç:** İçerik ile kenarlar arasında 15px boşluk.

-----
**3. Hem Margin Hem Padding Kullanımı**

```css
div {
`    `margin: 20px;
`    `padding: 10px;
`    `background-color: lightcoral;
}

```
**Sonuç:** Öğenin dışı ile diğer öğeler arasında 20px, içerik ile kenarlar arasında 10px boşluk.

-----
**HTML ve CSS Örneği**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
.margin-ornek {
`            `margin: 20px;
`            `background-color: lightblue;
`        `}
.padding-ornek {
`            `padding: 20px;
`            `background-color: lightgreen;
`        `}
.margin-padding-ornek {
`            `margin: 30px;
`            `padding: 15px;
`            `background-color: lightcoral;
`        `}
`    `</style>
</head>
<body>
`    `<h1>CSS Margin ve Padding Örnekleri</h1>
`    `<div class="margin-ornek">Bu kutunun dışı 20px boşluklu.</div>
`    `<div class="padding-ornek">Bu kutunun içi 20px boşluklu.</div>
`    `<div class="margin-padding-ornek">Bu kutunun dışı 30px, içi 15px boşluklu.</div>
</body>
</html>

```
-----
**İpuçları**

1. **Boşluklarla Tasarımı Dengeli Hale Getirin:**
   **Margin** ile öğeleri birbirinden ayırabilir, **padding** ile içeriği daha düzenli gösterebilirsiniz.
1. **auto Kullanımı:**
   **margin: auto;**, öğeyi yatayda ortalamak için kullanılabilir.
1. **Responsive Tasarım:**
   Yüzdelik değerler kullanarak boşlukları ekran boyutuna göre ayarlayabilirsiniz.

**CSS Text ve Font Nedir?**

CSS, bir web sayfasındaki metinlerin görünümünü (rengi, boyutu, hizalaması, yazı tipi vb.) özelleştirmek için kullanılır. **Text (metin)** ile ilgili özellikler metnin düzenini, **font (yazı tipi)** ile ilgili özellikler ise yazı tipini ve stilini ayarlamak için kullanılır.

-----
**Metin (Text) ile İlgili Özellikler**

**1. color: Metin Rengini Belirler**

Metnin rengini ayarlamak için kullanılır.

```css
p {
`    `color: blue; /\* Metin rengi mavi olur \*/
}

```
**2. text-align: Metin Hizalaması**

Metni sola, sağa, ortaya veya iki yana yaslama yapabilirsiniz.

```css
p {
`    `text-align: center; /\* Metni ortaya hizalar \*/
}

```
Değerler:

- left: Sola hizalar (varsayılan).
- right: Sağa hizalar.
- center: Ortaya hizalar.
- justify: İki yana yaslar.

**3. text-decoration: Metin Çizgisi**

Metnin altını çizebilir, üstünü çizebilir veya çizgiyi kaldırabilirsiniz.

```css
a {
`    `text-decoration: none; /\* Alt çizgiyi kaldırır \*/
}

```
Değerler:

- none: Çizgi yok.
- underline: Altını çizer.
- line-through: Üstünü çizer.

**4. text-transform: Harflerin Biçimi**

Metindeki harflerin büyük/küçük olması için kullanılır.

```css
h1 {
`    `text-transform: uppercase; /\* Tüm harfleri büyük yapar \*/
}

```
Değerler:

- uppercase: Tüm harfleri büyük yapar.
- lowercase: Tüm harfleri küçük yapar.
- capitalize: Her kelimenin ilk harfini büyük yapar.

**5. letter-spacing ve word-spacing: Harf ve Kelime Aralığı**

- letter-spacing: Harfler arasındaki boşluğu ayarlar.
- word-spacing: Kelimeler arasındaki boşluğu ayarlar.

```css
p {
`    `letter-spacing: 2px; /\* Harfler arasında 2px boşluk \*/
`    `word-spacing: 5px; /\* Kelimeler arasında 5px boşluk \*/
}

```
**6. line-height: Satır Yüksekliği**

Metin satırları arasındaki mesafeyi belirler.

```css
p {
`    `line-height: 1.5; /\* Satırlar arasında 1.5 kat boşluk \*/
}

```
-----
**Font (Yazı Tipi) ile İlgili Özellikler**

**1. font-family: Yazı Tipini Ayarlar**

Metnin yazı tipini seçmek için kullanılır.

```css
p {
`    `font-family: Arial, sans-serif; /\* Arial yazı tipini kullanır \*/
}

```
Not: Birden fazla yazı tipi belirtebilirsiniz. Tarayıcı ilk mevcut olanı kullanır.

**2. font-size: Yazı Boyutunu Ayarlar**

Metnin boyutunu ayarlamak için kullanılır.

```css
p {
`    `font-size: 16px; /\* Yazı boyutu 16 piksel \*/
}

```
Değerler:

- **Pixel (px):** Sabit bir boyut.
- **Yüzde (%):** Orantılı boyut.
- **Em:** Ebeveyn öğeye göre boyut.

**3. font-weight: Yazının Kalınlığını Ayarlar**

Metnin ince veya kalın olmasını sağlar.

```css
p {
`    `font-weight: bold; /\* Kalın yazı \*/
}

```
Değerler:

- normal: Normal kalınlık.
- bold: Kalın.
- lighter: Daha ince.
- 100-900: Sayıya göre kalınlık (100 çok ince, 900 çok kalın).

**4. font-style: Yazının Eğikliği**

Metni italik yapar.

```css
p {
`    `font-style: italic; /\* Yazıyı italik yapar \*/
}

```
Değerler:

- normal: Normal yazı.
- italic: İtalik yazı.
- oblique: Hafif eğik yazı.

**5. font-variant: Küçük Büyük Harf Yazımı**

Metni küçük büyük harf şeklinde biçimlendirir.

```css
p {
`    `font-variant: small-caps; /\* Küçük harfler büyük gibi görünür \*/
}

```
-----
**Örnek**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
`        `h1 {
`            `font-family: Arial, sans-serif;
`            `font-size: 24px;
`            `font-weight: bold;
`            `color: darkblue;
`            `text-align: center;
`            `text-transform: uppercase;
`        `}
`        `p {
`            `font-family: "Times New Roman", serif;
`            `font-size: 18px;
`            `line-height: 1.6;
`            `text-align: justify;
`            `letter-spacing: 1px;
`        `}
`        `a {
`            `color: red;
`            `text-decoration: underline;
`        `}
`    `</style>
</head>
<body>
`    `<h1>CSS Metin ve Yazı Tipi</h1>
`    `<p>Bu bir örnek paragraf. Yazı boyutu, rengi ve hizalaması ayarlanmıştır. CSS ile metni istediğiniz gibi düzenleyebilirsiniz.</p>
`    `<a href="#">Bu bir bağlantı metnidir.</a>
</body>
</html>

```
-----
**İpuçları**

1. **Okunaklılık:** Yazı tipi ve boyutunu kullanıcıların rahat okuyabileceği şekilde seçin.
1. **Tutarlılık:** Tüm web sayfasında benzer yazı tipleri ve boyutlar kullanarak düzenli bir görünüm sağlayın.
1. **Responsive Tasarım:** Yazı boyutunu yüzde (%) veya em birimleriyle ayarlamak, mobil cihazlarda daha iyi sonuç verir.
