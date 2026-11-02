# Hayat Navigatörü

**Hayatını bir ürün gibi yönet: alan alan, ama tek bir yerden.** Bir AI ajanıyla (Claude Code, Codex ya da `AGENTS.md` okuyan herhangi bir ajan) çalışan orkestratör ve altındaki alan navigatörleri.

![Hayat Navigatörü nasıl çalışır](diyagram.svg)

## Nasıl çalışır

- **Altı seçilebilir alan:** Kariyer, Para, Sağlık, İnsanlar, isteğe bağlı İnanç ve anlam, İş ve Ürünler. Yalnız seçtiğin alan açılır; diğerleri bekler. Her alan kendi kuralları ve kayıtlarıyla çalışır.
- **Tek giriş:** orkestratör sinyalleri doğru alana bağlar; **tek `HAFTA.md`** ile haftanın odağını, **tek `BUGUN.md`** ile bugünkü küçük adımı gösterir. Alan çalışmasını aynı ajan yürütebilir veya başka bir navigatöre devredebilir.
- **Sınır:** karar sende kalır; ajan dış hesaplarda değişiklik, mesaj, harcama veya yayın için onayladığın kapsam içinde çalışır. Döngü sohbeti açtığında işler; otomatik sabah çalışması değildir.

**Kariyer** senin mesleki gelişimin ve yönündür. **İş ve Ürünler** müşteriye sunduğun değer ve iş/ürün sonuçlarıdır; şirketin veya ürünün henüz olmasa da başlayabilirsin. **Para** kişisel finansındır. Aynı işin veya kanıtın tek ana kaydı olur; diğer alanlar bağlantıyla yararlanır, ikinci görev listesi açılmaz.

İş ve Ürünler alanı ihtiyacına göre müşteri ve problem, konumlandırma (kimin için neden tercih edilirsin), alternatifler, ürün öncelikleri, satış, pazara çıkış (müşteriye ulaşma yolu), fiyat varsayımları, teslim, kalite, maliyet ve sonuç ölçmeyi kapsar. Bunlar zorunlu dersler değildir: mevcut işin üzerinden **öğren → küçük dene → ölç → karar ver**. Bir şeyin okunması veya hazırlanması, öğrenildiği ya da iş sonucu alındığı anlamına gelmez.

## Budur, bu değildir

| Budur | Bu değildir |
|---|---|
| Hayatın alanlarını tek yerden görmek | Hayat koçluğu, terapi, motivasyon |
| Sinyalleri toplayıp doğru yere koymak | Senin adına onaysız mesaj göndermek |
| Alanlar arası bağı göstermek (iş → para → ev) | Tıbbi, finansal, hukuki tavsiye; dini hüküm |
| Sohbeti açtığında güncellenen tek günlük giriş | Seni takip eden veya kendiliğinden çalışan bir uygulama |

## Nasıl kullanılır

1. Kişisel çalışman için ayrı, boş bir klasör aç; `AGENTS.md` ve `CLAUDE.md` dosyalarını içine kopyala. Bu repo kopyalanabilir bir yöntemdir; kurulacak bir skill paketi değildir.
2. Ne istediğini anlat; ajan ihtiyacını kısa geri söyler. Alan belli değilse "Hangi alandan başlayalım?" diye sorar. Yalnız seçtiğin alan açılır.
3. Şimdi ne var, ne değişsin, ne belirsiz: kısa sohbet yeterli. Dosya, şirket, ürün veya geçmiş kayıt şart değildir. Kaynak paylaşmak isteğe bağlıdır; ilk küçük soru veya denemeyle başlanabilir.
4. Üzerinde anlaştığınız adım için gereken kayıtları kurun. Sohbeti açtığında `BUGUN.md` üzerinden ilerle; sonucu "bitti / takıldım" ve varsa kanıtıyla paylaş.

**Dosyasız başlangıç örneği:** "İş ve Ürünler alanından başlamak istiyorum; henüz ürünüm yok." Ajan mevcut deneyimini ve merak ettiğin ihtiyacı kısa sorar; örneğin bir kişinin bir işi bugün nasıl çözdüğünü öğrenmek ilk küçük adım olabilir. Önce bütün alanları veya uzun bir iş planını kurmaz.

**Mevcut kurulumda devam örneği:** "Dünkü denemeye devam edelim." Ajan `overview.md` → `BUGUN.md` → `HAFTA.md` → ilgili alanın `AGENTS.md` ve `overview.md` dosyalarını okur; son kayıt ve kanıttan ilerler. Kimlik görüşmesini tekrarlamaz. Yapıldı / sürüyor / öneri / belirsiz ayrımını korur; kapanışta istenen kapsamı gözlenen sonuçla karşılaştırır.

Kariyer alanının hazır yöntemi: [kariyer-navigatoru](https://github.com/sdogukan/kariyer-navigatoru). Burada kullanırken günlük ve haftalık girişleri kökteki tek `BUGUN.md` ve `HAFTA.md` dosyalarına bağla.

## İlkeler

Yalan yok, şişirme yok · öneri karar değildir · onaylanan kapsamda ilerle · kişinin, ekibin ve AI'ın katkısını ayır · tek güncel odak, diğer fikirler sonra · bir iş ve kanıt tek yerde · gerektiğinde diyagram · uzman gereken yerde "uzmana git" · inançta hüküm yok, yargı yok; geleneği kullanıcı seçer.

Kişisel kayıtlar kullanıcının seçtiği depolamada tutulur; kullanılan bulut veya bağlı araç açıkça belirtilir. Bu genel depoya kişisel veri ekleme. Zaten yetkilendirilmiş kaynakların okunması için tekrar izin gerekmez; dışarıya yazma ve paylaşma ayrı kapsamlardır.

## Klasör yapısı

Aşağıdaki **kurulum örneğidir**; bu genel depodaki mevcut dosyaları göstermez. Yalnız ihtiyaç duyulan kayıtlar ve seçilen alan oluşturulur.

```text
hayat/
├── overview.md · HARITA.md · BUGUN.md · HAFTA.md · gunluk.md
├── sinyaller/                      # gerektiğinde kısa notlar veya asıl kayda bağlantılar
└── seçilen alan/                   # kariyer/ · para/ · saglik/ · insanlar/ · inanc/ · is-ve-urunler/
    ├── AGENTS.md                   # alanın sorumluluğu ve sınırları
    └── overview.md                 # durum, istek, belirsizlik, denemeler, kanıt bağlantıları
```

## Köken

Bir kurucu ortağın "hayatımı da şirketim gibi, bir orkestratörle yönetmek istiyorum" sözünden doğdu; Kariyer Navigatörü'nün üstüne kuruldu. Kişisel veri içermez; yalnız yöntemi paylaşır.

MIT lisansı.
