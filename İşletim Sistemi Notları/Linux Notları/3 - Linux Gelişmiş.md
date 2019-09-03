# Linux Gelişmiş <!-- omit in toc -->

## Dosya içeriğinden Türünü Bulma

| Satr Metni              | Açıklama                      |
| ----------------------- | ----------------------------- |
| `!`                     | Çalıştırılabilir (executable) |
| `#!/bin/bash`           | Bash script                   |
| `#usr/bin/env xdg-open` | Desktop uygulamaları          |
| `#!/usr/bin/python`     | Python dosyaları              |

## Başka İşletim Sistemlerinin Dosyalarına Erişme

Erişim yapmak için `mount` işlemi ile sisteme bağlamalısınız.

- Disk yolunu öğrenmek için `gparted` kullanabilisiniz
- `sudo apt install gparted`
- `sudo gparted`
- Partition kısmının altındaki disk yoludur

```sh
sudo mount <disk_yolu> <bağlacağı_yer>
# Örn: sudo mount /dev/sda4 /mnt/
```

## Çalışma Alanlarını Bağımsızlaştırma (Isolate Workspace)

Bu işlem için `isolate workspaces` ayarını dash, dock ya da panel ayarlarında aktif hale getirmemiz lazım.

> Panel için `dock` yazan kısma `panel` yazıp komutu kullanın.

```sh
gsettings set org.gnome.shell.extensions.dash-to-dock isolate-workspaces true
```

## Dosya İzinleri

Dosya izinleri `chmod <parametre> <izin_no> <dosya_veya_dizin>` komutuyla yapılır.

| Parametmerler | Açılımı   | Anlamı                               |
| ------------- | --------- | ------------------------------------ |
| `-R`          | Recursive | Dizin ve alt dizinlerini de ele alır |

### İzin Kodu Hesaplama

İzin kodu, aşağıdaki formattaki kod yapısıdır.

- Sırasıyla `owner`, `group`, `others` basamaklarına alttaki yetkilerin toplamının atanmasıdır
  - `4` Read (okuma)
  - `2` Write (yazma)
  - `1` Execute (çalıştırma)
  - `0` No permission (izin yok)

```sh
mkdir temp
sudo chmod 777 temp # Her gruba tüm yekileri verme
sudo chmod 751 temp # Oner: Hepsi Group: Read & Write Others: Execute
sudo chmod 000 temo # Hiç yetki yok
sudo chmod -R 777 temp # Dizine ve altdizinlere herkes için tam yetki verme
```

> `Root` her şeye erişebilir.

### Dizine ve Alt Dizinlerine Okuma ve Yazma İzni Verme

Alttaki komutla dizine ve alt dizinlerine herkes için okuma ve yazma erişimi verebilirsin.

```sh
sudo chmod -R 757 /opt/lampp/htdocs/wordpress/
```

## Desktop kısayolu oluşturma

Text editörü açıp

```sh
gedit dosya/yolu.desktop
```

Alttaki alanda gerekli yerleri doldurun.

```ini
#!/usr/bin/env xdg-open

[Desktop Entry]
Version=1.0
Type=Application
Terminal=false
Exec=command to run here
Name=visible name here
Comment=comment here
Icon=icon path here
```

Son olarak dosyanın bulunduğu dizinde terminali açıp, dosyayı güvenilir olarak işaretleyin (?)

```bash
chmod +x dosyadi.desktop
```

> Detaylı bilgi için [buraya][linux desktop entry oluşturma] bakabilirsin.

### Whatsapp Kısayolu

Text editörü açıp;

```sh
sudo -H gedit /usr/share/applications/whatsapp-webapp.desktop
```

açılan yere alttaki verileri kopyalayın;

```ini
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=WhatsApp
GenericName=WhatsApp
Comment=WhatsApp desktop webapp
#Exec=webapp-container --store-session-cookies --webappUrlPatterns=https?://*.whatsapp.com/* --user-agent-string='Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.36' https://web.whatsapp.com %u
Exec=/opt/google/chrome/google-chrome --app=https://web.whatsapp.com/
Terminal=false
Type=Application
StartupNotify=true
MimeType=text/plain;
# Alttaki alana ikon yolunuzu kopyalayın
# Icon=
Categories=Network;Application;
Keywords=WhatsApp;webapp;
X-Ubuntu-Gettext-Domain=WhatsApp
StartupWMClass=web.whatsapp.com
```

#### Whatsapp İkonu Ekleme

İlk olarak [buradaki][whatsapp svg] ikonu indirin.

- İndirdiğiniz dosyanın yolunu kopyalayın
- `gedit /usr/share/applications/whatsapp-webapp.desktop` komutu ile dosyayı tekrar açın
- İçerisinde `Icon=` olan satırın başındaki `#` karkterini silin ve yolu kopyalayın
  - Örn: `Icon=/home/yemreak/Pictures/Ikons/Svg/whatsapp-webapp.svg`

#### Wmctrl ile Kısayol Oluşturma

Alttaki komut ile wapp açıksa gösterme, kapalıysa oluşturmayı sağlayabilirsin.

```sh
bash -c "wmctrl -xa web.whatsapp.com || /opt/google/chrome/google-chrome --app=https://web.whatsapp.com/"
```

## Font Yükleme

```sh
mkdir -p ~/.font # Yerel font dizinini oluşturma
mv <font.ttf> ~/.font # Font dosyasını gerekli yere aktarma
fc-cache -fv # Fontları yeniden derleme
```

## USB Bağlanma Sorunlarını Düzeltme

```sh
sudo apt install ntfs-3g
ntfsfix <adres>
```

- `<adres>` Takılan USB'nin bağlanmaya çalıştığı adres
  - Örn: `/dev/sbd1`

> Detaylar için [buraya][usb ntfs onarımı] bakabilirsin.

## Gnome Geliştmiş Ayarlar

| Ayar              | Yol                    |
| ----------------- | ---------------------- |
| Çekirdek Ayarları | `org.gnome.shell`      |
| Pencere Ayarları  | `org.gnome.desktop.wm` |

### Gnome Alt Gelişmiş Ayarlar

| Ayar               | Yol           |
| ------------------ | ------------- |
| Klavye Kısayolları | `keybindings` |
| Eklenti aayarları  | `extension`   |

## Pencere İşlemleri

### Ubuntu 19.04 için Pencere Kısayollarını Kaldırma (Super + Num)

```sh
gsettings set org.gnome.shell.extensions.dash-to-dock hot-keys false
gsettings set org.gnome.shell.keybindings switch-to-application-1 []
gsettings set org.gnome.shell.keybindings switch-to-application-2 []
gsettings set org.gnome.shell.keybindings switch-to-application-3 []
gsettings set org.gnome.shell.keybindings switch-to-application-4 []
gsettings set org.gnome.shell.keybindings switch-to-application-5 []
gsettings set org.gnome.shell.keybindings switch-to-application-6 []
gsettings set org.gnome.shell.keybindings switch-to-application-7 []
gsettings set org.gnome.shell.keybindings switch-to-application-8 []
gsettings set org.gnome.shell.keybindings switch-to-application-9 []
```

### Window Manager Controls

Uygulamaların durumlarını kontrol eden `wmctrl` adlı komuttur.

- `wmctrl -xa <uygulama_komutu>` uygulama açıksa ekrana getirir.
- `wmctrl -v <uygulama>` Uygulama varsa 1 döndürür
- `wmctrl -xc <uygulama_komutu>` uygulamayı kibarca kapatma
- `wmctrl -lxG` açık olan uygulamalar hakkında bilgi basar.
- `wmctrl -xr $WM_CLASS -b toggle,shaded` uygulamayı gizleme (shaded özelliğini toggle'lar)
- `wmctrl -xr $WM_CLASS -b add,maximize_vert,maximize_hor` uygulmaya tam ekran özelliği verir

### Window ID Alma

- `xwininfo | grep "Window id:"` Pencere yöneticisi üzerinden Fare seçimiyle Windows ID olarak alma
- `xprop | grep "window id #"` Process yöneticisi üzerinden Fare seçimiyle Windows ID olarak alma
- `xprop -id $WID | grep _NET_WM_STATE` Pencere durumunu gösterme

### Xdotool ile Pencere Yönetimi

- `$NAME` Pencere başlığı
- `xdotool search --name $NAME` VM_NAME'e (isme) göre Windows ID alma
- `xdotool search --class $WM_CLASS` Temel VM_CLASS'a (sınıfa) göre Windows ID alma (en sondaki WM_CLASS öğesi)
- `xdotool search --classname $WM_CLASS` VM_CLASS'a (sınıfa) göre Windows ID alma
- `xdotool search --desktop $(xdotool get_desktop) --class $WM_CLASS` Aktif masaüstünde temel VM_CLASS'a (sınıfa) göre Windows ID alma (en sondaki WM_CLASS öğesi)
- `xdotool search --desktop $(xdotool get_desktop) --classname $WM_CLASS` Aktif masaüstünde VM_CLASS'a (sınıfa) göre Windows ID alma
- `xdotool getwindowfocus` Seçili olan ekranın WID'ini alır
- `xdotool getwindowfocus getwindowname` Seçili olan ekranın ismini alır
- `WID=$(xdotool search --name $NAME)` Windows ID'yi değişkende tutma
- `xdotool windowminimize $WID` Pencereyi gizleme
- `xdotool windowactivate $WID` Pencreyi gösterme ve odaklanma
- `xdotool get_desktop` Seçili olan masaüstünü gösterir (0, 1, 2...)

> Burada WID xdotool'a özgü id değeridir.

## Uygulamaların Terminal Komutlarını öğrenme

Alttaki komutu yazdıktan sonra pencerenin üstüne tıklamanız yeterlidir.

```sh
xprop | grep WM_CLASS
```

## Ubuntu Soluk Renk Sorunu

Tek seferlik:

```sh
xrandr --output HDMI-1 --set "Broadcast RGB" "Full"
```

Kalıcı ayar:

```sh
echo 'xrandr --output HDMI-1 --set "Broadcast RGB" "Full"' >> ~/.xprofile
```

## Herhangi bir Uygulama için Kısayol Oluşturma

### Uygulama için `WM_CLASS` metnini tanımlama

To do this, you need to make desktop app.

- Terminale `sudo -H gedit /usr/share/applications/<appname>.desktop` komutunu yazın
- Açılan dosyada gerekli bilgileri, [buradaki][linux desktop entry oluşturma] bilgiden de yararlanarak doldurun
- Örnek dosya içeriği aşağıdaki gibi olacaktır

```ini
#!/usr/bin/env xdg-open
[Desktop Entry]
Name=WhatsApp
GenericName=WhatsApp
Comment=WhatsApp desktop webapp
Exec=/opt/google/chrome/google-chrome --app=https://web.whatsapp.com/
Terminal=false
Type=Application
StartupNotify=true
MimeType=text/plain;
# Alttaki alana ikon yolunuzu kopyalayın
# Icon=
Categories=Network;Application;
Keywords=WhatsApp;webapp;
X-Ubuntu-Gettext-Domain=WhatsApp
StartupWMClass=web.whatsapp.com
```

### Herhangi bir uygulamanın `WM_CLASS` metnini alma

- Terminal üzerinde `xprop | grep WM_CLASS` komutu ile `WM_CLASS` metnini alabiliriz
- Komutu yazıp <kbd>ENTER</kbd>'a bastıktan sonra kısayolunu oluşturmak istediğimiz uygulamaya tıklıyoruz
- Yandaki gibi bir çıktı gelecektir `WM_CLASS(STRING) = "gnome-terminal-server", "Gnome-terminal`
- `gnome-terminal-server` olan metni <kbd>✲ Ctrl</kbd> + <kbd>⇧ Shift</kbd> + <kbd>C</kbd> ile kopyalıyoruz

### Kısayolu oluşturma

- <kbd>SUPER</kbd> tuşuna basıp arama yerine `shortcut` yazıyoruz
- Açılan pencerenin en altındaki `+` butonuna tıklayarak kısayol ekliyoruz
- **name** alanına herhangi bir isim giriyoruz
- Ardından **command** alanına `bash -c "wmctrl -xa <wm_class> || <wm_class>` yazıyoruz
- Son olarak klavye kısayolunu atıyoruz ve kaydediyoruz

## Grub Menüyü Atlama

- `sudo nano /etc/default/grub` ile grub yapılandırma dosyasını açın
- En alt kısmına `GRUB_HIDDEN_TIMEOUT=0` yazın ve `GRUB_TIMEOUT=0` yapın
- <kbd>✲ Ctrl</kbd> + <kbd>S</kbd> e basarak kaytıt edin, <kbd>✲ Ctrl</kbd> + <kbd>X</kbd> ile çıkış yapın
- `sudo update-grub` ile yine grub ayarlarını aktifleştirin

## Donanım Komutları

- `nproc` İşlemci çekirdek sayısını gösterir.
- `uname -v` Kernel sürümünü gösterir
- `lspci` Donanum bilgilerini gösterir

## Silinen Yerel Dosyaları Kurtarma

Home dizinin yanlışlıkla (ya da bilinçli 🧐) `rm -rf *` komutu uygulanması durumunda bu sorun meydana gelir. İster en alttaki script ile isterseniz talimatlarla sorunu çözebilirsiniz.

- `cd ~` ile `Home` dizinine gelin ve dizinlerinizi oluşturun
- `gedit ~/.config/user-dirs.dirs` ile dizinleri ayarların
- `xdg-user-dirs-update` komutu ile dizinleri güncelleyin

```sh
cd ~
mkdir Downloads Templates Shares Documents Musics Pictures Videos Desktop
echo '# This file is written by xdg-user-dirs-update' > ~/.config/user-dirs.dirs
echo '# If you want to change or add directories, just edit the line you are' >> ~/.config/user-dirs.dirs
echo '# interested in. All local changes will be retained on the next run.' >> ~/.config/user-dirs.dirs
echo '# Format is XDG_xxx_DIR="$HOME/yyy", where yyy is a shell-escaped' >> ~/.config/user-dirs.dirs
echo '# homedir-relative path, or XDG_xxx_DIR="/yyy", where /yyy is an' >> ~/.config/user-dirs.dirs
echo '# absolute path. No other format is supported.' >> ~/.config/user-dirs.dirs
echo '# YEmreAk' >> ~/.config/user-dirs.dirs
echo 'XDG_DOWNLOAD_DIR="$HOME/Downloads"' >> ~/.config/user-dirs.dirs
echo 'XDG_TEMPLATES_DIR="$HOME/Templates"' >> ~/.config/user-dirs.dirs
echo 'XDG_PUBLICSHARE_DIR="$HOME/Shares"' >> ~/.config/user-dirs.dirs
echo 'XDG_DOCUMENTS_DIR="$HOME/Documents"' >> ~/.config/user-dirs.dirs
echo 'XDG_MUSIC_DIR="$HOME/Musics"' >> ~/.config/user-dirs.dirs
echo 'XDG_PICTURES_DIR="$HOME/Pictures"' >> ~/.config/user-dirs.dirs
echo 'XDG_VIDEOS_DIR="$HOME/Videos"' >> ~/.config/user-dirs.dirs
echo 'XDG_DESKTOP_DIR="$HOME/Desktop"' >> ~/.config/user-dirs.dirs
xdg-user-dirs-update
```

## Process İşlemleri

| Komut   | Açıklama                 |
| ------- | ------------------------ |
| `pgrep` | PID (process id) Bulma   |
| `kill`  | PID öldürme, sonlandırma |

### Process Id (PID) Bulma

```sh
pgrep [option] <pattern>
```

## Bashrc Dosyası Yedeği

Dosyaya [buradan][bashrc dosyası] erişebilirsin, ek olarak:

- Sudo ile yeni komutların kullanılmasını sağlar

## Kernel Güncelleme

Kernel güncelleme yazım için [buraya][kernel güncelleme] bakabilirsin.

## Harici Bağlantılar

- [Windows yanına linux kurulduğunda windows saatinin bozulması]
- [Linux desktop entry oluşturma]
- [Uygulamalar için neden sudo -h kullanılmalı]
- [Ubuntu soluk renk]
- [Ubuntu 19.04 yenilikleri]
- [Linux bilgisayarlarını birbirine bağlama](https://www.maketecheasier.com/netcat-transfer-files-between-linux-computers/)

[kernel güncelleme]: https://medium.com/@yyunussemree/linux-kernel-g%C3%BCncelleme-4ce3ce55de36
[windows yanına linux kurulduğunda windows saatinin bozulması]: https://www.howtogeek.com/323390/how-to-fix-windows-and-linux-showing-different-times-when-dual-booting/
[linux desktop entry oluşturma]: https://askubuntu.com/a/282187
[whatsapp svg]: ../../res/whatsapp-webapp.svg
[uygulamalar için neden sudo -h kullanılmalı]: https://askubuntu.com/questions/270006/why-should-users-never-use-normal-sudo-to-start-graphical-applications
[ubuntu soluk renk]: https://askubuntu.com/questions/621964/colors-on-display-are-washed-out#
[ubuntu 19.04 yenilikleri]: https://itsfoss.com/ubuntu-19-04-release-features/
[bashrc dosyası]: ../../res/.bashrc
[usb ntfs onarımı]: https://askubuntu.com/a/47711/898692
