# Katkı rehberi

Tr AI-Daw; ses motoru, beste/düzenleme, miks, eklentiler, AI/MCP araçları, masaüstü uygulaması, platform paketleri, test ve belgeleriyle geliştirilen tam bir DAW projesidir. Bu alanların tümünden katkı bekliyoruz; Türkçe yerelleştirme bunlardan yalnızca biridir.

## Nereden başlamalı?

- Hata veya özellik önerisi: [Issues](https://github.com/TrKeyboarder/tr-ai-daw/issues)
- Tasarım ve genel ürün tartışmaları: [Discussions](https://github.com/TrKeyboarder/tr-ai-daw/discussions)
- Geliştirme kapsamı: [ROADMAP.md](./ROADMAP.md) ve [GitHub Project panosu](https://github.com/users/TrKeyboarder/projects/2)
- İlk katkı: etiketlenmiş küçük bir Issue, test iyileştirmesi veya dokümantasyon düzeltmesi seçebilirsin.

Büyük bir değişikliğe başlamadan önce yaklaşımı bir Issue veya Discussion'da konuşmak, çalışmanın ürün hedefiyle uyumlu olmasını sağlar.

## Pull request süreci

1. Depoyu fork et ve `main` dışında açıklayıcı bir dal aç.
2. Değişikliği odaklı tut; ilgili issue veya kullanım senaryosunu açıkla.
3. Kapsamına uygun kontrolleri çalıştır ve sonuçları PR'da belirt.
4. Pull request'ini `main` dalına gönder; olağan katkılar bir onaylı incelemeden sonra birleştirilir. Depo yöneticileri bu koruma kuralından muaftır.

Yeni bir commit, daha önceki inceleme onayını geçersiz kılabilir. Geri bildirimleri ele alırken testleri ve kullanıcı etkisini güncelle.

## Geliştirme kontrolleri

Ön uç değişiklikleri:

```bash
pnpm install --frozen-lockfile
pnpm build
```

Daemon/Rust değişiklikleri (gerekli yerel sistem bağımlılıkları kuruluysa):

```bash
cargo fmt --all -- --check
cargo test -p ai-daw-daemon --lib --no-default-features
```

Her PR'da tüm komutları çalıştırmak gerekmez; ilgili olanları seç ve çalıştırmadıklarını not et. Derlenmiş paketleri, model ağırlıklarını, kimlik bilgilerini veya kişisel ses dosyalarını commit etme.

## Çeviri katkıları

Türkçe arayüz için doğal ve tutarlı dil kullan; mevcut anahtarları ve `{name}` biçimindeki yer tutucuları koru. Yeni terimlerde diğer ekranlardaki kullanımı izle ve bağlamı PR açıklamasında belirt. Çeviri çalışmaları, uygulama ve ses altyapısı geliştirmesiyle aynı ürün yol haritasının parçasıdır.

## Kaynak ve lisans

Bu proje [heshengtao/ai-daw](https://github.com/heshengtao/ai-daw) kod tabanı üzerine kuruludur. Kaynak dosyalardaki telif/lisans bildirimlerini ve [NOTICE](./NOTICE) atıflarını koru; yeni üçüncü taraf bağımlılık veya içeriklerin lisansını açıkça belirt.
