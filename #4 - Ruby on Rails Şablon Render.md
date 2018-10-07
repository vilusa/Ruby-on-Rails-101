
**Ruby on Rails Şablon Render**
Controller üzerinde tanımlı methodlar üzerinden şablon render etme işlemlerini örnekler üzerinde inceleyelim.
RoR'de bir şablonu render etmek; controllerımız aracılığıyla o şablonu ilgili `view`'dan çağırıp tarayıcıda göstermek olarak tanımlayabiliriz.  

Şablon Tanımlama
=
Şablonlarımız `app/views` dizini içerisinden tanımlanmaktadır.
`views` dizini altındaki `deneme` dizininde `merhaba.html.erb` dosyamızı oluşturalım. 

    <h1>Merhaba Şablonu</h1>
şeklinde dosyamızı kaydedelim.

 Controller Dosyamızda;


    def merhaba
    	render('index') #index.html.erb dosyasını çağırır
    end


`deneme/merhaba` adresine istek yaptığımızda `index.html.erb dosyasını çağırır ekrana basacaktır.

Önemli Not
==
Tarayıcıdan `localhost:3000/deneme/merhaba` şeklinde bir istekte bulunduğumuzda; isteğin `deneme` kısmı controller tarafından temsin edilmektedir, `merhaba` kısmı ise action tarafından temsil edilmektedir. Yani action tarafından temsil edilen kısım  `controller` içerisindeki  tanımlı olan methodlarla ilişkilidir.
> Written with [StackEdit](https://stackedit.io/).


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjU5NDUwNTQwXX0=
-->