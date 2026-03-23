# 🤖 Otomasyon Sistemleri Platformu — Tam Website Prompt Dökümanı

**Yazan:** Yasin  
**Amaç:** Antigravity / Claude üzerinde sıfırdan prompt yazarak SaaS landing page oluşturmak  
**Teknik seviye:** Sıfır — tüm promptlar kopyala-yapıştır kullanıma hazır

---

## 📋 Bu Döküman Nasıl Kullanılır?

1. Her bölümdeki promptu kopyala
2. Antigravity'de Claude'a yapıştır
3. Sonucu gör, beğenmezsen aynı bölümdeki "Düzeltme Promptu"nu kullan
4. Sırayla devam et

---

---

# BÖLÜM 1 — Projenin Genel Kurulumu

## 🔧 İlk Prompt (Her şeyi başlat)

```
Sen bir senior full-stack geliştirici ve UI/UX tasarımcısısın. Benim için modern, premium bir SaaS landing page oluşturacaksın.

PROJE: Yerel işletmelere yapay zeka destekli otomasyon sistemleri satan bir platform. Müşteri iletişimini, randevu yönetimini ve satış süreçlerini otomatikleştiriyor.

PLATFORM ADI: AutoFlow (veya benim söyleyeceğim bir isim)

TASARIM REFERANSI: Stripe, Linear, Vercel gibi modern SaaS markaları. Temiz, beyaz ağırlıklı, minimal ama premium.

RENK PALETİ:
- Ana renk: Koyu lacivert (#0F172A)
- Vurgu rengi: Elektrik mavisi (#2563EB)
- Arka plan: Saf beyaz (#FFFFFF) ve çok açık gri (#F8FAFC)
- Yazı: #1E293B (koyu) ve #64748B (gri)

FONT: DM Sans veya Outfit (başlıklar için ağır, gövde için normal)

TEKNOLOJİ: Tek dosya HTML — tüm CSS ve JavaScript aynı dosyada olsun. Hiçbir harici framework kurulumu gerektirmesin, sadece Google Fonts CDN kullan.

Şimdi sadece temel yapıyı (HTML iskelet + CSS değişkenleri + navigasyon) oluştur. Diğer bölümleri tek tek ekleyeceğim.
```

---

---

# BÖLÜM 2 — Navigasyon (Header)

## 🔧 Prompt

```
Şimdi navigasyon bölümünü ekle. Şu özelliklere sahip olsun:

LOGO: Sol tarafta "AutoFlow" metni + yanında küçük bir otomasyon ikonu (SVG)

MENÜ LİNKLERİ (ortada):
- Çözümler
- Nasıl Çalışır
- Sektörler
- Demo

SAĞ TARAF:
- "Giriş Yap" (ghost/outline buton)
- "Demo Al" (mavi dolu buton, hafif gölgeli)

DAVRANIM:
- Sayfa scroll edilince navbar arka plan bulanık cam efekti (backdrop-filter: blur) alsın
- Scroll'da hafif gölge çıksın
- Mobilde hamburger menü açılsın
- Aktif bölüm menüde underline animasyonuyla belirtilsin

Navigasyon sabit (sticky) kalmalı, sayfa kaydırılınca üstte durmalı.
```

---

---

# BÖLÜM 3 — Hero Bölümü

## 🔧 Prompt

```
Hero bölümünü ekle. Bu bölüm sayfanın ilk ekranı, ziyaretçinin gördüğü ilk şey.

BAŞLIK (büyük, etkileyici):
"Müşterilerinize 7/24
Anında Cevap Verin"

ALT BAŞLIK:
"Yapay zeka destekli otomasyon sistemiyle WhatsApp mesajlarına otomatik yanıt verin, randevuları otomatik alın, müşteri kaybetmeyin."

BUTONLAR:
- Sol: "Ücretsiz Demo Al" — mavi, büyük, hafif gradient, hover'da yukarı kayma animasyonu
- Sağ: "Nasıl Çalışır? →" — şeffaf, alt çizgi efektli

GÖRSELLER:
Sol tarafta metin, sağ tarafta bir dashboard mockup görseli. Dashboard şunları göstersin:
- Gelen WhatsApp mesajları listesi
- Otomatik yanıt durumu (yeşil tik ile "Yanıtlandı")
- Randevu takvimi özeti
- Bugünkü müşteri sayısı widget'ı

ARKA PLAN:
Çok hafif bir grid pattern (noktalı veya ızgara) + sol üst köşeden sağ alta doğru çok soluk mavi gradient

ANİMASYON:
- Başlık kelime kelime soldan gelsin (staggered)
- Dashboard görsel hafif float/yüzme animasyonu yapsın
- Scroll aşağı ok ikonuyla bounce animasyonu

SOSYAL KANIT (hero altında, küçük):
"500+ işletme otomasyon sistemimizi kullanıyor" yazısı + 5 küçük şirket logosu (placeholder olabilir)
```

---

---

# BÖLÜM 4 — Problem Bölümü

## 🔧 Prompt

```
Problem bölümünü ekle. Ziyaretçinin "evet tam benim sorunum bu" demesini sağlamalı.

BÖLÜM BAŞLIĞI:
"Her Gün Müşteri Kaybediyorsunuz"

ALT BAŞLIK:
"Ve bunun farkında bile değilsiniz."

SORUNLAR — 2 sütunlu grid, her kart şunları içersin:
1. Kırmızı/turuncu uyarı ikonu
2. Kısa başlık
3. 1-2 cümle açıklama

6 sorun kartı:
1. 📵 "WhatsApp Mesajları Cevapsız Kalıyor" — Çalışırken ya da uyurken gelen mesajlar karşılıksız, müşteri rakibinize gidiyor.
2. ⏱️ "Geç Yanıt = Müşteri Kaybı" — Araştırmalar gösteriyor: ilk 5 dakikada yanıt verilmezse %80 müşteri ayrılıyor.
3. 📅 "Manuel Randevu Kaosu" — Telefon, mesaj, not defteri... Randevular karışıyor, çift rezervasyon oluyor.
4. 💸 "Potansiyel Satışlar Elden Gidiyor" — Saat 22:00'de fiyat soran müşteri sabah başkasını bulmuş.
5. 🗂️ "Müşteri Bilgileri Dağınık" — Kim ne istedi, ne zaman geldi, tekrar aradı mı? Hiçbir şey kayıt altında değil.
6. 😓 "Tüm Gün İletişimle Geçiyor" — Mesajlara bakıyor, randevu alıyor, takip ediyorsunuz — asıl işinize vakit kalmıyor.

TASARIM:
- Kartlar hafif kırmızımsı/turuncu kenarlıkla, soluk krem arka planla
- Hover'da kart hafif büyüsün
- Scroll animasyonuyla birer birer çıksınlar

ALT KISIM (geçiş):
Bölüm altında şu yazı: "Bunların hepsi çözülebilir. Hem de tamamen otomatik olarak." — mavi renkle, büyükçe, ortada
```

---

---

# BÖLÜM 5 — Çözüm Bölümü

## 🔧 Prompt

```
Çözüm bölümünü ekle. Problem bölümünden sonra "işte cevap bu" hissi vermeli.

BÖLÜM ETİKETİ (küçük, mavi): "ÇÖZÜM"

BAŞLIK:
"İşletmeniz İçin Akıllı
Bir Otomasyon Sistemi"

ALT BAŞLIK:
"Müşterileriniz mesaj atar, sistem devreye girer. Siz sadece gelen randevulara bakarsınız."

ÖZELLİK GRİD (3 sütun, 6 kart):

Kart 1 — AI Mesajlaşma:
İkon: Chat balonu + yıldız
Başlık: "Anında Akıllı Yanıt"
Açıklama: Müşteri WhatsApp'tan mesaj atar atmaz sistem anlar ve doğal bir dille yanıt verir. Sanki siz yazmış gibi.

Kart 2 — Randevu:
İkon: Takvim
Başlık: "Otomatik Randevu"
Açıklama: Müşteri istediği saati seçer, sistem takvime ekler, size bildirim gönderir. Hiç dokunmanıza gerek yok.

Kart 3 — Müşteri Yönetimi:
İkon: Kişiler
Başlık: "Müşteri Kartları"
Açıklama: Her müşterinin tüm geçmişi, tercihleri ve notları otomatik olarak saklanır ve gruplanır.

Kart 4 — Bildirimler:
İkon: Zil
Başlık: "Akıllı Bildirimler"
Açıklama: Yeni randevu, iptal veya önemli mesaj geldiğinde anında telefonunuza bildirim gelir.

Kart 5 — 7/24 Aktif:
İkon: Ay + yıldız
Başlık: "Gece de Çalışır"
Açıklama: Siz uyurken, tatildeyken ya da başka bir işle meşgulken sistem müşterilerinizi karşılamaya devam eder.

Kart 6 — Teklif Oluşturma:
İkon: Döküman + ok
Başlık: "Otomatik Teklif"
Açıklama: Düğün salonu, klinik veya gayrimenkul gibi işletmeler için müşteri isteklerine göre teklif hazırlanır.

TASARIM:
- Kartlar beyaz, çok hafif gölgeli, köşeleri yuvarlak
- Her kart ikonunun arkasında hafif mavi daire
- Hover'da mavi vurgu rengi border çıksın
- Sağ üstte "Yeni" etiketi olan 1-2 kart
```

---

---

# BÖLÜM 6 — Nasıl Çalışır (Workflow)

## 🔧 Prompt

```
"Nasıl Çalışır" bölümünü ekle. Sistemin adım adım işleyişini göstermeli.

BAŞLIK: "5 Adımda Tam Otomatik"

5 adım, dikey timeline veya yatay steps layout:

Adım 1 — Mavi daire "1"
Başlık: "Müşteri Mesaj Atar"
Açıklama: WhatsApp, Instagram DM veya web sitesi formu üzerinden müşteri sizi ulaşır.
Mini görsel: WhatsApp konuşma baloncukları

Adım 2 — Mavi daire "2"
Başlık: "Sistem Anlar"
Açıklama: Yapay zeka mesajın ne hakkında olduğunu anlar: randevu mu, fiyat mı, bilgi mi istiyor?
Mini görsel: Düşünen robot/AI simgesi

Adım 3 — Mavi daire "3"
Başlık: "Bilgi Toplanır"
Açıklama: Sistem gereken soruları sorar: isim, tarih, hizmet türü — müşteri adım adım yönlendirilir.
Mini görsel: Form doldurma animasyonu

Adım 4 — Mavi daire "4"
Başlık: "Randevu Onaylanır"
Açıklama: Uygun saat bulunur, takvime işlenir, müşteriye onay mesajı gönderilir.
Mini görsel: Takvimde yeşil onay

Adım 5 — Mavi daire "5"
Başlık: "Siz Haberdar Olursunuz"
Açıklama: Telefonunuza anlık bildirim gelir. Müşteri adı, randevu saati, hizmet türü — hepsi hazır.
Mini görsel: Telefon bildirimi

TASARIM:
- Adımlar arasında çizgi/oklu bağlantı
- Her adım scroll'da sırayla animate olarak gelsin
- Sağ tarafta adıma karşılık gelen mini UI önizlemesi göster (opsiyonel olarak bir mockup telefon içinde)
```

---

---

# BÖLÜM 7 — Sektör Çözümleri

## 🔧 Prompt

```
Sektöre özel çözümler bölümünü ekle.

BAŞLIK: "Her Sektöre Özel Otomasyon"
ALT BAŞLIK: "Sistemimiz hangi işi yaptığınıza göre kendini ayarlar."

4 sektör kartı, hover'da detay açılan flip veya expand efektli:

Kart 1 — Güzellik Merkezi 💆‍♀️
Arka plan: Yumuşak pembe/rose tonu
Başlık: Güzellik & Estetik
Sorun: "Gün boyu telefon, mesaj, randevu kargaşası"
Çözüm listesi:
- Saç, cilt, tırnak randevusu otomatik alınır
- Hizmet menüsü WhatsApp'tan paylaşılır
- İptal ve hatırlatma mesajları otomatik gönderilir
- Müşteri geçmişi ve tercihleri kayıt altında

Kart 2 — Düğün & Organizasyon 💒
Arka plan: Krem/altın tonu
Başlık: Düğün Salonu & Organizasyon
Sorun: "Her çiftten gelen onlarca soru, teklif süreçleri"
Çözüm listesi:
- Uygunluk takvimi anlık gösterilir
- Müşteri bilgilerine göre teklif otomatik hazırlanır
- Kaparo ve ödeme hatırlatmaları gönderilir
- Tedarikçi koordinasyonu notları tutulur

Kart 3 — Klinik & Sağlık 🏥
Arka plan: Açık mavi/mint
Başlık: Klinik & Sağlık Merkezi
Sorun: "Sekreter yükü, randevu kargaşası, hasta takibi"
Çözüm listesi:
- Doktor/uzman bazında randevu sistemi
- Hasta formu önceden WhatsApp'tan doldurulur
- Kontrol randevusu hatırlatmaları otomatik
- Randevu iptali durumunda boş slot doldurulur

Kart 4 — Gayrimenkul 🏠
Arka plan: Açık kahve/toprak tonu
Başlık: Gayrimenkul & Kiralama
Sorun: "Portföy sorularına tek tek cevap vermek"
Çözüm listesi:
- İlan detayları, fiyat, konum otomatik paylaşılır
- Randevu/gezinti tarihi ayarlanır
- Potansiyel alıcı profili oluşturulur
- Takip mesajları otomatik gönderilir

TASARIM:
- Her kart sektör rengine uygun ince bir border üstten
- Kart hover'da biraz büyüsün ve gölge artsın
- İkon büyük, üstte
- "Daha fazla sektör yakında" küçük notu altta
```

---

---

# BÖLÜM 8 — Demo Bölümü

## 🔧 Prompt

```
Demo bölümünü ekle. Ziyaretçiyi aksiyona geçirmeye odaklanmalı.

BÖLÜM ARKA PLANI: Koyu lacivert (#0F172A) — sayfanın geri kalanından kontrast oluşsun

BAŞLIK (beyaz): "Sistemi Canlı Görün"
ALT BAŞLIK (açık gri): "Size özel bir demo hazırlayalım. 20 dakikada işletmenize nasıl uygulanacağını gösterelim."

İKİ SEÇENEKLİ KART LAYOUT:

Sol Kart — "Demo Randevusu Al"
İkon: Takvim
Başlık: Canlı Demo (20 dk)
Liste:
- Kendi işletmenize özel kurulum gösterimi
- Sorularınızı canlı yanıtlıyoruz
- Fiyatlandırma ve kurulum süreci
Buton: "Demo Randevusu Al →" (mavi)

Sağ Kart — "Sistemi Dene"
İkon: Play butonu
Başlık: Simülasyon Dene
Liste:
- WhatsApp bot simülasyonunu tarayıcıda dene
- Gerçek bir müşteri gibi mesaj gönder
- Sistemin nasıl yanıt verdiğini gör
Buton: "Hemen Dene →" (outline/beyaz)

ALTTA — Güven çubuğu:
"✓ Kurulum 48 saatte tamamlanır  ✓ Sözleşme yok  ✓ İlk ay ücretsiz deneme"

ANİMASYON:
- Koyu arka plan scroll'da soldan kayarak gelsin
- Kartlar sırayla çıksın
```

---

---

# BÖLÜM 9 — Güven Bölümü (Trust)

## 🔧 Prompt

```
Güven bölümünü ekle. Bu bölüm şirketin güvenilirliğini pekiştirmeli.

BAŞLIK: "Neden Bize Güveniyorlar?"

BÖLÜM 1 — Sayılar (metrik bar):
4 büyük metrik, yatay veya 2x2 grid:
- "500+" → Aktif İşletme
- "2.4M+" → Otomatik Yanıtlanan Mesaj
- "%94" → Müşteri Memnuniyeti
- "48 saat" → Ortalama Kurulum Süresi

Sayılar scroll'da count-up animasyonuyla artsın.

BÖLÜM 2 — Referanslar (testimonials, 3 kart):

Kart 1:
İsim: Selin Aydın | Meslek: Güzellik Merkezi Sahibi | Şehir: İstanbul
Yorum: "Artık telefona bakmak zorunda kalmıyorum. Randevular kendiliğinden doluyor, müşterilerim memnun, ben memnunum."
Rating: ⭐⭐⭐⭐⭐

Kart 2:
İsim: Mehmet Kara | Meslek: Düğün Salonu İşletmecisi | Şehir: Ankara
Yorum: "Hafta sonu sistemin kaç tane teklif hazırladığına inanamadım. Biz tatildeyken iş yapıyordu."
Rating: ⭐⭐⭐⭐⭐

Kart 3:
İsim: Dr. Ayşe Tekin | Meslek: Klinik Direktörü | Şehir: İzmir
Yorum: "Randevu kargaşası tamamen bitti. Hastalarımız artık sekreter beklemeden randevu alabiliyor."
Rating: ⭐⭐⭐⭐⭐

TASARIM:
- Testimonial kartlar beyaz, hafif gölgeli
- Sol tarafta büyük tırnak işareti (dekoratif, açık mavi)
- Avatar dairesi + isim + unvan + şehir
- Otomatik geçişli slider (her 4 saniyede bir)

BÖLÜM 3 — Kurucular Hakkında (küçük bir blok):
Başlık: "Kim Yaptı?"
2 kişilik küçük ekip kartı (fotoğraf placeholder + isim + unvan)
Kısa bir metin: "Biz de işletmeciyiz. Aynı sorunları yaşadık. Bu yüzden bu sistemi kurduk."

NOT: Fotoğraflar için placeholder kullan (initials avatar — ismin baş harfleri, renkli daire içinde)
```

---

---

# BÖLÜM 10 — SSS (Sıkça Sorulan Sorular)

## 🔧 Prompt

```
SSS bölümü ekle. Accordion/açılır-kapanır format olsun.

BAŞLIK: "Aklınızdaki Sorular"

10 soru-cevap:

S1: Kurulum ne kadar sürer?
C1: Sistemi 48 saat içinde aktive ediyoruz. Siz sadece bize işletme bilgilerinizi veriyorsunuz, gerisi bizden.

S2: Teknik bilgi gerekiyor mu?
C2: Hiç gerekmez. Sistemi sizin için biz kuruyoruz ve yönetiyoruz. Siz sadece telefonunuza gelen bildirimlere bakıyorsunuz.

S3: Hangi uygulamalar üzerinden çalışıyor?
C3: Öncelikli olarak WhatsApp Business API üzerinden çalışır. Instagram DM ve web sitesi chat entegrasyonu da mevcuttur.

S4: Müşteriler bunun bir bot olduğunu anlıyor mu?
C4: Sistem doğal bir dille konuşacak şekilde ayarlanır. Ancak isterseniz "otomatik yanıt sistemi" olduğunu belirten bir not da eklenebilir.

S5: Randevularımı nereden takip ederim?
C5: Size özel bir panel üzerinden tüm randevularınızı, müşterilerinizi ve mesaj geçmişinizi görebilirsiniz. Telefon uygulaması da mevcuttur.

S6: Fiyatlandırma nasıl?
C6: İşletme türünüze ve kullanım yoğunluğuna göre değişen planlarımız var. Demo görüşmesinde size özel bir teklif hazırlıyoruz.

S7: Sözleşme zorunlu mu?
C7: Hayır. Aylık abonelik modeliyle çalışıyoruz. İstediğiniz zaman iptal edebilirsiniz.

S8: Mevcut WhatsApp numaram kullanılabilir mi?
C8: Evet, mevcut işletme WhatsApp numaranıza entegrasyon yapılabilir. Bu süreç biraz zaman alabilir, detayları demo'da aktarıyoruz.

S9: Birden fazla çalışanım varsa ne olur?
C9: Sistem birden fazla kullanıcıyı destekler. Her çalışan kendi takvimini yönetebilir, tüm konuşmalar merkezi bir panelden takip edilebilir.

S10: Verilerim güvende mi?
C10: Evet. Tüm müşteri verileri şifrelenmiş sunucularda saklanır, KVKK uyumlu çalışıyoruz.

TASARIM:
- Her soru tıklanınca smooth animasyonla açılsın
- Açık soru mavi arka plan ve sol kenarda mavi çizgiyle belirlensin
- + / - ikonu sağda, açılınca rotate animasyonu
```

---

---

# BÖLÜM 11 — Son CTA (Call To Action)

## 🔧 Prompt

```
Sayfanın en altındaki son call-to-action bölümünü ekle.

ARKA PLAN: Çok hafif mavi gradient, neredeyse beyaz (soldan sağa #EFF6FF → #F0F9FF)

BÜYÜK BAŞLIK (merkez):
"İşletmenizi Otomasyona Hazır mısınız?"

ALT BAŞLIK:
"Rakipleriniz uyurken siz de uyuyor musunuz? İlk ücretsiz demo'yu alın, farkı görün."

BUTON (büyük, mavi, gölgeli):
"Ücretsiz Demo Al →"

Butonun altında küçük yazı:
"Kredi kartı gerekmez · Kurulum 48 saatte · İstediğiniz zaman iptal"

DEKORASYON:
Arka planda çok soluk mavi büyük daireler (blur efektli, soyut)

ANİMASYON:
Buton hover'da sağa ok kayar, hafif scale büyür
```

---

---

# BÖLÜM 12 — Footer

## 🔧 Prompt

```
Footer bölümünü ekle.

ARKA PLAN: Koyu lacivert (#0F172A)

LAYOUT (4 sütun):

Sütun 1 — Marka:
Logo (beyaz)
Kısa açıklama: "Yerel işletmeler için yapay zeka destekli otomasyon sistemleri."
Sosyal medya ikonları: Instagram, LinkedIn, Twitter/X (sadece ikonlar, linkler placeholder)

Sütun 2 — Ürün:
Başlık: Ürün
Linkler: Özellikler, Nasıl Çalışır, Fiyatlandırma, Demo, Güncellemeler

Sütun 3 — Sektörler:
Başlık: Sektörler
Linkler: Güzellik Merkezi, Düğün Salonu, Klinik, Gayrimenkul, Restoran, Fitness

Sütun 4 — İletişim:
Başlık: İletişim
E-posta: info@autoflow.com.tr
WhatsApp: +90 XXX XXX XX XX
Konum: İstanbul, Türkiye
Buton: "Demo Al" (küçük, mavi outline)

ALT KISIM (footer bottom):
Sol: © 2025 AutoFlow. Tüm hakları saklıdır.
Sağ: Gizlilik Politikası · Kullanım Koşulları · KVKK

TASARIM:
- Yazılar açık gri (#94A3B8)
- Başlıklar beyaz
- Ayırıcı çizgi üstte ince, koyu
- Hover'da linkler mavi oluyor
```

---

---

# BÖLÜM 13 — Animasyon ve Scroll Efektleri

## 🔧 Prompt

```
Sayfaya genel scroll animasyonları ve micro-interaction efektleri ekle.

SCROLL REVEAL:
Her bölümdeki kartlar ve başlıklar viewport'a girerken:
- Aşağıdan yukarıya kayarak (translateY: 30px → 0)
- Opaklık artarak (opacity: 0 → 1)
- 0.6 saniye, ease-out easing
- Birden fazla eleman varsa 0.1s stagger (sıralı gecikme)

Kullan: Intersection Observer API (hiçbir kütüphane gerekmez)

HOVER EFEKTLERİ:
- Tüm kartlar: translateY(-4px) + gölge artışı
- Butonlar: Scale 1.02 + hafif parlaklık
- Menü linkleri: Aşağıdan yukarıya renkli underline animasyonu

SAYAÇ ANİMASYONU (güven bölümü sayılar):
- Scroll'a girerken 0'dan hedef sayıya kadar count-up
- 1.5 saniye süre, ease-out

PARALLAX (çok hafif):
- Hero arka plan grid: scroll'da çok yavaş yukarı kayar (%30 yavaşlık)

CURSOR (opsiyonel, masaüstünde):
- Özel cursor: Küçük mavi daire, mouse hareketini 0.1s gecikmeyle takip eder

Tüm animasyonlar:
- prefers-reduced-motion medya sorgusuna saygılı olsun
- Mobilde basitleştirilsin (sadece opacity geçişi)
```

---

---

# BÖLÜM 14 — Mobil Uyumluluk

## 🔧 Prompt

```
Sayfanın tüm bölümlerini mobil uyumlu hale getir.

BREAKPOINT'LER:
- Mobil: 0-768px
- Tablet: 768-1024px
- Masaüstü: 1024px+

MOBİL DÜZENLEMELER:
- Hero: Tek sütun, görsel üstte, metin altta. Dashboard mockup küçülsün.
- Özellik grid: 1 sütun
- Sektör kartları: 1 sütun, kaydırmalı veya accordion
- Workflow adımları: Dikey liste
- Footer: 2 sütuna düş, altta 1 sütun
- Tüm butonlar full-width olsun

HAMBURGER MENÜ:
- Sağ üstte 3 çizgi ikonuyla
- Tıklanınca tam ekran overlay menü açılsın
- Geçiş animasyonu: yukarıdan aşağı slide
- X ikonu ile kapansın

TOUCH TARGETS:
- Tüm tıklanabilir alanlar minimum 44x44px

FONT BOYUTLARI:
- Mobilde başlıklar biraz küçülsün (clamp() kullan)
- Okunabilirlik öncelikli

TEST:
Her breakpoint'te gözden geçir, taşmalar, hizalama sorunları düzelt.
```

---

---

# BÖLÜM 15 — Son Kontrol ve Optimizasyon

## 🔧 Prompt (Son Adım)

```
Sayfanın tamamını gözden geçir ve şunları kontrol et/düzelt:

GÖRSEL KONSİSTANSI:
- Tüm bölümlerde aynı renk paleti kullanılmış mı?
- Font boyutları tutarlı mı? (H1, H2, H3, body, small için hiyerarşi)
- Bölümler arası padding/margin tutarlı mı? (önerilen: 80-120px dikey)
- Butonlar aynı stil mi?

KOPYA (METİN) DÜZELTMELERİ:
- Teknik jargon yok mu? (API, LLM, webhook gibi terimler ortalama kullanıcıya hitap edecek şekilde değiştirilmiş mi?)
- Tüm metinler Türkçe mi?
- Eylem odaklı yazılmış mı? (fayda → zaman kazan, müşteri kaybetme, otomatik çalış)

PERFORMANS:
- Google Fonts sadece kullanılan weight'leri çeksin
- Gereksiz animasyonlar kaldırılsın
- CSS değişkenleri tek bir :root bloğunda toplanmış olsun

ERİŞİLEBİLİRLİK:
- Tüm butonlarda aria-label var mı?
- Görseller için alt text var mı?
- Renk kontrastı yeterli mi?

BÜTÜNLÜK KONTROLÜ:
- Sayfa en üstten en alta scroll edildiğinde mantıklı bir hikaye anlatıyor mu?
- Hero → Problem → Çözüm → Nasıl → Demo → Güven → CTA akışı net mi?

Son olarak sayfanın tamamını tek bir HTML dosyası olarak ver, indirmeye hazır.
```

---

---

# 🔄 DÜZELTME PROMPTLARI (Sorun Çıkarsa Kullan)

## Renk değiştirmek için:
```
Hero bölümündeki vurgu rengini #2563EB'den #7C3AED'ye (mor) değiştir. Tüm butonlar, ikonlar ve underline'lar bu renge uygun olsun. CSS değişkenini güncelle, tek tek aramak zorunda kalmayayım.
```

## Başlığı değiştirmek için:
```
Hero bölümündeki ana başlığı şu şekilde değiştir: "[YENİ BAŞLIĞINIZ]". Sadece başlık metni değişsin, tasarım aynı kalsın.
```

## Yeni bir sektör eklemek için:
```
Sektörler bölümüne yeni bir kart ekle: Restoran & Kafe. Renk tonu sıcak kırmızı/turuncu olsun. Sorun: "Rezervasyon ve sipariş kaosunu yönetmek". Çözümler: rezervasyon otomasyonu, menü paylaşımı, müşteri sadakat sistemi. Diğer kartlarla aynı stilte olsun.
```

## Türkçe'den İngilizce'ye çevirmek için:
```
Sayfanın tamamını İngilizce'ye çevir. Copywriting tonunu koru: güvenilir, outcome-focused, jargonsuz. Özel isimler (şehir adları, kişi isimleri) değiştirilebilir. Teknik terimler ortalama İngilizce konuşan işletme sahibine hitap edecek şekilde düzenlensin.
```

## Demo bölümüne form eklemek için:
```
Demo bölümüne bir iletişim formu ekle. Alanlar: Ad Soyad, İşletme Adı, Telefon (WhatsApp), Sektör (dropdown: Güzellik, Düğün, Klinik, Gayrimenkul, Diğer). Gönder butonu: "Demo Randevusu Talep Et". Form gönderilince "Teşekkürler! 24 saat içinde sizi arayacağız." success mesajı göster. Backend yok, sadece frontend validation ve success state.
```

## Fiyatlandırma bölümü eklemek için:
```
Workflow bölümünden sonra bir fiyatlandırma bölümü ekle. 3 plan:
- Başlangıç: 1.490 TL/ay — 1 kanal, 500 mesaj/ay, temel randevu
- Profesyonel: 2.990 TL/ay — 3 kanal, sınırsız mesaj, müşteri yönetimi, teklif sistemi — "En Popüler" etiketi mavi
- İşletme: 5.990 TL/ay — sınırsız kanal, öncelikli destek, özel entegrasyonlar, çoklu kullanıcı
Her kartın altında "Demo Al" butonu. Yıllık ödeme seçeneği toggle'ı ekle (%20 indirim göster). Tasarım Stripe pricing page gibi temiz olsun.
```

---

---

# 📌 NOTLAR VE İPUÇLARI

## Platform Adı
Bu döküman boyunca "AutoFlow" kullanıldı. Bunu kendi marka adınızla değiştirmek için ilk prompta şunu ekleyin:
```
Platform adı: [MARKANIZIN ADI]
```

## İletişim Bilgileri
Footer'daki e-posta, telefon ve konum placeholder olarak bırakıldı. Demo hazır olduğunda:
```
Footer'daki iletişim bilgilerini güncelle: E-posta: [email], Telefon: [numara], Adres: [adres]
```

## Demo Linki / Randevu Bağlantısı
```
"Demo Al" butonlarının tümünü şu linke yönlendir: [RANDEVU LINK]
```

## Logo
```
Sol üstteki "AutoFlow" logo metnini SVG veya PNG logo ile değiştir. Logoyu base64 olarak buraya yapıştır: [BASE64]
```

---

*Bu döküman Yasin tarafından hazırlanmıştır. Antigravity platformunda Claude ile kullanım için optimize edilmiştir.*
