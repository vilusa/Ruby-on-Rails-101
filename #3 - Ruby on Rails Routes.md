
 **Ruby on Rails Routes**
 

    config/routes.rb  #dizininden yapılandırılır

Tarayicindan gelen isteği ilgili controller'a ileten bir RoR yapısıdır.

    rails generate controller deneme index 
controller oluşturma komutunu daha önceden kullanmıştık, komutu uyguladıktan sonra gerçekleşen olaylar sırasıyla; `controllers` dizini içerisinde `deneme_controller.rb` adıyla bir controller dosyası oluşturur, `routes.rb` dosyamız içerisinde `get "deneme/index"` ifadesi yer almıştı, `views` dizini içerisinde ise `deneme` adında bir dizin oluşturup içerisine `index.html.erb` doyasını eklemişti.

controller oluşturma komutunu çalıştırdığımızda yapılan işlemler controller'a bağlı ve controller'ı ilgilendiren işlemlerdir(olaylardır). 

Routes'ın Çalışması
===================
    localhost:3000/deneme/index
tarayıcımızdan rails uygulamamıza böyle bir istekte bulunduğumuzda bu istek ilk olarak `public` dizini içerisinde değerlendirilir ve uygun bir sonuç elde edilirse bu sonuç tarayıcıya geri gönderilip tarayıcı üzerinde bu sonuç görüntülenecektir.
`public` dizininde uygun bir eşleme bulunmadığında, public bunu `routes` a iletir, routes'dan isteği karşılayacak eşleşme olacağı için routes tarayıcı isteğine bağlı yönlendirmeyi `deneme controller`'ına iletecek, ardından bu controller ise gelen istek doğrultusunda kendisine bağlı `deneme` dizininin içindeki `index` sayfasını tarayıcıya gönderir.

## Public Dizini
RoR uygulamamızda `public` dizininde `deneme` adında bir dizin oluşturup içerisinde `index.html` adında bir dosya oluşturuduğumuzu varsayalım.
 Tarayıcımızdan tekrar `localhost:3000/deneme/index` adresine erişmek istediğimizde RoR uygulamamızın bizi direkt olarak `public` dizini içerisindeki `deneme/index.html` dosyasına yönlendirip bize bu sayfayı gösterdiğiniz görebiliriz. Yani bu durumda `routes` dosyasında bakmaksızın eğer varsa `public` dizini içerisindeki bir eşleme olduğunda bu dizindeki dosyaya erişmiş oluruz.

## Routes Çeşitleri (Türleri)
### Basit Routes
 Routes dosyamızı incelediğimizde ;

    get 'deneme/index'
şeklinde bir tanımlama olduğunu görüyoruz, bu yönlendirme ifadesi controller oluşturduğumuzda otomatik olarak eklenen bir yönlendirmedir. Bu şekilde yönlendirme/tanımlamaları **Basit Yönlendirme** olarak adlandırılır. Bu tanımalamadaki `get` ifadesi yönlendirme işlemi yapılırken sayfaya gönderilen isteğin hangi **method** ile gönderileceğini ifade eder. Örneğin bu tanımlamada `get` metoduyla istekte bulunuyoruz. 
### Kök (root) Route
Kök route belirleyeceğimiz bir sayfanın projemizin anasayfası olması istiyorsak kök route yönlendirmesi yapabiliriz.

    root 'deneme#index'
   şeklinde **routes** dosyamızda tanımlama yaptığımızda uygulamamızın anasayfası olarak `deneme` dizinindeki `index.html.erb` sayfası ayarlanmış olacaktır. Bu tanımlamada `/` yerine `#` kullanarak tanımlama yapmış olduk. İşlemin ardından artık RoR uygulamamızın anasayfasına erişmek istediğimizde karşımıza belirlediğimiz kök(root) route çıkacaktır.

 


 > Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg1NDMzNDQzXX0=
-->