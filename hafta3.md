# 3.Hafta: CSS'e Giriş

# 1- CSS Temelleri

- **CSS nedir ve neden kullanılır?**
- **CSS ekleme yöntemleri:** Inline, Internal, External
- **Temel CSS seçicileri:** element, class, id
- **Renk ve arka plan özellikleri**

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
- **Uygulama:** HTML sayfalarına temel stiller ekleme

# 2-CSS Box Model ve Sayfa Düzeni

- **Margin, padding, border kavramları**
- **Genişlik ve yükseklik ayarlama**
- **Display özellikleri:** block, inline, inline-block
- **Basit konumlandırma:** static, relative, absolute

- **Uygulama:** Önceki projenin sayfa düzenini CSS ile geliştirme

- **CSS Box Model:** Bu modelde, her HTML elementinin bir kutu gibi davranır ve bu kutunun içerik **(content)**,
dolgu **(padding)**, kenarlık **(border)** ve kenar boşluğu **(margin)** olmak üzere dört bölümden oluşur.
- **Margin (Kenar Boşluğu):** Elemanın dışındaki boşluk. Diğer elementlerle arasındaki mesafeyi belirler.
- **Border (Kenarlık):** Padding ve içeriğin etrafındaki çizgi.
- **Padding (Dolgu):** İçerik ile border arasındaki iç boşluk.
- **Content (İçerik):** Elemanın asıl içeriğinin bulunduğu alan.

Örnek:

    ```css
div {
    margin: 10px;
    border: 2px solid black;
    padding: 15px;
    width: 300px;
}

    ```

- **Genişlik ve Yükseklik Ayarlama:** Elementlerin boyutlarını kontrol etmek için kullanılır.
- **width:** Genişlik
- **height:** Yükseklik

Örnek:

    ```css
    img {
    width: 100px;
    height: 100px;
}
    ```

- **Display Özellikleri:** Elementlerin nasıl görüntüleneceğini belirler.
- **block:** Elementi blok seviyesi yapar (tam genişlik alır, yeni satırda başlar)
- **inline:** Elementi satır içi yapar (sadece içeriği kadar yer kaplar)
- **inline-block:** Inline gibi davranır ama blok özellikleri alabilir
Örnek:

    ```css
span {
    display: block;
}
div {
    display: inline;
}

    ```

- **Basit Konumlandırma:** Elementlerin sayfadaki konumunu belirler.
- **static:** Varsayılan değer, normal akışta kalır
- **relative:** Normal konumuna göre göreceli olarak konumlandırılır
- **absolute:** En yakın konumlandırılmış üst elemente göre konumlandırılır
- **fixed:** Görüntü alanına göre sabit konumda kalır
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

- **Bu örnekte:**
- **Box Model:** Her element için padding ve margin kullanılmıştır.
- **Genişlik ve Yükseklik:** Container, sidebar ve main içerik için width kullanılmıştır.
- **Display:** Nav menüsünde inline elementler kullanılmıştır.
- **Konumlandırma:** Sidebar ve main içerik float ile yan yana konumlandırılmıştır.

# 3-Kapsamlı Proje ve Tekrar
•	Öğrenciler, öğrendikleri tüm HTML ve CSS bilgilerini kullanarak kişisel bir blog veya portfolyo sitesi oluşturacak
