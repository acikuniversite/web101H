# 2.Hafta: HTML Yapıları ve Tablolar

# 1-HTML Tabloları

- **Tablo yapısı:**
    - **table, th, td, tr, rowspan - colspan:**
    - **tablo, th, caption :** tablo başlıkarı
    - **td :** satırlardaki datalar
    - **tr :** row satır 
    - **rowspan :** satırları birleştirip başlığı hizalar 
    - **colspan :** sütunları birleştirip başlığı hizalar

**Uygulama:** Ders programı oluşturma

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

- **•	Form yapısı** 
- **•	Metin girişi** 
- **•	Seçim elemanları**
- **•	Butonlar**  

- **•	Uygulama:** Basit bir iletişim formu oluşturma

# 3-Semantik HTML ve Sayfa Yapısı
-**•	Konu:**  Sayfa yapısını oluşturma ve bölümlere ayırma 
-**•	Semantik etiketler:**
    -**Article:** Kendi başına anlamlı bir yazı veya içerik parçasını ifade eder. Örneğin, bir blog yazısı veya haber makalesi.
    -**Section:** Bir konuyu ya da içeriği düzenlemek için kullanılan bir bölüm. Sayfayı konulara göre ayırmak için kullanılır.
    -**Nav:** Sayfadaki menü veya bağlantılarla gezinme kısmıdır. Örneğin, bir site içi menü veya yönlendirme bağlantıları burada olur.
    -**Aside:** Ana içerikten bağımsız, ek bilgi veya yan bilgi içeren bölümdür. Örneğin, bir makalenin yanındaki küçük notlar veya reklamlardır.
    -**Footer:** Sayfanın en alt kısmıdır. Genelde iletişim bilgileri, telif hakları, sosyal medya bağlantıları gibi şeyler burada bulunur.
    -**Header:** Sayfanın ya da bir bölümün üst kısmıdır. Genellikle başlıklar, logolar veya menü bağlantıları içerir.

![Semantic Html Örneği]([https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiJnp5jBUlXTjj-AgoqYdPNAH0i4XvyOWeJLl3IVYwLzApd5vonev2Z5NPNggLRtp7GbseNUjKb8B5b0mzdvT3o_GS-3g-NGgcxdsUEjbVFWwbC4dp7n71k0w_GWl-qH_voeHf-LZfMjjKpdW8OEDpMIhG0azdNt9FAJEy5vBclZepigSPH7QdvXV-wpc4/s627/SemanticHTML.jpg](https://www.google.com/url?sa=i&url=https%3A%2F%2Fmuratbilginer.net%2Ffrontend-developer-roadmap-html-5-tutorial-27-semantik-etiketler-div-elementi-2%2F&psig=AOvVaw261zUQXG1uv6QEOnAisJyQ&ust=1728126710199000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCMjEjOnL9IgDFQAAAAAdAAAAABAE))
    
- **•	Uygulama:** Önceki projeyi semantik etiketlerle yeniden düzenleme
