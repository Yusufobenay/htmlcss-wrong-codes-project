# Hata Avı Raporu

| No | Ne Bozuktu? | Nerede Bulundu? | Nasıl Düzeltildi? |
|:--|:---|:---|:---|
| 1 | CSS dosyası bağlanmıyordu. | index.html (Satır 9) & Console | `href="css/style.css"` yerine `href="style.css"` yapıldı.
(2) Kapanmamış tırnak işareti | index.html (Satır 24) | Tırnak işareti kapatıldı.
(3) <img> etiketinde alt özelliği yoktu.| index.html 33.satırda| alt="Doğa Manzarasi"
(4) <div class="about__image"> etiketinin kapanış etiketi eksikti görsel içine hapsoluyordu o yüzden ve .about__grid çalıştıramıyordu.| index.html(47-50. satırlar) | <img> altına </div> eklenerek.
(5) Html etiketleri çapraz kapatılmıştı <strong><em>....</strong></em> | index.html (satır147)| </em></strong> olarak değiştirildi.
(6) <input type="email"> etiketinde name eksikti. | index.html (179) | name="email" ekledim.
(7) color özelliği yanlış yazılmıştı | style.css (satır 86) | colr ifadesi color olarak düzelttim.
(8) z-idnex: 10; geçersiz olur ve navbar altında kalma riski taşıyordu. | style.css (98) | z-idnex: 10; ifadesi z-index: 10; olarak düzeltildi.
(9) .navbar__links display özelliği yanlış yazılmıştı. menü bağlantıları yan yana gelmiyordu ve alt alta diziliyordu. dispaly:flex; | style.css (satır 124) | dispaly yerine display olarak düzeltildi.
(10)  @media (max-width: 768px) kapanış süslü parantezi eksikti. o yüzden dosyadaki tüm alt kurallar içerisine hapsolmuştu. | style.css (satır 139-143) | .navbar__links kuralının altına eksik olan süslü parantezi eklenerek media query kapatıldı.
(11)  .route-card__body sınıfında padding değeri birimsiz yazılmıştı.| style.css (satır252)|
padding: 20px; olarak düzeltildi.
(12) .stamp sınıfında geçersiz hex renk kodu(#12x45) tanımlanmıştı. x karakteri hex renk kodunda yer almaz rozetin arka plan rengi çalışmıyordu. | style.css (satır 277) | background: var(--sand); ile değiştirildi.
(13) .contact sınıfında background: var(--forest) kuralının sonunda noktalı virgül eksikti. tarayıcıda iletişim kısmında metin ve rengi uygulanmıyordu ondan kaynaklı. | style.css(satır 324) | background: var(--forest); noktalı virgülü ekleyerek sonuna.