
**Ruby on Rails**
Ruby on Rails MVC mimarisiyle çalışan bir web uygulama geliştirme çatısıdır. MVC yazılıma ait arayüz kodlarıyla çalışma mantığı içerisinde işlevselliğe sahip programlama kodlarıyla ve veritabanı işlerini birbirine karıştırmadan yazılım geliştirmemize imkan sağlayan bir yazılım mimarisidir.

Kullanıcı öncelikler tarayıcı aracılığıyla istekte bulunur, tarayıcı üzerinden gerçekleştirilen bu istek rails üzerindeki router tarafından algılanır ve bu kullanıcı isteğine bağlı istek türü ve bu istekle beraber bir veri varsa Controller'a iletilir. Daha sonra  Controller route tarafından gelen isteği tetikler ve üretilen sonuca göre ilgili modelde devreye girerek veritabanı üzerinde işlem yapılır. Ardından veritabanı üzerinden yapılan işlemin sonucuna bağlı veriler model aracılığıyla controller'a iletilir, controller verileri inceleyerek gelen verilerin hangi view tarafından işlenip ekran görüntüsü oluşturulacağına karar verir ve buna bağlı olarak veriler ilgili view'e gönderilir. View'de eldeki verilerden ekran görüntüsünü oluştururarak cotroller aracılığıyla kullanıcının isteğine bağlı ekran sonucunu tarayıcıya gönderir.

**Router**
Kullanıcının tarayıcı üzerinde yaptığı isteği belirleyip controller'a gönderir.

**Controller**
Router'ın yapmasını istediği işlemi ve gönderdiği verilerin methodlar aracılığıyla yapar ve sonuç üretir. Bu üretilen sonuçtan hangi modelin devreye gireceğini belirler ve ilgili modeli devreye sokar, ayrıca ürettiği sonuç ile hangi view'ın devreye girerek nasıl bir ekran çıktısı üretileceğini kontrol eder.

**Model**
Veritabanı işlemlerini kısaca veritabanı komutlarını kullanmadan Rails deyimleriyle kısa yoldan gerçekleştiren yapıdır. Model veritabanı sistemiyle sürekli iletişim halinde olup veritabanı işlemlerini Rails üzerinden gerçekleştirir.

**View**
Kullanıcının isteğine bağlı olarak ortaya çıkan ekran görüntüsünün oluşturulduğu kısımdır. Başka bir deyimle uygulamamızın arayüzünü ilgilendiren işlemlerin yapıldığı bölümdür.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUxMTU4MTM3M119
-->