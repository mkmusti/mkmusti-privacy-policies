Özel Yerlerim

Anılarınızı Haritaya İşleyin 

"Özel Yerlerim", kullanıcıların kişisel olarak önemli buldukları konumları kaydetmeleri ve yönetmeleri için tasarlanmış kapsamlı bir Flutter uygulamasıdır. Bu proje, bir yerin adını , kişisel notları , fotoğraflarını , coğrafi konumunu (enlem/boylam) ve 1-5 yıldız arası puanını  saklamalarına olanak tanır.



Uygulama, hem çevrimdışı (yerel) hem de çevrimiçi (bulut) çalışabilen hibrit bir veri depolama modeli üzerine kurulmuştur.

🚀 Kilit Özellikler
Bu projenin öne çıkan teknik ve fonksiyonel özellikleri şunlardır:

1. Hibrit Veri Depolama Modeli
Uygulama, kullanıcının durumuna göre akıllı bir veri depolama stratejisi kullanır (database_service.dart):


Yerel Depolama (Ücretsiz Sürüm): Kullanıcı giriş yapmamışsa veya premium değilse, tüm veriler cihazda yerel bir SQLite veritabanında (ozel_yerler.db) güvenle saklanır . Ücretsiz sürüm, AppConfig dosyasına göre 15 yer kaydı ile sınırlıdır .






Bulut Depolama (Premium Sürüm): Kullanıcı Firebase Authentication (Google Sign-In ile) kullanarak giriş yapmışsa ve premium üyeyse, tüm verileri Firebase Firestore üzerinde bulutta saklanır .






Akıllı Veri Taşıma: Uygulama, kullanıcı premium üyeliğe geçtiği anda, cihazdaki tüm yerel SQLite verilerini otomatik olarak Firestore bulut hesabına taşıyan bir migrateLocalDataToFirestore fonksiyonuna sahiptir .

2. Yapay Zeka Destekli Fotoğraf Analizi

vision_service.dart  dosyası sayesinde uygulama, fotoğraf ekleme sürecini akıllı hale getirir:

Kullanıcı image_picker ile bir fotoğraf çektiğinde veya seçtiğinde, bu fotoğraf Google Vision API'ye gönderilir .


Yapay zeka, fotoğraftaki bir anıtsal yapıyı (LANDMARK_DETECTION) veya bir nesneyi (LABEL_DETECTION) tanır.

Başarılı bir tanıma olursa, yerin adını (_adController.text) ve o yerle ilgili bir Wikipedia bağlantısını (_infoUrl)  otomatik olarak doldurur.



3. Para Kazanma (Monetization) Entegrasyonu
Proje, gelir elde etmek için iki ana modeli destekler:


Reklamlar (Google AdMob): google_mobile_ads paketi  entegre edilmiştir.


Ana sayfada sabit bir BannerAdWidget (Banner Reklam) gösterilir .


AdHelper servisi , bir yer silme veya kaydetme gibi işlemlerden sonra showInterstitialAd (Geçiş Reklamı) gösterir.


Premium Üyelik: in_app_purchase paketi ve PremiumService  desteği mevcuttur. Bu servis, kullanıcının premium olup olmadığını yönetir ve bulut depolama gibi özellikleri premium kullanıcılara açar.



4. Gelişmiş Güvenlik (Uygulama Kilidi)
Kullanıcı verilerinin gizliliğini sağlamak için local_auth paketi  kullanılarak bir güvenlik katmanı eklenmiştir:



Kullanıcılar dilerse "Ayarlar" menüsünden  uygulama kilidini aktif edebilir.



Uygulama, hem Biyometrik doğrulama (Parmak İzi / Yüz Tanıma) hem de 4 haneli PIN Kodu  ile kilitlenmeyi destekler.


5. Harita ve Konum Servisleri
Uygulama, tam teşekküllü bir konum yönetimi sunar:
Maps_flutter paketi ile kaydedilen tüm yerler bir harita üzerinde pinlenerek gösterilir .
geolocator  paketi ile yeni yer eklerken kullanıcının mevcut konumu alınabilir.
url_launcher sayesinde kaydedilen bir yer için harici harita uygulamasından (Google Maps vb.) yol tarifi alınabilir .




6. Modern Arayüz ve Dil Desteği
7. 
Proje, provider  paketini state management (durum yönetimi) için kullanır ve modern UI/UX standartlarını takip eder:
Çoklu Dil Desteği: LanguageService , uygulama içindeki tüm metinleri yönetir ve Türkçe (TR) ile İngilizce (EN) dilleri arasında geçiş yapılmasını sağlar.
Çoklu Tema Desteği: ThemeService , kullanıcının Açık (Light), Koyu (Dark) veya Sistem varsayılanı  temalarından birini seçmesine olanak tanır.
Güvenli Anahtar Yönetimi: Firebase, AdMob ve Vision API anahtarları gibi tüm hassas bilgiler, flutter_dotenv paketi aracılığıyla .env dosyasından  güvenli bir şekilde okunur.


🛠️ Kullanılan Teknolojiler ve API'ler

Platform: Flutter 
Veritabanı: SQLite (yerel) & Firebase Firestore (bulut) 
Kimlik Doğrulama: Firebase Authentication (Google Sign-In ile )
Durum Yönetimi: Provider 
Reklam: Google Mobile Ads (AdMob) 
Yapay Zeka: Google Vision API 
Harita: Google Maps Flutter 
Konum: Geolocator 
Güvenlik: Local Auth (Biyometrik & PIN) 

Anahtar Yönetimi: flutter_dotenv 

Yardımcı Paketler: image_picker, url_launcher, share_plus, http 

💻 Desteklenen Platformlar
Bu Flutter projesi, tek bir kod tabanından altı platformun tamamı için yapılandırılmıştır:

Android 

iOS 

Web 

macOS 

Windows 

Linux
