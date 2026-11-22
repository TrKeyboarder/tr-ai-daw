# Tr AI-Daw geliştirme yol haritası

Tr AI-Daw, ses üretiminden ajan entegrasyonuna kadar tam bir DAW ürününü geliştirmeyi hedefler. Bu belge sabit teslim tarihleri veya garanti edilmiş sürüm vaatleri içermez; ürün kapsamını ve topluluğun katkı sunabileceği alanları görünür kılar. Öncelikler [GitHub Project panosunda](https://github.com/users/TrKeyboarder/projects/2) ve Issues bölümünde tartışılır.

## Mevcut ürün temeli

- Tauri masaüstü kabuğu ve Vue 3 tabanlı arayüz; tarayıcı istemcisi de desteklenir.
- Rust tabanlı ses zamanlaması, DSP/render ve proje yönetimi.
- Çok kanallı ses/MIDI düzenleme, piyano rulosu, otomasyon, mikser ve dışa aktarma.
- VST3/CLAP barındırma, yerleşik ses araçları ve SoundFont desteği.
- MCP ve `aidaw` CLI ile çalışan uygulama oturumunu bir AI ajanından yönetme.
- İsteğe bağlı, yerel çalışan ses analizi ve üretim iş akışları.

## Açık geliştirme alanları

### Ses motoru ve performans

- Gerçek zamanlı oynatma, zamanlama ve ses aygıtı uyumluluğu.
- DSP, miks, yönlendirme, efekt ve render kalitesi.
- Düşük gecikme, kaynak kullanımı, kararlılık ve hata ayıklama araçları.

### Beste ve DAW iş akışları

- Klip, nota, otomasyon ve proje düzenleme deneyimi.
- Kayıt, dışa aktarma, içe aktarma ve oturum kurtarma.
- Klavye erişimi, kullanılabilirlik ve büyük projelerde verimlilik.

### Eklentiler ve ses kütüphaneleri

- VST3/CLAP ana bilgisayar uyumluluğu ve eklenti editörleri.
- Eklenti tarama/yönetim, presetler, SoundFont ve yerleşik efektler.
- Platformlar arasında tutarlı davranış ve uyumluluk testleri.

### AI, MCP ve ajan iş akışları

- Araç kapsamı, doğrulama, geri alma ve kullanıcı onayı deneyimi.
- Ses analizi, MIDI ve diğer yaratıcı iş akışlarının iyileştirilmesi.
- MCP istemcileriyle birlikte çalışabilirlik ve daha iyi hata raporları.

### Uygulama, dil ve topluluk

- Linux, Windows ve macOS için kurulum, güncelleme ve paketleme.
- Başlangıç deneyimi, erişilebilirlik, dokümantasyon ve test altyapısı.
- Türkçe ve İngilizce arayüz kalitesi; yeni diller için sürdürülebilir yerelleştirme.

## Bir başlığı ileri taşımak

Bir geliştirme önerisi, hata veya tasarım tartışması için [Issue](https://github.com/TrKeyboarder/tr-ai-daw/issues) ya da [Discussion](https://github.com/TrKeyboarder/tr-ai-daw/discussions) aç. Uygulama değişiklikleri küçük ve odaklı pull request'ler olarak gönderilir; ilgili testleri ve kullanıcı etkisini açıklamak incelemeyi kolaylaştırır. Katkı adımları [CONTRIBUTING.md](./CONTRIBUTING.md) içinde.
