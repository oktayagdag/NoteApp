![Ekran görüntüsü 2023-05-21 233601](https://github.com/oktayagdag/NoteApp/assets/120986651/94ee2803-6845-44d1-9bb5-0042aaaf68b9)

# NoteApp

Düşüncelerinizin ve notlarınızın güvende olduğu, organize bir şekilde saklanabileceği kullanıcı dostu bir not defteri uygulaması arıyorsanız, aradığınızı buldunuz! NoteApp, hayatınızı düzenlemek ve not alma deneyiminizi geliştirmek için tasarlanmış harika bir uygulama.

NoteApp ile kağıt üzerinde notlarınızı taşımak veya kaybetmek zorunda kalmadan, not alma deneyiminizi dijital bir seviyeye taşıyın. Hayatınızı düzenleyin, verimliliğinizi artırın ve önemli bilgileri her zaman yanınızda bulundurun. NoteApp ile notlarınızı tutmanın ve organize etmenin keyfini çıkarın!


## İşte NoteApp'ın Öne Çıkan Özellikleri

- Kullanıcı dostu arayüz ve minimalist tasarıma sahip.
- Hızlı ve etkili not oluşturabilirsiniz.
- Not içeriğine göre sayfalar oluşturarak notları kategorize edebilirsiniz.
- Kategorize edilen not sayfalarını, düzenleyebilir, yeniden adlandırabilir veya silebilirsiniz.
- Metin boyutunu ayarlayabilir, metinleri renklendirebilebilirsiniz.

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



