# Python Fonksiyonlar <!-- omit in toc -->

## İçerikler <!-- omit in toc -->

- [Dahili Fonksiyon Kullanımları](#dahili-fonksiyon-kullan%C4%B1mlar%C4%B1)
  - [Genel Fonksiyonlar](#genel-fonksiyonlar)
  - [String İşlemleri](#string-i%CC%87%C5%9Flemleri)
- [Harici Fonksiyon Kullanımları](#harici-fonksiyon-kullan%C4%B1mlar%C4%B1)
  - [Harici String İşlemleri](#harici-string-i%CC%87%C5%9Flemleri)
  - [Dizin ve Yol İşlemleri](#dizin-ve-yol-i%CC%87%C5%9Flemleri)
- [Fonksiyon Oluşturma](#fonksiyon-olu%C5%9Fturma)
  - [Fonksiyon İskeleti](#fonksiyon-i%CC%87skeleti)
  - [Fonksiyon Örneği](#fonksiyon-%C3%B6rne%C4%9Fi)
  - [Fonksyion Dökümantasyonu](#fonksyion-d%C3%B6k%C3%BCmantasyonu)
  - [Fonksyion Varsayılan Parametreler](#fonksyion-varsay%C4%B1lan-parametreler)
  - [Fonksiyonlarda Keyfi Parametreler](#fonksiyonlarda-keyfi-parametreler)
- [Özyineleyen Fonksiyonlar](#%C3%B6zyineleyen-fonksiyonlar)
  - [Özyineleyen Fonksiyonların Avantajları](#%C3%B6zyineleyen-fonksiyonlar%C4%B1n-avantajlar%C4%B1)
  - [Özyineleyen Fonksiyonların Zararları](#%C3%B6zyineleyen-fonksiyonlar%C4%B1n-zararlar%C4%B1)
- [Lambda Fonksiyonlar](#lambda-fonksiyonlar)
  - [Filter ile Lambda Kullanımı](#filter-ile-lambda-kullan%C4%B1m%C4%B1)
  - [Map ile Lambda Kullanımı](#map-ile-lambda-kullan%C4%B1m%C4%B1)
- [İç İçe Fonksiyonlar](#i%CC%87%C3%A7-i%CC%87%C3%A7e-fonksiyonlar)
- [Global, Local ve Nonlocal Kavramları](#global-local-ve-nonlocal-kavramlar%C4%B1)
  - [Global, Local ve Nonlocal Kavramlarına Örnek (Scopes and Namespaces)](#global-local-ve-nonlocal-kavramlar%C4%B1na-%C3%B6rnek-scopes-and-namespaces)
  - [Global Kullanımına Örnek](#global-kullan%C4%B1m%C4%B1na-%C3%B6rnek)
  - [Global Kullanımına Karmaşık Örnek](#global-kullan%C4%B1m%C4%B1na-karma%C5%9F%C4%B1k-%C3%B6rnek)

## Dahili Fonksiyon Kullanımları

### Genel Fonksiyonlar

| Fonksiyon         | Açıklama                  | Örnek                     | Çıktı              |
| ----------------- | ------------------------- | ------------------------- | ------------------ |
| `print(<string>)` | Ekrana yazma              | `print("X: {1}, Y: {2}")` | `X: {1}, Y: {2}`   |
| `eval(<string>)`  | Verilen stringi hesaplama | `eval("x + 5")`           | `6`                |
| `type(<obje>)`    | Objenin türünü bulma      | `type(x)`                 | `<class 'number'>` |

### String İşlemleri

Çok önemli ve ileride kullanılacak bir konudur. 🌟

<!-- TODO linkleri ekle -->

| Link    | Metot                   | Açıklama                | Örnek                                  | Çıktı                  |
| ------- | ----------------------- | ----------------------- | -------------------------------------- | ---------------------- |
|         | `len`                   | Uzunluk                 | `len("yemreak")`                       | 7                      |
|         | `format`                | Formatlama              | `"X: {}, Y: {}".format(1, 2)`          | `'X: 1, Y: 2'`         |
|         | `%`                     | Operatör ile formatlama | `'new(%s %d)' % ('help', 5)`           | `'new(help 5)'`        |
|         | `f`                     | Format string ön eki    | `f'X: {a}'`                            | `'X: 2'`               |
|         | `r`                     | Raw String ön eki       | `r"C:\Users"`                          | `C:\\Users`            |
|         | `"""`                   | Çok satırlı string      |
|         | `split`                 | Parçalama               | `"ye mre ak".split(" ")`               | `['ye', 'mre', 'ak']`  |
| [Slice] | `[<başlangıç>:<bitiş>]` | Kesme                   | `"yemreak".[2:5]`, `"yemreak".[-3:-1]` | `"mre"`, `"ea"`        |
|         | `join`                  | Birleştirme             | `','.join(['do', 're', 'mi'])`         | `'do,re,mi'`           |
|         | `split & join`          | Yeniden formatlama      | `arr.split("\t").join("|")`            | `'İsim|Soyisim|Numara` |
|         | `replace`               | Metin değiştirme        | `"yemreak".replace("ak", "")`          | `'yemre'`              |
|         | `strip`                 | Metin düzeltme          | `' abc '.strip()`                      | `'abc'`                |
|         | `ltrip`                 | Metnin solunu düzeltme  | `' abc '.ltrip()`                      | `'abc '`               |
|         | `rtrip`                 | Metnin sağını düzeltme  | `' abc '.rtrip()`                      | `' abc'`               |
|         | `sort`                  | Metni sıralama          | `['n', 'a', 'i']`                      | `['a', 'i', 'n']`      |

> Daha fazla bilgi için [buraya](https://www.programiz.com/python-programming/methods/string) ve [buraya](https://stackoverflow.com/questions/10660435/pythonic-way-to-create-a-long-multi-line-string) bakabilirsin.

## Harici Fonksiyon Kullanımları

- Fonksiyonları kullanmadan önce `import <paket>` ile paketi dahil etmeniz lazım
- Fonksiyonların kullanımı `<paket>.<fonksiyon>` şeklindedir

### Harici String İşlemleri

| Paket | Fonksiyon                                | Açıklama                              |
| ----- | ---------------------------------------- | ------------------------------------- |
| `re`  | `split(<ayırıcı_karakterler>, <string>)` | Birden fazla karaktere göre parçalama |

- `<ayırıcı_karakterler>` Metni hangi karakterlere göre böleceğimizi ifade eder
  - Birden fazla olacaksa `|` ile birbirinden ayrılır
  - Ayırma sırasında `boşluk karakteri`nin kullanılması sorun oluşturur
  - *Örn:* `'\n|\t|\*'`
- `<string>` Ayrıştırılacak metin
  - *Örn:* `'yemreak.com'`

### Dizin ve Yol İşlemleri

| Paket     | Fonksiyon                      | Açıklama                                                                         |
| --------- | ------------------------------ | -------------------------------------------------------------------------------- |
| `os`      | `listdir(<yol>)`               | Yolu verilen dizinin içindekileri döndürür                                       |
| `os`      | `rename(<eski_ad>, <yeni_ad>)` | Dosya veya dizin adlandırma                                                      |
| `os.path` | `isfile(<yol>)`                | Dosya mı kontrolü                                                                |
| `os.path` | `join(<yol1>, <dosya_adı>)`    | Dizinleri birleştirme                                                            |
| `os.path` | `basename(<yol>)`              | Yolu verilen dosyanın salt adını ve uzantısını bulma                             |
| `os.path` | `splittext(<dosya_adı>)`       | Dosyanın başlığını ve uzantısını döndürür (title, ext)                           |
| `glob`    | `glob(<yol_şablonu>)`          | Verilen sorguya veya yola uygun dosya ve dizinleri döndürür                      |
| `glob`    | `iglob(<yol_şablonu>)`         | Verilen sorguya veya yola uygun dosya ve dizinleri generator yapısı ile döndürür |

- `<yol>` Path, dosya yolu
  - *Örn: C:\Users\Username\help.txt*
- `<dosya_adı>` Dosyanın uzantısıyla birlikteki adı
  - *Örn: help.txt*
- `<yol_şablonu>` Özel dizin sorguları
  - *Örn: `*.txt`, `../help`*

## Fonksiyon Oluşturma

Kodların derlenme yapısı yukarıdan aşağı olduğu için fonksiyonlar **yukarıda (önceden) tanımlanmadan** kullanılamaz.

### Fonksiyon İskeleti

```py
def function_name(parameters):
  """docstring"""
  statement(s)
```

### Fonksiyon Örneği

```py
def greet(name):
  """This function greets to
  the person passed in as
  parameter"""
  print("Hello, " + name + ". Good morning!")
```

### Fonksyion Dökümantasyonu

```cmd
>>> print(greet.__doc__)
This function greets to
  the person passed into the
  name paramete
```

### Fonksyion Varsayılan Parametreler

```py
def greet(name, msg = "Good morning!"):
   """
   This function greets to
   the person with the
   provided message.

   If message is not provided,
   it defaults to "Good
   morning!"
   """

   print("Hello",name + ', ' + msg)

greet("Kate") # Varsayılan parametreyi kullanma
greet("Bruce","How do you do?") # Sıralı parametre verme
greet("Bruce", msg="Naber") # İşaretleyerek paremetre verme
```

### Fonksiyonlarda Keyfi Parametreler

```py
def greet(*names):
   """This function greets all
   the person in the names tuple."""

   # names is a tuple with arguments
   for name in names:
       print("Hello",name)

greet("Monica","Luke","Steve","John")
```

> `*` ön eki ile ile kaç tane isim gelirse o kadar kullanıyoruz.

## Özyineleyen Fonksiyonlar

```py
def calc_factorial(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1:
        return 1
    else:
        return (x * calc_factorial(x-1))

num = 4
print("The factorial of", num, "is", calc_factorial(num))
```

```out
calc_factorial(4)              # 1st call with 4
4 * calc_factorial(3)          # 2nd call with 3
4 * 3 * calc_factorial(2)      # 3rd call with 2
4 * 3 * 2 * calc_factorial(1)  # 4th call with 1
4 * 3 * 2 * 1                  # return from 4th call as number=1
4 * 3 * 2                      # return from 3rd call
4 * 6                          # return from 2nd call
24                             # return from 1st call
```

### Özyineleyen Fonksiyonların Avantajları

- Özyineleyen fonksiyonlar kodun daha temiz ve zarif gözükmesini sağlar
- Karmaşık bir görev alt görevlere ayrılarak rahat çözülebilir
- İç içe döngülere göre daha iyidir

### Özyineleyen Fonksiyonların Zararları

- Bazı durumlarda anlaşılabilmesi zordur
- Uzun tekrarlarda çok fazla vakit ve zaman harcarlar
- Hata ayıklama oldukça zordur

## Lambda Fonksiyonlar

```py
double = lambda x: x * 2 # lambda fonksiyon


def double(x): # Fonksiyon
   return x * 2
```

### Filter ile Lambda Kullanımı

Sadece koşulu sağlayan değerleri döndürür.

```py
listem = [1, 5, 4, 6, 8, 11, 3, 12]

cift_listem = list(filter(lambda x: (x%2 == 0) , listem))
print(cift_listem) # [4, 6, 8, 12]
```

### Map ile Lambda Kullanımı

Her eleman için işlem yapar.

```py
listem = [1, 5, 4, 6, 8, 11, 3, 12]

katlanmis_listem = list(map(lambda x: x * 2 , listem))
print(katlanmis_listem) # Output: [2, 10, 8, 12, 16, 22, 6, 24]
```

## İç İçe Fonksiyonlar

Python ile fonksiyon içinde fonksiyon tanımalamak mümkündür.

> Hatırlatma: Kodların derlenme yapısı yukarıdan aşağı olduğu için fonksiyonlar **yukarıda (önceden) tanımlanmadan** kullanılamaz.

```py
def func1():

    # func2() bu alanda kullanılamaz

    def func2():
        print("Selam2")

    print("Selam1")
    func2() # Bu alanda ekrana 'Selam2' basar

```

## Global, Local ve Nonlocal Kavramları

| Kavram     | Açıklama                                                                                    | Erişim         |
| ---------- | ------------------------------------------------------------------------------------------- | -------------- |
| `global`   | Tüm modülde geçerli değişkenler                                                             | Okuma          |
| `local`    | Fonksiyonların içerisindeki yerel değişkenler                                               | Okuma ve Yazma |
| `nonlocal` | Modül ile fonksiyon arasında kalan, genellikle iç içe fonksiyonlarda kullanılan değişkenler | Okuma          |

### Global, Local ve Nonlocal Kavramlarına Örnek (Scopes and Namespaces)

```py
x = 5 # Global değişken

def func1():

    x = 4 # Nonlocal değişken
  
    def func11():
      x = 1 # Local değişken

    print(x)
    # Python otomatik olarak `global x` deyimini kullanır
    #  x'i global değişkenlerde arar ve ekrana '5' basar

    # print(x)
    # x = 3
    # Yukarıdaki işlemde x'e atama yapıldığından `nonlocal x` olarak tanımlanır.
    # Bu sebeple `print(x)` komutu çalışmaz hata verir.
    # x tanımlanmadan kullanıldı (`global x` olarak yazılması lazım)
    global x
    print(x)
    x = 3
    print(x)

```

### Global Kullanımına Örnek

```py
x = 5
  
  def xDegistir():
    x = 3 # Yerel x değişkenine 3 değeri atanır, evrensel x değişmez.

  
  def globalXDegistir():
    global x
    x = 4 # Evrensel x değişir
```

### Global Kullanımına Karmaşık Örnek

```py
def scope_test():
    def do_local():
        spam = "local spam"

    def do_nonlocal():
        nonlocal spam
        spam = "nonlocal spam"

    def do_global():
        global spam
        spam = "global spam"

    spam = "test spam"
    do_local()
    print("After local assignment:", spam)
    do_nonlocal()
    print("After nonlocal assignment:", spam)
    do_global()
    print("After global assignment:", spam)

scope_test()
print("In global scope:", spam)
```

```txt
After local assignment: test spam
After nonlocal assignment: nonlocal spam
After global assignment: nonlocal spam
In global scope: global spa
```

[Slice]: https://www.webucator.com/how-to/how-slice-strings-python.cfm