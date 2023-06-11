![Ekran Alıntısı](https://github.com/oktayagdag/NoteApp/assets/120986651/e9f7942f-c005-4d9e-b05c-5f8f33a4a35b)


# NoteApp

Düşüncelerinizin ve notlarınızın güvende olduğu, organize bir şekilde saklanabileceği kullanıcı dostu bir not defteri uygulaması arıyorsanız, aradığınızı buldunuz! NoteApp ile not alma deneyiminizi geliştirmek için tasarlanmış harika bir uygulama.

NoteApp ile kağıt üzerinde notlarınızı taşımak veya kaybetmek zorunda kalmadan, not alma deneyiminizi dijital bir seviyeye taşıyın. Hayatınızı düzenleyin, verimliliğinizi artırın ve önemli bilgileri her zaman yanınızda bulundurun. Notlarınızı tutmanın ve organize etmenin keyfini çıkarın!

Tasarım düzeni ile üst bilgi çubuğunda uygulama adını, araç çubuğunda yeni sayfa oluşturma ve kaydetme gibi temel işlevleri, not alanında metin girişi, alt bilgi alanında uygulama sürüm bilgisini ve ders menüsünde seçilebilecek farklı ders seçeneklerini sağlar. Tasarım, arka plan rengi, kenarlık ve öğelerin hizalaması gibi stil özellikleriyle görsel olarak etkileyici bir görünüm sunar.


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

## Üst Bilgi Çubuğu (Header Bar):
- İlk border etiketi (#FF383737 arka plan rengi) bu bölümü oluşturur.
- İçinde bir DockPanel bulunur. DockPanel, içindeki öğeleri yatay olarak hizalar.
- DockPanel içinde bir resim (Image) ve bir etiket (Label) yer alır.
- Resim, "images/icon.png" dosyasından alınır ve 24x24 boyutuna sahiptir.
- Etiket, "Not Defteri" metnini içerir ve beyaz renkte görüntülenir.

```xml
  <Border Background="#FF383737" Grid.Column="0" Grid.Row="0">
     <Grid>
         <Grid.RowDefinitions>
             <RowDefinition/>
               </Grid.RowDefinitions>
                 <Border Grid.Row="0">
                    <DockPanel VerticalAlignment="Center">
                        <Image Source="images/icon.png" Height="24" Width="24" VerticalAlignment="Center" Margin="5,0,0,0"/>
                        <Label Content="Not Defteri" Foreground="White" Margin="5" VerticalAlignment="Center" FontSize="13" bFontWeight="Bold"/>
                    </DockPanel>
         </Border>
     </Grid>
</Border>
```
## Araç Çubuğu (Toolbar):
- İkinci border etiketi (#FF383737 arka plan rengi) bu bölümü oluşturur.
- İçinde bir Grid yer alır. Grid, iki sütunlu bir düzen sağlar.
- İki düğme (Button) içerir:
 - İlk düğme, "images/newpage.png" resmiyle birlikte "Yeni Sayfa" metnini içeren bir StackPanel içerir.
 - İkinci düğme, "images/save.png" resmiyle birlikte "Kaydet" metnini içeren bir StackPanel içerir.

```xml
 <Border Background="#FF383737" Grid.Column="1" Grid.Row="0">
            <Grid>
                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="100" />
                    <ColumnDefinition Width="100" />
                </Grid.ColumnDefinitions>
                <Button  Background="#FF383737" Grid.Column="0">
                    <StackPanel Orientation="Horizontal" Margin="4">
                        <Image Source="images/newpage.png" Width="24" Height="24"/>
                        <Label Foreground="White" Padding="0" VerticalAlignment="Center"  Margin="5" >Yeni Sayfa</Label>
                    </StackPanel>
                </Button>
                <Button  Background="#FF383737" Grid.Column="1">
                    <StackPanel Orientation="Horizontal" Margin="4">
                        <Image  Source="images/save.png" Width="24" Height="24" />
                        <Label Foreground="White" Padding="0" VerticalAlignment="Center" Margin="5">Kaydet</Label>
                    </StackPanel>
                </Button>
            </Grid>
        </Border>
```

## Not Alanı (Note Area):
- Üçüncü border etiketi (#FF383737 arka plan rengi) bu bölümü oluşturur.
- İçinde bir Grid yer alır. Grid, iki satırlı bir düzen sağlar.
- İlk satır, düğmelerden oluşan bir Grid içerir:
 - Dört düğme içeren bir alt Grid yer alır. Bu düğmeler, sayfa silme, sayfa adını değiştirme, yazı boyutu ve yazı rengi gibi işlevleri temsil eder.
 - Her düğme bir resim ve bir etiket içeren bir StackPanel ile stilize edilmiştir.
- İkinci satır, metin giriş alanı olarak TextBox öğesini içerir:
 - TextBox, 10 birimlik iç boşluk (Padding), arka plan rengi (#FF2D2B2B), yazı rengi (Foreground) olarak beyaz ve metin kaydırma (TextWrapping) özelliklerine sahiptir.

```xml
   <Border Background="#FF383737" Grid.Column="1" Grid.Row="1">
            <Grid>
                <Grid.RowDefinitions>
                    <RowDefinition Height="30"/>
                    <RowDefinition Height="*"/>
                </Grid.RowDefinitions>

                <Grid  Grid.Row="0">
                    <Grid>
                        <Grid.ColumnDefinitions>
                            <ColumnDefinition Width="100"/>
                            <ColumnDefinition Width="150"/>
                            <ColumnDefinition Width="150"/>
                            <ColumnDefinition Width="150"/>
                        </Grid.ColumnDefinitions>
                        <Button  Background="#FF383737" Grid.Column="0">
                            <StackPanel Orientation="Horizontal" Margin="4">
                                <Image Source="images/delete.png"/>
                                <Label Foreground="White" Padding="0" VerticalAlignment="Center">Sayfayı Sil</Label>
                            </StackPanel>
                        </Button>
                        <Button  Background="#FF383737" Grid.Column="1">
                            <StackPanel Orientation="Horizontal" Margin="4">
                                <Image Source="images/rename.png"/>
                                <Label Foreground="White" Padding="0" VerticalAlignment="Center">Yeniden Adlandır</Label>
                            </StackPanel>
                        </Button>
                        <Button  Background="#FF383737" Grid.Column="2">
                            <StackPanel Orientation="Horizontal" Margin="4">
                                <Image Source="images/size.png"/>
                                <Label Foreground="White" Padding="0" VerticalAlignment="Center">Yazı Boyutu</Label>
                            </StackPanel>
                        </Button>
                        <Button  Background="#FF383737" Grid.Column="3">
                            <StackPanel Orientation="Horizontal" Margin="4">
                                <Image Source="images/color.png"/>
                                <Label Foreground="White" Padding="0" VerticalAlignment="Center">Yazı Rengi</Label>
                            </StackPanel>
                        </Button>
                    </Grid>
                </Grid>

                <TextBox Grid.Row="1" Padding="10" Height="Auto" Width="Auto" Background="#FF2D2B2B" Foreground="White" TextWrapping="Wrap" AcceptsReturn="True" HorizontalAlignment="Stretch"/>
            </Grid>
        </Border>
```


