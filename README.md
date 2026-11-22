<p align="center">
  <img src="./assets/readme/tr-ai-daw-hero.svg" width="100%" alt="Tr AI-Daw — açık kaynak dijital ses iş istasyonu">
</p>

<p align="center">
  <a href="https://github.com/TrKeyboarder/tr-ai-daw/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/TrKeyboarder/tr-ai-daw/ci.yml?branch=main&style=for-the-badge&label=CI" alt="CI durumu"></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/lisans-Apache--2.0-d72b4a?style=for-the-badge" alt="Apache 2.0 lisansı"></a>
  <a href="https://github.com/TrKeyboarder/tr-ai-daw/pulls"><img src="https://img.shields.io/badge/katkılar-açık-1f9d78?style=for-the-badge" alt="Katkılara açık"></a>
  <a href="https://github.com/TrKeyboarder/tr-ai-daw/discussions"><img src="https://img.shields.io/github/discussions/TrKeyboarder/tr-ai-daw?style=for-the-badge&label=topluluk" alt="GitHub tartışmaları"></a>
</p>

<p align="center">
  <a href="./README.md"><b>Türkçe</b></a> ·
  <a href="./README_EN.md"><b>English</b></a> ·
  <a href="https://github.com/heshengtao/ai-daw/blob/main/README_zh.md"><b>简体中文</b></a>
</p>

<h3 align="center">Müziğini üret. Düzenle. Miksle. Yapay zekânla birlikte çalış.</h3>

**Tr AI-Daw, tam kapsamlı ve geliştirilebilir bir dijital ses iş istasyonu (DAW) projesidir.** Beste ve düzenlemeden ses motoruna, miks ve eklenti barındırmadan yerel yapay zekâ ve MCP ajan iş akışlarına kadar uygulamanın tamamı bu deponun geliştirme alanıdır. Türkçe arayüz projenin önemli bir parçasıdır; projenin tamamı değildir.

Tr AI-Daw, [heshengtao/ai-daw](https://github.com/heshengtao/ai-daw) açık kaynak kod tabanı üzerine kurulmuş bağımsız bir topluluk ürünüdür. Hedefimiz hafif, yerel öncelikli ve insanların yapay zekâ ajanlarıyla aynı müzik oturumunda çalışabildiği bir DAW'ı geliştirmektir. Upstream projesiyle resmî bağlantımız veya onayımız yoktur; lisans ve kaynak atıflarını koruyoruz.

<p align="center">
  <img src="./assets/screenshots/01-arrange.png" width="100%" alt="Tr AI-Daw çok kanallı düzenleme zaman çizelgesi">
</p>

## Bir müzik üretim ortamı

Tr AI-Daw, yalnızca çeviri dosyalarından veya bir arayüz demosundan ibaret değildir. Düzenleme, çalma, miksleme ve dışa aktarma iş akışları; masaüstü ve tarayıcı arayüzüyle, ses motoru ve ajan araçlarıyla birlikte geliştirilen çalışan bir uygulamada buluşur.

### Beste ve düzenleme

- MIDI ve ses kliplerini çok kanallı zaman çizelgesinde düzenle; kes, taşı, kopyala ve değişiklikleri geri al.
- Piyano rulosunda notaları, hız değerlerini ve klipleri düzenle.
- Tempo, ölçü, döngü ve otomasyon değişikliklerini proje boyunca yönet.
- MIDI, MusicXML, WAV ve MP3 dışa aktar.

### Ses motoru, miks ve eklentiler

- Gerçek zamanlı ses oynatma, zamanlama, miks ve render altyapısı.
- Parça ve master kanallarında gain, pan, send, bus, mute/solo ve seviye ölçümü.
- Yerleşik sentezleyici ve efektler; VST3 ve CLAP eklenti barındırma.
- SoundFont kütüphaneleri, eklenti tarama ve eklenti yönetimi.

### Yerel yapay zekâ ve birlikte çalışma

- MCP sunucusu ve `aidaw` CLI ile bir ajan aynı projeyi okuyup düzenleyebilir; değişiklikler arayüzde görünür ve geri alınabilir.
- Yerel ses araçları tempo algılama, sesten MIDI üretme, vokal temizleme ve stem ayırma gibi işleri destekler.
- İsteğe bağlı büyük modeller yalnızca kullanıldığında indirilir; işlem yerel donanımda yürütülür.
- Aynı oturuma masaüstü uygulamasından veya tarayıcı arayüzünden erişilebilir.

<p align="center">
  <img src="./assets/screenshots/05-ai-panel.png" width="100%" alt="Yerel yapay zekâ ve MCP araçlarının bulunduğu Tr AI-Daw paneli">
</p>

## Geliştirme kapsamı

Tr AI-Daw'ın geliştirilmesi ürünün tüm katmanlarını kapsar. Aşağıdaki başlıklar katkıya açıktır; sabit tarihler veya yayımlanmış sürüm taahhütleri değildir:

- **Ses ve müzik motoru:** oynatma kararlılığı, zamanlama, DSP, miks ve render performansı.
- **DAW deneyimi:** beste, düzenleme, kayıt, otomasyon, proje yönetimi ve erişilebilirlik.
- **Eklenti ekosistemi:** VST3/CLAP uyumluluğu, eklenti keşfi, SoundFont ve efekt iş akışları.
- **AI ve MCP:** ajan araçları, müzik üretim iş akışları, yerel analiz ve kullanıcı denetimi.
- **Uygulama ve dağıtım:** Linux/Windows/macOS derlemeleri, kurulum, güncelleme ve bellek/başlangıç performansı.
- **Dil ve topluluk:** Türkçe/İngilizce arayüz, kullanım belgeleri, testler ve yeni katkıcıların projeye katılımı.

Önerileri ve iş başlıklarını [GitHub Project panosunda](https://github.com/users/TrKeyboarder/projects/2), hata/özellik bildirimlerini [Issues](https://github.com/TrKeyboarder/tr-ai-daw/issues) bölümünde takip ediyoruz. Fikir paylaşmak için [Discussions](https://github.com/TrKeyboarder/tr-ai-daw/discussions) herkese açık.

## Mimari

```text
Vue 3 arayüzü ── IPC / HTTP ── Rust daemon ── Ses motoru ve eklenti altyapısı
                                      │
                                      ├── MCP / aidaw CLI
                                      └── Yerel AI araçları
```

| Yol | Sorumluluk |
| --- | --- |
| `src/` | Vue 3 arayüzü; masaüstü ve tarayıcı istemcisi |
| `src-tauri/` | Tauri masaüstü kabuğu, yerel pencereler ve paketleme |
| `crates/daemon/` | Uygulama komutları, proje yönetimi, ses/eklenti koordinasyonu, MCP ve HTTP |
| `crates/engine/` | Ses zamanlaması, DSP ve render motoru |
| `crates/ipc/` | Arayüz, daemon, CLI ve MCP arasında paylaşılan komut/veri şeması |

## Başlarken

Bu depoda henüz yayımlanmış kurulum paketi yok; [Releases](https://github.com/TrKeyboarder/tr-ai-daw/releases) sayfası yeni sürümler için kullanılacaktır. Kaynak koddan geliştirme için Rust stable, Node.js 22+, pnpm 10 ve [Tauri sistem önkoşulları](https://v2.tauri.app/start/prerequisites/) gerekir.

```bash
git clone https://github.com/TrKeyboarder/tr-ai-daw.git
cd tr-ai-daw
pnpm install --frozen-lockfile
pnpm tauri dev
```

### Linux x86_64 için optimize Debian paketi

```bash
CARGO_BUILD_JOBS=1 \
CARGO_PROFILE_RELEASE_LTO=thin \
CARGO_PROFILE_RELEASE_CODEGEN_UNITS=1 \
AIDAW_TARGET=x86_64-unknown-linux-gnu \
pnpm tauri build --target x86_64-unknown-linux-gnu --bundles deb
```

Bu yapılandırma genel x86_64 uyumluluğunu korur; makineye özel işlemci bayrağı kullanmaz. Derleme hedefleri ve bağımlılıklar için Tauri [Linux önkoşulları](https://v2.tauri.app/start/prerequisites/) ile [upstream derleme notlarını](https://github.com/heshengtao/ai-daw#build-from-source) incele.

## Geliştirmeye katıl

Ses motoru, arayüz, miks, eklentiler, AI/MCP, test, performans, dokümantasyon ve çeviri: **ürünün her katmanına katkı bekliyoruz.** Yeniysen bir Issue veya Discussion aç; çözmek istediğin konu belli ise fork edip bir dalda geliştir ve pull request gönder.

- Katkı süreci ve yerel kontroller: [CONTRIBUTING.md](./CONTRIBUTING.md)
- Hata veya özellik önerisi: [Issues](https://github.com/TrKeyboarder/tr-ai-daw/issues)
- Tasarım ve genel fikirler: [Discussions](https://github.com/TrKeyboarder/tr-ai-daw/discussions)
- Proje kapsamı ve açık geliştirme alanları: [ROADMAP.md](./ROADMAP.md)

`main` dalına gönderilen normal pull request'ler bir onaylı inceleme gerektirir. Proje yöneticileri bu koruma kuralından muaftır. Küçük, iyi açıklanmış bir hata düzeltmesi veya test de projeye anlamlı katkıdır.

## Lisans ve atıflar

Uygulama kodu Apache-2.0 lisanslıdır; ayrıntılar [LICENSE](./LICENSE) ve [NOTICE](./NOTICE) dosyalarındadır. İndirilen yapay zekâ model ağırlıklarının ve bazı isteğe bağlı modellerin ayrı lisansları vardır; [MODELS.md](./MODELS.md) dosyasını inceleyin. Upstream kaynak kodunun lisans ve telif bildirimleri korunur.

---

<p align="center"><b>Birlikte daha güçlü, erişilebilir ve geliştirilebilir bir müzik üretim aracı yapalım. 🎶</b></p>
