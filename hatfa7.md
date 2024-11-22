# 7.Hafta: CSS Özellikleri (parent-child, Overflow(Taşma))

**CSS Parent-Child (Ebeveyn-Çocuk) İlişkisi Nedir?**

Bir HTML belgesinde, öğeler birbirleriyle **ebeveyn (parent)** ve **çocuk (child)** ilişkisi kurar. **CSS**'te, bu ilişkiyi kullanarak bir ebeveyn öğeye stil verirken onun içindeki (çocuk) öğeleri de etkileyebiliriz.

-----
**Ebeveyn ve Çocuk Nedir?**

Diyelim ki HTML kodunda şöyle bir yapı var:

```html
<div class="parent">
`    `<p class="child">Bu bir paragraf.</p>
`    `<p class="child">Bu da başka bir paragraf.</p>
</div>

```
Burada:

- **<div>**: Ebeveyn (Parent) öğe.
- **<p>**: Çocuk (Child) öğeler.

**Ebeveyn:** Kendisinin içine başka öğeler alan elemandır.
**Çocuk:** Bir öğenin içinde bulunan elemandır.

-----
**CSS ile Ebeveyn ve Çocuk İlişkisi**

**1. Tüm Çocukları Etkilemek**

Bir ebeveynin tüm çocuklarını seçmek için **ebeveyn\_adı çocuk\_adı** yazılır.

Örnek:

```css
.parent p {
`    `color: blue; /\* Ebeveyn içindeki tüm <p> öğeleri mavi olur. \*/
}

```
**2. Sadece Doğrudan Çocukları Etkilemek**

Doğrudan çocukları seçmek için > operatörü kullanılır.

Örnek:

```css
.parent > p {
`    `color: red; /\* Sadece ebeveynin doğrudan içindeki <p> öğeleri kırmızı olur. \*/
}

```
**3. Tüm Torunları Etkilemek**

Ebeveynin altındaki her seviyedeki çocukları (torunları da dahil) seçmek için boşluk kullanılır.

Örnek:

```css
.parent p {
`    `font-size: 16px; /\* Ebeveyn içindeki her seviyedeki <p> öğeleri etkilenir. \*/
}

```
-----
**Örneklerle Anlayalım**

**HTML Kodu**

```html
<div class="parent">
`    `<h1>Başlık</h1>
`    `<div class="child">
`        `<p>Bu bir paragraf.</p>
`        `<span>Bu bir span.</span>
`    `</div>
</div>

```
**CSS Kodu**

```css
/\* Ebeveynin tüm çocuklarını etkiler \*/
.parent \* {
`    `border: 1px solid black; /\* Tüm alt öğelere siyah çerçeve ekler \*/
}
/\* Sadece doğrudan çocukları etkiler \*/
.parent > h1 {
`    `color: blue; /\* Sadece <h1> mavi olur \*/
}
/\* Belirli bir alt öğeyi etkiler \*/
.child span {
`    `background-color: yellow; /\* Sadece <span> öğesinin arka planı sarı olur \*/
}

```
-----
**Sonuç**

Bu kodlar şu görünüme neden olur:

- **Başlık** mavi renkte olur.
- **Paragraflar** ve diğer öğeler siyah çerçeve ile çevrilir.
- **Span** öğesi sarı arka plana sahip olur.
-----
**CSS Parent-Child Kullanım İpuçları**

1. **Hedefi Daraltın:** Gereksiz geniş stillerden kaçınmak için sadece ihtiyaç duyulan çocuk öğelere stil verin.
1. **Doğrudan Çocukları Seçmek:** > operatörünü kullanarak, sadece doğrudan çocukları etkileyebilirsiniz.
1. **CSS Sadelik:** Ebeveyn-çocuk ilişkisini etkili kullanarak kodlarınızı sade ve okunabilir hale getirin.
-----
**Tam Örnek**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
`        `/\* Ebeveynin tüm alt öğelerine stil \*/
.parent \* {
`            `margin: 10px;
`            `padding: 5px;
`        `}
`        `/\* Sadece doğrudan çocuk <h1> \*/
.parent > h1 {
`            `font-size: 24px;
`            `text-align: center;
`            `color: blue;
`        `}
`        `/\* Altındaki spesifik bir öğeye stil \*/
.child p {
`            `color: green;
`        `}
.child span {
`            `font-style: italic;
`        `}
`    `</style>
</head>
<body>
`    `<div class="parent">
`        `<h1>Parent Başlığı</h1>
`        `<div class="child">
`            `<p>Bu bir paragraf.</p>
`            `<span>Bu bir span.</span>
`        `</div>
`    `</div>
</body>
</html>

```
**CSS Overflow Konusu**

Web tasarımında **overflow** (taşma), bir öğenin içeriğinin, öğenin belirlenen boyutlarından taşması durumudur. Bu, genellikle bir kutunun içinde çok fazla içerik olduğunda ortaya çıkar. **CSS overflow** özelliği, bu taşmayı nasıl kontrol edebileceğimizi belirler.

**Overflow Nedir?**

Bir öğenin içine sığmayan içerikler, o öğenin sınırlarını taşabilir. Bu taşma, sayfanın düzenini bozabilir. **overflow** özelliği, taşan içeriğin nasıl görüntüleneceğini kontrol etmemizi sağlar.

**Overflow Özelliği**

**overflow** özelliği, dört farklı değerden birini alabilir:

1. **visible** (Varsayılan Değer)
1. **hidden**
1. **scroll**
1. **auto**

Her bir değerin ne işe yaradığını şu şekilde açıklayabiliriz:

-----
**1. overflow: visible;**

Bu, varsayılan değerdir. Eğer içerik kutuya sığmazsa, taşan içerik görünür ve kutuyu aşar.

**Örnek:**

```css
Kodu kopyala

div {

`    `width: 200px;

`    `height: 100px;

`    `overflow: visible;

`    `border: 1px solid black;

}

- **Taşan içerik görünecektir** ve kutunun dışına taşacaktır.
-----
**2. overflow: hidden;**

Bu değer, taşan içeriğin **gizlenmesini** sağlar. İçerik kutunun dışına taşarsa, dışarıdaki kısımlar **görünmez** olur.

**Örnek:**

```css
Kodu kopyala

div {

`    `width: 200px;

`    `height: 100px;

`    `overflow: hidden;

`    `border: 1px solid black;

}

- **Taşan içerik gizlenir** ve kullanıcı bunu göremez.
-----
**3. overflow: scroll;**

Bu değer, taşan içeriği **kaydırılabilir** hale getirir. İçerik taşarsa, dikey ve yatay kaydırma çubukları görünür.

**Örnek:**

```css
div {
`    `width: 200px;
`    `height: 100px;
`    `overflow: scroll;
`    `border: 1px solid black;
}

```
- **Kaydırma çubukları her zaman görünür** olur, içerik taşsa da taşmasa da.
-----
**4. overflow: auto;**

Bu değer, içerik taşarsa kaydırma çubuklarını **otomatik olarak** gösterir. Eğer içerik kutuya sığarsa, kaydırma çubuğu **görünmez** olur.

**Örnek:**

```css
div {
`    `width: 200px;
`    `height: 100px;
`    `overflow: auto;
`    `border: 1px solid black;
}

```
- Eğer içerik taşarsa, **kaydırma çubukları görünür** olur. Taşmazsa, kaydırma çubuğu görünmez.
-----
**Örneklerle Overflow Kullanımı**

```html
<!DOCTYPE html>
<html lang="en">
<head>
`    `<style>
.box {
`            `width: 200px;
`            `height: 100px;
`            `border: 1px solid black;
`        `}
.visible {
`            `overflow: visible;
`        `}
.hidden {
`            `overflow: hidden;
`        `}
.scroll {
`            `overflow: scroll;
`        `}
.auto {
`            `overflow: auto;
`        `}
`    `</style>
</head>
<body>
`    `<h3>Overflow: visible</h3>
`    `<div class="box visible">
`        `Bu kutunun içeriği taşarsa, taşan kısımlar dışarıya taşar. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
`    `</div>
`    `<h3>Overflow: hidden</h3>
`    `<div class="box hidden">
`        `Bu kutunun içeriği taşarsa, taşan kısımlar gizlenir. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
`    `</div>
`    `<h3>Overflow: scroll</h3>
`    `<div class="box scroll">
`        `Bu kutunun içeriği taşarsa, kaydırma çubukları görünür. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque vel sem nec nulla hendrerit facilisis non ac turpis.
`    `</div>
`    `<h3>Overflow: auto</h3>
`    `<div class="box auto">
`        `Bu kutunun içeriği taşarsa, kaydırma çubukları otomatik olarak görünür. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque vel sem nec nulla hendrerit facilisis non ac turpis.
`    `</div>
</body>
</html>

```
-----
**Özet:**

- **visible**: Taşan içerik görünür ve kutuyu aşar.
- **hidden**: Taşan içerik gizlenir, görünmez olur.
- **scroll**: İçerik taşarsa, her zaman kaydırma çubukları görünür.
- **auto**: İçerik taşarsa, kaydırma çubukları görünür, taşmazsa görünmez olur.
