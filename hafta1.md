# 1.Hafta: Frontend Geliştirme ve Html-Css'e Giriş

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

- **HTML nedir?**

- **Tanım:** HyperText Markup Language, web sayfalarının iskeletini oluşturan işaretleme dilidir.
- **Doğası:** HTML, web tarayıcılarının web sayfalarını görüntülemek için anladığı bir dil.

- **Temel HTML yapısı:** 
    - **DOCTYPE:** HTML belgesinin türünü belirtir.
  
    - **html Etiketi:** Sayfadaki tüm içerikleri içine alan en dıştaki etikettir. Bir nevi her şeyi kapsayan büyük kutu gibi düşünebilirsin.
  
    - **head Etiketi:** Sayfanın arka planda çalışan, izleyicilere görünmeyen bilgilerini içerir. Örneğin, sayfanın adı, arama motorlarının anlayacağı açıklamalar ve tasarım için kullanılan dosyalar burada yer alır.

    - **body Etiketi:** Sayfada gördüğün her şey buradadır. Metinler, resimler, videolar ve diğer tüm içerikler body etiketi içinde bulunur.

- **Metin etiketleri:**
    - **hr :** bir satır çizgi çeker

    - **br :** bir satır boşluk bırakır

    - **strong :** kalın yapar

    - **b :** kalın yapar

   - **strong ve bFarkı:** strong metni kalın yapmasının yanı sıra, bu metne daha fazla anlam ve önem katar. Tarayıcılar genelde metni yine kalın olarak gösterir, ancak ekran okuyucular bu metni daha vurgulu şekilde okuyabilir ve metnin önemli olduğunu belirtir. b etiketi ise sadece görsel bir vurgudur ve metnin anlamı üzerinde bir etkisi yoktur.

    - **i :** italic yapar

    - **mark :**  yazı üzerine sarı şerit çeker

- **Uygulama:** Basit bir kişisel tanıtım sayfası oluşturma

    ```html
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

- **Sıralı ve sırasız listeler:**
    - **ol (ordinary list), ul (unordinary list) :** ol 1,2,3 a,b,c şeklinde numaralı veya sıralı listeler, ul noktalarla listeler sıralı değildir.
    - **Bağlantılar:** <a href="...">
    - **Resimler:** <img src="..." alt="..."> 

- **Liste Yapısı Örnek :**

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

- **Uygulama:** Hobi listesi ve favori web sitelerine bağlantılar içeren bir sayfa oluşturma

- **Mini Proje**
•	Öğrenciler, öğrendikleri tüm HTML etiketlerini kullanarak çok sayfalı basit bir kişisel web sitesi oluşturacak
•	Ana sayfa  ve ilgi alanları sayfası içermeli