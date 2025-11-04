# Özel Yerlerim Gizlilik Politikası

**Son Güncelleme:** 4 Kasım 2025

Bu gizlilik politikası, Mustafa KARAOSMAN ("mkmusti", "biz", "bizim") tarafından sağlanan "Özel Yerlerim" ("Uygulama") mobil uygulamasını kullanımınız sırasında hangi bilgilerin toplandığını, nasıl kullanıldığını ve korunduğunu açıklamaktadır.

Uygulamamızı kullanarak, bu politikada açıklanan veri toplama ve kullanma uygulamalarını kabul etmiş olursunuz.

### 1. Topladığımız Bilgiler

Uygulamanın temel işlevlerini yerine getirebilmesi için çeşitli türde bilgilere erişir ve bu bilgileri toplarız:

**a) Sizin Sağladığınız Kişisel Bilgiler:**

* **Kullanıcı Hesabı Bilgileri:** Premium özellikler ve bulut yedekleme için Google ile Giriş (`firebase_auth`) kullandığınızda, Google hesabınızla ilişkili temel profil bilgilerinizi (e-posta adresiniz, adınız ve profil fotoğrafınız) toplarız.
* **Kullanıcı İçeriği:** Uygulamaya eklediğiniz "Özel Yerler" ile ilgili veriler. Bunlar:
    * Yer Adı
    * Notlar
    * Puan (Rating)
    * Yer Fotoğrafları
    * Konum Bilgileri (Enlem ve Boylam)

**b) Otomatik Olarak Toplanan Bilgiler:**

* **Konum Verisi:** Yeni bir yer eklerken "Mevcut Konumu Al" özelliğini (`geolocator`) kullandığınızda, cihazınızın hassas coğrafi konum (GPS) verisini toplarız. Bu veri, yalnızca o anki yeri etiketlemek için kullanılır ve siz kaydetmediğiniz sürece saklanmaz.
* **Reklam Kimliği:** Uygulamayı ücretsiz olarak sunabilmek için Google AdMob (`google_mobile_ads`) kullanıyoruz. AdMob, ilgi alanlarınıza yönelik reklamlar göstermek için cihazınızın reklam kimliğini (IDFA veya AAID) toplayabilir.

**c) Eriştiğimiz Cihaz İzinleri:**

* **Kamera (`image_picker`):** Bir yere fotoğraf eklemek için doğrudan kameranızı açmanıza izin vermek amacıyla kamera izni isteriz.
* **Galeri/Depolama (`image_picker`):** Cihazınızın galerisinden mevcut bir fotoğrafı seçip bir yere eklemenize izin vermek için galeri/depolama okuma izni isteriz.
* **Konum (`geolocator`):** "Mevcut Konumu Al" özelliği için `ACCESS_FINE_LOCATION` izni isteriz.

### 2. Bilgilerinizi Nasıl Kullanıyoruz?

Topladığımız bilgileri aşağıdaki amaçlar doğrultusunda kullanırız:

* **Uygulamanın Temel İşlevselliği:** Özel yerlerinizi oluşturmanıza, kaydetmenize (yerel olarak `sqflite` veritabanına) ve yönetmenize olanak tanımak.
* **Bulut Senkronizasyonu (Premium Özellik):** Google hesabınızla giriş yaptığınızda, kaydettiğiniz yerleri (fotoğraflar, notlar ve konumlar dahil) güvenli bir şekilde `Google Cloud Firestore` ve `Firebase Storage` üzerinde yedeklemek ve cihazlarınız arasında senkronize etmek.
* **Konum Etiketleme:** Yeni yerler eklerken coğrafi konumu otomatik olarak doldurmak.
* **Uygulama İçi Satın Almalar:** `in_app_purchase` paketi aracılığıyla Premium üyelik durumunuzu yönetmek ve doğrulamak.
* **Reklam Gösterimi:** Uygulamanın geliştirme ve bakım maliyetlerini karşılamak amacıyla Google AdMob üzerinden kişiselleştirilmiş veya genel reklamlar göstermek.

### 3. Veri Paylaşımı ve Güvenliği

Kişisel verilerinizi üçüncü taraflara satmayız veya kiralamayız. Verileriniz yalnızca aşağıdaki hizmet sağlayıcılarla paylaşılabilir:

* **Google (Firebase / Google Cloud):** Kimlik doğrulama (Auth), bulut veritabanı (Firestore) ve dosya depolama (Storage) hizmetleri için kullanılır. Verileriniz Google'ın güvenli sunucularında saklanır.
* **Google (AdMob):** Reklam sunumu amacıyla.
* **Google (Play Store):** Uygulama içi satın alma işlemlerini yönetmek için.

Verilerinizin güvenliğini sağlamak için (hem yerel `sqflite` veritabanında hem de Firebase
