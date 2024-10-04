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

- **Form yapısı** 
- **Metin girişi** 
- **Seçim elemanları**
- **Butonlar**  

- **Uygulama:** Basit bir iletişim formu oluşturma

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
