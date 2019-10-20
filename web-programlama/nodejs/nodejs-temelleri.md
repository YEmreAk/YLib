---
description: Nodejs'i kullanma
---

# 🧱 Nodejs Temelleri

## Paket Yönetimi

Paket kurulumları `npm` komutu yardımıyla yapılır.

### Paketler ve Açıklamaları

Paketler NPM ile `npm install <paket>` komutu yardımıyla indirilir.

* **Normal kurulum:** Ön ek gerektirmez
* **Global kurulum:** `-g` ön eki ile yapılır
* **Dev kurulum:** `--save-dev` son eki ile yapılır

#### Normal Paketler

| Paket | Açıklama | Bağlantılar |
| :--- | :--- | :--- |
| nodemon | Hata ve değişiklik durumunda otomatik derleme |  |
| exporess | Sunucu işlemlerinnde kolaylık sağlar |  |
| colors | Consola renkli çıktılar yazma |  |
| faker | Rastgele veri oluşturmayı sağlar | [🌐](https://cdn.rawgit.com/Marak/faker.js/master/examples/browser/index.html) [👁](https://github.com/marak/Faker.js/) [📥](https://www.npmjs.com/package/faker) |

#### Geliştirici Paketleri

| Paket | Açıklama |
| :--- | :--- |
| nodemon | Hata ve değişiklik durumunda otomatik derleme |

### NPM Kullanım Yapısı

```bash
npm <operasyon> <varsa_ön_ek> <paket> <varsa_son_ek>
```

* `<operasyon>` install, remove ...
* `<varsa_ön_ek>` -g ...
* `<paket>` nodemon, colors, express ...
* `<varsa_son_ek>` --save-dev ...

### Paket Kurulum Örnekleri

```text
npm install nodemon --save-dev
npm install -g babel-cli
npm install colors
```

### Nodejs Dependency Prefixes

`<prefix><dependency_version>`

* ~ This version
* ^ latest version

## Ortam Değişkenleri

Ortam ön ayarları scriptler çalıştırılmadan önce girilen komutlardır.

> [Heroku](https://www.heroku.com/nodejs) gibi sitelerde üretim modu ön eki uygulama çalıştırılmadan uygulanır.

### Ortam Değişkenleri Açıklamaları

Kod içerisinde `process.env.<değişken>` şeklinde erişilir.

| Değişken | Kullanım | Açıklama |
| :--- | :--- | :--- |
| `DEBUG` | `set DEBUG=<dosya ismi>` | Debug modunu belli dosyalar için açma |
| `NODE_ENV` | `set NODE_ENV=<özel_mod>` | Özel modlarda projeyi çalıştırma |
| `PORT` | `set PORT=<port>` | Çalıştıralacak port |

* `<dosya_ismi>` örnekleri:
  * `*` ile her şeyi
  * `lib\*` ile lib'le başlayan herşeyi
  * `index` ile index.js dosyasını
* `<özel_mod>` örnekleri:
  * `stagging` Normal iskelet
  * `production` Üretim iskeleti
* `<port>` örnekleri:
  * `3000` Normal port
  * `5000` Üretim portu

> Değişken örnekleri keyfidir.

### Ortam Değişkenleri Kullanımı

```text
set NODE_ENV=production & set DEBUG=* & npm run-script dev
```

### Herokunun Kullandığı Ortam Değişkenleri

Ücretsiz nodejs sunucularından biri olan [heroku](https://www.heroku.com/nodejs)'nun hali hazırda sunduğu ortam değişkenler:

| Değişken | Değeri | Tipi |
| :--- | :--- | :--- |
| `PORT` | Rastgele | number |
| `NODE_ENV` | "production" | string |

## Nodejs ES6 Yapısını Kullanma

Nodejs'de ES6 yapısı `babel` yardımcısı ile kullanabilinmektedir.

> Tarayıcı es5 yapısını kullanmaktadır.

### Babel Paketleri

| Paket | Açıklama | Kurulum |
| :--- | :--- | :--- |
| `babel-cli` | Konsoldan "babel" ile başlayan komutlara izin verir | Global |
| `babel-register` | NPM üzerinden require ile babel modüllerine erişimi sağlar | Dev |
| `babel-preset-env` | ES5'i derlemek için kullanılır | Dev |

* **Global kurulum:** `-g` ön eki ile yapılır
* **Dev kurulum:** `--save-dev` son eki ile yapılır

### Babel Paketlerinin Kurulumu

Global olarak babel consol komutlarını ve işleyicisini ekler.

```bash
npm install -g babel-cli
npm install babel-register babel-preset-env --save-dev
```

> `babel-cli` global olarak kurulmazsa babel komutları her yerde tanınmaz.

### Babel Yapılandırması

> Bu adım ve sonrasındaki işlemler projenin \(`index.js`\) dizininde yapılmalıdır

#### Babel Derleyici Yapılandırmasını Oluşturma

Babelrc dosyası belli ayarlarla oluşturma

```text
@echo {"presets":[["env",{"targets":{"edge":"17","firefox":"60","chrome":"67","safari":"11.1","node":"current"}}]]} > .babelrc
```

> `targets` isteğe bağlıdır. Hedeflenen tarayıcıları gösterir.

#### Babel Derleme Araçlarını Yapılandırma

Tools dizini oluşturup, içindeki dosyaya derleme parametrelerini yazıyoruz.

```text
mkdir tools & @echo require("babel-register") > tools/dev && @echo require("./../index.js") >> tools/dev
```

> Not: Bu kısımdaki `tools/dev` ile diğer adımdaki işlemler yapılmaktadır

### Packege.json Oluşturma

```text
npm init
```

> Bu işlem oluşturulması istenen dizinde yapılmalıdır.

### Package.json Scriptlerini Oluşturma

`package.json` dosyası içerisindeki script kısmında alttakiler eklenir.

```javascript
"scripts": {
  "test": "node test",
  "start": "node dist/index.js",
  "dev": "set DEBUG=* & node tools/dev",
  "build": "mkdir dist & babel *.js lib/**/*.js -s -d dist & xcopy public dist\\public /s /i /e /y",
  "build:db": "mkdir dist & babel *.js lib/**/*.js -s -d dist & xcopy public dist\\public /s /i /e /y & xcopy database dist\\database /s /i /e /y",
  "build:start": "npm run-script build & npm run-script start",
  "clean": "xcopy dist\\database database /s /i /e /y & rd /s /q dist",
  "clean:all": "rd /s /q dist",
  "rebuild": "npm run-script clean & npm run-script build",
  "rebuild:db": "npm run-script clean & npm run-script build:db"
}
```

#### Build Script Yapısı

* `mkdir dist` Dist adlı klasör oluşturulur
* `babel [her bir js dosyasının yolu] -s -d dist` Javasciprt dosyaları es5 tipinde düzenlenip dist içine atılır
* `xcopy [klasör] dist\\[klasör] /s /i /e /y` Dinamik veri tutan klasörler varsa dist içine kopyalanır

### Package.json için Script Açıklamaları

| Script | Açıklama |
| :--- | :--- |
| `test` | Tanımlanmamıştır |
| `start` | Dist klasöründeki es5 formatındaki index.js'i çalıştırır. Build edilmeyi gerektirir |
| `dev` | Geliştirici modunda çalıştırır. Es6 tipineki kodlar babel aracılığı ile kullanılır |
| `build` | Dist klasörü içine es6 tipindeki kodların es5'i oluşturulur. Start scripti için gerekli işlemdir |
| `build:db` | Veri tabanı'nı da dahil ederek build işlemini yapar |
| `build:start` | Build işleminden sonra start işlemini başlatır |
| `clean` | Veri tabanını depolayarak dist klasörünü temizler |
| `clean:all` | Veri tabanı dahil tüm dist dizinini temizler |
| `rebuild` | Eski dist klasörünü kaldırır, yenisi oluşturur |
| `rebuild:db` | Eski dist klasörünü veritabanını depolayarak kaldırır, yenisi oluşturur |

### Programı Derleme İşlemi

Package.json dosyasındaki scriptleri çalıştırma

```text
npm run-script [script]
```

* `[script]` scripts içindeki isimler; start, dev, build

## VsCode için Debug Ayarları

Açıklama [videosu](https://www.youtube.com/watch?v=yFtU6_UaOtA) ve [metni](https://github.com/yedhrab/YWiki/tree/169abadfd1b8862c004399268f6ca1f9f9359d61/1%20-%20Programlama%20Notları/5%20-%20Web%20Programlama/Uygulama%20Notları/VsCode.md#nodejs-için-debug-ayarı) için üzerlerine tıklayabilirsin.

```javascript
## Kod Bankası

### Fonksiyon İsmi, Satırı ve Dosya Adı Alma

```js
export function _getCallerInfo() {
  const err = new Error();
  let index = 3;
  let line = err.stack.split("\n")[index];
  let functionName = line.split(" at ")[1].split(" ")[0];

  while (functionName.includes(`C:/`)) {
    index++;
    line = err.stack.split("\n")[index];
    functionName = line.split(" at ")[1].split(" ")[0];
  }

  let callerInfo = line.split(`${projectName}/`);
  callerInfo = callerInfo[callerInfo.length - 1];

  const filename = callerInfo.split(".")[0];
  const lineInfos = callerInfo.replace(filename + ".js:", "").replace(")", "");
  return `${filename}:${functionName}:${lineInfos}`; // lib\server:func(12:21)
}
```

## Harici Bağlantılar

* [Callback yerine Async Kullanma](https://medium.freecodecamp.org/javascript-from-callbacks-to-async-await-1cc090ddad99)
* [Async & Await](https://medium.com/@tkssharma/writing-neat-asynchronous-node-js-code-with-promises-async-await-fa8d8b0bcd7c)
* [Fonksiyonu Çağıran Dosya İsmini Bulma](https://stackoverflow.com/a/29581862/9770490)
* [Debugging Visual Studio Code \(Node\)](https://www.youtube.com/watch?v=yFtU6_UaOtA)
* [Nodejs React ve Redux ile Medium Klonu](https://github.com/krissnawat/medium-clone-on-node)
* [Top 10 Es6 Feature](https://webapplog.com/es6/)
* [Chrome API](https://stackoverflow.com/a/52257595/9770490)

