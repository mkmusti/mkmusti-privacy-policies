# Özel Yerlerim Gizlilik Politikası

**Son Güncelleme:** 1 Kasım 2025

Mustafa Karaosman ("mkmusti", "biz") olarak, "Özel Yerlerim" ("Uygulama") kullanıcılarımızın gizliliğine saygı duyuyoruz. Bu Gizlilik Politikası, Uygulamamızı kullandığınızda bilgilerinizi nasıl topladığımızı, kullandığımızı, ifşa ettiğimizi ve koruduğumuzu açıklamaktadır.

Lütfen bu gizlilik politikasını dikkatle okuyun. Bu politikayı kabul etmiyorsanız, lütfen uygulamayı kullanmayın.

## TOPLADIĞIMIZ VERİLER

Uygulamamızı kullandığınızda sizden çeşitli bilgiler toplayabiliriz:

### 1. Kişisel ve Kullanıcı Tarafından Oluşturulan Veriler

* **Hesap Bilgileri (Premium Üyeler):** Google ile Giriş yapmayı (Firebase Authentication)  seçerseniz, adınızı, e-posta adresinizi ve profil fotoğrafı URL'nizi (Google hesabınızdan sağlanan) toplarız 
* **Kayıt Verileri:** Uygulamaya girdiğiniz "Özel Yer" kayıtları. Buna yerin adı, notlarınız, verdiğiniz puan (1-5) ve kaydettiğiniz fotoğraf dahildir.

### 2. Cihaz İzinleri Yoluyla Toplanan Veriler

Uygulamanın temel özelliklerini sunabilmek için cihazınızdan bazı izinler isteriz:

**Konum Bilgisi (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`):**  "Mevcut Konumu Al" özelliğini kullandığınızda, hassas coğrafi konumunuzu (enlem ve boylam) toplarız 
**Kamera (`CAMERA`):**  Bir yere fotoğraf eklemek için "Kamera" seçeneğini kullandığınızda cihazınızın kamerasına erişim isteriz 
**Galeri/Fotoğraflar (Dolaylı İzin):** "Galeri" seçeneğini kullandığınızda, cihazınızın fotoğraf kütüphanesinden bir görüntü seçmenize olanak tanırız
**Biyometrik Veri (`USE_BIOMETRIC`):**  "Uygulama Kilidi" özelliğini kullanmayı seçerseniz, cihazınızın parmak izi veya yüz tanıma donanımına erişim için izin isteriz. **ÖNEMLİ:** Biyometrik verileriniz ASLA tarafımızdan toplanmaz, saklanmaz veya sunucularımıza gönderilmez . Bu izin, yalnızca cihazınızın kendi işletim sistemine (Android) kimliğinizi doğrulatmak için kullanılır.

### 3. Otomatik Olarak Toplanan Veriler

**Reklam Verileri:** Uygulama, Google AdMob aracılığıyla reklamlar gösterir. AdMob, kişiselleştirilmiş reklamlar sunmak amacıyla (cihaz modeli, işletim sistemi, anonim reklam kimliği gibi) verileri toplayabilir.

## VERİLERİNİZİ NASIL KULLANIYORUZ

Verilerinizi aşağıdaki amaçlarla kullanırız:

* **Uygulamanın Çalışması İçin:**
    * Yerel (Ücretsiz) Kullanıcılar: Tüm kayıt verileriniz (notlar, fotoğraflar vb.) **yalnızca cihazınızda yerel bir SQLite veritabanında** saklanır ve internete gönderilmez.
    * Premium (Bulut) Kullanıcılar: Google ile giriş yaptığınızda, kayıtlarınız (mevcut yerel kayıtlarınız dahil hesabınızla ilişkilendirilir ve **Google Firebase Firestore** bulut sunucularında güvenle saklanır. Bu, verilerinize birden fazla cihazdan erişmenizi ve verilerinizi kaybetmemenizi sağlar.

* **Özellikleri Sunmak İçin:**
    * Konum veriniz, kaydettiğiniz yerin harita üzerinde gösterilmesi ve o yere "Yol Tarifi Al" özelliğinin çalışması için kullanılır.
    * Kamera ve Galeri erişimi, yer kayıtlarınıza görsel anılar eklemeniz için kullanılır.
    * "Uygulama Kilidi" için Biyometrik veya PIN doğrulaması kullanılır.

* **Yapay Zeka Analizi İçin:**
    * Bir fotoğraf eklediğinizde, bu fotoğraf (anonim olarak) yerin adını otomatik olarak algılayabilmek amacıyla (örn: "Eyfel Kulesi") analiz için **Google Vision API** servisine gönderilir. Analizden sonra fotoğrafın kendisi Google sunucularında saklanmaz.

* **Gelir Elde Etmek İçin:**
    * Uygulamanın ücretsiz sürümünü desteklemek amacıyla Google AdMob üzerinden reklamlar göstermek için.

## VERİLERİNİZİ KİMLERLE PAYLAŞIYORUZ

Verilerinizi üçüncü taraflara satmayız. Ancak, uygulamanın çalışması için aşağıdaki iş ortaklarıyla veri paylaşımı yapabiliriz:

* **Google (Firebase, AdMob, Google Maps, Vision API):** Uygulamamızın altyapısı büyük ölçüde Google servislerine dayanmaktadır (Kimlik doğrulama, bulut veritabanı, haritalar, reklamlar ve fotoğraf analizi). Bu servisler kendi gizlilik politikalarına tabidir.
* **Yasal Zorunluluklar:** Yasal bir yükümlülük veya resmi bir talep olması durumunda verilerinizi paylaşabiliriz.

## VERİ GÜVENLİĞİ

Verilerinizin güvenliğini ciddiye alıyoruz. Veriler, cihazınızda (SQLite) veya güvenli Google Firebase sunucularında (Premium ise) saklanır. İletim sırasındaki tüm veriler (örn: Vision API'ye gönderilen fotoğraflar) şifrelenir.

## VERİLERİNİZİ SİLME

Uygulama içindeki kayıtlarınızı istediğiniz zaman silebilirsiniz. Bir kaydı silmeniz, o kaydın veritabanından (yerel SQLite  veya bulut Firestore kalıcı olarak kaldırılmasına neden olur.

## ÇOCUKLARIN GİZLİLİĞİ

Bu uygulama 13 yaşın altındaki çocuklara yönelik değildir.

## BU POLİTİKADAKİ DEĞİŞİKLİKLER

Bu Gizlilik Politikasını zaman zaman güncelleyebiliriz. Yeni politikayı bu sayfada yayınlayacağız.

## İLETİŞİM

Bu Gizlilik Politikası hakkında herhangi bir sorunuz veya yorumunuz varsa, lütfen bizimle iletişime geçin:

**Mustafa Karaosman**
mkmusti@gmail.com
