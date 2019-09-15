---
description: Kişisel veya kurumsal sitenizi yönetmek için bilgiler 📓
---

# Web Sitesi Yönetimi 

## 🌎 Sitenizi Kendi Alan Adınıza Bağlama (Domain)

CNAME kayıtları ile halledilen bir işlemdir

- Domaininiz bağlamak istediğiniz siteye girin ve oradaki yönergeleri takip ederek, hosting (sunucu) urli alın.
- Domaini satın aldığınız siteye giriş yapın ve **DNS Hizmeti ve Yönetimi** alanına girin
- **CNAME Kayıtları** altında:
  - `Alt alan adı` olarak belirtilen yere _subdomain_'i yazın (örn: wiki.yemreak.com)
  - `Sunucu` alanına size verilen bağlantıyı kopyalayın. (örn: hosting.github.com)

## 🔍 Google Search Console ile Arama Motoru Yönetimi

- [Google Search Console](https://search.google.com/search-console/welcome?utm_source=about-page)'a giriş yapın
- Çıkan seçeneklerden **domain** alanını seçin ve domaininizi yazın
- Domaini satın aldığınız siteye giriş yapın ve **DNS Hizmeti ve Yönetimi** alanına girin
- **TXT Kayıtları** altında:
  - `Key` alanını boş bırakın
  - `Value` alanına google'ın size verdiği metni kopyalayın. 
    - (örn: `google-site-verification=********************************`)
- Çıkan arayüzde arama alanına URL'lerinizi yazın, indekslenmeyen URL için talepte bulunun

## 📊 Google Analytic ile Sitenize Gelenleri Analiz Etme

- [Google Analytics](http://analytics.google.com)'e giriş yapın
- Sol alt köşedeki <kbd>⚙ Admin</kbd> butonuna tıklayın
- `Property` alanında hiç hesap yoksa, `Add Propery`'e tıklayın, varsa isterseniz onu seçin
- `Tracking Info` alanından `Tracking Code`'u açın
  - **Tracking Id**'yi kopyalayın
  - Eğer sitenizin desteği yoksa **Website Tracking** adı altındaki **HTML** kodlarını kopyalayın.
- Sitenizin **HTML** kodlarına girin ve en üste `<scripts>`'lerinizin olduğu alana yapıştırın

### 💠 Google Analytic Üzerinden Filtre Uygulama 

Admin - Property - Filter - Add Filter alanından aşağıdaki özelliklere sahip filtre ekleyin

- Filter Type: Custom
- Include
- Pattern `\.domain\.com` (örn: `\.yemreak\.com`) yazın
- Filter Verification alannından kontrol edip kaydedin.
