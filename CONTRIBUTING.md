# Katkı rehberi

Tr AI-Daw'a hoş geldin! Çeviri, dokümantasyon, hata düzeltmesi, test ve kullanılabilirlik iyileştirmelerine açığız. İlk katkın olacaksa küçük bir yazım veya çeviri düzeltmesiyle başlayabilirsin.

## Başlamadan önce

- Hata bildirimleri ve özellik önerileri için [Issues](https://github.com/TrKeyboarder/tr-ai-daw/issues), açık uçlu fikir alışverişi için [Discussions](https://github.com/TrKeyboarder/tr-ai-daw/discussions) kullan.
- Büyük bir değişikliğe başlamadan önce bir Issue veya Discussion açıp yaklaşımı konuş; bu, emeğinin projeyle uyumlu olmasına yardımcı olur.
- Bu depo, [heshengtao/ai-daw](https://github.com/heshengtao/ai-daw) projesinin Apache-2.0 lisanslı topluluk sürümüdür. Upstream telif ve lisans bildirimlerini koru; üçüncü taraf içeriklerin lisansını ayrıca belirt.

## Pull request iş akışı

1. Depoyu fork et ve `main` dışında açıklayıcı bir dal aç.
2. Değişikliği tek bir amaca odaklı ve mevcut proje biçemine uygun tut.
3. İlgili kontrolleri çalıştır ve pull request açıklamasında sonuçlarını yaz.
4. Pull request'ini `main` dalına gönder. Birleştirme için en az bir onaylı inceleme gerekir; yeni bir commit inceleme onayını geçersiz kılabilir.

`main` doğrudan katkı dalı değildir. Pull request'ler topluluk incelemesinden geçer; lütfen inceleme geri bildirimlerini yapıcı şekilde ele al.

## Yararlı kontroller

Ön uç değişiklikleri için:

```bash
pnpm install --frozen-lockfile
pnpm build
```

Daemon/Rust değişiklikleri için, yerel sistem bağımlılıkları kuruluysa:

```bash
cargo fmt --all -- --check
cargo test -p ai-daw-daemon --lib --no-default-features
```

Her değişiklik için tüm kontrolleri çalıştırmak zorunlu değildir; kapsamına uygun olanları seç ve çalıştırmadıklarını PR açıklamasında belirt. Derlenmiş uygulama paketlerini, yerel model ağırlıklarını, kimlik bilgilerini veya kişisel ses dosyalarını commit etme.

## Türkçe çeviri

- Mevcut çeviri anahtarlarını ve `{name}` gibi yer tutucuları aynen koru.
- Arayüzde doğal, anlaşılır ve tutarlı Türkçe kullan; teknik terimlerde proje içindeki mevcut kullanımı izle.
- Çevrilmemiş metinler yedek dillere dönebildiğinden yeni metinlerin anlamını ve bağlamını PR açıklamasında belirt.
