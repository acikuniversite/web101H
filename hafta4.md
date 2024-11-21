# 4.Hafta: Div ve Form Yapıları

# `<div>` Nedir?

`<div>` kelimesi "division" yani "bölüm" kelimesinden gelir. HTML'de sayfayı bölümlere ayırmak için kullanılır. Kısaca, "içine başka öğeler koyabileceğiniz bir kutu" gibidir. Görünüşte bir etkisi yoktur (yani ekrana bir şey yazmaz), ama düzenleme ve tasarım yapmak için çok önemlidir.

## `<div>` Nerelerde Kullanılır?

### Sayfayı Düzenlemek:
Sayfanın farklı bölümlerini (örneğin, üst menü, içerik, alt bilgi) ayrı ayrı yönetmek için kullanılır.

### CSS ile Stil Vermek:
Bir `<div>` etiketiyle istediğiniz bölüme renk, boyut veya kenarlık ekleyebilirsiniz.

### Grup Oluşturmak:
Benzer içerikleri (örneğin, birden fazla paragraf veya resim) bir grup haline getirmek için.

## Örnek 1: Basit Kullanım

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        .kutu {
            width: 200px;
            height: 100px;
            background-color: lightblue;
            border: 2px solid blue;
        }
    </style>
</head>
<body>
    <div class="kutu">
        Bu bir kutudur!
    </div>
</body>
</html>

```
# HTML Formları Nedir?

Formlar, kullanıcıdan bilgi toplamak (örneğin, ad, şifre, e-posta vb.) ve bu bilgileri sunucuya göndermek için kullanılır.  
Formlar, `<form>` etiketiyle oluşturulur.

## Formun Temel Yapısı

```html
<form action="işlem_adresi" method="GET veya POST">
    <!-- Form elemanları buraya eklenir -->
</form>
- `action`: Verilerin gönderileceği adresi belirtir.  
- `method`: Verilerin nasıl gönderileceğini belirtir:
    - `GET`: Veriler URL'ye eklenir (kısa ve az hassas bilgiler için).
    - `POST`: Veriler gizli olarak gönderilir (daha güvenlidir).

## Form Elemanları

- `<input>`: Kullanıcıdan bilgi almak için kullanılır.  
  Tipleri (type):
    - `text`: Tek satırlık metin giriş kutusu.
    - `password`: Şifre kutusu (yazılan karakterler gizlenir).
    - `email`: E-posta adresi girişi için.
    - `number`: Sadece sayı girişi yapılabilir.
    - `radio`: Seçeneklerden birini seçmek için.
    - `checkbox`: Birden fazla seçenek seçmek için.
    - `submit`: Formu göndermek için bir düğme.
    - `button`: Normal bir düğme.
    
## Örnek

```html
<form action="/submit" method="POST">
    Adınız: <input type="text" name="ad"><br>
    Şifre: <input type="password" name="sifre"><br>
    <button type="submit">Gönder</button>
</form>
- **`<label>`**: Giriş kutularına açıklama ekler.

```
**Kullanımı:**

```html
<label for="ad">Adınız:</label>
<input type="text" id="ad" name="ad">
### `<textarea>`: Uzun Metinler İçin Kutu Oluşturur

```
**Örnek:**

```html
<textarea name="mesaj" rows="4" cols="50"></textarea>
### `<select>` ve `<option>`: Açılır Menü Oluşturur

```
**Örnek:**

```html
<label for="sehir">Şehir:</label>
<select id="sehir" name="sehir">
    <option value="ankara">Ankara</option>
    <option value="istanbul">İstanbul</option>
    <option value="izmir">İzmir</option>
</select>

```
### `<button>`: Formda Bir Düğme Oluşturur

**Örnek:**

```html
<button type="submit">Gönder</button>

```
