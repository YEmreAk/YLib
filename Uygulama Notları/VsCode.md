# VsCode <!-- omit in toc -->

> `HOME` tuşu ile yukarı yönlenebilrsiniz.

- [VsCode için Önemli Notlar](#vscode-i%C3%A7in-%C3%B6nemli-notlar)
- [VsCode kısayolları](#vscode-k%C4%B1sayollar%C4%B1)
  - [Hızlı Notlar](#h%C4%B1zl%C4%B1-notlar)
  - [Verimlilik Kısayolları](#verimlilik-k%C4%B1sayollar%C4%B1)
  - [Aksiyon Penceresi](#aksiyon-penceresi)
  - [İmleç Kısayolalrı](#i%CC%87mle%C3%A7-k%C4%B1sayolalr%C4%B1)
  - [Metin Kısayolları](#metin-k%C4%B1sayollar%C4%B1)
  - [Editör Kısayolları](#edit%C3%B6r-k%C4%B1sayollar%C4%B1)
  - [Görünüm Kısayolları](#g%C3%B6r%C3%BCn%C3%BCm-k%C4%B1sayollar%C4%B1)
- [Faydalı Eklentiler](#faydal%C4%B1-eklentiler)
  - [Proje Yönetimi Eklentileri](#proje-y%C3%B6netimi-eklentileri)
  - [Verimlilik Eklentileri](#verimlilik-eklentileri)
  - [Görsellik Eklentileri](#g%C3%B6rsellik-eklentileri)
  - [Programlama Eklentileri](#programlama-eklentileri)
    - [Web Programlama Eklentileri](#web-programlama-eklentileri)
    - [Javascript - Nodejs Eklentileri](#javascript---nodejs-eklentileri)
  - [Yapılandırma Eklentileri](#yap%C4%B1land%C4%B1rma-eklentileri)
  - [Dökümantasyon Eklentileri](#d%C3%B6k%C3%BCmantasyon-eklentileri)
- [Editör ayarları](#edit%C3%B6r-ayarlar%C4%B1)
  - [Editör Ayar Dosyaları](#edit%C3%B6r-ayar-dosyalar%C4%B1)
  - [Intellicode Ayaları](#intellicode-ayalar%C4%B1)
  - [Editör Değişkenleri](#edit%C3%B6r-de%C4%9Fi%C5%9Fkenleri)
  - [Editör Klavye Kısayollarım](#edit%C3%B6r-klavye-k%C4%B1sayollar%C4%B1m)
    - [Windows10 Klavye Kısayolları](#windows10-klavye-k%C4%B1sayollar%C4%B1)
    - [Linux Klavye Kısayolları](#linux-klavye-k%C4%B1sayollar%C4%B1)
  - [Editör JSON Ayarlarım](#edit%C3%B6r-json-ayarlar%C4%B1m)
  - [Editör Eklentilerim](#edit%C3%B6r-eklentilerim)
    - [Python için Eklentiler](#python-i%C3%A7in-eklentiler)
- [Eski Ayarlarım](#eski-ayarlar%C4%B1m)
  - [Java Ayarları](#java-ayarlar%C4%B1)
  - [Code Runner Ayarları](#code-runner-ayarlar%C4%B1)
    - [Code Runner Kısayollar](#code-runner-k%C4%B1sayollar)
- [Debug Ayarları](#debug-ayarlar%C4%B1)
  - [Nodejs için Debug Ayarı](#nodejs-i%C3%A7in-debug-ayar%C4%B1)
- [VsCode Değişkenleri](#vscode-de%C4%9Fi%C5%9Fkenleri)
- [Yapılacaklar](#yap%C4%B1lacaklar)
- [Harici Linkler](#harici-linkler)

## VsCode için Önemli Notlar

VsCode dünyanın en çok kullanılan text editörü olarak geçmektedir.

- İlk defa VsCode kullanıyor isen [buradaki][Vscode Intro Videos] videoları izlemen ve açıklamaları okuman oldukça önemli (okumadan öğrenemezsin 😔)
- VsCode'a başlamadan önce [buradan][Vscode Doc] üzerinden, hangi dile odaklı çalışacaksanız onun dökümasyanunu okuyun
- Ardından gerekli olan eklentileri, eklenti mağazasından indirin (<kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>X</kbd>)
- Sağ taraftaki kodların ön izlesinin olduğu alanı (minimap) kaldırmak için `"editor.minimap.enabled": false`

## VsCode kısayolları

PDF dökümanı 📃 için [buraya](..\pdfs\keyboard-shortcuts-windows.pdf) bakabilirsin.

> [Vscode ipuçları](https://code.visualstudio.com/docs/getstarted/tips-and-tricks#_files-and-folders)

### Hızlı Notlar

- [Snipped](https://code.visualstudio.com/docs/getstarted/tips-and-tricks#_snippets)

### Verimlilik Kısayolları

- Zen Mode <kbd>CTRL</kbd> + <kbd>K</kbd> + <kbd>Z</kbd>

### Aksiyon Penceresi

`CTRL` + `P` ile aksiyon penceresiini erişebilirsiniz.

| Kısayol    | Açıklama                                             |
| ---------- | ---------------------------------------------------- |
| `#`        | Çalışma dizininde arama                              |
| `@` & `@:` | Dosya içerisnde sembole özgü arama (gruplu gösterme) | <kbd> CTRL </kbd> + <kbd> SHIFT </kbd> + <kbd> O </kbd> |
| `>`        | Komutlarda arama                                     |
| `:`        | Satıra yönelme                                       |
| `?`        | Yardım                                               |

### İmleç Kısayolalrı

- <kbd>ALT</kbd> Birden fazla işaretçi belirleme
- <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>Yukarı yada Aşağı Tuşu</kbd> İşaretçi sayısını arttırma
- <kbd>CTRL</kbd> + <kbd>U</kbd> Bir önceki imleci seçer

### Metin Kısayolları

- <kbd>SHIFT</kbd> + <kbd>ALT</kbd> + <kbd>Sağ veya Sol</kbd> Bir sonraki bloğu seçme
- <kbd>SHIFT</kbd> + <kbd>ALT</kbd> + <kbd>Yukarı veya Aşağı</kbd> Satırı çoğaltma
- <kbd>CTRL</kbd> + <kbd>D</kbd> Kelimeyi seçme
  - Birden fazla tekrarlanırsa aynı metinleri seçer yanlarına imleç getirir
  - Değişkenleri yeniden adlandırmada çok faydalıdır
- <kbd>CTRL</kbd> + <kbd>L</kbd> Satırı seçme
- <kbd>CTRL</kbd> + <kbd>X</kbd> Satırı kesme
- <kbd>ALT</kbd> + <kbd>Yukarı yada Aşağı Tuşu</kbd> Satırı taşıma
  - Sırasıya: Kelime, Satır, Kod bloğu, ..., Tüm metin

### Editör Kısayolları

- <kbd>ALT</kbd> tuşuna basılı tutarak dosyalara tıklarsan yan panelde açılır
- <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Sağ veya Sol</kbd> Pencereyi sağa veya sola alır
- <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>A</kbd> Seçili alanı yorum satırı yapma
- Tüm kodları gizleme (*fold all*)
  - Windows and Linux için <kbd>Ctrl</kbd> + <kbd>K</kbd>, <kbd>Ctrl</kbd> + <kbd>0</kbd> (sıfır)
  - macOS için <kbd>⌘</kbd> + <kbd>K</kbd>, <kbd>⌘</kbd> + <kbd>0</kbd> (sıfır)
- Kodları seviyeye göre gizleme
  - <kbd>Ctrl</kbd> + <kbd>K</kbd>, <kbd>Ctrl</kbd> + <kbd><sayı></kbd>
  - Örn: <kbd>Ctrl</kbd> + <kbd>K</kbd>, <kbd>Ctrl</kbd> + <kbd>2</kbd>
- Tüm kodları gösterme (*unfold all*)
  - Windows and Linux için <kbd>Ctrl</kbd> + <kbd>K</kbd>, <kbd>Ctrl</kbd> + <kbd>J</kbd> (sıfır)
  - macOS için <kbd>⌘</kbd> + <kbd>K</kbd>, <kbd>⌘</kbd> + <kbd>J</kbd>

### Görünüm Kısayolları

- <kbd>CTRL</kbd> + <kbd>Yukarı yada Aşağı Tuşu</kbd> Görünen ekranı kaydırma
- <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>V</kbd> *Markdown preview*'i açar
- <kbd>CTRL</kbd> + <kbd>J</kbd> Alt paneli görünür kılar

## Faydalı Eklentiler

Eklentiler üzerine bir yazı olan [bu linke](https://www.freecodecamp.org/news/here-are-some-super-secret-vs-code-hacks-to-boost-your-productivity-20d30197ac76/) tıklamanda fayda var.

### Proje Yönetimi Eklentileri

| Eklenti                                                                                                                | Açıklama                                        |
| ---------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| [VS Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)                        | Anlık olarak kod paylaşma                       |
| [Live Share Audio](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-audio)               | Anlık olarak ses paylaşma                       |
| [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)                                 | Yapılacakları gösteren arayüz                   |
| [Git Project Manager](https://marketplace.visualstudio.com/items?itemName=felipecaputo.git-project-manager)            | Proje kısayolları, sık kullanılanlar vs.        |
| [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)                      | Git yönetimi arayüzü                            |
| [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)                             | Git commit geçmişini gösterir                   |
| [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)                              | Docker sanal makinesi için uyumluluk            |
| [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) | Uzak bilgisayarlarda metni VsCode ile açma      |
| [GitBlame](https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame)                                      | Satırların en son ne zaman değiştiğini gösterir |

### Verimlilik Eklentileri

| Eklenti                                                                                                         | Açıklama                                        |
| --------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Scratchpad                                                                                                      | Anlık derleyiciler                              |
| [WakaTime](https://marketplace.visualstudio.com/items?itemName=WakaTime.vscode-wakatime)                        | Kodlama başında geçen vakti raporlar            |
| [Paste Image](https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image)                    | Pano'dan resim kopyalama                        |
| [advanced-new-file](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file)           | Klavye üzerinden dosya işlemleri                |
| [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) | İmla kontrolü                                   |
| [vscode-spotify](https://marketplace.visualstudio.com/items?itemName=shyykoserhiy.vscode-spotify)               | Spotify ile müzik desteği                       |
| [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)              | Tag'ları otomatik kapatma                       |
| [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)            | Tag'ların biri değişirse, diğeri de güncellenir |

### Görsellik Eklentileri

| Eklenti                                                                                                           | Açıklama                        |
| ----------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| [Deepdark Material Theme](https://marketplace.visualstudio.com/items?itemName=Nimda.deepdark-material)            | Çok karanlık bir tema           |
| [Sublime Material Theme](https://marketplace.visualstudio.com/items?itemName=jprestidge.theme-material-theme)     | Sublime Editörün temaları       |
| [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)              | Dosya ikon teması               |
| [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)            | En sık kullanılan karanlık tema |
| [Material Theme](https://marketplace.visualstudio.com/items?itemName=Equinusocio.vsc-material-theme)              | Popüler tema seti               |
| [Base16 Tomorrow Dark+](https://marketplace.visualstudio.com/items?itemName=Shurelia.base16-tomorrow-dark-vscode) | Karanlık tema                   |
| [Dracula Official](https://marketplace.visualstudio.com/items?itemName=dracula-theme.theme-dracula)               | Karanlık bir tema               |

### Programlama Eklentileri

VsCode programlama dökümantasyon için [buraya](https://code.visualstudio.com/docs) bakabilirsin.

| Eklenti                                                                                                                             | Açıklama                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| [Visual Studio IntelliCode - Preview ☆](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode) | AI ile en sık kullanılan metodları önerir. 2 kez `CTRL` + `SPACE` yaparsanız detaylarını da gösterir |
| Scratchpad                                                                                                                          | Anlık derleyiciler                                                                                   |
| [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)                                        | Editör üzerinden projeleri derleme & çalıştırma                                                      |
| [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)                         | Dosya yollarını yazarken yardımcı olur                                                               |
| [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype)                                       | JSON'ı koda uyarlama                                                                                 |
| [Open File](https://marketplace.visualstudio.com/items?itemName=Fr43nk.seito-openfile)                                              | Yolu verilen dosyayı vscode içinde açma                                                              |
| *Code Snippets*                                                                                                                     | Dil'e özel anahtar kelimeler ile kod tamamlama                                                       |
| Fire Code                                                                                                                           | == >= gibi simgeler yerine alışkın olduğumuz elle yazılan simgeler gelir                             |
| [30 seconds of code](https://marketplace.visualstudio.com/items?itemName=30-seconds.30-seconds-of-code)                             | Code snippet'leri                                                                                    |
| [Matlab](https://marketplace.visualstudio.com/items?itemName=Gimly81.matlab)                                                        | Matlab                                                                                               |
| [Java](https://marketplace.visualstudio.com/items?itemName=redhat.java)                                                             | Language Support for Java(TM) by Red Hat                                                             |

#### Web Programlama Eklentileri

| Eklenti                                                                                                                         | Açıklama                                     |
| ------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| [IntelliSense for CSS class names in HTML](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion) | CSS classlarını önerme                       |
| [Icon Fonts](https://marketplace.visualstudio.com/items?itemName=idleberg.icon-fonts)                                           | İkon kısayolları sağlar                      |
| [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)                                            | Postman gibi istemci istekleri arayüzü sunar |
| [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)                         | Chrome için hata ayıklama özelliği           |

#### Javascript - Nodejs Eklentileri

| Eklenti                          | Açıklama                                                                                |
| -------------------------------- | --------------------------------------------------------------------------------------- |
| [Quokka.js]                      | Anlık derleyici ve hata ayıklama ([video](https://www.youtube.com/watch?v=eyzO1xPI6_k)) |
| [Prettier - Code formatter]      | Kod formatlama ve güzelleştirme                                                         |
| [JavaScript (ES6) code snippets] | Kod kısayolları                                                                         |
| [Babel Javascript]               | ES6 tipinde yazmayı sağlar                                                              |
| [npm Intellisese]                | NPM modüllerini önerir                                                                  |
| [jshint]                         | Javascript imla kontrolcüsü                                                             |
| [Eslint]                         | JS için imla kontrolcüsü                                                                |
| [Import Cost]                    | Bellek kullanımını gösterir                                                             |

### Yapılandırma Eklentileri

| Eklenti                                                                                                   | Açıklama |
| --------------------------------------------------------------------------------------------------------- | -------- |
| [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) |          |

### Dökümantasyon Eklentileri

| Eklenti                                                                                                    | Açıklama                                                                  |
| ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)      | Markdown için gerekli tüm içeriklere, kısayollara ve formatlayıcıya sahip |
| [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)         | Markdown hatalarının altını çizme ve uyarma                               |
| [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)                     | Markdown'u PDF'e çevirme                                                  |
| [MarkDown To-Do](https://marketplace.visualstudio.com/items?itemName=TomasHubelbauer.vscode-markdown-todo) | Yapılacaklar listesini gösteren arayüz                                    |
| [Paste Image](https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image)               | Panodan resim kopyalama                                                   |
| [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)              | Latex, matematik dökümanı hazırlama eklentisi                             |

## Editör ayarları

> Sol alt köşedeki `ayarlar` simgesi -> Sağ üst köşedeki `{}` simgesine tıklayıp oraya bunlardan istediklerini kopyalayabilirsin.

### Editör Ayar Dosyaları

- Windows: `%APPDATA%\Code\User\settings.json`
- macOS: `$HOME/Library/Application Support/Code/User/settings.json`
- Linux: `$HOME/.config/Code/User/settings.json`

### Intellicode Ayaları

Buradan [detaylara][Intellicode] erişebilirsin.

### Editör Değişkenleri

Değişkenlerin kullanım şekilleri:

- `${<değişken>}`
  - Eğer özel karakter içeriyorsa bu yöntem daha sağlıklıdır
- `$<değişken>`

| Değişken          | Açıklama                 |
| ----------------- | ------------------------ |
| `workspaceFolder` | Çalışma dizini yolu      |
| `file`            | Açık olan dosya yolu     |
| `fullFileName`    | Tam açık olan dosya yolu |
| `pythonPath`      | Python yolu              |

### Editör Klavye Kısayollarım

#### Windows10 Klavye Kısayolları

```json
// Place your key bindings in this file to override the defaults
[
    {
        "key": "ctrl+[KeyI] ctrl+[KeyI]",
        "command": "git.sync"
    },
    {
        "key": "ctrl+[KeyI] ctrl+p",
        "command": "git.pull"
    },
    {
        "key": "ctrl+shift+[KeyI] ctrl+shift+p",
        "command": "git.pullFrom"
    },
    {
        "key": "ctrl+[KeyI] ctrl+o",
        "command": "git.checkout"
    },
    {
        "key": "ctrl+oem_7",
        "command": "markdown.extension.editing.toggleItalic",
        "when": "editorTextFocus && !editorReadonly && editorLangId == 'markdown'"
    },
    {
        "key": "ctrl+j",
        "command": "workbench.action.terminal.toggleTerminal"
    },
    {
        "key": "ctrl+j",
        "command": "-workbench.action.togglePanel"
    },
    {
        "key": "ctrl+shift+a",
        "command": "editor.action.blockComment",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "alt+v",
        "command": "extension.pasteImage",
        "when": "editorTextFocus"
    },
    {
        "key": "ctrl+alt+v",
        "command": "-extension.pasteImage",
        "when": "editorTextFocus"
    }
]

```

#### Linux Klavye Kısayolları

```json
[
    {
        "key": "ctrl+[KeyI] ctrl+[KeyI]",
        "command": "git.sync"
    },
    {
        "key": "ctrl+[KeyI] ctrl+p",
        "command": "git.pull"
    },
    {
        "key": "ctrl+shift+[KeyI] ctrl+shift+p",
        "command": "git.pullFrom"
    },
    {
        "key": "ctrl+[KeyI] ctrl+o",
        "command": "git.checkout"
    },
    {
        "key": "ctrl+j",
        "command": "workbench.action.terminal.toggleTerminal"
    },
    {
        "key": "ctrl+j",
        "command": "-workbench.action.togglePanel"
    }
]
```

### Editör JSON Ayarlarım

```json
{
    // Tasarım ve arayüz ayarları
    "workbench.iconTheme": "material-icon-theme",
    "workbench.colorTheme": "Deepdark Material Theme | Full Black Version",
    "window.menuBarVisibility": "toggle",
    "window.titleBarStyle": "custom",
    // Terminal ayarları
    "terminal.integrated.cursorStyle": "line",
    // Gizlilik ayarları
    "telemetry.enableTelemetry": false,
    "telemetry.enableCrashReporter": false,
    // Editör ayarları
    "editor.formatOnSave": true,
    "editor.minimap.enabled": false,
    "editor.acceptSuggestionOnEnter": "off", // Enter ile tavsiye seçimini kapatır, Tab ile seçilir
    "files.insertFinalNewline": true, // Dosyaların sonuna boş satır koyar
    // Font Ayarları https://github.com/tonsky/FiraCode/releases/download/1.206/FiraCode_1.206.zip
    "editor.fontFamily": "Fira Code Retina, 'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'", // Linux fontu: Droid Sans Mono
    "editor.fontLigatures": true,
    "editor.fontSize": 13.1,
    // Terminal ayarlarım
    "terminal.integrated.fontSize": 13,
    "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",
    // Satır uzunluğu ayarı
    "editor.wordWrap": "bounded",
    "editor.wordWrapColumn": 200,
    // Dosya işlemleri ayarları
    "explorer.confirmDragAndDrop": false,
    "explorer.confirmDelete": false,
    // Git ayarları
    "git.confirmSync": false,
    "git.autofetch": false,
    // Markdown ayarları
    "markdownlint.config": {
        "MD033": false, // <kbd>
        "MD010": false // No-hard tabs
    },
    // Pano'dan resim kopyalam ayarı
    "pasteImage.path": "${projectRoot}/res",
    // Markdown PDF ayarları
    "markdown-pdf.outputDirectory": "Dökümanlar",
    "markdown-pdf.styles": [
        "http://tiny.cc/yek86y"
    ],
    "markdown-pdf.headerTemplate": "<div style=\"width: 100%; font-size: 7px; margin: 0 auto; font: Segoe UI Light; text-align: center;\"><div style=\"float: left; width: 33.33%;\"><a style='text-decoration: none; font: Risque; color: red;' href='https://gogetfunding.com/yemreak/'>Destek ❤</a></div><div style=\"float: left; width: 33.33%;\"><a style='text-decoration: none; color: navy;' href='https://www.yemreak.com'>Yunus Emre Ak ©</a></div><div style=\"float: left; font-size: 7px; width: 33.33%; color: gainsboro;\"><span class='date'></span></div></div>",
    "markdown-pdf.footerTemplate": "<div style=\"width: 100%; font-size: 7px; margin: 0 auto; font: Segoe UI Light\"> <div style=\"float: left; width: 20%; text-align: center\"><a style=\"text-decoration: none; display: inline-block; color: dodgerblue;\" href=\"https://yemreak.com\">Website</a></div><div style=\"float: left; width: 20%; text-align: center\"><a style=\"text-decoration: none; display: inline-block; color: dodgerblue;\" href=\"https://github.com/yedhrab \">Github</a></div><div style=\"float: left; width: 20%; text-align: center\"><span class=\"pageNumber \">3 </span> / <span class=\"totalPages \"> 5</span></div><div style=\"float: left; width: 20%; text-align: center\"><a style=\"text-decoration: none; display: inline-block; color: dodgerblue;\" href=\"https://www.linkedin.com/in/yemreak/\">LinkedIn</a></div><div style=\"float: left; width: 20%; text-align: center\"><a style=\"text-decoration: none; display: inline-block; color: dodgerblue;\" href=\"mailto::yedhrab@gmail.com?subject=YPDF%20%7C%20Github\">İletişim</a></div></div>"
}

```

### Editör Eklentilerim

- [WakaTime]
- [Deepdark Material Theme]
- [Material Icon Theme]
- [Markdown All in One]
- [Markdown PDF]
- [markdownlint]
- [Better Comments]
- [Todo Tree]
- [Paste Image]

#### Python için Eklentiler

- [kite](https://marketplace.visualstudio.com/items?itemName=kiteco.kite)
- [autoDocstring]
- [Python]
- [AREPL For Python]
- [Visual Studio IntelliCode - Preview]

## Eski Ayarlarım

### Java Ayarları

```json
{
    "java.home": "C:\\Program Files\\Java\\jdk1.8.0_202"
}
```

### Code Runner Ayarları

Path değiştirme örneği detayına [buraya](https://stackoverflow.com/questions/50689210/how-to-setup-code-runner-in-visual-studio-code-for-python) tıklayarak ulaşabilirsin.

```json
"code-runner.executorMap": {
    "python": "$pythonPath -u $fullFileName",
},
```

#### Code Runner Kısayollar

- `ALT` + `SHIFT` + `F` Yazıları uzantıya göre formatlama
- `CTRL` + `"` Gömülü terminali gösterme / gizleme

## Debug Ayarları

Debug ayarlarına erişmek için:

- `CTRL` + `SHIFT` + `D` ile debug sekmesini açın
  - İsterseniz soldaki **activity bar** üzerinden erişebilirsiniz
- Sağ üstteki `ayarlar ikonuna` tıklayın
- `Launch.json` dosyası açılacaktır

### Nodejs için Debug Ayarı

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "program": "${workspaceFolder}\\index.js",
      "outFiles": [ "${workspaceRoot}/dist/**/**/*.js" ]
    },
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Current File",
      "program": "${file}",
      "outFiles": [ "${workspaceRoot}/dist/**/**/*.js" ]
    }
  ]
}
```

## VsCode Değişkenleri

Değişkenler için [buraya](https://code.visualstudio.com/docs/editor/variables-reference) bakabilirisin.

## Yapılacaklar

- [x] Her dilin eklentileri kendilerine özgü notların içine taşınacaktır
- [x] Sadece genel VsCode eklentileri burada yer alacaktır

## Harici Linkler

- [Vs Code Can Do That](https://vscodecandothat.com/)
- [My Top 10 VSCode Extension Recommendation](https://medium.com/backticks-tildes/my-top-10-vscode-extension-recommendation-ac2c2f62ffe5)
- [Best Visual Studio Code Extension](https://blog.elmah.io/best-visual-studio-code-extensions/)
- [10 Essential VS Code Extensions for JavaScript Developers in 2019](https://hackernoon.com/10-essential-vs-code-extensions-for-javascript-developers-in-2019-e8320e3f421e)
- [Debugging ES6 in Visual Studio Code](https://medium.com/@drcallaway/debugging-es6-in-visual-studio-code-4444db797954)
- [Vscode faydalı eklentiler 1]

[Intellicode]: https://code.visualstudio.com/docs/editor/intellisense
[Vscode extension yazma]: https://scotch.io/tutorials/create-your-first-visual-studio-code-extension
[Vscode faydalı eklentiler 1]: https://itnext.io/12-vs-code-extensions-you-should-consider-using-4747e6281ee

[autoDocstring]: https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring
[Better Comments]: https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments
[Deepdark Material Theme]: https://marketplace.visualstudio.com/items?itemName=Nimda.deepdark-material
[Markdown All in One]: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one
[Markdown PDF]: https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf
[markdownlint]: https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint
[Material Icon Theme]: https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme
[Python]: https://marketplace.visualstudio.com/items?itemName=ms-python.python
[Todo Tree]: https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree
[Visual Studio IntelliCode - Preview]: https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode
[AREPL For Python]: https://marketplace.visualstudio.com/items?itemName=almenon.arepl
[WakaTime]: https://marketplace.visualstudio.com/items?itemName=WakaTime.vscode-wakatime
[Best Vscode Extension Javascript and Shell]: https://www.elsewebdevelopment.com/vs-code-the-best-extensions-for-general-use-javascript-and-shell/
[Paste Image]: https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image

[Vscode Doc]: https://code.visualstudio.com/docs
[Vscode Intro Videos]: https://code.visualstudio.com/docs/getstarted/introvideos

[Quokka.js]: https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode
[Prettier - Code formatter]: https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
[JavaScript (ES6) code snippets]: https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets
[Babel Javascript]: https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel
[npm Intellisese]: https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense
[jshint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.jshint
[Eslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
[Import Cost]: https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost
