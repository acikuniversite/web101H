# 1.	Hafta: Frontend Geliştirme ve Html-Css'e Giriş

- **HTML (HyperText Markup Language):** Web sayfalarının iskeletini oluşturur. Yapı ve içerik sağlamak için kullanılır.
    
    ```html
    <h1>Merhaba Dünya</h1>
    <p>Bu bir paragraftır.</p>
    
    ```
    
- **CSS (Cascading Style Sheets):** Web sayfalarının görünümünü ve düzenini tasarlamak için kullanılır. Renkler, yazı tipleri, düzenler ve diğer stil özelliklerini belirler.
    
    ```css
    h1 {
      color: blue;
      text-align: center;
    }
    
    p {
      font-size: 16px;
    }
    
    ```
    
- **JavaScript:** Web sayfalarına dinamik özellikler ve etkileşim eklemek için kullanılır. Olaylar, animasyonlar ve veri işleme gibi işlemleri gerçekleştirir.
    
    ```jsx
    document.querySelector('h1').addEventListener('click', function() {
      alert('Başlık tıklandı!');
    });
    
    ```
# 1- HTML Temelleri

**•	HTML nedir?**

- **Tanım:** HyperText Markup Language, web sayfalarının iskeletini oluşturan işaretleme dilidir.
- **Doğası:** HTML, web tarayıcılarının web sayfalarını görüntülemek için anladığı bir dil.
- 
**•	Temel HTML yapısı:** <!DOCTYPE html>, <html>, <head>, <body>
- **DOCTYPE:** HTML belgesinin türünü belirtir. Örneğin: `<!DOCTYPE html>`
-**html Etiketi:** Sayfadaki tüm içerikleri içine alan en dıştaki etikettir. Bir nevi her şeyi kapsayan büyük kutu gibi düşünebilirsin.
-**head Etiketi:** Sayfanın arka planda çalışan, izleyicilere görünmeyen bilgilerini içerir.
  Örneğin, sayfanın adı, arama motorlarının anlayacağı açıklamalar ve tasarım için kullanılan dosyalar burada yer alır.
-**body Etiketi:** Sayfada gördüğün her şey buradadır. Metinler, resimler, videolar ve diğer tüm içerikler body etiketi içinde bulunur.
-**•	Metin etiketleri:** <h1> - <h6>, <p>, <br>, <strong>, <em> 
**`hr :`** bir satır çizgi çeker

**`br :`** bir satır boşluk bırakır

**`strong :`** kalın yapar

**`b :`** kalın yapar

**`strong` ve `b`Farkı:** <strong> metni kalın yapmasının yanı sıra, bu metne daha fazla anlam ve önem katar.
Tarayıcılar genelde metni yine kalın olarak gösterir, ancak ekran okuyucular bu metni daha vurgulu şekilde okuyabilir ve
metnin önemli olduğunu belirtir. <b> etiketi ise sadece görsel bir vurgudur ve metnin anlamı üzerinde bir etkisi yoktur.

**`i :`** italic yapar

**`mark :`**  yazı üzerine sarı şerit çeker

**•	Uygulama:** Basit bir kişisel tanıtım sayfası oluşturma
```html
    <!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>Benim İlk Sayfam</title>
</head>
<body>
    <h1>Merhaba, Ben [İsim]</h1>
    <h2>Hakkımda</h2>
    <p>Bu benim ilk <strong>HTML</strong> sayfam.</p>
    <p><mark>Ben web geliştirme öğreniyorum ve çok heyecanlıyım!</mark></p>
    <p>Ben web geliştirme öğreniyorum ve çok heyecanlıyım!</p>
    <p>Ben web geliştirme öğreniyorum ve çok heyecanlıyım!</p>
</body>
</html>
```
# 2-HTML Listeleri ve Bağlantılar
**•	Sıralı ve sırasız listeler:** <ul>, <ol>, <li>
**ol (ordinary list), ul (unordinary list) :** ol 1,2,3 a,b,c şeklinde numaralı veya sıralı listeler,
ul noktalarla listeler sıralı değildir.
**•	Bağlantılar:** <a href="...">
**•	Resimler:** <img src="..." alt="..."> 

**Liste Yapısı Örnek :**

´´´html
    <ol type="1">
        <li>
            İç Donanım Birimleri
            <ol type="I">
                <li>Anakart</li>
                <li>İşlemci</li>
                <li>Bellek</li>
            </ol>
        </li>
        <li>
            Dış Donanım Birimleri
            <ol type="1">
                <li>Monitor
                    <ol type="a">
                        <li>LCD</li>
                        <li>LED</li>
                    </ol>
                </li>
                <li>Klavye</li>
                <li>Fare</li>
            </ol>
        </li>
    </ol>
´´´

**•	Uygulama:** Hobi listesi ve favori web sitelerine bağlantılar içeren bir sayfa oluşturma

**Mini Proje**
•	Öğrenciler, öğrendikleri tüm HTML etiketlerini kullanarak çok sayfalı basit bir kişisel web sitesi oluşturacak
•	Ana sayfa  ve ilgi alanları sayfası içermeli

# 2.	Hafta: HTML Yapıları ve Tablolar
# 1-HTML Tabloları
**•	Tablo yapısı:** <table>, <tr>, <th>, <td>, <caption>
**table, th, td, tr, rowspan - colspan:**
**tablo, th, caption :** tablo başlıkarı
**td :** satırlardaki datalar
**tr :** row satır 
**rowspan :** satırları birleştirip başlığı hizalar 
**colspan :** sütunları birleştirip başlığı hizalar

**•	Uygulama:** Ders programı oluşturma

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

# 2-Formlar ve Giriş Elemanları

**•	Form yapısı:** <form>
**•	Metin girişi:** <input type="text">, <textarea>
**•	Seçim elemanları:** <input type="radio">, <input type="checkbox">, <select>
**•	Butonlar:** <input type="submit">, <button> 

**•	Uygulama:** Basit bir iletişim formu oluşturma

# 3-Semantik HTML ve Sayfa Yapısı
**•	Konu:** Sayfa yapısını oluşturma ve bölümlere ayırma 
**•	Semantik etiketler:** <header>, <nav>, <main>, <article>, <section>, <aside>, <footer>
    **Article (<article></article>)**: Kendi başına anlamlı bir yazı veya içerik parçasını ifade eder. Örneğin, bir blog yazısı veya haber makalesi.
    **Section (<section></section>):** Bir konuyu ya da içeriği düzenlemek için kullanılan bir bölüm. Sayfayı konulara göre ayırmak için kullanılır.
    **Nav (<nav></nav>):** Sayfadaki menü veya bağlantılarla gezinme kısmıdır. Örneğin, bir site içi menü veya yönlendirme bağlantıları burada olur.
    **Aside (<aside></aside>):** Ana içerikten bağımsız, ek bilgi veya yan bilgi içeren bölümdür. Örneğin, bir makalenin yanındaki küçük notlar veya reklamlardır.
    **Footer (<footer></footer>):** Sayfanın en alt kısmıdır. Genelde iletişim bilgileri, telif hakları, sosyal medya bağlantıları gibi şeyler burada bulunur.
    **Header (<header></header>):** Sayfanın ya da bir bölümün üst kısmıdır. Genellikle başlıklar, logolar veya menü bağlantıları içerir.

    ![Semantic Html Örneği]([https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiJnp5jBUlXTjj-AgoqYdPNAH0i4XvyOWeJLl3IVYwLzApd5vonev2Z5NPNggLRtp7GbseNUjKb8B5b0mzdvT3o_GS-3g-NGgcxdsUEjbVFWwbC4dp7n71k0w_GWl-qH_voeHf-LZfMjjKpdW8OEDpMIhG0azdNt9FAJEy5vBclZepigSPH7QdvXV-wpc4/s627/SemanticHTML.jpg](https://www.google.com/url?sa=i&url=https%3A%2F%2Fmuratbilginer.net%2Ffrontend-developer-roadmap-html-5-tutorial-27-semantik-etiketler-div-elementi-2%2F&psig=AOvVaw261zUQXG1uv6QEOnAisJyQ&ust=1728126710199000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCMjEjOnL9IgDFQAAAAAdAAAAABAE))
    
**•	Uygulama:** Önceki projeyi semantik etiketlerle yeniden düzenleme

# 3.	Hafta: CSS'e Giriş
# 1- CSS Temelleri
**•	CSS nedir ve neden kullanılır?**
**•	CSS ekleme yöntemleri:** Inline, Internal, External
**•	Temel CSS seçicileri:** element, class, id
**•	Renk ve arka plan özellikleri**
**•	Uygulama:** HTML sayfalarına temel stiller ekleme

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    color: #333;
}

h1 {
    color: #0066cc;
    text-align: center;
}

.menu {
    background-color: #333;
    color: white;
    padding: 10px;
}

.menu a {
    color: white;
    text-decoration: none;
    margin-right: 15px;
}
```

# 2-CSS Box Model ve Sayfa Düzeni

**•	Margin, padding, border kavramları**
**•	Genişlik ve yükseklik ayarlama**
**•	Display özellikleri:** block, inline, inline-block

**•	Basit konumlandırma:** static, relative, absolute

**•	Uygulama:** Önceki projenin sayfa düzenini CSS ile geliştirme
**CSS Box Model:** Bu modelde, her HTML elementinin bir kutu gibi davranır ve bu kutunun içerik **(content)**,
dolgu **(padding)**, kenarlık **(border)** ve kenar boşluğu **(margin)** olmak üzere dört bölümden oluşur.
**•	Margin (Kenar Boşluğu):** Elemanın dışındaki boşluk. Diğer elementlerle arasındaki mesafeyi belirler.
**•	Border (Kenarlık):** Padding ve içeriğin etrafındaki çizgi.
**•	Padding (Dolgu):** İçerik ile border arasındaki iç boşluk.
**•	Content (İçerik):** Elemanın asıl içeriğinin bulunduğu alan.
Örnek:
```css
div {
    margin: 10px;
    border: 2px solid black;
    padding: 15px;
    width: 300px;
}
```

**Genişlik ve Yükseklik Ayarlama:** Elementlerin boyutlarını kontrol etmek için kullanılır.
**•	width:** Genişlik
**•	height:** Yükseklik

Örnek:
```css
img {
    width: 100px;
    height: 100px;
}
```

**Display Özellikleri:** Elementlerin nasıl görüntüleneceğini belirler.
**•	block:** Elementi blok seviyesi yapar (tam genişlik alır, yeni satırda başlar)
**•	inline:** Elementi satır içi yapar (sadece içeriği kadar yer kaplar)
**•	inline-block:** Inline gibi davranır ama blok özellikleri alabilir
Örnek:
```css
span {
    display: block;
}
div {
    display: inline;
}
```

**Basit Konumlandırma:** Elementlerin sayfadaki konumunu belirler.
**•	static:** Varsayılan değer, normal akışta kalır
**•	relative:** Normal konumuna göre göreceli olarak konumlandırılır
**•	absolute:** En yakın konumlandırılmış üst elemente göre konumlandırılır
**•	fixed:** Görüntü alanına göre sabit konumda kalır
Örnek:

```css
.relative {
    position: relative;
    left: 30px;
    top: 20px;
}
.absolute {
    position: absolute;
    right: 0;
    bottom: 0;
}
```

Bu kavramları uygulamalı olarak göstermek için, basit bir sayfa düzeni oluşturabiliriz:

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>CSS Düzen Örneği</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }
        .container {
            width: 80%;
            margin: 0 auto;
        }
        header {
            background-color: #333;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            background-color: #f2f2f2;
            padding: 10px 0;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            text-align: center;
        }
        nav ul li {
            display: inline;
            margin: 0 10px;
        }
        .content {
            padding: 20px 0;
        }
        .sidebar {
            float: right;
            width: 30%;
            background-color: #f9f9f9;
            padding: 20px;
            box-sizing: border-box;
        }
        .main {
            float: left;
            width: 70%;
            padding-right: 20px;
            box-sizing: border-box;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            clear: both;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Benim Web Sitem</h1>
        </div>
    </header>
    <nav>
        <div class="container">
            <ul>
                <li>Ana Sayfa</li>
                <li>Hakkımda</li>
                <li>İletişim</li>
            </ul>
        </div>
    </nav>
    <div class="container">
        <div class="content">
            <div class="sidebar">
                <h3>Yan Menü</h3>
                <p>Burası yan menü içeriği.</p>
            </div>
            <div class="main">
                <h2>Ana İçerik</h2>
                <p>Burası ana içerik bölümü. CSS ile düzenlenmiş bir sayfa örneği.</p>
            </div>
        </div>
    </div>
    <footer>
        <div class="container">
            <p>&copy; 2024 Benim Web Sitem</p>
        </div>
    </footer>
</body>
</html>
```

**Bu örnekte:**
**•	Box Model:** Her element için padding ve margin kullanılmıştır.
**•	Genişlik ve Yükseklik:** Container, sidebar ve main içerik için width kullanılmıştır.
**•	Display:** Nav menüsünde inline elementler kullanılmıştır.
**•	Konumlandırma:** Sidebar ve main içerik float ile yan yana konumlandırılmıştır.

# 3-Kapsamlı Proje ve Tekrar
•	Öğrenciler, öğrendikleri tüm HTML ve CSS bilgilerini kullanarak kişisel bir blog veya portfolyo sitesi oluşturacak
