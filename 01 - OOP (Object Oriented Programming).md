# OOP (Object Oriented Programming - Nesne Yönelimli Programlama)

Object --> Nesne: Kendine ait özellikleri, fonksiyonları olan varlıklardır.

**Somut Nesne (Concrete):** Elle tutulan gözle görülen

**Somut Nesne (Abstract):** Zihnimizde var olan

C#'da bir nesne oluşturulmadan önce, nesnenin kavramsal tanımı yapılmalıdır. **(CLASS)** yapılmalıdır. Daha sonra bu tanımdan faydalanarak nesne oluşumu **(INSTANCE)** sağlanır.

**CLASS:** Bir nesnenin nasıl birşey olacağını, özelliklerinin, fonksiyonlarının varsa eylemlerinin vs. tanımlandığı yapıdır. Class'lar namespacelere ait yapılardır.

Nesneyi oluşturmak için "new" anahtar kelimesi kullanılır.

***NOT:*** C#'da kullandığımız tipler temelde 2 ana gruba ayrılır.

1. **VALUE TYPES (DEĞER TİPLERİ)**
	Byte, bool, int, char vs.. gibi isimlendirilebilen değerlerdir.

2. **REFERENCE TYPES (REFERANS TİPLERİ)**
	class, interface vs. gibi tipler referans tiplerdir.
	
**Value Type** ile oluşturulan veriler, RAM'de **STACK** alanında yer alır, bu varlığa ait değer de **STACK** alanına yerleşir.

**Referance** Type ile oluşturulan veriler, RAM'de **STACK** alanında yer alır, bu varlığa ait değer de **HEAP** alanına yerleşir.

![image](https://github.com/kutayozturk/csharp-oop/assets/94574681/052be8fc-2309-4e01-811c-4da3b9c3096b)

Yukarıda görselden de anlaşılacağı üzere,

deger: referans
new Deger(); ifadesi ise Nesne'dir.

> Bir nesne oluşturmak için **"new"** operatörünün kullanıldığını daha önceden söylemitşik. Dolayısı ile ***bir nesne referansı olmadan da oluşturulabilir.*** Ancak oluşturulan nesneyi refere eden bir yapı olmadığından kullanılamaz.

> HEAP'de yer alan veriye doğrudan erişmek mümkün değildir, o veriye ancak STACK'deki bir referans üzerinden erişilebilir.
