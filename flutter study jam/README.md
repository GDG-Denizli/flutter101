![alt](https://flutter.dev/assets/flutter-lockup-c13da9c9303e26b8d5fc208d2a1fa20c1ef47eb021ecadf27046dea04c0cebf6.png)

# Flutter 101





> Widgetleri tanıyalım

### Widget

> ![alt](https://miro.medium.com/max/1362/1*Jai1GwDJtBtLaV08mB_rfA.png)



### Stateless Widget

> Bu Widget ekran ilk oluşturulduğunda bir kez çalışan ve orada sabit bir şekilde kalan widget’lar için tasarlanmış. Örnek verecek olursak Text bir stateless widget’dir ve uygulama oluştuğu anda biz onu ekranın en tepesine koyarız, onunla herhangi bir işlem yapmayız ve o hala orada durmaya devam eder. Ta ki uygulama kapatılana kadar.


### Statesfull Widget

> Stateful ise değişken halinde olabilecek widget’ler için kullanılır. Örnek verecek olursak ekranımızda ortadaki butona tıkladıkça sayının artmasını istiyoruz(Yeni bir proje oluşturduğumuz da otomatik gelen uygulama gibi…) sayının uygulama içinde kullanıcı tıkladıkça artmasını göstermek için bu sınıfı stateful olarak yapmak zorundayız.


#### Widgetler

> Container : Kullanacağımız text , resim vb durumları daha kolay yönetmemizi ve yönlendirmemizi sağlayan widget

```dart
child: Container(
    margin: const EdgeInsets.all(10.0),
    padding: // child widgetinde bulunan nesne ile container sınırları arasındaki boşluğu ayarlarız.
    color: Colors.amber[600],
    width: 48.0,
    height: 48.0,
    child: // oluşturuacağımız widgetleri yazacağımız yer.
  ),

  



```

-----
> Image : Resimleri göstereceğimiz widget.

```dart

const Image(
  image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
)


```


-------
> Column : Widgetleri dikey (y) ekseninde gösteren widget

**children içinde birden fazla widget alabilir**

```dart

Column(
  crossAxisAlignment: CrossAxisAlignment.start,
  mainAxisSize: MainAxisSize.min,
  children: <Widget>[
    Text('We move under cover and we move as one'),
    Text('Through the night, we have one shot to live another day'),
    Text('We cannot let a stray gunshot give us away'),
    Text('We will fight up close, seize the moment and stay in it'),
    Text('It’s either that or meet the business end of a bayonet'),
    Text('The code word is ‘Rochambeau,’ dig me?'),
    Text('Rochambeau!', style: DefaultTextStyle.of(context).style.apply(fontSizeFactor: 2.0)),
  ],
)


```


-----
> Raised Button : 
> Bir işlem vb bir şey yaptırmak için kullanırız.
>  

```dart

    RaisedButton(
          onPressed: () {},
          child: const Text(
            'Aktif Button',
            style: TextStyle(fontSize: 20)
          ),
        ),


```

------












AppBar: Uygulamanın en üstünde bulunan ve gerekli işlemleri yapmamıza yarayan widget
```dart
appBar: AppBar(
        title: Text("Flutter Study Jam"),
        actions: <Widget>[
         //uygulamaya etkleyeceğimiz farklı özellikleri buradaki aksiyonlar listesine yazabiliriz
        ],
        elevation: // appBar'ın altına gölge ekleyebiliriz.
        iconTheme: // AppBar içinde oluşturuduğumuz iconlara temel görüntü özelliklerini verebiliriz.
        centerTitle: // oluşturuğumuz başlığın yönünü belirleyebiliriz.,




      ),
```


