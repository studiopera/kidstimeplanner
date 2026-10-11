# Gizlilik Politikası

**Uygulama:** Kids Time Planner
**Veri Sorumlusu:** Erhan Serin
**İletişim:** studioperaturkey@gmail.com
**Yürürlük tarihi:** 31 Mayıs 2026
**Son güncelleme:** 11 Ekim 2026

> Bu politika, KVKK (6698 sayılı Kişisel Verilerin Korunması Kanunu), GDPR ve
> GDPR-K (16 yaş altı veriler), Google Play Families Policy ve COPPA prensipleri
> dikkate alınarak hazırlanmıştır.

---

## 1. Özet

Kids Time Planner, **ebeveynlerin çocuklarına ait günlük görev planını yönetmesi
için tasarlanmış** bir mobil uygulamadır. Hesapları ebeveynler açar; çocuklar
uygulamaya kendi adlarına kayıt olmaz. Ebeveyn isterse çocuğuna kendi
cihazında giriş imkânı verebilir (bkz. 2.3). Uygulama:

- Çocuk verilerini **yalnızca ebeveynin girdiği biçimde** saklar (ad, emoji,
  görev verisi).
- Çocuk verilerini **reklam amacıyla kullanmaz**, üçüncü taraflarla
  **satmaz veya paylaşmaz** (Google Firebase altyapı sağlayıcısı hariç).
- **Reklam göstermez**, analitik / takip SDK'ları içermez (Firebase Analytics
  şu anda etkin değildir).

## 2. Topladığımız veriler

### 2.1 Ebeveyne ait veriler

| Veri | Nereden | Amaç | Saklama |
|---|---|---|---|
| E-posta adresi | Üyelik formu / Google Sign-In / Apple ile Giriş | Hesap oluşturma, kimlik doğrulama, parolanın sıfırlanması, OTP doğrulama kodlarının iletilmesi | Hesap aktif olduğu sürece |
| Görünen ad | Üyelik / Google veya Apple profili | Ekran içi selamlama | Hesap aktif olduğu sürece |
| Parola | Üyelik formu | Kimlik doğrulama | Firebase tarafından şifrelenmiş biçimde; düz metin asla saklanmaz |
| Premium abonelik durumu | Google Play / Apple App Store | Premium özelliklere erişim | Hesap aktif olduğu sürece |
| FCM cihaz token'ı | Cihazınız (Firebase Messaging) | Görev tamamlanma bildirimi, haftalık özet gönderebilmek | Cihaz değiştirilene veya hesap silinene kadar |
| PIN doğrulayıcısı | Cihazınızdaki ayar | Ebeveyn paneline erişimi sınırlamak | Yalnızca cihazınızda (SharedPreferences); şifrelenmiş hash + tuz olarak |

### 2.2 Çocuğa ait veriler (ebeveyn tarafından girilir)

| Veri | Amaç | Saklama |
|---|---|---|
| Çocuğun adı veya takma adı | Profili tanıma | Profil silinene kadar |
| Emoji / avatar seçimi | Görsel tanım | Profil silinene kadar |
| Görevler, tamamlanma kayıtları, yıldızlar, ödüller, rutinler | Uygulamanın temel işlevi | Hesap aktif olduğu sürece |

Çocuk verisi yalnızca ebeveynin (hesap sahibinin) Firebase UID'sine bağlıdır.
Başka bir ebeveynin verisine erişilemez (Firestore Security Rules ile zorunludur).

### 2.3 Çocuğun kendi cihazından girişi (isteğe bağlı)

Ebeveyn, çocuğunun başka bir telefon veya tablette **yalnızca kendi çocuk
profilini** açabilmesine izin verebilir. Ebeveyn bunu ebeveyn panelinde bir
çocuk profili için açmadıkça hiçbir şey oluşturulmaz.

| Veri | Nereden | Amaç | Saklama |
|---|---|---|---|
| Ebeveynin belirlediği kullanıcı adı ve şifre | Ebeveyn paneli | Çocuğun girişi | Ebeveyn girişi kaldırana, profili veya hesabı silene kadar; şifre Firebase Auth tarafından hash'lenmiş olarak saklanır |
| Çocuğun kendi Apple, Google veya e-posta hesabı (yalnızca ebeveyn o adrese davet gönderirse) | Ebeveyn paneli, ardından çocuğun girişi | Çocuğun girişi | Yukarıdakiyle aynı; davetteki e-posta adresi yalnızca davet kabul edilene veya kaldırılana kadar tutulur |
| Çocuk cihazının FCM token'ı | Çocuğun cihazı | O cihazda görev hatırlatmaları | Giriş kaldırılana veya profil/hesap silinene kadar |

Çocuk hesabı yalnızca kendi profiline ait görevleri, ödülleri ve hedefleri
görebilir ve kendi görevlerini tamamlandı olarak işaretleyebilir. Ebeveyn
panelini açamaz, satın alma yapamaz, ayarları değiştiremez, diğer çocukları
göremez.

### 2.4 Otomatik olarak toplanan veriler

| Veri | Amaç | Saklama |
|---|---|---|
| Hata günlükleri (Firebase Crashlytics) | Hata gidermek | Firebase varsayılan (~90 gün) |
| Cihaz işletim sistemi sürümü (Firebase tarafından) | Altyapı uyumluluğu | Firebase varsayılan süresi |

Uygulamada konum, kişi listesi, mikrofon, takvim, SMS, IMEI veya reklam
kimliği toplanmaz.

## 3. Verileri kimlerle paylaşıyoruz

Verileriniz **satılmaz, kiralanmaz, reklam ekosistemiyle paylaşılmaz**. Aşağıdaki
veri işleyenler yalnızca hizmetin sağlanması için kullanılır:

| Hizmet sağlayıcı | Hangi veri | Amaç | Sözleşmesi |
|---|---|---|---|
| Google Firebase (Auth, Firestore, Storage, Functions, Messaging) | Tüm hesap & uygulama verisi | Hosting ve veritabanı | Google Veri İşleme Sözleşmesi (DPA) |
| Google Play Billing | Abonelik makbuzu | Premium doğrulama | Google Play geliştirici sözleşmesi |
| Apple App Store (Uygulama İçi Satın Alma) | Abonelik makbuzu | Premium doğrulama | Apple Developer Program lisans sözleşmesi |
| Apple ile Giriş | E-posta (gizli yönlendirme adresi olabilir) + ad | Giriş | Apple gizlilik politikası |
| Google Sign-In | E-posta + ad | Tek tıkla giriş | Google Hesabı politikası |

Yasal yükümlülük (mahkeme kararı vb.) durumunda yetkili makamlara veri paylaşımı
yapılabilir.

## 4. Çocukların verisinin korunması (önemli)

- Uygulama Google Play Families Policy ve COPPA prensiplerine uygundur.
- Çocuklar kendi başlarına kayıt olamaz. Çocuk girişi yalnızca ebeveyn
  oluşturursa vardır, yalnızca o çocuğun kendi profiliyle sınırlıdır ve
  ebeveyn istediği an kaldırabilir.
- Çocuk verileri **reklam amacıyla işlenmez**, analitik için profillenmez.
- Uygulama içinde **çocuğa yönelik reklam yoktur**, üçüncü taraf reklam SDK'ları
  yüklü değildir.
- Premium abonelik satın alma akışı **yalnızca ebeveyn paneli üzerinden,
  PIN ile korunarak** erişilebilir; çocuk modunda satın alma başlatılamaz.

## 5. Verilerinizin saklandığı yer

Firebase altyapısı tarafından, Google Cloud'un seçtiğimiz bölge sunucularında
şifreli olarak saklanır. Bu sunucular Türkiye dışında (Avrupa Birliği veya
Amerika Birleşik Devletleri) konumlandırılabilir. Bu durumda **uluslararası
veri aktarımı** söz konusudur. Google, GDPR Standart Sözleşme Maddeleri (SCC)
çerçevesinde aktarımı güvence altına alır.

## 6. Saklama süreleri

- Hesap aktif olduğu sürece veriler korunur.
- Ebeveyn bir çocuk girişini kaldırdığında veya çocuk profilini sildiğinde
  ilgili çocuk giriş hesabı hemen silinir.
- Hesap silindiğinde **30 gün içinde** tüm kullanıcı verisi (kullanıcı belgesi,
  çocuk profilleri, çocuk giriş hesapları, görev geçmişi, FCM token'ları,
  OTP geçmişi) kalıcı
  olarak silinir.
- Yasal saklama yükümlülüğü olan kayıtlar (örn. satın alma makbuzu) ilgili
  yasal süre dolana kadar arşivlenmiş biçimde saklanır.

## 7. Haklarınız

KVKK m. 11 ve GDPR m. 15-22 kapsamında aşağıdaki haklara sahipsiniz:

- Verilerinize **erişme** ve **kopya talep etme**
- Yanlış / eksik verilerinizin **düzeltilmesini** isteme
- Verilerinizin **silinmesini** isteme ("unutulma hakkı")
- İşlemenin **kısıtlanmasını** isteme
- Otomatik karar verme / profilleme yapılmamasını isteme
- Şikayet hakkınızı kullanma (KVK Kurumu / yerel veri koruma otoritesi)

Bu hakları kullanmak için: **studioperaturkey@gmail.com** adresine yazabilir
veya uygulama içinden **Ayarlar → Hesabımı sil** seçeneğini kullanabilirsiniz.
Taleplere en geç **30 gün içinde** yanıt verilir.

## 8. Güvenlik

- Tüm trafik TLS (HTTPS) ile şifrelenir.
- Firestore Security Rules, kullanıcıların yalnızca kendi verilerine erişmesini
  zorlar; başka bir hesabın verisine erişim sunucu tarafında reddedilir.
- Parolalar Firebase Auth tarafından bcrypt ile saklanır; düz metin parola
  asla görülmez.
- Ebeveyn PIN'i cihazda SHA-256 + salt + 10.000 PBKDF2 iterasyonu ile hash'lenir.
- OTP kodları yalnızca **hash** olarak bellekte tutulur, düz kod gönderildikten
  sonra cihazda saklanmaz.
- Satın alma doğrulaması **sunucu tarafında** (Cloud Function) Play Developer
  API ile yapılır; istemci `isPremium` alanını yazamaz.

## 9. Çerezler ve izleme

Uygulama mobil platformda çalışır; web çerezi kullanmaz. Reklam veya analiz
amaçlı izleme SDK'sı içermez. Cihazda yalnızca aşağıdaki yerel depolama
mekanizmaları kullanılır:

- **SharedPreferences** (yerel ayarlar, PIN hash, tema seçimi, streak)
- **Firebase yerel önbelleği** (çevrimdışı çalışabilmek için)

## 10. Politikadaki değişiklikler

Bu politikayı zaman zaman güncelleyebiliriz. Önemli değişiklikler önceden
uygulama içi bildirim veya e-posta ile duyurulur. "Son güncelleme" tarihi
yukarıda gösterilir.

## 11. İletişim

Sorularınız, talepleriniz veya şikayetleriniz için:

**Erhan Serin**
E-posta: studioperaturkey@gmail.com

---

*Bu doküman bilgi amaçlıdır ve yasal danışmanlık niteliği taşımaz. Tereddüt
ettiğiniz durumlarda KVK Kurumu veya bir avukata danışmanız önerilir.*
