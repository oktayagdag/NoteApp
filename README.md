![Ekran Alıntısı](https://github.com/oktayagdag/NoteApp/assets/120986651/e9f7942f-c005-4d9e-b05c-5f8f33a4a35b)


# NoteApp

Düşüncelerinizin ve notlarınızın güvende olduğu, organize bir şekilde saklanabileceği kullanıcı dostu bir not defteri uygulaması arıyorsanız, aradığınızı buldunuz! NoteApp ile not alma deneyiminizi geliştirmek için tasarlanmış harika bir uygulama.

NoteApp ile kağıt üzerinde notlarınızı taşımak veya kaybetmek zorunda kalmadan, not alma deneyiminizi dijital bir seviyeye taşıyın. Hayatınızı düzenleyin, verimliliğinizi artırın ve önemli bilgileri her zaman yanınızda bulundurun. Notlarınızı tutmanın ve organize etmenin keyfini çıkarın!


## İşte NoteApp'ın Öne Çıkan Özellikleri

- Kullanıcı dostu arayüz ve minimalist tasarıma sahip.
- Hızlı ve etkili not oluşturabilirsiniz.
- Not içeriğine göre sayfalar oluşturarak notları kategorize edebilirsiniz.
- Kategorize edilen not sayfalarını, düzenleyebilir, yeniden adlandırabilir veya silebilirsiniz.
- Metin boyutunu ayarlayabilir, metinleri renklendirebilebilirsiniz.

## Neden Not Defteri'ni tercih etmelisiniz?
- **Kolay Kullanım**: Not Defteri, kullanıcı dostu bir arayüzle tasarlanmıştır, bu da notlarınızı hızla oluşturmanızı ve düzenlemenizi sağlar. Zaman kaybetmeden önemli bilgilerinizi kaydedebilirsiniz.
- **Organize Etme**: Notlarını kategorilere veya etiketlere göre düzenlemek, daha hızlı erişim sağlamanızı sağlar. Karmaşayı unutun, notlarınızı kolayca bulun!
- **Biçimlendirme Seçenekleri**: Zengin metin düzenleme araçları sayesinde notlarınızı biçimlendirebilir, renklendirebilir ve önemli bölümleri vurgulayabilirsiniz. Daha okunabilir ve düzenli bir not alma deneyimi için idealdir.
- **Güvenli ve Güvenilir**: Not Defteri, notlarınızın güvende kalmasını sağlamak için güçlü bir şifreleme ve parola koruma özelliği sunar. Hassas bilgilerinizin güvenliğini sağlayın.



## Kullanılan Teknolojiler
C# kodlama dili, Xaml tasarım dili kullanılarak geliştirildi.


## Ana Tasarım Düzeni
Tüm arayüz ana 2 satır ve ana 2 sütun ızgaraya ayrılarak tasarlandı.
Satırlardan ilki 40 yüksekliğe, ikincisi ise kalan tüm yüksekliğe sahip.
Sütunlardan ilki tüm genişliğin 2/8'ine, diğeri ise 6/8 ine sahip.

```xml
<Grid.RowDefinitions>
   <RowDefinition Height="40"/>
   <RowDefinition Height="*"/>
</Grid.RowDefinitions>
<Grid.ColumnDefinitions>
  <ColumnDefinition Width="2*"/>
  <ColumnDefinition Width="6*"/>
</Grid.ColumnDefinitions>
```



