<h1 align="center">Community</h1>

<p align="center">
  <b>Duyuruları, toplantıları, görevleri ve sohbetleri tek bir uygulamada toplayan kurum içi iletişim uygulaması.</b><br>
  Rol tabanlı ve çok kiracılı (multi-tenant) yapıda tasarlandı. Birden fazla kurum aynı altyapıyı kullanabilir.
</p>

<p align="center">
  <i>İnönü Üniversitesi Siber Güvenlik Topluluğu · 4 kişilik ekip projesi</i>
</p>

---

<h2 align="center">Proje hakkında</h2>

Community, kurumların iç iletişimini **tek bir çatı altında** toplayan bir
**Flutter mobil uygulamasıdır**. Çalışanlar görevlerini, toplantılarını, kurum
haberlerini ve mesajlarını tek bir yerden takip eder. Yöneticiler ise kendi
kuruluşlarının içeriğini ve üyelerini yönetir.

Proje, **İnönü Üniversitesi Siber Güvenlik Topluluğu** çatısı altında bir araya
gelen **4 kişilik bir ekip** tarafından yaz döneminde geliştirildi.

<h2 align="center">Neden yaptık?</h2>

Şirketlerde duyurular e-postada, toplantılar takvimde, görevler bir tabloda,
sohbetler ise başka bir uygulamada kalıyor. **Bilgi dağıldıkça takip zorlaşıyor.**

Amacımız bu süreçleri **tek bir uygulamada birleştirmekti**. Bu projeyle birlikte
**durum yönetimi**, **rol bazlı ekran akışları**, **ölçeklenebilir proje yapısı**
ve **ekip içi iş birliği** üzerine uygulamalı deneyim kazandık.

<h2 align="center">Özellikler</h2>

| | |
|---|---|
| **Görev takibi** | Alt görevler, ilerleme çubukları ve **rapor yükleme** ile aktif görevlerin takibi |
| **Etkinlikler** | Görselli ve etiketli etkinlik paylaşımı ve etkinlik akışı |
| **Toplantılar** | Takvim görünümü, **çevrimiçi veya yüz yüze** toplantı oluşturma ve yönetme |
| **Mesajlaşma** | Çevrimiçi kullanıcılar, birebir sohbet ve okunmamış mesaj göstergesi |
| **Haberler** | Duyuru, güncelleme, etkinlik ve rapor kategorilerine ayrılmış kurum haberleri |
| **QR tarayıcı** | QR kod ile **hızlı giriş** ve etkinliklere katılım |
| **Ayarlar** | Bildirim ve gizlilik tercihleri, şifre değiştirme |
| **Temalar** | **6 kurumsal tema** (Ocean, Indigo, Forest, Plum, Charcoal, Burgundy). Seçilen tema hatırlanır |

<h2 align="center">Roller</h2>

| Rol | Yetki |
|---|---|
| **Süper Admin** | **Tüm kuruluşları** yönetir ve sistem istatistiklerini izler |
| **Şirket Admin** | **Kendi kuruluşunun** içeriğini ve üyelerini yönetir |
| **Çalışan** | Kendi akışını takip eder, görev, etkinlik ve toplantılara katılır |

Giriş yapan kullanıcının **rolüne göre farklı bir açılış paneli** gösterilir.
Diğer sekmeler (mesajlar, QR, toplantılar, haberler) tüm rollerde ortaktır.

<h2 align="center">Nasıl çalışıyor?</h2>

```
Arayüz (Flutter, Material)
        │
        ├── Provider ............ oturum, profil, görev ve etkinlik durumları
        │
        ├── Feature modülleri ... auth · home · events · meetings · news · chat · settings · admin
        │
        ├── SharedPreferences ... tema ve kullanıcı tercihleri cihazda saklanır
        │
        ├── mobile_scanner ...... kamera ile QR kod okuma
        │
        └── Backend & API ....... ayrı olarak geliştiriliyor
```

Kod tabanı **feature-first** yapıdadır: her özellik kendi `data`, `presentation`
ve `state` katmanlarıyla ayrı bir klasörde durur.

Backend ve API'ler ayrı olarak geliştiriliyor. Mobil uygulama şu an **örnek (mock)
veri katmanıyla** çalışıyor ve bu katman **API'ye geçişe hazır** olacak şekilde ayrıldı.

<h2 align="center">Kullanılan teknolojiler</h2>

| Katman | Teknoloji |
|---|---|
| Dil | Dart |
| Arayüz | Flutter, flutter_animate |
| Durum yönetimi | Provider |
| Yerel veri | SharedPreferences |
| Donanım | mobile_scanner (QR), image_picker, file_picker |
| Yerelleştirme | flutter_localizations, intl |

<h2 align="center">Ekip</h2>

| Üye | Rol | Katkılar |
|---|---|---|
| **Osman Nuri Yaşar** | **Ekip lideri · Proje yöneticisi** · Mobil geliştirici | Pop-up menü, QR okuyucu, rapor ekranı, admin paneli *(devam ediyor)* |
| **Egemen Ulutaş** | Mobil geliştirici | Ana ekran, toplantı ekranı, giriş ekranı |
| **Safa Şentürk** | Mobil geliştirici | Mesaj kutusu (DM), haber ekranı, admin paneli *(devam ediyor)* |
| **Mert Doğuç** | Backend geliştirici | Backend ve API'ler |

Ekip liderliği kapsamında **projenin yol haritası**, **görev dağılımı**,
**ilerleme takibi** ve **ortak kod tabanının düzeni** yürütüldü.

<h2 align="center">Durum</h2>

**Arayüz ve temel ekranlar tamamlandı.** Arayüz dili Türkçedir.

Sıradaki adımlar:

- [ ] Backend entegrasyonu
- [ ] Admin paneli tasarımlarının tamamlanması
- [ ] Gerçek zamanlı mesajlaşma
- [ ] Push bildirimler

<h2 align="center">Kaynak kod</h2>

Kaynak kod **özel bir depoda** tutuluyor. İnceleme için **talep üzerine** paylaşılabilir.

<h2 align="center">İletişim</h2>

<p align="center">
  <b>osmnnuri</b> · <a href="https://github.com/osmnnuri">GitHub</a> · <a href="https://osmnnuri.github.io">Web sitesi</a> · osmannuriyasar57@gmail.com
</p>
