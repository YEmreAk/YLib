# 🌟 Linux için Faydalı Uygulamalar

## 📋 Faydalı Uygulamaların Hepsi

| Uygulama               | Açıklama                                             |
| ---------------------- | ---------------------------------------------------- |
| gnome-tweaks 🌟        | Gnome özelleştirme ayarları                          |
| unrar 🌟               | `.rar` uzantılı sıkıştırılmış dosyaları çıkarma      |
| flameshot 🌟           | Screenshot alma uygulaması lighthot gibi             |
| Emoji Selector 👌      | Gnome eklentisi olarak indirilebilen emoji klavyesi  |
| Clipboard Indicator 📄 | Pano (kopyalama geçmişi) kontrolü                    |
| Chrome 🌟              | Google Chrome tarayıcı                               |
| mailspring 🌟          | Mail yönetim uygulaması                              |
| kolourpaint 🌟         | Paint alternatifi resim düzenleyici                  |
| VsCode 🌟              | Çok fonksiyonel microsoft yapımı editör              |
| Rambox                 | Mesajlaşma ve eposta yönetim uygulaması              |
| stacer 🌟              | System Optimizer & Monitor                           |
| gpick 🌟               | Renk seçme uygulaması (<kbd>SPACE</kbd> ile seçilir) |
| simplescreenrecorder   | Sade ekran kaydedicisi                               |
| zenkit                 | Proje yönetim uygulaması                             |
| wine                   | Windows uygulamalarını çalıştırma                    |
| nomachine              | Uzaktan PC bağlantısı                                |
| vlc                    | En çok sevilen video oynatıcısı                      |
| Onlyoffice             | Office alternatifi sade ve şık arayüzü olan uygulama |
| dictd                  | Terminal üzerinden çeviri                            |
| retropie               | Atari oyunlarını içerisinde barındıran platform      |
| autocity               | Ses ile ilgili işlemleri barındıran uygulama         |
| OBS                    | Gelişmiş video kaydı hizmeti                         |
| kdenlive               | Windows media player alternatifi                     |
| Open Shot              | Video düzenleme                                      |
| uget                   | Download manager (idm alternatifi)                   |

## Temel Araçların Kurulumu (Flameshot, Font, Gnome Tweaaks, Unrar)

```sh
sudo apt install -y unrar, fonts-noto-color-emoji gnome-tweaks flameshot
```

### Flameshot Hakkında Notlar

Kısayolları için [buraya](https://github.com/lupoDharkael/flameshot#keyboard-shortcuts) bakabilirsin.

| Komut                                       | Açıklama                                |
| ------------------------------------------- | --------------------------------------- |
| `flameshot full -p ~/Pictures/Screenshots/` | Tüm ekranın görüntüsünü path'e kaydetme |
| `flameshot gui`                             | Ekran görüntüsü alma arayüzünü açar     |
| `flameshot config`                          | Yapılandırma ayarları                   |

> Yapılandırma ayarlarından `General` sekmesi adı altında; `Show help message`'ın kapatılması, `Launch at startup`'ın açılması önerilir.

## Sistem Bakım Aracı Kurulumu (Stacer)

```sh
wget -O stacer.deb https://github.com/oguzhaninan/Stacer/releases/download/v1.0.9/stacer_1.0.9_amd64.deb
sudo dpkg -i stacer.deb
rm stacer.deb
```

### Paket Yöneticisi Üzerinden Stacer Kurulumu

```sh
sudo add-apt-repository ppa:oguzhaninan/stacer -y
sudo apt-get update
sudo apt-get install stacer -y
```

## Tarayıcı Kurulumu (Chrome)

```sh
wget -O chrome.deb https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i chrome.deb
rm chrome.deb
```

### Chrome Gnome Eklentisi

Gnome özelleştirme eklentilerinin chrome üzeriinden yönetimini sağlar.

```sh
sudo apt install -y chrome-gnome-shell
google-chrome https://extensions.gnome.org/extension/1160/dash-to-panel/ https://extensions.gnome.org/extension/750/openweather/ https://extensions.gnome.org/extension/1162/emoji-selector/
```

## Gnome Eklentileri

Gnome eklentileri ile ubuntu distronuzu özelleştirebilirsiniz.

- `sudo apt install chrome-gnome-shell` ile chrome için gnome çekirdeğini kurun
- [Chrome](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep), [Firefox](https://addons.mozilla.org/en-US/firefox/addon/gnome-shell-integration/) veya [Opera](https://addons.opera.com/en/extensions/details/gnome-shell-integration/) için gnome eklentisini kurun

> En iyi 19 gnome eklentisi için [buraya][best gnome extension] bakabilirsin.

## Ubuntu Üstteki Çubuğu Gizleme

Gnome eklentisini kurduktan sonra [buradan](https://extensions.gnome.org/extension/545/hide-top-bar/) eklentiyi `ON/OFF` ile açıp kapatabilirsiniz.

## Dash to Dock ile MacOS Durum Çubuğu Görünümü

Tam ekranı kaplayan uzun görüntü yerine, içerdiği uygulama kadar yer kaplayan bir görüntü sağlar, [buradan](https://extensions.gnome.org/extension/307/dash-to-dock/) indirebilirsiniz.

- `Ubuntu Software` uygulamasını açın
- `Dash to Dock` yazıp aratın ev indirin
- `Extension Settings` kısmından özelleştirebilirsiniz

## Dast to Panel

Windows 10 görev çubuğu izlenimi verir, [buraya](https://extensions.gnome.org/extension/1160/dash-to-panel/) tıklayarak erişebilirsiniz

## Emoji Selector (Emoji Klavyesi)

Emoji klavyesi ile emojiyi panoya kopyalar, [buradan](https://extensions.gnome.org/extension/1162/emoji-selector/) indirebilirsiniz.

- <kbd>✲ Ctrl</kbd> + <kbd>V</kbd> ile yapıştırarak kullanabilirsiniz
- <kbd>SUPER</kbd> + <kbd>E</kbd> Emoji klavyesini açar

## Clipboard Indicator

Pano'yu yönetme imkanı sağlar, [buradan](https://extensions.gnome.org/extension/779/clipboard-indicator/) indirebilirsin.

## EasyScreenCast

Ekranı paylaşma eklentisidir. Kurulum öncesi alttaki komutla gereksinimleri kurman gerekmektedir. Eklentiyi kurmak için [buraya](https://extensions.gnome.org/extension/690/easyscreencast/) tıklayabilirsin.

```sh
sudo apt-get install gir1.2-clutter-1.0 gir1.2-clutter-gst-3.0 gir1.2-gtkclutter-1.0
```

## GS Connect

Mobil cihaz ile bilgisayarı entegre etmeyi sağlar, [buradan][gs connect - extension] erişebilirsin.

[flameshot]: https://github.com/lupoDharkael/flameshot
[simplescreenrecorder]: https://www.maartenbaert.be/simplescreenrecorder/
[gs connect - extension]: https://extensions.gnome.org/extension/1319/gsconnect/
[best gnome extension]: https://www.ubuntupit.com/19-best-gnome-shell-extensions-ubuntu-gnome-desktop/
[best gnome applications]: https://www.maketecheasier.com/best-gnome-applications/
[best desktop environment]: https://www.ubuntupit.com/best-linux-desktop-environment-reviewed-and-compared/
