**CSS ID, Class ve Genel Seçiciler Nedir?**

CSS'te HTML elemanlarına stil vermek için seçiciler kullanılır. Bu seçiciler sayesinde hangi öğenin stil alacağını belirleriz. **ID**, **Class**, ve **Genel Seçiciler** bu amaçla kullanılan en temel seçicilerdendir.

-----
**1. ID Seçici**

- **ID**, bir HTML elemanını **benzersiz** bir şekilde tanımlamak için kullanılır.
- Her sayfada bir **ID** sadece bir kez kullanılabilir.
- **CSS'te ID seçici # ile tanımlanır.**

**Örnek**

**HTML:**

```html
<div id="benimID">Bu bir ID örneğidir.</div>

```

**CSS:**

```css

#benimID {
    color: blue;
    font-weight: bold;
}

```

**Çıktı:**

- ID'si benimID olan <div> mavi renkte ve kalın yazılır.

**Neden Kullanılır?**

- Tek bir öğeye özel stil vermek gerektiğinde kullanılır.
-----
**2. Class Seçici**

- **Class**, birden fazla öğeye uygulanabilir.
- Bir öğeye birden fazla **class** atanabilir.
- **CSS'te Class seçici . ile tanımlanır.**

**Örnek**

**HTML:**

```html
<p class="paragraf">Bu bir paragraf örneğidir.</p>
<p class="paragraf">Bu başka bir paragraf örneğidir.</p>

```

**CSS:**

```css
.paragraf {
    color: green;
    font-size: 18px;
}

```
**Çıktı:**

- class="paragraf" olan tüm <p> etiketleri yeşil renkte ve 18px boyutunda yazılır.

**Neden Kullanılır?**

- Birden fazla öğeye aynı stili vermek gerektiğinde kullanılır.
-----
**3. Genel Seçiciler**

Genel seçiciler, tüm öğelere veya belirli bir gruptaki öğelere stil vermek için kullanılır.

**a. Evrensel Seçici (\*)**

- Tüm öğelere stil verir.

```css

\* {
    margin: 0;
    padding: 0;
}

```

**Örnek:** Tüm öğelerin dış ve iç boşluklarını sıfırlar.

**b. Etiket Seçicileri**

- Belirli bir HTML etiketine stil verir.

```css
h1 {
    color: red;
}

```

**Örnek:** Sayfadaki tüm ` <h1> ` etiketleri kırmızı renkte yazılır.

**c. Birleşik Seçiciler**

- Aynı anda birden fazla seçici kullanılır.

```css
h1, p {
    font-family: Arial, sans-serif;
}

```

**Örnek:** Tüm `<h1>` ve `<p>` etiketleri aynı yazı tipiyle yazılır.

**d. Alt Seçiciler**

- Belirli bir öğenin içindeki başka bir öğeyi hedefler.

```css
    .container p {
    color: purple;
}

```

**Örnek:** class="container" olan bir öğenin içindeki <p> etiketleri mor olur.

-----
**ID ve Class Karşılaştırması**

|**Özellik**|**ID**|**Class**|
| :- | :- | :- |
|**Benzersizlik**|Her sayfada yalnızca bir tane|Birden fazla öğeye atanabilir|
|**CSS Sembolü**|#|.|
|**Kullanım Alanı**|Tekil öğeler|Grup öğeleri|

-----
**Örneklerle Anlayalım**

**HTML Kodu:**

```html
<div id="header">Bu ID ile seçildi.</div>
<p class="content">Bu class ile seçildi.</p>
<p class="content">Bu da aynı class ile seçildi.</p>
<div>
    <p>Bu sadece etiket seçiciyle seçilir.</p>
</div>

```

**CSS Kodu:**

```css
#header {
    background-color: lightblue;
    padding: 10px;
    text-align: center;
}
.content {
    font-size: 18px;
    color: darkgreen;
}
p {
    font-style: italic;
}

```

**Sonuç:**

1. id="header" olan <div> açık mavi bir arka plana ve ortalanmış bir metne sahip olur.
1. class="content" olan <p> öğeleri koyu yeşil renkte ve 18px boyutunda yazılır.
1. Tüm <p> etiketleri italik olur.
-----
**İpuçları**

1. **ID'yi Az Kullanın:** ID'yi yalnızca benzersiz, özel durumlarda kullanın.
1. **Class ile Esneklik:** Stil grupları oluşturmak için class kullanın.
1. **Genel Seçicileri Dikkatli Kullanın:** \* tüm öğeleri seçtiği için performansı etkileyebilir.
-----
**Tam Örnek**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
    #header {
        background-color: lightcoral;
        color: white;
        text-align: center;
        padding: 15px;
        }
.highlight {
        color: orange;
        font-weight: bold;
        }
    p {
        font-family: "Times New Roman", serif;
        }
    \* {
        margin: 0;
        padding: 0;
        }
    </style>
</head>
<body>
    <div id="header">Merhaba, CSS ID ve Class Öğreniyoruz!</div>
    <p class="highlight">Bu bir örnek metindir.</p>
    <p>Bu başka bir paragraftır.</p>
</body>
</html>

```

**Sonuç:**

- id="header" olan bölüm açık kırmızı arka plana ve beyaz metne sahip olur.
- class="highlight" olan metin turuncu ve kalın yazılır.
- Diğer tüm <p> etiketleri varsayılan stil ile gösterilir.

**CSS Renklendirme Yöntemleri**

Web tasarımında renkler, sayfanın görünümünü ve estetiğini belirleyen önemli unsurlardır. **CSS** ile renkleri farklı yöntemlerle tanımlayabiliriz. İşte CSS'te renkleri tanımlamanın çeşitli yolları:

-----
**1. Renk İsimleri (Color Names)**

CSS'te, yaygın kullanılan renklerin **adlarıyla** renkleri belirtebiliriz. Örneğin, "red", "blue", "green" gibi.

**Örnek:**

```css
body {
    background-color: blue; /\* Arka plan rengi mavi \*/
    color: white; /\* Yazı rengi beyaz \*/
}

```
**Desteklenen Renk İsimleri:**

- red, blue, green, yellow, black, white, gray vb.
-----
**2. Hexadecimal (Hex) Renk Kodu**

Hexadecimal (kısaca **hex**) renk kodları, renkleri altı haneli bir sayı ile temsil eder. Bu kodlar **#** işareti ile başlar ve her iki haneli sayı, renklerin kırmızı (R), yeşil (G) ve mavi (B) bileşenlerini gösterir.

- **Format:** #RRGGBB

**Örnek:**

```css
body {
    background-color: #FF5733; /\* Bu renk turuncuya yakın bir kırmızı \*/
}

```
Buradaki #FF5733 şu şekilde açıklanabilir:

- FF: Kırmızı (red) bileşeni, 255 (maksimum değeri)
- 57: Yeşil (green) bileşeni, 87
- 33: Mavi (blue) bileşeni, 51
-----
**3. RGB Renk Modeli**

**RGB (Red, Green, Blue)**, renkleri üç ana renk olan kırmızı (red), yeşil (green) ve mavi (blue) bileşenlerinin bir araya gelmesiyle oluşturur. RGB değerleri 0 ile 255 arasında değişebilir.

- **Format:** rgb(kırmızı, yeşil, mavi)

**Örnek:**

```css
body {
    background-color: rgb(255, 87, 51); /\* Aynı renk, RGB ile belirtilmiş \*/
}

```

- Burada, 255 kırmızı, 87 yeşil, 51 mavi bileşenlerinin yoğunluğunu gösterir.
-----
**4. RGBA (RGB + Alpha) Renk Modeli**

**RGBA**, **RGB** modeline **alpha** (şeffaflık) kanalını ekler. Alpha değeri, rengin ne kadar şeffaf olduğunu belirler. Değer 0 (tam şeffaf) ile 1 (tam opak) arasında değişir.

- **Format:** rgba(kırmızı, yeşil, mavi, alfa)

**Örnek:**

```css
body {
    background-color: rgba(255, 87, 51, 0.5); /\* Yarı şeffaf turuncu \*/
}

```
- Burada, 0.5 alpha değeri, rengin %50 şeffaf olduğunu gösterir.
-----
**5. HSL (Hue, Saturation, Lightness) Renk Modeli**

**HSL**, bir rengin **tonunu (Hue)**, **doygunluğunu (Saturation)** ve **açıklığını (Lightness)** belirtir. HSL modelinde, renkler daha anlaşılır bir şekilde tanımlanabilir.

- **Format:** hsl(ton, doygunluk%, açıklık%)
  - **Ton**: 0 ile 360 arasında, renk çarkındaki yerini belirtir (0 = kırmızı, 120 = yeşil, 240 = mavi, vb.)
  - **Doygunluk**: 0% (gri) ile 100% (tam doygun renk) arasında.
  - **Açıklık**: 0% (karanlık) ile 100% (tam aydınlık) arasında.

**Örnek:**

```css
body {
    background-color: hsl(9, 100%, 60%); /\* Turuncuya yakın bir renk \*/
}

```
- Burada, 9 ton değeri turuncu rengini, 100% doygunluk ve 60% açıklık değeri ile renk belirlenmiştir.
-----
**6. HSLA (HSL + Alpha) Renk Modeli**

**HSLA**, HSL modeline alpha kanalını ekler. Bu, renge şeffaflık ekler.

- **Format:** hsla(ton, doygunluk%, açıklık%, alfa)

**Örnek:**

```css
body {
    background-color: hsla(9, 100%, 60%, 0.5); /\* Yarı şeffaf turuncu \*/
}

```
-----
**7. CSS Renk Kısaltmaları**

Hex renk kodları 3 haneli olarak da yazılabilir. Örneğin, #FFF yerine #FFFFFF yazılabilir. Aynı şekilde, bazı CSS renk adları da kısaltılabilir.

**Örnek:**

- #F00 = #FF0000 (kırmızı)
- #000 = #000000 (siyah)
-----
**Renk Seçicilerin Karşılaştırılması**

|**Yöntem**|**Örnek**|**Açıklama**|
| :- | :- | :- |
|**Renk İsimleri**|red, blue|Kolay, ama sınırlı renkler.|
|**Hex**|#FF5733|Altı haneli renk kodları, yaygın ve esnek.|
|**RGB**|rgb(255, 87, 51)|Kırmızı, yeşil, mavi bileşenleriyle renkler.|
|**RGBA**|rgba(255, 87, 51, 0.5)|RGB + şeffaflık, yarı şeffaf renkler.|
|**HSL**|hsl(9, 100%, 60%)|Ton, doygunluk, açıklık ile renk seçimi.|
|**HSLA**|hsla(9, 100%, 60%, 0.5)|HSL + şeffaflık, yarı şeffaf tonlar.|

-----
**Tam Örnek**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
`        `body {
`            `background-color: #FF5733; /\* Hex \*/
`            `color: rgb(255, 255, 255); /\* RGB \*/
`        `}
`        `h1 {
`            `color: hsl(120, 100%, 50%); /\* HSL \*/
`        `}
`        `p {
`            `color: rgba(0, 0, 255, 0.5); /\* RGBA \*/
`        `}
`    `</style>
</head>
<body>
`    `<h1>Başlık</h1>
`    `<p>Bu bir paragraf. Yarı şeffaf mavi renkte!</p>
</body>
</html>

```
**Sonuç:**

- Arka plan **turuncu** (#FF5733).
- Yazı rengi **beyaz** (rgb(255, 255, 255)).
- Başlık rengi **yeşil** (hsl(120, 100%, 50%)).
- Paragraf rengi ise **yarı şeffaf mavi** (rgba(0, 0, 255, 0.5)).
-----
**Sonuç**

CSS ile renkler farklı yöntemlerle tanımlanabilir. **Hex**, **RGB**, **HSL**, **RGBA** gibi seçenekler sayesinde, istediğiniz renkleri web sayfanızda kullanabilirsiniz. Her yöntem, farklı ihtiyaçlara göre avantajlar sağlar.

**CSS Border Radius Nedir?**

- **border-radius**, HTML öğelerinin köşelerini yuvarlatmak için kullanılan bir CSS özelliğidir.
- Kare veya dikdörtgen bir öğeyi yuvarlak köşeli hale getirmek ya da tamamen bir daireye dönüştürmek için kullanılır.
-----
**Nasıl Kullanılır?**

1. **Temel Yazım:**

```css
border-radius: değer;

```
1. **Değer Tipleri:**
   1. **Pixel (px):** Kesin bir uzunluk belirler.
      Örnek: border-radius: 10px;
   1. **Yüzde (%):** Öğenin boyutuna göre yuvarlama yapar.
      Örnek: border-radius: 50%; (Bu genelde bir öğeyi tam bir daire yapmak için kullanılır.)
-----
**Örnekler**

**1. Köşeleri Hafif Yuvarlatmak**

```css
div {
`    `border: 2px solid black;
`    `border-radius: 10px;
}

```
**Sonuç:** Köşeler hafif yuvarlanır.

-----
**2. Tamamen Daire Yapmak**

```css
div {
`    `width: 100px;
`    `height: 100px;
`    `background-color: lightblue;
`    `border-radius: 50%;
}

```
**Sonuç:** Daire şeklinde bir öğe oluşturulur.

-----
**3. Sadece Belirli Köşeleri Yuvarlatmak**

- **border-top-left-radius**: Sol üst köşeyi yuvarlatır.
- **border-top-right-radius**: Sağ üst köşeyi yuvarlatır.
- **border-bottom-left-radius**: Sol alt köşeyi yuvarlatır.
- **border-bottom-right-radius**: Sağ alt köşeyi yuvarlatır.

```css
div {
`    `border: 2px solid black;
`    `border-top-left-radius: 20px;
`    `border-bottom-right-radius: 30px;
}

```
**Sonuç:** Sadece sol üst ve sağ alt köşe yuvarlanır.

-----
**4. Farklı Köşelere Farklı Değerler Vermek**

```css
div {
`    `border: 2px solid black;
`    `border-radius: 10px 20px 30px 40px; /\* Sırasıyla sol üst, sağ üst, sağ alt, sol alt \*/
}

```
**Sonuç:** Her köşe farklı oranlarda yuvarlanır.

-----
**Basit HTML ve CSS Örneği**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
.kare {
`            `width: 150px;
`            `height: 150px;
`            `background-color: lightcoral;
`            `border: 2px solid black;
`            `margin: 10px;
`        `}
.yuvarlak {
`            `width: 150px;
`            `height: 150px;
`            `background-color: lightblue;
`            `border-radius: 50%;
`            `border: 2px solid black;
`            `margin: 10px;
`        `}
.ozel {
`            `width: 150px;
`            `height: 150px;
`            `background-color: lightgreen;
`            `border-radius: 20px 40px 10px 30px;
`            `border: 2px solid black;
`            `margin: 10px;
`        `}
`    `</style>
</head>
<body>
`    `<h1>CSS Border Radius Örnekleri</h1>
`    `<div class="kare">Kare</div>
`    `<div class="yuvarlak">Yuvarlak</div>
`    `<div class="ozel">Özel</div>
</body>
</html>

```
-----
**Bu Örnekte Neler Oluyor?**

- **Kare:** Yuvarlama yok, sadece düz bir dikdörtgen.
- **Yuvarlak:** **border-radius: 50%;** kullanılarak tam bir daire oluşturulmuş.
- **Özel:** Köşelere farklı değerler verilerek değişik bir şekil oluşturulmuş.
-----
**İpuçları**

1. **Tam Daire Yapmak İçin:**
   **border-radius: 50%;** ve genişlik ile yükseklik eşit olmalıdır.
1. **Deneme Yanılma ile Şekillendirme:**
   Farklı **pixel** ve **%** değerlerini deneyerek öğenizin köşelerini istediğiniz gibi şekillendirebilirsiniz.
1. **Hangi Köşelerin Yuvarlanacağını Seçmek:**
   Belirli köşeler için **border-top-left-radius** gibi özellikler kullanabilirsiniz.
