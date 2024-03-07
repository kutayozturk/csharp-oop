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

// kapsul1.a = 5;
// Yukarıdaki komut hata verecektir. Çünkü "a" değeri private'dir ve class dışından erişilemez.
// Ancak;

kapsul1.setA(5);
kapsul1.getA();

```

Yukarıdaki komutlar çalıştırıldığında Ekran Çıktısı: 
``` 
5
```

Olacaktır.

Görüldüğü üzere, "a" değişkeni doğrudan kullanıcı tarafındaan kullanılamamıştır. set ve get metodları ile (Butonlarımız) değer atanmış ve atanan değer çağrılmıştır.
