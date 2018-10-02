

**Ruby on Rails Controller**
controllerın bulunduğu dizin `app/controller` 

    rails generate controller deneme index
Bu komut deneme isminde bir controller oluşturup, index methodunu controller'a yazıp bununla birlikte `app/views/deneme` dizininde `index.html.erb` isimli bir view dosyası oluşturur. Bununla birlikte `config/routes.rb` dosyasına `get 'deneme/index'` şeklinde bir route tanımlar.

    get 'deneme/index'
    
kodu tarayıcıdan bu dizinle alakalı bir istekte bulunduğumuzda bizi `views` dizini içerisindeki `deneme`  dizini altındaki `index.html.erb` dosyasına bizi yönlendirir.

    app/views
   dizini içerisindeki dosyalar projemizin görselliğini ilgilendiren dosyalardır. İncelediğimizde genelde `HTML` kodlarının kullanıldığı dosyalardır.

    rails server
    rails s #kısa kullanımı
komutuyla rails sunucumuzu çalıştırırız. `localhost:3000` adresinden projemize erişebiliriz.

    localhost:3000/deneme/index
   adresine erişmek istediğimizde karşımıza `views/deneme` dizinindeki index.html.erb dosyasına erişmiş oluruz.
> Witten with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTU1MjkyMzgwOF19
-->