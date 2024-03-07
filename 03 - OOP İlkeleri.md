**OOP PRINCIPLES (OOP İLKELERİ)**
  1. ENCAPSULATION (KAPSUÜLLEME)
  2. INHERITANCE (KALITIM)
  3. POLYMORPHISM (ÇOK BİÇİMLİLİK)
  4. ABSTRACTION (SOYUTLAMA)
> Aslında 4. ABSTRACTION (SOYUTLAMA) kavramı, diğer 3'ünün doğal bir sonucu olarak ortaya çıkar.

**1. ENCAPSULATION (KAPSUÜLLEME)**

OOP için oldukça önemli bir kavramdır. Kapsülleme aslında programcıyı korumak için tasarlanmış bir yöntemdir. Programcının yazdığı kodlara, farklı programcıların veya kullanıcıların doğrudan erişimini kesmek ve geliştirilen yapının korunması amaçlanmaktadır.

Örneğin bir televizyon kumandası düşünelim. Bu kumanda plastik bir koruyucu kap ile kaplıdır. İçerisindeki devre kartını doğrudan kullanamayız ancak, kumandanın üzerinde bulunan butonlar vasıtası ile kumandayı kullanabilir.

Burada devre kartı, kullanıcıların doğrudan erişimine kapalıdır ancak, işlevlerininin kullanımı kullanıcıya açıktır.

Kapsülleme yapısında, GET ve SET metodları kullanılarak private tasarlanmış veri parçalarına erişim sağlanarak, kullanılması hedeflenmektedir. Bir örnek ile açıklayalım.
```
class Kapsulleme{

private int a;

  public int setA(int x){
    a=x;
    return a;
  }
  public void getA(){
    Console.WriteLine(a);
  }

}
```

Yukarıdaki örnekten bir "Kapsulleme" adında sınıf oluşturulmuştur. Bu sınıfın içerisinde yer alan "int a" verisi, private odluğundan bir nesne oluşturulduğunda, "a" değeri sınıf dışında kullanılamaz.
```
Kapsulleme kapsul1 = new Kapsulleme();

// kapsul1.a = 5; // Bu ifade hata verecektir. Çünkü "a" değeri private'dir ve class dışından erişilemez. Ancak;

kapsul1.setA(5);
kapsul1.getA();

```

Yukarıdaki komutlar çalıştırıldığında Ekran Çıktısı: 
``` 
5
```

Olacaktır.

Görüldüğü üzere, "a" değişkeni doğrudan kullanıcı tarafındaan kullanılamamıştır. set ve get metodları ile (Butonlarımız) değer atanmış ve atanan değer çağrılmıştır.

> Kapsülleme denilen kavram, varlığa ait bir takım yapılaraın dışarıya tamamen kapatılması yada kontrolün bir şekilde açılması ilkesidir.

**NOT:** PROPERTY (Özellik)'ler class içindeki fieldları dışarıya kontrollü bir şekilde açmamızı sağlayan yapılardır. 

Property örneği;
```
public class Kisi{

  private string isim;

// Özellik (property)
public string Isım
{
  get { return isim; }
  set { isim = value;}
}
```
Program içerisinde kullanımı (class program içiersinde)

```
Kisi kisiNesnesi = new Kisi();
kisiNesnesi.Isım="Kutay";
// set metodu çalışır

Console.WriteLine(kisiNesnesi.Isım);
// get metodu çalışır ve ekrana Kutay yazar.
}
```

Yukarıdaki örnekte, **"Kisi"** sınıfının **"Isım"** adında bir özelliği var. Bu özellik, **"isim"** adlı özel bir alanı (private field) kullanarak veriyi saklar. **get** metodu, özelliğin derğerini okumak için kullanılırkern; **set** metodu, özelliğe değer atamak istediğinde çalışır. **value** anahtar kelimesi, **set** metodun atanan değeri temsil eder. 

>property içerisinde get-set metedu kullanılır. set içerisinde "value" anahtar kelimesi kullanılır.

**NOT:** Nesneye ait asıl veriyi RAM'de tutacak olan yapılar değişkenlerdir. Ancak bu yapıya metod içinde **DEĞİŞKEN**, class içinde **FIELD** denir.

KISAYOL:
propfull yazarak iki kez TAB tuşuna basarasanız. Field ve Property yapısı otomatik olarak oluşturulur.
```
private int myVar;

public int MyProperty
{
    get { return myVar; }
    set { myVar = value; }
}
```
prop yazarak 2 kez TAB tuşuna basarsak, property otomatik oluşturulur.
```
public int MyProperty { get; set; }
```

***NOT:*** Şart olmamakla beraber field'ler _ ile başlar.