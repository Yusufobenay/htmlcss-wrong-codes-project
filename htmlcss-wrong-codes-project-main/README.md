# Atlas Rota — HTML & CSS Hata Avı Projesi

Bu proje, HTML ve CSS temellerini pekiştirmek için hazırlanmış bir **butik seyahat stüdyosu** tanıtım sitesidir. Site görünüşte tamamlanmış ve profesyonel görsellerle hazırlanmıştır, ama içine **bilerek hatalar** eklenmiştir. Görevin bu hataları bulup düzeltmek.

---

## 1. Ne Kullandık, Neden Kullandık

| Teknoloji | Neden |
|---|---|
| **HTML5** | Sayfanın iskeleti ve içeriği. Semantik etiketler (`header`, `section`, `article`, `footer`) kullanıldı ki hem tarayıcı hem de ekran okuyucular sayfayı doğru yorumlasın. |
| **CSS3** | Görsel tasarım: renkler, tipografi, grid/flexbox ile yerleşim, responsive (duyarlı) davranış. |
| **Google Fonts** (Fraunces, Work Sans, JetBrains Mono) | Başlıklarda karakterli bir serif (Fraunces), gövde metninde okunaklı bir sans-serif (Work Sans), rota kodları/etiketler gibi küçük detaylarda mono bir font (JetBrains Mono). Tek font yerine üç farklı rolde font kullanmak tasarıma hiyerarşi kazandırır. |
| **Unsplash görselleri** | Gerçek, yüksek çözünürlüklü fotoğraflarla profesyonel bir izlenim vermek için doğrudan URL üzerinden bağlandı (proje içine görsel dosyası eklemedik). |

Harici bir framework (Bootstrap, Tailwind vb.) **kullanılmadı** — amaç saf HTML/CSS ile çalışmak.

---

## 2. Klasör Yapısı (Mimari)

```
atlas-rota/
├── index.html          → Sayfanın tüm içeriği ve yapısı
├── css/
│   └── style.css        → Tüm görsel stiller (renk, tipografi, layout)
├── README.md             → Bu dosya
```

Tek sayfalık (single-page) bir site olduğu için tüm bölümler `index.html` içinde `id`'leri ile ayrılmış durumda: `#anasayfa`, `#hakkimizda`, `#rotalar`, `#yorumlar`, `#iletisim`. Navbar'daki linkler bu id'lere yönlenir.

CSS tek dosyada tutuldu ama içeride bölümlere ayrılmış durumda (yorum satırlarıyla `NAVBAR`, `HERO`, `ABOUT`, `ROTALAR`, `YORUMLAR`, `İLETİŞİM`, `FOOTER`). Ayrıca dosyanın en üstünde `:root` içinde renk ve font **değişkenleri (custom properties)** tanımlı — tüm proje bu değişkenler üzerinden renklenir, böylece bir rengi değiştirmek tek satırda yapılabilir.

---

## 3. Nasıl Başlamalı — Adım Adım

1. **Projeyi indir.** GitHub'daki repodan `Code → Download ZIP` ile indir ya da `git clone` ile klonla.
2. **Klasörü bir kod editöründe aç** (VS Code önerilir).
3. **`index.html` dosyasını tarayıcıda aç.** VS Code kullanıyorsan "Live Server" eklentisiyle açman değişiklikleri anında görmeni sağlar.
4. **Sayfayı incele.** Bazı bölümlerin yerleşiminin bozuk olduğunu, bazı butonların/rozetlerin renksiz kaldığını, menünün alt alta dizildiğini fark edeceksin. Bunların hepsi bilerek bırakılmış hatalar.
5. **Tarayıcının Geliştirici Araçları'nı aç** (sağ tık → İncele / `F12`). "Elements" ve "Console" sekmeleri hataları bulmanda en büyük yardımcın olacak — bir CSS kuralı geçersizse tarayıcı genelde üstünü çizerek gösterir.
6. **Hataları tek tek bul ve düzelt.** Her düzeltmeden sonra sayfayı yenileyip sonucu gözlemle.
7. **Bulduğun her hatayı not al:** ne bozuktu, nerede buldun, nasıl düzelttin. (Bunu kısa bir liste halinde teslim edeceksin.)

### Hataları ararken nereye bakmalısın?
- **HTML tarafında:** kapanmamış etiketler, yanlış/eksik öznitelikler (`alt`, `name` gibi), yanlış iç içe geçmiş etiketler, eksik tırnak işaretleri.
- **CSS tarafında:** yazım hataları (özellik adı yanlış yazılmış), eksik birim (`px`, `%` gibi), eksik noktalı virgül, geçersiz renk kodu, kapanmamış süslü parantez `{ }`.

Tek bir küçük hata (örneğin kapanmamış bir süslü parantez) sayfanın **büyük bir bölümünü** etkileyebilir — bu yüzden bir hatayı düzelttikten sonra sayfanın tamamını tekrar kontrol et.

---

## 4. Teslim

- Düzelttiğin dosyaları (`index.html`, `css/style.css`) kendi GitHub deponda paylaş.
- Bulduğun hataların kısa bir listesini (`HATALAR.md` gibi bir dosyada) ekle: hata neydi, nerede buldun, nasıl düzelttin.

Kolay gelsin — iyi avlar! 🧭
