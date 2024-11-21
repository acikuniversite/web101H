# 2.Hafta: HTML Etiketleri ve Tablolar

# HTML Temel Etiketler

- **`<hr>`**: Bir yatay çizgi çeker. Sayfanın farklı bölümlerini ayırmak için kullanılır.
- **`<br>`**: Satır sonu bırakır. Bu etiketi kullanarak bir satır boşluk bırakabilirsiniz.
- **`<strong>` ve `<b>`**: Her ikisi de metni kalın yapar. Ancak `<strong>` anlam açısından vurgulamak için, `<b>` ise sadece görsel olarak kalın yapmak için kullanılır.
- **`<i>`**: Metni italik yapar, yani eğik yazı.
- **`<mark>`**: Yazı üzerine sarı renkli bir arka plan (şerit) ekler, genellikle vurgulamak için kullanılır.
- **`src`**: Bir resmin kaynağını belirtir. Örneğin, `<img src="image.jpg">` etiketi ile bir resmi sayfada gösterirsiniz.
- **`<center>`**: İçine aldığı tüm öğeleri sayfa ortasında hizalar.

# HTML Etiketleriyle Listeleme

- **`<ol>`**: Sıralı liste oluşturur (1, 2, 3, ...).
- **`<ul>`**: Sırasız liste oluşturur (● gibi işaretler ile).
- **`<li>`**: Liste öğesi ekler. Hem sıralı hem de sırasız listelerde kullanılır.

# Tablolar

- **`<table>`**: Tabloyu başlatır.
- **`<tr>`**: Tablo satırıdır. Tabloda bir satır eklemek için kullanılır.
- **`<th>`**: Tablo başlık hücresidir. Genellikle tabloların üst kısmındaki başlıklar için kullanılır.
- **`<td>`**: Tablo veri hücresidir. Satırlardaki verileri eklemek için kullanılır.
- **`rowspan` ve `colspan`**: Bu özellikler, hücrelerin birden fazla satır veya sütun boyunca birleşmesini sağlar.
- **Uygulama:** Ders programı oluşturma

```html
<table border="1">
    <caption>Haftalık Ders Programı</caption>
    <tr>
        <th>Saat</th>
        <th>Pazartesi</th>
        <th>Salı</th>
        <th>Çarşamba</th>
    </tr>
    <tr>
        <td>09:00-10:30</td>
        <td>Matematik</td>
        <td>Türkçe</td>
        <td>Fen Bilgisi</td>
    </tr>
    <tr>
        <td>10:45-12:15</td>
        <td colspan="2">Web Tasarım</td>
        <td>İngilizce</td>
    </tr>
</table>

```

# Blok ve Satır İçi Elemanlar

- **Blok Elemanlar (block)**: Sayfanın tamamını kaplar. Örneğin, `<div>`, `<p>` gibi etiketler blok elemanlardır.
- **Satır İçi Elemanlar (inline)**: Sadece gerektiği kadar yer kaplar, diğer öğelerle aynı satırda devam eder. Örneğin, `<span>`, `<a>` gibi etiketler satır içi elemanlardır.

# CSS Seçiciler ve Özellikler

- **`#` (ID Seçici)**: Belirli bir öğeyi ID'sine göre seçer. Örneğin, `#header` bir öğeyi `id="header"` olan öğeyi seçer.
- **`.` (Class Seçici)**: Belirli bir öğeyi class'ına göre seçer. Örneğin, `.button` bir öğeyi `class="button"` olan öğeyi seçer.
- **`*` (Genel Seçici)**: Tüm öğelere stil verir.

# CSS Etkileşimli Özellikler

- **`:hover`**: Bu özellik, fare imleci bir öğenin üzerine geldiğinde çalışır. Örneğin, bir butona tıklandığında renginin değişmesini sağlamak için `:hover` kullanabilirsiniz.

# 3-Semantik HTML ve Sayfa Yapısı
- **Konu:**  Sayfa yapısını oluşturma ve bölümlere ayırma 
- **Semantik etiketler:**
    - **Article:** Kendi başına anlamlı bir yazı veya içerik parçasını ifade eder. Örneğin, bir blog yazısı veya haber makalesi.
    - **Section:** Bir konuyu ya da içeriği düzenlemek için kullanılan bir bölüm. Sayfayı konulara göre ayırmak için kullanılır.
    - **Nav:** Sayfadaki menü veya bağlantılarla gezinme kısmıdır. Örneğin, bir site içi menü veya yönlendirme bağlantıları burada olur.
    - **Aside:** Ana içerikten bağımsız, ek bilgi veya yan bilgi içeren bölümdür. Örneğin, bir makalenin yanındaki küçük notlar veya reklamlardır.
    - **Footer:** Sayfanın en alt kısmıdır. Genelde iletişim bilgileri, telif hakları, sosyal medya bağlantıları gibi şeyler burada bulunur.
    - **Header:** Sayfanın ya da bir bölümün üst kısmıdır. Genellikle başlıklar, logolar veya menü bağlantıları içerir.

![Semantic Html Örneği](https://muratbilginer.net/wp-content/uploads/2022/09/2021-10-11_01-13-04.png)
    
- **Uygulama:** Önceki projeyi semantik etiketlerle yeniden düzenleme
