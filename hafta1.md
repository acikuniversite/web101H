# 1.Hafta: HTML Temelleri

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
- **Uygulama:** Basit bir kişisel tanıtım sayfası oluşturma

# 2-HTML Listeleri ve Bağlantılar

- **Sıralı ve sırasız listeler:**
    - **ol (ordinary list), ul (unordinary list) :** ol 1,2,3 a,b,c şeklinde numaralı veya sıralı listeler, ul noktalarla listeler sıralı değildir.
    - **Bağlantılar** 
    - **Resimler**  
- **Uygulama:** Hobi listesi ve favori web sitelerine bağlantılar içeren bir sayfa oluşturma

- **Mini Proje**
- •	Öğrenciler, öğrendikleri tüm HTML etiketlerini kullanarak çok sayfalı basit bir kişisel web sitesi oluşturacak
- •	Ana sayfa  ve ilgi alanları sayfası içermeli
